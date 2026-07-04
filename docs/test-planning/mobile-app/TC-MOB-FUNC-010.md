# Título

Se muestra ventana emergente "Sin acceso a Internet" al completar un pedido.

# Entorno

- Emulador Android: Galaxy A3, Android 9

- Postman 12.17.3

# Componente

Falta de Acceso a Internet - Ventana Emergente

# Precondiciones

- Se tiene acceso a internet en el dispositivo/emulador.

1. Crear un pedido con POST /api/v1/orders.

2. Crear una cuenta de mensajero con ""login"": ""apm96"", "password": "1234", "firstName": "Ariel" con POST /api/v1/courier.

3. Ingresar la url del backend en la pantalla de inicio de sesión de la aplicación móvil.

4. Iniciar sesión con las credenciales de la cuenta del mensajero que se creó.

5. Tocar "Aceptar" en la tarjeta del pedido.

6. Tocar "Mis pedidos".

# Pasos para reproducir

1. Activar el modo avión.

2. Tocar ""Completar"" en la tarjeta del pedido.


# Resultado esperado

Aparece ventana emergente "Sin acceso a Internet".