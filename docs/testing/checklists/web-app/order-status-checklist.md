# Functional Checklist - Order Status Screen

## Navigation and Access
1. Clicking "Estado del pedido" in the header displays the "Número de pedido" field.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟢 PASSED
    - Opera 71 or higher, 1280x720: 🟢 PASSED

2. The "Número de pedido" field accepts text input.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟢 PASSED
    - Opera 71 or higher, 1280x720: 🟢 PASSED

3. Pressing Enter with a valid number displays the order information.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

4. After clicking "Pedir" with valid data, no intermediate confirmation dialog appears (per BRD and Figma).
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🔴 FAILED
    - Opera 71 or higher, 1280x720: 🔴 FAILED
    - [[BUG US-1]](/docs/testing/bug-reports/US-1.md)

5. Pressing Enter with an invalid number displays the message: "No existe tal pedido. ¿Seguro que ese es el número correcto?"
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟢 PASSED
    - Opera 71 or higher, 1280x720: 🟢 PASSED

6. It is possible to enter another order number after checking one.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

## Order Data Display
7. The user name is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

8. The last name is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

9. The address is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

10. The metro station is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🔴 FAILED [[BUG US-2]](/docs/testing/bug-reports/US-2.md)

11. The user phone number is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

12. The scooter delivery date is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

13. The rental period is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

14. The scooter color is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

15. The user comment is displayed.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

16. If a text field exceeds one line, it wraps to a second line.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

## Status Flow (4 states)

### "El scooter está en el almacén"
17. It activates automatically after placing an order.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

### "El repartidor o repartidora está en camino"
18. It activates when the courier confirms acceptance of the order.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

19. It displays the message: "El repartidor [Nombre] está en camino".
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

20. If the courier name exceeds one line, it wraps to the second line.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🔴 FAILED [[BUG US-3]](/docs/testing/bug-reports/US-3.md)

### "El servicio de entrega llegó"
21. It activates when the courier presses "Completar".
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🔴 FAILED [[BUG US-4]](/docs/testing/bug-reports/US-4.md)

### "Bien, vamos a dar un paseo"
22. It activates when the courier confirms completion.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟡 SKIPPED: The state activates when the courier presses "Completar" from the app. [[BUG US-6]](/docs/testing/bug-reports/US-6.md)

23. It displays "El alquiler finalizará el <fecha>".
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🔴 FAILED [[BUG US-7]](/docs/testing/bug-reports/US-7.md)

24. The date matches the calculation from delivery and the rental days.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟡 SKIPPED: The date is not displayed. [[BUG US-7]](/docs/testing/bug-reports/US-7.md)

25. At the end of the period, the state changes to "Periodo de alquiler terminado" with the legend "El repartidor o repartidora recogerá el scooter pronto."
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🔴 FAILED [[BUG US-8]](/docs/testing/bug-reports/US-8.md)

26. Only one state can be active at a time.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

27. The active state is highlighted in black.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

28. Inactive states are gray.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

29. When moving from one state to the next, the number before the state changes to a check mark.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

## Order Cancellation
30. Clicking "Cancelar pedido" shows a popup with the text "¿Deseas cancelar el pedido?".
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

31. The "Atrás" button closes the popup and returns to the status screen.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

32. The "Cancelar" button shows the popup: "El pedido ha sido cancelado. Siéntete libre de volver en cualquier momento :)" and a "Bien" button.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

33. The "Bien" button redirects to the home page.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

34. The "Cancelar el pedido" button is enabled only before the courier picks up the order.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

35. Once the courier has the order, the button is not clickable.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟡 SKIPPED: The button disappears when the courier has the order. [[BUG US-9]](/docs/testing/bug-reports/US-9.md)

36. The canceled order is removed from the system and is not visible to the user.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟡 SKIPPED: The order is not canceled. [[BUG US-10]](/docs/testing/bug-reports/US-10.md)

## Delayed Order
37. An order not delivered by 23:59 on the agreed day changes to "El repartidor o repartidora se demoró".
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

38. It displays the message: "No podremos entregar el scooter a tiempo. Para aclarar el estado de tu pedido, llama a soporte: 0101".
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

39. The state and the legend are highlighted in red.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

40. If the delayed order is delivered, the rental countdown starts at the moment of delivery.
    - Test type: Functional
    - Chrome 85 or higher, 1280x720: 🟡 SKIPPED: Cannot create order. [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
    - Opera 71 or higher, 1280x720: 🟢 PASSED

# API - Order Acceptance - PUT /api/v1/orders/accept/:id
1. When accepting an order via the API, the order's inDelivery field is updated from false to true in the Orders table and the order record is not duplicated.
    - Test type: Functional
    - Ez-scooter API version 1.0.0: 🔴 FAILED [[BUG US-5]](/docs/testing/bug-reports/US-5.md)
