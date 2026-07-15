# Title

No notification is received if the order is already completed.

# Environment

- Android Emulator: Galaxy A3, Android 9

- Postman 12.17.3

# Component

Notification

# Preconditions

- Server time is before 21:59.

1. Create a courier account with "login": "apm96", "password": "1234", "firstName": "Ariel" using POST /api/v1/courier.

2. Create an order with POST /api/v1/orders, in the body, use "deliveryDate": "<today_date>".

3. The mobile application has notification permissions granted.

4. Enter the backend URL in the login screen of the mobile application.

5. Log in with the credentials of the courier account that was created.

6. Accept the order on the orders screen, "Todos los pedidos" tab.

# Steps to Reproduce

1. Tap "Completar" on both order cards (There should not be two cards for the same order).

2. Tap "Sí" on each confirmation popup.

2. Wait for server time to be 21:59.

3. Observe the emulator.

# Expected Result

- No push notification is received for that order.