# US-6: The "finished" field is set when "Completar" is pressed (status 3); possible requirements inconsistency

# Key details

## Severity
🔵 Minor

## Priority
🟨 Medium

## Environment
- Opera 132, 1280x720 (Chrome blocked by [US-1](./US-1.md))
- Postman 12.16.4
- Ez-scooter API version 1.0.0
- Back-end
    - Node.js v12.17.0
- PostgreSQL database

## Component
Backend - Order Status Logic

## Description

### Link
Blocked by [US-5](./US-5.md).

During status chain testing, it was observed that the `finished` field in the `Orders` table changes to `true` when the courier presses **"Completar"** (which activates the status "El servicio de entrega llegó"). However, the backend requirements document indicates that *the logical finished field is assigned when the order has been sent,* **(Database content description > Orders)**.

Clarification is needed:
- Does "Enviado" correspond to the moment the courier presses “Completar“ (status 3) or when completion is confirmed (status 4)?
- If `finished` should reflect rental completion (status 4), then it is changing prematurely.

**Note:** This verification was performed with bug [US-5](./US-5.md). It is likely the behavior is the same without duplicates, but it should be confirmed once resolved.

### Preconditions
- [US-5](./US-5.md) resolved.
- Order created and accepted by the courier.

### Steps to reproduce
1. Accept an order with a courier.
2. Query `Orders`: verify that `finished = false`.
3. Press “Completar” (simulate via API or from the mobile app).
4. Query `Orders` again for the same order.
5. Compare the value of `finished` with what is specified in the requirements.


### Expected result (according to requirements interpretation)
To confirm. If “Enviado“ = status 4, `finished` should remain `false` after “Completar”, and switch to `true` only when completion is confirmed.

### Actual result (with [US-5](./US-5.md) present)
`finished` changed to `true` immediately after “Completar” (status 3).