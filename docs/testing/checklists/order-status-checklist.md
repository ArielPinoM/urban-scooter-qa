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