# Ventana emergente de confirmación no documentada bloquea la creación del pedido en Chrome (funciona en Opera)

# Detalles clave

## Severidad
🟠 Major

## Prioridad
🟧 High

## Entorno
Chrome 149, 1280x720 (falló) / Opera 132, 1280x720 (funciona con desviación)

## Componente
Realizar Pedido - Formulario "Alquiler"

## Descripción

### Desviación respecto a requisitos y diseño
Al hacer clic en “Pedir“ con datos válidos, aparece una ventana emergente de confirmación “¿Deseas hacer un pedido?“ y los botones “No“ y “Sí“. Esta ventana:

- No está descrita en los requisitos de negocio.
- No aparece en los diseños de Figma.

Según el BRD, el comportamiento esperado es:

> 'Si todos los campos se rellenaron correctamente, el pedido se hará cuando el usuario o usuaria haga clic en el botón "Pedir". Aparecerá una ventana emergente con el mensaje "Número de pedido NNNNN. Escríbelo: será útil para darle seguimiento al estado" mediante el botón "Comprueba el estado".'

No se menciona ningún paso intermedio de confirmación.

### Comportamiento por navegador
- Chrome 149: La ventana aparece. Al hacer clic en “Sí“ ocurre nada. El pedido no se crea.
- Opera 132: La ventana aparece. Al hacer clic en “Sí” funciona: se crea el pedido y se muestra el número.

### Impacto
- En Chrome, el Happy Path está completamente bloqueado.
- En Opera, el flujo avanza, pero introduce un paso no documentado que contradice los requisitos y el diseño.

### Pasos para reproducir
1. Abrir la aplicación en Chrome 149 (1280x720).
2. Hacer clic en “Pedir“.
3. Ingresar “Ariel“ en el campo “Nombre“.
4. Ingresar “Pino“ en el campo “Apellido“.
5. Ingresar “1st Street“ en el campo “Dirección“.
6. Seleccionar “5th Street“ en el campo “Estación de metro“.
7. Ingresar “+19999999999“ en el campo “Teléfono“.
8. Hacer clic en “Siguiente“.
9. Seleccionar la fecha de mañana en el campo “Fecha de entrega“.
10. Seleccionar “un día“ en el campo “Periodo de alquiler“.
11. Hacer clic en “Pedir“.
12. En la ventana emergente, hacer clic en “Sí“.

### Resultado esperado
Tras “Pedir“, aparece directamente la ventana emergente “El pedido ha sido realizado“ con el número de pedido.

### Resultado actual
Aparece la ventana emergente de confirmación “¿Deseas hacer un pedido?“ no documentada.
- En Chrome, al hacer clic en “Sí“, no pasa nada.
- En Opera, el flujo continúa y se crea el pedido.

### Evidencia

#### Captura de la ventana emergente en Chrome
![](../test-evidence/US-1/pop-up-window-chrome.png)

#### Captura de la ventana emergente en Opera tras el clic exitoso
![](../test-evidence/US-1/order-success-opera.png)