---
name: Book an at-home diagnostic collection
description: Check serviceability, pick a slot, and create a home-collection order with Orange Health, then track it to completion.
api: openapi/orange-health-partner-openapi.yml
operations: [fetchServiceability, createOrder, getOrderStatus, getTestResults]
---

# Book an at-home diagnostic collection

Use the Orange Health Partner API to schedule a home blood-sample collection.

## Auth
Send your partner key in the `api_key` request header on every call. Sandbox keys:
`partner-alwaysPartner`, `partner-alwaysOH`, `partner-decidedAtOrderLevel`. Base URL
`https://sandbox-partner-api.orangehealth.dev` (test) / `https://partner-api.orangehealth.in` (prod).

## Steps
1. **`fetchServiceability`** — `GET /v1/partner/serviceability` with `latitude`, `longitude`
   and `request_date` (YYYY-MM-DD, >= today). Sandbox test point: `13.0240`, `77.6433`.
   A 200 with a `slots` map means the location is serviceable; pick a `slot_datetime`.
   A 400/404 means unserviceable — stop.
2. **`createOrder`** — `POST /v1/partner/order` with `address`, `location`, the chosen
   `slot_datetime`, `payment_type`, `primary_patient_name`/`_number`, and `patient_details[]`
   (each with `patient_name`, `patient_phone`, `age`, `gender`, `tests[].test_id`, `partner_reference_id`).
   A 202 returns `request_id` + `token` — **persist both**; they are required for every follow-up call.
   Do not blindly retry: an identical payload within 60s returns **425** (already accepted).
3. **`getOrderStatus`** — `GET /v1/partner/order-details/{requestID}?token=...` to poll status,
   or subscribe to webhooks (order.created → … → order.completed), deduping on `x-oh-event-id`.
4. **`getTestResults`** — `GET /v1/partner/test-results?request_id=...` once reports are ready
   to pull structured investigation values (`investigation_is_abnormal` = `A` flags abnormal).

## Rules
- Errors are a single `status` string (not problem+json). Handle 400/404/425 explicitly.
- Reschedule/cancel are only possible before the phlebotomist starts (before a tracking link appears).
