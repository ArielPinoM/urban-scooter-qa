# Title

"Sin acceso a Internet" popup window is displayed when completing an order.

# Environment

- Android Emulator: Galaxy A3, Android 9

- Postman 12.17.3

# Component

No Internet Access - Popup Window

# Preconditions

- Internet access is available on the device/emulator.

1. Create an order with POST /api/v1/orders.

2. Create a courier account with "login": "apm96", "password": "1234", "firstName": "Ariel" using POST /api/v1/courier.

3. Enter the backend URL in the login screen of the mobile application.

4. Log in with the credentials of the courier account that was created.

5. Tap "Aceptar" on the order card.

6. Tap "Mis pedidos".

# Steps to Reproduce

1. Activate airplane mode.

2. Tap "Completar" on the order card.

# Expected Result

A "Sin acceso a Internet" popup window appears.