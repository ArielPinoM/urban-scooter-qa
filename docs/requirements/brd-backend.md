# Requirements for the application back-end

## Technologies

- The application language is JavaScript.

- It runs in the Node.js v12.17.0 environment

- Access to the application through the HTTP 1.1 protocol.

## General Requirements

The application uses the PostgreSQL database. The application interacts with the database through the npm package `sequelize` over the `pg` package. `sequelize` is an ORM for working with different databases in node.js.

Requests are logged through the `winston` module. Application documentation is organized through the `apidoc` module.

The application must comply with REST requirements.

The application must have a global error handler. If exceptions occur, they must be handled and the application must continue running.

Application errors (failed requests, exceptions, non-2XX responses) must be logged to a separate `error.log` file.

## URL Requirements

### Helper URLs

- There must be a URL that helps you check that the back-end is running and accepting requests. Status `200 OK` should be returned if the response is successful.

- There must be a URL through which metro station search works. If the search is successful, the station number, color, and name should be returned. If there is more than one station, the number, color, and name of each station must be returned. If no stations are found, an empty list must be returned.

### URLs for Couriers [Test]

- **The URL must be present: upon access, a courier can register in the application. The URL must accept the username, password, and courier name. The login, password hash, and courier name must be written to the `login`, `passwordHash`, and `firstName` fields of the Couriers table. The `passwordHash` field stores the password hash. It is generated using standard functions, so you can check the hash-password match through authorization.**

- **The login field must be unique. If registration is successful, the corresponding entry must appear in the database; if unsuccessful, an error must be returned. Learn more about errors in the documentation `/docs/en/#api-Orders-CreateOrder`.**

- There must be a URL to log in to a courier account. The courier username and password must be sent when logging in. The courier ID must be returned when successfully logged in. If login fails, an error must be returned.

- **The URL to delete the courier account must be present. When accessed, the `ID` of the courier in the Couriers table must be obtained. When deleting, linked orders in the Orders table must be deleted.**

### URLs for Orders [Test]

Whenever any of the URLs returns complete order data, the response must also contain the status of each order. The status should have these values:

- `0`: order was created, nothing else happened;

- `1`: courier has accepted the order;

- `2`: order has been completed;

- `-1`: order has been canceled.

The status must be calculated in relation to the values of the fields in the database in the Orders table (see "Database Content Description"). The fields are listed in priority order:

- `finished = true` → status = 2

- `cancelled = true` → status = -1

- `inDelivery = true` → status = 1

- `Other cases` → status = 0

There must be a URL to create an order; when creating an order, the following parameters are specified:

- first name

- last name

- address

- nearest metro station

- phone

- number of rental days

- delivery date

- comment

- list of matching colors

An individual tracking number must be assigned to the order when it is created.

The sent parameters are written to the `Orders` table as follows:

- first name: `firstName`

- last name: `lastName`

- address: `address`

- nearest metro station: `subwayStation`

- phone: `phone`

- rental period: `rentTime`

- delivery date: `deliveryDate`

- comment: `comment`

- list of matching colors: `color`

- tracking number: `track`

If the order was created successfully, its tracking number must be returned; otherwise, an error must be returned. Read more about errors in the documentation: `/docs/en/#api-Orders-CreateOrder`.

- **There must be a URL to retrieve order data from its tracking number. A number must be obtained on access. If an order matching is found, its data must be returned; otherwise, an error must be returned.**

- There must be a URL for the courier to accept the order. The URL takes the order tracking number and the courier ID. If there is a problem accepting the order, an error must be returned.

- There must be a URL **to cancel the order**. The URL accepts the order tracking number. In case of unsuccessful cancellation, an error must be returned.

- There must be a URL to complete the order. The order number is sent when logging in. In case it is not completed correctly, an error must be returned.

- There must be a URL to retrieve all orders that match the specified parameters. The search parameters are the nearest metro station and the courier ID. Output record limits and page number must also be sent. Read more about errors and use cases in the documentation: `/docs/#api-Orders-GetOrdersPageByPage`.

- The URL for the number of completed orders by courier must be present. The courier ID must be obtained when logging in. Read more about errors and use cases in the documentation: `/docs/en/#api-Couriers-GetOrdersCountByCourierId`.

### Field Restrictions [Test]

| Element      | Requirements                                                          | Required |
| :------------ | :------------------------------------------------------------------ | :---------- |
| **login**     | Latin letters only. Text length is 2 to 10 characters. | ☑️          |
| **firstName**  | Latin letters only. Text length is 2 to 10 characters. | ⬜          |
| **password** | Integers only. Length is exactly 4 characters.   | ☑️          |

## Database Content Description

The database consists of two tables: `Couriers` and `Orders`. The first table contains data about couriers, the second stores data about orders.

### Couriers

| Name           | Type   | Description                                     |
| :--------------- | :----- | :--------------------------------------------- |
| **login**        | string | Login of the courier. |
| **passwordHash** | string | Password hash of the courier.  |
| **firstName**    | string | First name of the courier.    |

### Orders

| Name           | Type             | Description                                               |
| :--------------- | :--------------- | :------------------------------------------------------- |
| **courierId**    | number           | The field that links this table to the `Couriers` table. |
| **firstName**    | string           | Customer first name.                                      |
| **lastName**     | string           | Customer last name.                                    |
| **address**      | string           | Address.                                               |
| **metroStation** | string           | Nearest metro station.                           |
| **phone**        | string           | Phone number.                                      |
| **rentTime**     | number           | Rental period.                                     |
| **deliveryDate** | date            | Delivery date.                                        |
| **track**        | number           | Tracking number.                                   |
| **color**        | array of strings | Preferred scooter colors.                           |
| **comment**      | string           | A comment for the courier.          |
| **cancelled**    | string           | A comment for the courier.          |
| **finished**     | boolean           | The order has been delivered.                               |
| **inDelivery**   | boolean           | The order is being delivered.                            |