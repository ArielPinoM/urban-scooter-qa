# Título

No se recibe la notificación push 2 horas y 1 minuto después del plazo.

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

4. Ingresar la url del backend en la pantalla de inicio de sesión de la aplicación móvil.

5. Iniciar sesión con las credenciales de la cuenta del mensajero que se creó.

# Pasos para reproducir

- No se recibe ninguna notificación.


# Resultado esperado

- No se recibe ninguna notificación.