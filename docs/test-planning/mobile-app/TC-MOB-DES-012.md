# Título

El mensaje de la ventana emergente coincide con "Comprueba la conexión o espera una notificación de que se ha restablecido".

# Entorno

- Emulador Android: Galaxy A3, Android 9
- Postman 12.17.3

# Componente

Falta de Acceso a Internet - Ventana Emergente

# Precondiciones

- Se tiene acceso a internet en el dispositivo/emulador.

1. Crear una cuenta de mensajero con "login": "apm96", "password": "1234", "firstName": "Ariel" con POST /api/v1/courier.

2. Ingresar la url del backend en la pantalla de inicio de sesión de la aplicación móvil.

3. Iniciar sesión con las credenciales de la cuenta del mensajero que se creó.

3. Iniciar sesión con las credenciales de la cuenta del mensajero que se creó."

# Pasos para reproducir

1. Activar el modo avión.

2. Tocar "Todos los pedidos".

3. Leer el mensaje de la ventana emergente.

# Resultado esperado

- El mensaje de la ventana emergente coincide con "Comprueba la conexión o espera una notificación de que se ha restablecido".

# Evidencia

![](../../testing/test-evidence/no-internet-access/popup.png)