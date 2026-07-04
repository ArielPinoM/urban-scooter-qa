# Título

No se recibe notificación si el pedido ya fue completado.

# Entorno

- Emulador Android: Galaxy A3, Android 9

- Postman 12.17.3

# Componente

Notificación

# Precondiciones

- La hora del servidor es antes de las 21:59.

1. Crear una cuenta de mensajero con ""login"": ""apm96"", ""password"": ""1234"", ""firstName: ""Ariel"" con POST /api/v1/courier.

2. Crear un pedido con POST /api/v1/orders, en el body, usar ""deliveryDate"": ""<fecha_de_hoy>"".

3. La aplicación móvil tiene permisos de notificación concedidos.

4. Ingresar la url del backend en la pantalla de inicio de sesion de la aplicación móvil.

5. Iniciar sesión con las credenciales de la cuenta del mensajero que se creó.

6. Aceptar el pedido en la pantalla de pedidos, pestaña "Todos los pedidos".

# Pasos para reproducir

1. Tocar ""Completar"" en ambas tarjetas del pedido (No deberían de haber dos tarjetas del mismo pedido).

2. Tocar ""Sí"" en cada ventana emergente de confirmación.

2. Esperar a que la hora del servidor sea 21:59.

3. Observar el emulador.


# Resultado esperado

- No se recibe ninguna notificación push para ese pedido.