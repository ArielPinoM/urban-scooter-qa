# US-9: The "Cancelar el pedido" button disappears instead of remaining disabled after courier acceptance

# Key details

## Severity
🔵 Minor

## Priority
🟩 Low

## Environment
- Opera 132, 1280x720 (Chrome bloqueado por [US-1](./US-1.md))
- Postman 12.16.4
- Api Ez-scooter versión 1.0.0

## Component
Order Status

## Description

### Preconditions
- A new order has been created and its number has been saved.
- Using Postman, the order has been requested by its order number and the returned ID has been saved.
- A courier account has been created.
- Using Postman, a login has been performed with the newly created courier credentials and the returned ID has been saved.

### Steps to reproduce
1. Open the "Inicio" page.
2. Click "Estado del pedido".
3. Enter the order number and click "¡Vamos!".
4. Observe the presence of the button in the bottom left of the screen.
5. Using Postman, accept the order using the courier ID and order ID.
6. Click the Urban Scooter logo to return to the home page.
7. Check the order again with the "Estado del pedido" button.
8. Observe the bottom left of the screen.

### Expected result
The "Cancelar el pedido" button remains visible but appears disabled (not clickable).

### Actual result
The "Cancelar el pedido" button disappears completely from the screen.

### Evidence

#### Screenshot before acceptance
![](../test-evidence/US-9/button-visible-clickable.png)

#### Screenshot after acceptance
![](../test-evidence/US-9/button-disappeared.png)