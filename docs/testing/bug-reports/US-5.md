# US-5: Order duplicates in the "Orders" table when accepted

# Key details

## Severity
🟠 Major

## Priority
🟧 High

## Environment
- Opera 132, 1280x720 (Chrome blocked by [US-1](./US-1.md))
- Postman 12.16.4
- Ez-scooter API version 1.0.0
- Mobile device
    - Samsung Galaxy S23+
    - Android version: 16
- Urban Scooter mobile app version 1.0

## Component
API - Order Acceptance

## Description
When the courier accepts an order through the API, an additional record is inserted into the `Orders` table with the same `track` and the original order data. This causes the courier to see **two identical order cards** in the mobile app.

For the end user to see the status change reflected in tracking, the courier must complete both records separately.

### Preconditions
- There is an order with a unique `track`.
- There is a valid message with credentials.
- The courier has no accepted orders.
- The courier ID and order ID have been obtained via the API.

### Steps to reproduce
1. Create a valid order and get its number (`track`).
2. Using Postman, log in as a courier and obtain the `courierId`.
3. Get the order `id` with `GET /api/v1/orders/track?t=<track>`.
4. Verify that it returns 1 record when querying the `Orders` table filtered by the order `track` with `select * from "Orders" where "Orders".track = '<track>';`.
5. Send a single request `PUT /api/v1/orders/accept/<order_id>?courierId=<courierId>`.
6. Verify that it returns 2 records when querying the `Orders` table filtered by the `track` with `select * from "Orders" where "Orders".track = '<track>';`.
7. Log in to the courier mobile app and observe the “Mis pedidos” list.

### Expected result
- The database contains a single record with that `track` and `inDelivery = t`.
- The mobile app shows a single pending order for that courier in “Mis pedidos”.

### Actual result
- Two records appear in the `Orders` table with the same `track` (e.g. ids 1 and 2).
- The mobile app shows two identical cards with the same address, delivery date, etc.

### Evidence

#### Screenshot of the Orders table showing duplicated records (ids 1 and 2)
![](../test-evidence/US-5/duplicate-orders.png)

#### Captura de la app móvil con dos pedidos iguales
![](../test-evidence/US-5/my-orders-duplicate-mobile.png)