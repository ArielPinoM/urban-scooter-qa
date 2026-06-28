# Checklist Funcional - Pantalla Estado del Pedido

## Navegación y acceso
1. Hacer clic en "Estado del pedido" en el encabezado muestra el campo "Número de pedido".
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟢 Aprobado
    - Opera 71 o superior, 1280x720: 🟢 Aprobado

2. El campo "Número de pedido" acepta entrada de texto.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟢 Aprobado
    - Opera 71 o superior, 1280x720: 🟢 Aprobado

3. Presionar Enter con un número válido muestra la información del pedido.
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🟡 SKIPPED [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1280x720: 🟢 Aprobado

4. Tras hacer clic en "Pedir" con datos válidos, no aparece ninguna ventana de confirmación intermedia (según BRD y Figma).
    - Tipo de prueba: Funcional
    - Chrome 85 o superior, 1280x720: 🔴 FAILED
    - Opera 71 o superior, 1280x720: 🔴 FAILED
    - [[BUG US-1]](../bug-reports/US-1.md)
