# US-8: The status text "Período de alquiler terminado" does not match the BRD requirements (although it does match Figma)

# Key details

## Severidad
⚪ Trivial

## Prioridad
🟩 Low

## Environment
- Opera 132, 1280x720 (Chrome blocked by [US-1](./US-1.md))
- Postman 12.16.4
- Api Ez-scooter version 1.0.0

## Component
Order Status - Status Chain

## Description
When the rental period ends (forcing the date from the database), the 4th status correctly changes its text, but the content differs from the requirements document.

> - BRD: "Periodo de alquiler terminado" with the caption "El repartidor o repartidora recogerá el scooter pronto".
> - Figma: "El periodo de alquiler terminó" with the caption "El servicio de entrega recogerá el scooter".

The implementation matches the Figma design exactly, but contradicts the BRD. It is not defined which source of truth should be used for this text.

### Preconditions
- Order in status 4 ("Bien, vamos a dar un paseo").

### Steps to reproduce
1. In the database, execute `update "Orders" set "deliveryDate" = '2026-0x-xx 00:00:00+00' where "Orders".track = '<numero_pedido_en_estado_4>'`; (Update to a date 2 days earlier than the current `deliveryDate` value).
2. In Opera 1280x720, go to "Estado del pedido".
3. Enter the order number.
4. Observe the 4th status text.

### Expected result
- Status title: "Periodo de alquiler terminado".
- Caption: "El repartidor o repartidora recogerá el scooter pronto".

### Actual result
- Status title: "El periodo de alquiler terminó".
- Caption: "El servicio de entrega recogerá el scooter".

### Evidence

#### Screenshot of the active status after expiration showing the current texts
![](../test-evidence/US-8/4th-status-text.png)

#### Screenshot of the Figma design confirming they match
![](../test-evidence/US-8/4th-status-text-figma.png)