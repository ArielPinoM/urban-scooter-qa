# US-4: El estado "El servicio de entrega llegó" es gris y muestra la marca "✔" al completar pedido - posible consecuencia de registros duplicados

# Detalles clave

## Severidad
🟠 Major

## Prioridad
🟧 High

## Entorno
- Opera 132, 1280x720 (Chrome bloqueado por [US-1](./US-1.md))
- Postman 12.16.4
- Api Ez-scooter versión 1.0.0
- Dispositivo móvil
    - Samsung Galaxy S23+
    - Android version: 16
- Aplicación móvil “Urban Scooter“ versión 1.0

## Componente
Estado del Pedido - Cadena de Estados

## Descripción
Al intentar verificar que el tercer estado “El servicio de entrega llegó“ se activa cuando el repartidor presiona “Completar“ desde la aplicación móvil, se encontró que el pedido se había duplicado en la base de datos ([US-5](./US-5.md)). Para forzar el avance de estados fue necesario completar ambos registros; al hacerlo, el estado 3 apareció como inactivo y el 4 como activo.

Este comportamiento parece ser un síntoma de [US-5](./US-5.md), ya que la lógica de estados podría estar operando sobre múltiples registros del mismo pedido. Se requiere que se resuelva [US-5](./US-5.md), para poder volver a ejecutar esta prueba.

### Precondiciones
- US-5 resuelto.
- Existe un pedido creado con un número de pedido conocido.
- Se ha creado una cuenta de mensajero (vía API).
- Se ha instalado la aplicación móvil “Urban Scooter“ versión 1.0 en un dispositivo físico o un emulador con Android 16.
- Se ha iniciado sesión correctamente con las credenciales que se usaron para registrar al mensajero.

### Pasos para reproducir
1. Crear un pedido válido en Opera 1280×720 y guardar el número.
2. En la aplicación móvil, en la pantalla “Todos los pedidos“, localizar el pedido recién creado y tocar “Aceptar”.
3. Tocar “Sí” en la ventana emergente “¿Deseas aceptar el pedido?“.
4. Tocar “Mis pedidos”.
5. Tocar “Completar” en el 1er registro de 2 que aparecen (ambos registros son del mismo pedido).
6. Tocar “Sí” en la ventana emergente “¿Has completado el pedido?“.
7. Hacer lo mismo con el otro registro de pedido.
8. Abrir la página de inicio de la aplicación en Opera.
9. Hacer clic en “Estado del pedido“.
10. Ingresar el número de pedido que cumple las precondiciones anteriores y hacer clic en “¡Vamos!”.
11. Observar la cadena de estado.

### Resultado esperado
El estado 3 ("El servicio de entrega llegó") está activo (resaltado en negro, con el número 3 delante).

### Resultado actual (con [US-5](./US-5.md) presente)
El estado 3 aparece en gris con marca de completado.

### Evidencia

#### Captura de pantalla de la cadena de estado mostrando el estado 3 inactivo y el 4 activo
![](../test-evidence/US-4/3rd-status-inactive.png)