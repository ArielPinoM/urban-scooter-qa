# Título

La notificación incluye la misma dirección del pedido aceptado.

# Entorno

- Emulador Android: Galaxy A3, Android 9

- Postman 12.17.3

# Componente

Notificación

# Precondiciones

- La hora del servidor es antes de las 21:59.

1. Crear una cuenta de mensajero con ""login"": ""apm96"", ""password"": ""1234"", ""firstName: ""Ariel"" con POST /api/v1/courier.

2. Crear un pedido con POST /api/v1/orders, en el body, usar ""deliveryDate"": ""<fecha_de_hoy>"" y ""address"": ""State St 1214"".

3. La aplicación móvil tiene permisos de notificación concedidos.

4. Ingresar la url del backend en la pantalla de inicio de sesión de la aplicación móvil.

5. Iniciar sesión con las credenciales de la cuenta del mensajero que se creó.

6. Aceptar el pedido en la pantalla de pedidos, pestaña ""Todos los pedidos"".

7. Esperar a que la hora del servidor sea 21:59.

# Pasos para reproducir

1. Observar el emulador en espera de la notificación.

2. Leer el mensaje completo.


# Resultado esperado

- La notificación incluye exactamente la dirección del pedido aceptado.