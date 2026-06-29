# Checklist Funcional - Pantalla Estado del Pedido

## Navegación y acceso
1. Hacer clic en "Estado del pedido" en el encabezado muestra el campo "Número de pedido".
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED

2. El campo "Número de pedido" acepta entrada de texto.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED

3. Presionar Enter con un número válido muestra la información del pedido.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: Nose puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

4. Tras hacer clic en "Pedir" con datos válidos, no aparece ninguna ventana de confirmación intermedia (según BRD y Figma).
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🔴 FAILED
    - Opera 71 o superior, 1280x720: 🔴 FAILED
    - [[BUG US-1]](../bug-reports/US-1.md)

5. Presionar Enter con un número inválido muestra el mensaje: "No existe tal pedido. ¿Seguro que ese es el número correcto?"
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED

6. Se puede introducir otro número de pedido después de consultar uno.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

## Visualización de datos del pedido
7. Se muestra el nombre del usuario.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

8. Se muestra el apellido del usuario.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

9. Se muestra la dirección del usuario.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

10. Se muestra la estación del metro.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🔴 FAILED [[BUG US-2]](../bug-reports/US-2.md)

11. Se muestra el teléfono del usuario.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

12. Se muestra la fecha de entrega del scooter.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

13. Se muestra el periodo del alquiler.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

14. Se muestra el color del scooter.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

15. Se muestra el comentario del usuario.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

16. Si un campo de texto excede una línea, pasa a una segunda línea (regla de truncado/ajuste).
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

## Cadena de estado (4 estados)

### "El scooter está en el almacén"
17. Se activa automáticamente al realizar un pedido.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

### "El repartidor o repartidora está en camino"
18. Se activa cuando el repartido confirma que aceptó el pedido.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

19. Muestra el aviso: "El repartidor [Nombre] está en camino"/
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 PASSED

20. Si el nombre del repartidor excede una línea, pasa a una segunda línea.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🔴 FAILED [[BUG US-3]](../bug-reports/US-3.md)

### "El servicio de entrega llegó"
21. Se activa cuando el repartidor presiona "Completar".
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🔴 FAILED [[BUG US-4]](../bug-reports/US-4.md)

### "Bien, vamos a dar un paseo"
22. Se activa cuando el repartidor confirma finalización.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟡 SKIPPED: El estado se activa cuando el repartidor presiona "Completar" desde la app. [[BUG US-6]](../bug-reports/US-6.md)

23. Muestra "El alquiler finalizará el <fecha>".
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🔴 FAILED [[BUG US-7]](../bug-reports/US-7.md)

24. La fecha se coincide con el cálculo desde la entrega y el número de días de alquiler.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟡 SKIPPED: No se muestra la fecha. [[BUG US-7]](../bug-reports/US-7.md)

25. Al finalizar el periodo, el estado cambia a "Periodo de alquiler terminado" con la leyenda "El repartidor o repartidora recogerá el scooter pronto".
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED: No se puede crear pedido. [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🔴 FAILED [[BUG US-8]](../bug-reports/US-8.md)

### API - Aceptación de Pedidos - PUT /api/v1/orders/accept/:id
1. Al aceptar un pedido mediante la API, se actualiza el campo inDelivery = f a inDelivery = t en la tabla "Orders" de dicho pedido y no se duplica el registro del pedido.
    - Tipo de prueba: Funcional
    - Api Ez-scooter versión 1.0.0: 🔴 FAILED [[BUG US-5]](../bug-reports/US-5.md)