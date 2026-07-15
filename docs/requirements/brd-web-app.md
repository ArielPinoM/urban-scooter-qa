# Web Application Requirements - Urban Scooter

## Supported Versions

The application supports the following browsers: Opera 71 or higher, and Chrome 85 or higher. Screen resolutions of 1280x720 and 1920x1080 are supported.

## Home Screen

There is a title and a scooter layout. As the user scrolls, an animation is displayed: the layout is replaced by a photo and a table with the product description appears.

![](./assets/web/home-screen.jpg)

![](./assets/web/home-screen-scrolled.jpg)

There are two buttons in the home header: "Pedir" and "Estado del pedido".

The user is prompted to accept the use of cookies.

![](./assets/web/cookies-popup.jpg)

When the user scrolls to the third block, they find the following information: "Cómo funciona" and "Preguntas frecuentes".

![](./assets/web/como-funciona-screen.jpg)

![](./assets/web/preguntas-frecuentes-screen.jpg)

## Screen: "Realizar pedido"

To place an order, the user must complete two forms: "Para quién es el scooter" and "Alquiler".

### For whom the scooter is intended

![](./assets/web/para-quien-es-el-scooter-form.jpg)

The fields are: "Nombre", "Apellido", "Dirección: a dónde llevar el scooter", "Estación de metro", and "Teléfono: el repartidor o repartidora llamará".
All fields are mandatory. If the user does not complete them correctly, they cannot proceed to the next page. At the bottom, the "Siguiente" button leads the user to the "Alquiler" form.

### Rental

![](./assets/web/alquiler-form.jpg)

The fields are "Fecha de entrega", "Periodo de alquiler", "Color del scooter", and "Comentario".

The fields "Fecha de entrega" and "Periodo de alquiler" are mandatory. "Color" and "Comentario" are optional.

**The "Atrás" button**. Clicking it takes the user back to the "Para quién es el scooter" page. When the user navigates between pages, the information entered is saved.

**The "Pedir" button**. If all the fields are filled in correctly, the order is placed when the user clicks the "Pedir" button. A popup appears with the message "Número de pedido NNNNN. Escríbelo: será útil para darle seguimiento al estado" and the "Comprueba el estado" button. The "Comprueba el estado" button takes the user to the "Estado del pedido" screen, where the "Número de pedido" field is already filled in.

![](./assets/web/el-pedido-ha-sido-realizado-popup.jpg)

If all required fields are not completed correctly, clicking the "Pedir" button displays an error message: "Introduce un <nombre de campo> correcto".

The user can place multiple orders consecutively.

## Screen: "Estado del pedido"

![](./assets/web/estado-del-pedido-screen.jpg)

If the user clicks "Estado del pedido" in the home header, the "Número de pedido" field appears. The user must enter a value and press Enter. If the order number is entered correctly, the following information appears:

- User order details: name, surname, address, and other related information. A rule applies to all fields: if the text does not fit on one line, it wraps to the second line.
- The order status flow. The current state is highlighted in black, while the others are gray. When the status is passed, the number before it changes to a check mark.

If the order number is entered incorrectly, an error message appears: "No existe tal pedido. ¿Seguro que ese es el número correcto?".

There are four states on the order status screen. Only one can be active at any given time and it indicates the current stage of the order:

- **"El scooter está en el almacén"**. This is activated when the user has placed an order.
- **"El repartidor o repartidora está en camino"**. This is activated when the courier confirms in their application that they have accepted the order. When this state is active, the courier name appears in the message: "El repartidor Frodo está en camino". If the courier name is too long and the message does not fit on one line, the text wraps to the second line.
- **"El servicio de entrega llegó"**. This is activated when the courier presses the "Completar" button in their application.
- **"Bien, vamos a dar un paseo"**. This is activated when the courier confirms that the order has been completed. The text "El alquiler finalizará el" appears below the status title. The displayed time is calculated from the moment the scooter is delivered to the user, based on the number of days. When the rental period ends, the status changes to "Periodo de alquiler terminado" with the legend "El repartidor o repartidora recogerá el scooter pronto".

The user can enter another order number and view its status.

### Order cancellation

If the user clicks it, a popup appears with the text "¿Deseas cancelar el pedido?". There are two buttons in the popup: "Cancelar" and "Atrás".

![](./assets/web/deseas-cancelar-el-pedido-popup.jpg)

If the user clicks "Atrás", they return to the order status page.

If the user clicks "Cancelar", a popup appears with the text "El pedido ha sido cancelado. Siéntete libre de volver en cualquier momento :)" and a button "Bien". The "Bien" button takes the user to the home page.

![](./assets/web/el-pedido-ha-sido-cancelado-popup.jpg)

The user can cancel the order before the courier picks it up. Once the courier already has the order, the "Cancelar el pedido" button cannot be clicked.

The canceled order is removed from the system and the user can no longer view it.

### Delayed order

An order is considered delayed when the courier does not deliver it on time. For example, a user placed an order for a scooter on January 1. If the scooter is not delivered by 11:59 p.m. on January 1 or earlier, the order is delayed.

If the order is delayed, its status changes to "El repartidor o repartidora se demoró" and the message changes to "No podremos entregar el scooter a tiempo. Para aclarar el estado de tu pedido, llama a soporte: 0101." The status and the legend are highlighted in red.

![](./assets/web/delayed-order.jpg)

If a delayed order has been delivered to the user, the countdown for the end of the rental period begins when the order is received.

## Front-end enhancement

A fifth state has been added to the status flow: "El periodo de alquiler terminó". This is a feature that was implemented only on the front-end, while the back-end is not yet ready. This message used to appear instead of the fourth state when the rental period was about to end. Now the text of the fourth state does not change; it simply becomes gray, like the other states.

![](./assets/web/4th-status.jpg)

An example response is described in the API documentation under the _Pedidos_ section: get order by its number.

New status number in the request = 3.

## Field constraints

| Field name | Field type | Possible values | Required |
| :--------- | :--------- | :------------- | :------- |
| Nombre | Text field | Only Latin letters, spaces, and hyphens. Length must be 2 to 15 characters. If entered incorrectly, it is highlighted in red. The error message is "Introduce un nombre correcto". | Yes |
| Apellido | Text field | Only Latin letters, spaces, and hyphens. Length must be 2 to 15 characters. If the input is invalid, it is highlighted in red and the error message "Introduce un apellido válido" appears. | Yes |
| Dirección | Text field | Only Latin alphabet letters, numbers, spaces, hyphens, periods, and commas. Length must be 5 to 50 characters. Leading and trailing spaces are removed when focus is lost. If the input is invalid, it is highlighted in red and the error message "Introduce una dirección válida" appears. | Yes |
| Estación de metro | Text field with suggestions | Los Angeles metro stations. The station list is stored in the back-end (in the API). | Yes |
| Teléfono | Text field | Only numbers and the "+" symbol. Length must be 10 to 12 characters. If entered incorrectly, it is highlighted in red. The error message is "Introduce un número de teléfono válido". | Yes |
| Fecha de entrega | Dropdown calendar. Appears when the user clicks the input field | Only dates from the following day onward can be selected. The calendar opens with the current month. Values cannot be entered manually in the field. When the user selects a date, the value appears immediately in the field. The user can select a different date; the field is highlighted in blue. | Yes |
| Periodo de alquiler | Dropdown list | A value from 1 to 7 days can be selected. | Yes |
| Color | Checkbox | Black, gray. One or both options can be selected. | No |
| Comentario | Text field | Only Latin alphabet letters, numbers, spaces, hyphens, periods, and commas. Maximum length is 24 characters. | No |

## Preguntas frecuentes
- ¿Cuánto cuesta? ¿Y cómo lo puedo pagar?

Son $8 por día. El servicio de entrega recibe pagos en efectivo o con tarjeta.

- ¿Entregan un cargador junto con el scooter?

El scooter viene completamente cargado. Eso es suficiente para ocho días de paseo sin parar. No necesitarás un cargador.

- ¿Me pueden traer el scooter hoy?

Solo para el día siguiente después de realizar el pedido, pero próximamente podremos entregarlos antes.

- ¡Quiero varios scooters al mismo tiempo! ¿Es posible?

Por ahora, solo es un scooter por pedido. Si quieres dar un paseo con amigos, se pueden hacer varios pedidos.

- ¿Puedo extender un pedido o devolver el scooter antes?

¡Todavía no! Si es algo urgente, siempre puedes llamar a soporte al número 1010.

- ¿Puedo cancelar el pedido?

Sí, puedes cancelarlo antes de que el repartidor o repartidora te entregue el scooter. No habrá multa y no te pediremos una explicación.

- ¿Cómo se calcula el tiempo de alquiler?

Digamos que haces un pedido para el 8 de mayo. Te entregaremos el scooter en esa fecha antes del final del día. El tiempo de alquiler inicia cuando pagas tu pedido al servicio de entrega. Si te entregamos el scooter el 8 de mayo a las 8:30 p.m., el alquiler diario terminará el 9 de mayo a las 8:30 p.m.
