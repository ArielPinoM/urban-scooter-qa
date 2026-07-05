# API DOC: Ez-scooter

`version: 1.0.0`

## Couriers

### Couriers - Obtener el número de pedidos del mensajero

> `GET` /api/v1/courier/:id/ordersCount

#### Parámetro

| Campo | Tipo   | Descripción                        |
| :---- | :----- | :--------------------------------- |
| `id`  | number | Número de mensajero {"id": 123456} |

#### Número de pedidos del mensajero "1"

> /api/v1/courier/`1`/ordersCount

#### Éxito de respuesta

```json
HTTP/1.1 200
{
  "id": "123456",
  "ordersCount": "100500"
}
```

#### Solicitud sin número

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay suficientes datos para la búsqueda"
}
```

#### Solicitud con un número no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "Mensajero no encontrado"
}
```

## Mensajero

### Mensajero - Crear un mensajero

> `POST` /api/v1/courier

#### Parámetro

| Campo       | Tipo   | Descripción                                                                                                              |
| :---------- | :----- | :----------------------------------------------------------------------------------------------------------------------- |
| `login`     | string | El inicio de sesión del mensajero se escribe en la columna `login` (inicio de sesión) de la hoja de cálculo Mensajeros.  |
| `password`  | string | La contraseña del mensajero, el hash del valor se escribe en la columna `passwordHash` de la hoja de cálculo Mensajeros. |
| `firstName` | string | El nombre del mensajero se escribe en la columna `firstName` de la hoja de cálculo Mensajeros.                           |

#### Solicitud

```json
{
  "login": "ninja",
  "password": "1234",
  "firstName": "saske"
}
```

#### La cuenta ha sido creada con éxito

```json
HTTP/1.1 201 Created
{
    ok: true
}
```

#### Solicitud sin inicio de sesión ni contraseña

```json
HTTP/1.1 400 Bad Request
{
  "message": "No hay suficientes datos para crear una cuenta"
}
```

#### Solicitud con un inicio de sesión duplicado

```json
HTTP/1.1 409 Сonflict
{
  "message": "Este inicio de sesión no está disponible"
}
```

### Mensajero - El inicio de sesión del mensajero en el sistema

> `POST` /api/v1/courier/login

#### Parámetro

| Campo      | Tipo   | Descripción                                                                                                              |
| :--------- | :----- | :----------------------------------------------------------------------------------------------------------------------- |
| `login`    | string | El inicio de sesión del mensajero se escribe en la columna `login` (inicio de sesión) de la hoja de cálculo Mensajeros.  |
| `password` | string | La contraseña del mensajero, el hash del valor se escribe en la columna `passwordHash` de la hoja de cálculo Mensajeros. |

#### Solicitud

```json
{
  "login": "ninja",
  "password": "1234"
}
```

#### Inicio de sesión exitoso

```json
HTTP/1.1 200
{
    id: 12345
}
```

#### Solicitud sin inicio de sesión ni contraseña

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay datos suficientes para iniciar sesión"
}
```

#### Solicitud con un par de inicio de sesión y contraseña no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "Account not found"
}
```

### Mensajero - Eliminar un mensajero

> `DELETE` /api/v1/courier/:id

#### Parámetro

| Campo | Tipo   | Descripción                                                                             |
| :---- | :----- | :-------------------------------------------------------------------------------------- |
| `id`  | string | El número de mensajero se almacena en la columna `id` de la hoja de cálculo Mensajeros. |

#### Solicitud

```json
{
  "id": "3"
}
```

#### El mensajero ha sido eliminado con éxito

```json
HTTP/1.1 200 OK
{
    ok: true
}
```

#### Solicitud sin ID

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay datos suficientes para eliminar el mensajero"
}
```

#### Solicitud con una ID no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "No hay un mensajero con esta ID"
}
```

## Pedidos

### Pedidos - Aceptar el pedido

> `PUT` /api/v1/orders/accept/:id

#### Parámetro

| Campo       | Tipo   | Descripción                                                                                   |
| :---------- | :----- | :-------------------------------------------------------------------------------------------- |
| `id`        | number | El número del pedido se almacena en la columna `id` de la hoja de cálculo Pedidos.            |
| `courierId` | number | ID del mensajero (courierId) se almacena en la columna `id` de la hoja de cálculo Mensajeros. |

#### Solicitud

> /api/v1/orders/accept/`1`?courierId=`213`

#### Respuesta exitosa

```json
HTTP/1.1 200
{
    ok: true
}
```

#### Solicitud sin número

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay suficientes datos para la búsqueda"
}
```

#### Solicitud con un número no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "No hay un pedido con esta ID"
}
```

#### Solicitud con un número de mensajero no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "No hay un mensajero con esta ID"
}
```

#### El pedido ya fue procesado

```json
HTTP/1.1 409 Conflict
{
  "message": "El pedido se está procesando"
}
```

#### Sin ID del mensajero o ID del pedido

```json
HTTP/1.1 400 Conflict
{
  "message": "No hay suficientes datos para la búsqueda"
}
```

### Pedidos - Cancelar el pedido

> `POST` /api/v1/orders/cancel

#### Parámetro

| Campo   | Tipo   | Descripción                                                                                         |
| :------ | :----- | :-------------------------------------------------------------------------------------------------- |
| `track` | string | El número del pedido se almacena en la columna `track` (seguimiento) de la hoja de cálculo Pedidos. |

#### Solicitud

```json
{
  "track": 123456
}
```

#### Respuesta exitosa

```json
HTTP/1.1 200
{
    ok: true
}
```

#### Solicitud sin número

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay suficientes datos para la búsqueda"
}
```

#### Solicitud con un número no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "Pedido no encontrado"
}
```

#### El pedido se está procesando

```json
HTTP/1.1 409 Conflict
{
  "message": "El pedido se está procesando"
}
```

### Pedidos - Completar el pedido

> `PUT` /api/v1/orders/finish/:id

#### Parámetro

| Campo | Tipo   | Descripción                                                                        |
| :---- | :----- | :--------------------------------------------------------------------------------- |
| `id`  | number | El número del pedido se almacena en la columna `id` de la hoja de cálculo Pedidos. |

#### Solicitud

```json
{
  "id": 123
}
```

#### Respuesta exitosa

```json
HTTP/1.1 200
{
    ok: true
}
```

#### Solicitud sin número

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay suficientes datos para la búsqueda"
}
```

#### Solicitud con un número no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "No hay un pedido con esta ID"
}
```

#### Solicitud con un número de mensajero no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "No hay un mensajero con esta ID"
}
```

#### No se puede completar el pedido

```json
HTTP/1.1 409 Conflict
{
  "message": "Este pedido no se puede completar"
}
```

### Pedidos - Creación de un pedido

> `POST` /api/v1/orders

#### Parámetro

| Campo                | Tipo     | Descripción                                                                                                                             |
| :------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| `firstName`          | string   | El nombre del cliente se escribe en la columna `firstName` de la hoja de cálculo Pedidos.                                               |
| `lastName`           | string   | El apellido del cliente se escribe en la columna `lastName` de la hoja de cálculo de Pedidos.                                           |
| `address`            | string   | La dirección del cliente se escribe en la columna `address` (dirección) de la hoja de cálculo Pedidos.                                  |
| `metroStation`       | string   | La estación de metro más cercana al cliente se escribe en la columna `subwayStation` (estación de metro) de la hoja de cálculo Pedidos. |
| `phone`              | string   | El teléfono del cliente se escribe en la columna `phone` (teléfono) de la hoja de cálculo Pedidos.                                      |
| `rentTime`           | number   | El número de días de alquiler se escribe en la columna `rentTime` de la hoja de cálculo Pedidos.                                        |
| `deliveryDate`       | string   | La fecha de entrega se escribe en la columna `deliveryDate` (fecha de entrega) de la hoja de cálculo de Pedidos.                        |
| `comment` `optional` | string   | El comentario de un cliente se escribe en la columna `comment` (comentario) de la hoja de cálculo Pedidos.                              |
| `color` `optional`   | string[] | Los colores preferidos se escriben en la columna `color` de la hoja de cálculo Pedidos.                                                 |

#### Solicitud

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

#### El pedido ha sido creado con éxito

```json
HTTP/1.1 201 Created {
    track: 124124
}
```

### Pedidos - Obtener un pedido por su número

> `GET` /api/v1/orders/track

#### Parámetro

| Campo | Tipo   | Descripción                       |
| :---- | :----- | :-------------------------------- |
| `t`   | number | Número de seguimiento del pedido. |

#### Solicitud

> /api/v1/orders/track?`t=123456`

#### Éxito de respuesta

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

#### Solicitud sin número

```json
HTTP/1.1 400 Bad Request
{
  "message":  "No hay suficientes datos para la búsqueda"
}
```

#### Solicitud con un número no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "Pedido no encontrado"
}
```


### Pedidos - Obtener una lista de pedidos

#### Parámetro

| Campo | Tipo   | Descripción                       |
| :---- | :----- | :-------------------------------- |
| `courierId` `opcional`   | number | ID del mensajero. Si se especifica, devuelve todos los pedidos activos y completados del mensajero. |
| `nearestStation` `optional`   | string | Filtro de estaciones del metro. Enviado como JSON, por ejemplo, `{ nearestStation: ["1", "2"] }`. Al enviar, el resultado final se filtra por las estaciones de metro especificadas. |
| `limit` `optional`   | number | Número de pedidos por página. `Máximo: 30`. `Valor por defecto: 30`. |
| `page` `optional`   | number | Página de visualización de pedidos actuales. `Valor por defecto: 0`. |

#### Todos los pedidos del mensajero activos/completados

> /api/v1/orders?`courierId=1`

#### Todos los pedidos del mensajero activos/completados en las estaciones "First Avenue"(1) o "Broadway Junction"(2)

> /api/v1/orders?courierId=1&`nearestStation=["1", "2"]`

#### 10 pedidos disponibles para recolección por mensajero

> /api/v1/orders?`limit=10`&`page=0`

#### 10 pedidos disponibles para recolección por mensajero cerca de la estación de metro "York Street"(110)

> /api/v1/orders?`limit=10`&`page=0`&`nearestStation=["110"]`

#### Solicitud exitosa sin courierId

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

#### Solicitud con una ID no existente

```json
HTTP/1.1 404 Not Found
{
  "message": "No se encontró el mensajero con ID {courierId}"
}
```

## Utilidades

### Utilidades - Buscar estaciones de metro por nombre

> `GET` /api/v1/stations/search

#### Parámetro

| Campo | Tipo   | Descripción                       |
| :---- | :----- | :-------------------------------- |
| `s` | string | String de búsqueda de estación. |

#### Buscar metro "Del"
> /api/v1/stations/search?`s=Del`

#### Búsqueda exitosa

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

### Utilidades - Servidor de ping

> `GET` /api/v1/ping

#### Éxito de respuesta

```json
HTTP/1.1 200 Ok
pong;
```