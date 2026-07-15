# US-2: The subway station in "Order Status" does not match the one entered in the form

# Key details

## Severity
🟠 Major

## Priority
🟧 High

## Environment
Opera 132, 1280x720 (Chrome blocked by [US-1](./US-1.md))

## Component
Order Status - Order Information

## Description
When checking an order on the “Order Status” screen, the value shown in the “Estación de metro” field is different from the one entered in the “Para quién es el scooter” form.

### Steps to reproduce
1. Open the application in Opera (1280x720).
2. Click “Pedir”.
3. Enter “Ariel” in the “Nombre” field.
4. Enter “Pino” in the “Apellido” field.
5. Enter “1st Street” in the “Dirección” field.
6. Select “Arcadia” in the “Estación de metro” field.
7. Enter “+19999999999” in the “Teléfono” field.
8. Click “Siguiente”.
9. Select tomorrow’s date in the “Fecha de entrega” field.
10. Select “un día” in the “Periodo de alquiler” field.
11. Click “Pedir”.
12. In the “¿Deseas hacer un pedido?” popup, click “Sí”.
13. In the “El pedido ha sido realizado” popup, click “Comprueba el estado”.

### Expected result
“Arcadia” is displayed in the “Estación de metro” field.

### Actual result
“Artesia” is displayed in the “Estación de metro” field.

### Evidence

#### Screenshot of the form with the entered data
![](../test-evidence/US-2/form-data.png)

#### Screenshot of the "Estado del Pedido" screen showing the incorrect data
![](../test-evidence/US-2/order-status-wrong-data.png)