# API DOC: Ez-scooter

`version: 1.0.0`

## Couriers

### Couriers - Get the number of orders for the courier

> `GET` /api/v1/courier/:id/ordersCount

#### Parameter

| Field | Type   | Description                        |
| :---- | :----- | :--------------------------------- |
| `id`  | number | Courier number {"id": 123456} |

#### Number of orders for courier "1"

> /api/v1/courier/`1`/ordersCount

#### Success response

```json
HTTP/1.1 200
{
  "id": "123456",
  "ordersCount": "100500"
}
```

#### Request without number

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data for search"
}
```

#### Request with non-existent number

```json
HTTP/1.1 404 Not Found
{
  "message": "Courier not found"
}
```

## Courier

### Courier - Create a courier

> `POST` /api/v1/courier

#### Parameter

| Field       | Type   | Description                                                                                                              |
| :---------- | :----- | :----------------------------------------------------------------------------------------------------------------------- |
| `login`     | string | The courier login is written to the `login` column of the Couriers table.  |
| `password`  | string | The courier password, the hash of the value is written to the `passwordHash` column of the Couriers table. |
| `firstName` | string | The courier name is written to the `firstName` column of the Couriers table.                           |

#### Request

```json
{
  "login": "ninja",
  "password": "1234",
  "firstName": "saske"
}
```

#### Account created successfully

```json
HTTP/1.1 201 Created
{
    ok: true
}
```

#### Request without login or password

```json
HTTP/1.1 400 Bad Request
{
  "message": "Insufficient data to create an account"
}
```

#### Request with duplicate login

```json
HTTP/1.1 409 Сonflict
{
  "message": "This login is not available"
}
```

### Courier - Courier login to the system

> `POST` /api/v1/courier/login

#### Parameter

| Field      | Type   | Description                                                                                                              |
| :--------- | :----- | :----------------------------------------------------------------------------------------------------------------------- |
| `login`    | string | The courier login is written to the `login` column of the Couriers table.  |
| `password` | string | The courier password, the hash of the value is written to the `passwordHash` column of the Couriers table. |

#### Request

```json
{
  "login": "ninja",
  "password": "1234"
}
```

#### Successful login

```json
HTTP/1.1 200
{
    id: 12345
}
```

#### Request without login or password

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data to log in"
}
```

#### Request with non-existent login and password pair

```json
HTTP/1.1 404 Not Found
{
  "message": "Account not found"
}
```

### Courier - Delete a courier

> `DELETE` /api/v1/courier/:id

#### Parameter

| Field | Type   | Description                                                                             |
| :---- | :----- | :-------------------------------------------------------------------------------------- |
| `id`  | string | The courier number is stored in the `id` column of the Couriers table. |

#### Request

```json
{
  "id": "3"
}
```

#### Courier deleted successfully

```json
HTTP/1.1 200 OK
{
    ok: true
}
```

#### Request without ID

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data to delete the courier"
}
```

#### Request with non-existent ID

```json
HTTP/1.1 404 Not Found
{
  "message": "No courier with this ID"
}
```

## Orders

### Orders - Accept the order

> `PUT` /api/v1/orders/accept/:id

#### Parameter

| Field       | Type   | Description                                                                                   |
| :---------- | :----- | :-------------------------------------------------------------------------------------------- |
| `id`        | number | The order number is stored in the `id` column of the Orders table.            |
| `courierId` | number | Courier ID (courierId) is stored in the `id` column of the Couriers table. |

#### Request

> /api/v1/orders/accept/`1`?courierId=`213`

#### Successful response

```json
HTTP/1.1 200
{
    ok: true
}
```

#### Request without number

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data for search"
}
```

#### Request with non-existent number

```json
HTTP/1.1 404 Not Found
{
  "message": "No order with this ID"
}
```

#### Request with non-existent courier number

```json
HTTP/1.1 404 Not Found
{
  "message": "No courier with this ID"
}
```

#### Order already processed

```json
HTTP/1.1 409 Conflict
{
  "message": "Order is being processed"
}
```

#### Without courier ID or order ID

```json
HTTP/1.1 400 Conflict
{
  "message": "Insufficient data for search"
}
```

### Orders - Cancel the order

> `POST` /api/v1/orders/cancel

#### Parameter

| Field   | Type   | Description                                                                                         |
| :------ | :----- | :-------------------------------------------------------------------------------------------------- |
| `track` | string | The order number is stored in the `track` column of the Orders table. |

#### Request

```json
{
  "track": 123456
}
```

#### Successful response

```json
HTTP/1.1 200
{
    ok: true
}
```

#### Request without number

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data for search"
}
```

#### Request with non-existent number

```json
HTTP/1.1 404 Not Found
{
  "message": "Order not found"
}
```

#### Order is being processed

```json
HTTP/1.1 409 Conflict
{
  "message": "Order is being processed"
}
```

### Orders - Complete the order

> `PUT` /api/v1/orders/finish/:id

#### Parameter

| Field | Type   | Description                                                                        |
| :---- | :----- | :--------------------------------------------------------------------------------- |
| `id`  | number | The order number is stored in the `id` column of the Orders table. |

#### Request

```json
{
  "id": 123
}
```

#### Successful response

```json
HTTP/1.1 200
{
    ok: true
}
```

#### Request without number

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data for search"
}
```

#### Request with non-existent number

```json
HTTP/1.1 404 Not Found
{
  "message": "No order with this ID"
}
```

#### Request with non-existent courier number

```json
HTTP/1.1 404 Not Found
{
  "message": "No courier with this ID"
}
```

#### Cannot complete the order

```json
HTTP/1.1 409 Conflict
{
  "message": "This order cannot be completed"
}
```

### Orders - Order creation

> `POST` /api/v1/orders

#### Parameter

| Field                | Type     | Description                                                                                                                             |
| :------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| `firstName`          | string   | The customer name is written to the `firstName` column of the Orders table.                                               |
| `lastName`           | string   | The customer last name is written to the `lastName` column of the Orders table.                                           |
| `address`            | string   | The customer address is written to the `address` column of the Orders table.                                  |
| `metroStation`       | string   | The nearest metro station to the customer is written to the `subwayStation` column of the Orders table. |
| `phone`              | string   | The customer phone is written to the `phone` column of the Orders table.                                      |
| `rentTime`           | number   | The number of rental days is written to the `rentTime` column of the Orders table.                                        |
| `deliveryDate`       | string   | The delivery date is written to the `deliveryDate` column of the Orders table.                        |
| `comment` `optional` | string   | A customer comment is written to the `comment` column of the Orders table.                              |
| `color` `optional`   | string[] | The preferred colors are written to the `color` column of the Orders table.                                                 |

#### Request

```json
{
  "firstName": "Naruto",
  "lastName": "Uchiha",
  "address": "Konoha, 142 apt.",
  "metroStation": 4,
  "phone": "+7 800 355 35 35",
  "rentTime": 5,
  "deliveryDate": "2020-06-06",
  "comment": "Saske, come back to Konoha",
  "color": ["BLACK"]
}
```

#### Order created successfully

```json
HTTP/1.1 201 Created {
    track: 124124
}
```

### Orders - Get an order by its number

> `GET` /api/v1/orders/track

#### Parameter

| Field | Type   | Description                       |
| :---- | :----- | :-------------------------------- |
| `t`   | number | Order tracking number. |

#### Request

> /api/v1/orders/track?`t=123456`

#### Success response

```json
HTTP/1.1 200
{
         "order": {
             "id": 2,
             "firstName": "Naruto",
             "lastName": "Uzumaki",
             "address": "Kanoha, 142 apt.",
             "metroStation": "1",
             "phone": "+7 800 355 35 35",
             "rentTime": 5,
             "deliveryDate": "2020-06-06T00:00:00.000Z",
             "track": 521394,
             "status": 1,
             "color": [
                 "BLACK"
             ],
             "comment": "Saske, come back to Kanoha",
             "cancelled": false,
             "finished": false,
             "inDelivery": false,
             "courierFirstName": "Kaneki"
             "createdAt": "2020-06-08T14:40:28.219Z",
             "updatedAt": "2020-06-08T14:40:28.219Z"
  }
}
```

#### Request without number

```json
HTTP/1.1 400 Bad Request
{
  "message":  "Insufficient data for search"
}
```

#### Request with non-existent number

```json
HTTP/1.1 404 Not Found
{
  "message": "Order not found"
}
```

### Orders - Get a list of orders

#### Parameter

| Field | Type   | Description                       |
| :---- | :----- | :-------------------------------- |
| `courierId` `optional`   | number | Courier ID. If specified, returns all active and completed orders of the courier. |
| `nearestStation` `optional`   | string | Metro station filter. Sent as JSON, for example, `{ nearestStation: ["1", "2"] }`. When sent, the final result is filtered by the specified metro stations. |
| `limit` `optional`   | number | Number of orders per page. `Maximum: 30`. `Default value: 30`. |
| `page` `optional`   | number | Page number of current order view. `Default value: 0`. |

#### All active/completed orders of the courier

> /api/v1/orders?`courierId=1`

#### All active/completed orders of the courier at "First Avenue"(1) or "Broadway Junction"(2) stations

> /api/v1/orders?courierId=1&`nearestStation=["1", "2"]`

#### 10 available orders for collection by courier

> /api/v1/orders?`limit=10`&`page=0`

#### 10 available orders for collection by courier near "York Street"(110) metro station

> /api/v1/orders?`limit=10`&`page=0`&`nearestStation=["110"]`

#### Successful request without courierId

```json
HTTP/1.1 200
 {
    "orders": [
        {
            "id": 4,
            "courierId": null,
            "firstName": "John",
            "lastName": "Doe",
            "address": "1300 1st St",
            "metroStation": "2",
            "phone": "423424234432",
            "rentTime": 4,
            "deliveryDate": "2020-06-21T21:00:00.000Z",
            "track": 400443,
            "color": [
                "BLACK",
                "GREY"
            ],
            "comment": "Comment from John",
            "createdAt": "2020-06-21T13:21:30.067Z",
            "updatedAt": "2020-06-21T13:21:30.067Z",
            "status": 0
        },
        {
            "id": 5,
            "courierId": null,
            "firstName": "Jane",
            "lastName": "Doe",
            "address": "East 2nd Street, 601",
            "metroStation": "4",
            "phone": "1441412414",
            "rentTime": 4,
            "deliveryDate": "2020-06-08T21:00:00.000Z",
            "track": 189237,
            "color": [
                "BLACK",
                "GREY"
            ],
            "comment": "Comment from Jane",
            "createdAt": "2020-06-21T13:23:09.404Z",
            "updatedAt": "2020-06-21T13:23:09.404Z",
            "status": 0
        }
    ],
    "pageInfo": {
        "page": 0,
        "total": 3,
        "limit": 2
    },
    "availableStations": [
        {
            "name": "5th Street",
            "number": "2",
            "color": "#0173BD"
        },
        {
            "name": "7th Street/Metro Center",
            "number": "3",
            "color": "#0173BD"
        },
        {
            "name": "7th Street/Metro Center",
            "number": "4",
            "color": "#EC161F"
        }
    ]
 }
```

#### Request with non-existent ID

```json
HTTP/1.1 404 Not Found
{
  "message": "Courier with ID {courierId} not found"
}
```

## Utilities

### Utilities - Search metro stations by name

> `GET` /api/v1/stations/search

#### Parameter

| Field | Type   | Description                       |
| :---- | :----- | :-------------------------------- |
| `s` | string | Station search string. |

#### Search for metro "Del"
> /api/v1/stations/search?`s=Del`

#### Successful search

```json
HTTP/1.1 200 OK
[
    {
       "number": "25",
       "name": "Del Amo",
       "color": "#0173BD"
    },
    {
       "number": "26",
       "name": "Del Mar",
       "color": "#A05DA5"
   }
]
```

### Utilities - Ping server

> `GET` /api/v1/ping

#### Success response

```json
HTTP/1.1 200 Ok
pong;
```