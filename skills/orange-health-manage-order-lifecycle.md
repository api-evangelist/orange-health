---
name: Reschedule, add-on, or cancel a collection order
description: Amend an existing Orange Health order — add tests, reschedule the slot, or request cancellation — and confirm the terminal state via webhooks.
api: openapi/orange-health-partner-openapi.yml
operations: [addOnOrder, rescheduleOrder, cancelOrder, getOrderStatus]
---

# Reschedule, add-on, or cancel a collection order

All amendment calls need the `request_id` (path) and `token` (query) from the original
create-order response, plus the `api_key` header.

## Steps
- **Add tests/packages — `addOnOrder`**: `POST /v1/partner/{requestID}/add-on-order?token=...`
  with `patient_name`, `age`, `gender`, `patient_phone`, `tests[].test_id` and/or `packages[].package_id`.
  Returns the added order ref with `status: Created`.
- **Reschedule — `rescheduleOrder`**: `PATCH /v1/partner/{requestID}/reschedule?token=...` with a
  `requested_slot_time` (fetch it first via serviceability), `reschedule_reason`, `reschedule_explanation`.
  Only allowed before collection starts. Returns `{"result": "ok"}`.
- **Cancel — `cancelOrder`**: `PATCH /v1/partner/{requestID}/cancel?token=...` with
  `cancellationReason` and `cancellationExplanation`. The 200 is only an acknowledgement —
  cancellation is **asynchronous**.

## Confirming terminal state
Do not treat the cancel 200 as final. Confirm via the **`order.cancelled`** webhook (paired with
`task.deleted`) or by polling **`getOrderStatus`**. Webhooks are HMAC-SHA256 signed in
`X-OH-Signature`; verify the signature and dedupe on `x-oh-event-id`.
