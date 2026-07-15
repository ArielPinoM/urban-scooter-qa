# US-3: Long courier name is truncated instead of wrapping to a second line

# Key details

## Severity
🔵 Minor

## Priority
🟩 Low

## Environment
- Opera 132, 1280x720 (Chrome blocked by [US-1](./US-1.md))
- Postman 12.16.4

## Component
Order Status - Status Chain

## Description
When the “El repartidor o repartidora está en camino” status is active and the courier name is too long for one line, the notice does not wrap to a second line as the requirements specify. Instead, it is truncated with ellipsis (...).

According to the requirements document:

> “Si el nombre del repartidor o repartidora es
demasiado largo y el aviso no cabe en una línea, el texto se mueve a la segunda
línea.“

This is not followed; the text is cut off.

### Steps to reproduce
1. Create a valid order (use Opera 1280x720) and save the order number.
2. Using Postman, create a courier account with `POST /api/v1/courier` and the payload:
    ```json
    {
        "login": "arielpinomeza96arielpinomeza96",
        "password": "ariel",
        "firstName": "Ariel"
    }
    ```
3. Using Postman, log in with `POST /api/v1/courier/login` and the payload:
    ```json
    {
        "login": "arielpinomeza96arielpinomeza96",
        "password": "ariel"
    }
    ```
    Save the courier ID returned by the response.
4. Using Postman, retrieve the order data for the created order by order number with `GET /api/v1/orders/track?t=<order_number>`.
5. Using Postman, accept the order with `PUT /api/v1/orders/accept/:<order_id>?courierId=<courier_id>`.
6. Open the Urban Scooter home page.
7. Click “Estado del pedido”.
8. Enter the order number in the “Número de pedido” field.
9. Click “¡Vamos!”.
10. Observe the text of the second status.

### Expected result
The notice displays the courier's full name, and if it does not fit on one line, the text wraps to a second line.

### Actual result
The text is truncated: “El repartidor o repartidora ar ... está en camino”.

### Evidence

#### Screenshot of the status with truncated text
![](../test-evidence/US-3/truncated-text.png)