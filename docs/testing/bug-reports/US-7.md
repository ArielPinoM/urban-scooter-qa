# US-7: Fourth status text shows "{{data}}" unrendered and wording differs from requirements

# Key details

## Severity
🔵 Minor

## Priority
🟨 Medium

## Environment
- Opera 132, 1280x720 (Chrome blocked by [US-1](./US-1.md))
- Postman 12.16.4
- Ez-scooter API version 1.0.0

## Component
Order Status - Status Chain

## Description
When the fourth status “Bien, vamos a dar un paseo” becomes active, the notice that should show the rental end date appears with the template placeholder `{{data}}` unrendered. In addition, the wording differs from what is specified in the requirements.

> *“The text ‘El alquiler finalizará el’ appears below the status title. The time shown is calculated from the moment the scooter is delivered to the user, considering the number of days.“*

### Preconditions
- Order created, accepted by the courier, and with status 4 active.
- If [US-5](./US-5.md) persists, the duplicate records were forced to complete to reach status 4 (workaround). Even so, the text issue is independent of the duplicate.

### Steps to reproduce
1. In Opera 1280x720, go to “Estado del pedido”.
2. Enter an order number that is in status 4.
3. Observe the text below the title “Bien, vamos a dar un paseo”.

### Expected result
Displays: **“El alquiler finalizará el <calculated_date>“.**

### Actual result
**Displays: “El alquiler terminará el {{data}}“.**

### Evidence

#### Screenshot of the fourth active status showing the notice text
![](../test-evidence/US-7/delivery-date-text.png)

#### API response that feeds that field
![](../test-evidence/US-7/get-order-response.png)