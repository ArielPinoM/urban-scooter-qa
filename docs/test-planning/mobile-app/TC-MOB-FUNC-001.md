# Title

Reception of push notification 2 hours before the deadline.

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

# Steps to Reproduce

1. Accept the order on the orders screen, "Todos los pedidos" tab.

2. Wait for server time to be 21:59.

3. Observe the emulator waiting for the notification.

# Expected Result

- A push notification arrives with the text: "2 horas hasta el final del pedido"