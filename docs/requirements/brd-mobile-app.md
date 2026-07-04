# Requisitos aplicación móvil - Urban Scooter

![](./assets/mobile/login-screen.jpg)

## Pantalla "Inicio de sesión"

1. La primera vez que un usuario o usuaria inicia sesión en la aplicación, aparece una pantalla de inicio de sesión.
2. Si el repartidor o repartidora ya ha iniciado sesión, verá la pantalla de lista de pedidos predeterminada.
3. Hay dos campos de entrada en la pantalla: Iniciar sesión y Contraseña. Hay un botón "Iniciar sesión".
4. Si un usuario o usuaria toca "Olvidé la contraseña", aparecerá una notificación con el texto "Contacta a la gerencia: 0101" y el botón "Aceptar".
5. El usuario o usuaria puede salir de la aplicación desde cualquier pantalla. Luego, al iniciar sesión, volverá a la pantalla de inicio de sesión.

### Restricciones de los campos

| Elemento       | Requisitos                                                                                                                                                                                               |
| :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Iniciar sesión | Solo letras latinas. La longitud del texto es de 2 a 10 caracteres. Si el nombre de usuario o la contraseña se introducen de forma incorrecta, aparece la notificación "Usuario o contraseña no válido". |
| Contraseña     | Solo números enteros. La longitud es exactamente de 4 caracteres. Si el nombre de usuario o la contraseña se introducen de forma incorrecta, aparece la notificación "Usuario o contraseña no válido".   |

## Pantalla "Lista de pedidos"

![](./assets/mobile/order-list-screen.jpg)

Hay dos pestañas en la pantalla: "Todos los pedidos" y "Mis pedidos".

En la pestaña "Todos los pedidos", los repartidores y repartidoras ven la misma lista de pedidos: estos son pedidos no reclamados.

Tan pronto como un repartidor o repartidora acepta el pedido, este se mueve a la pestaña "Mis pedidos" y los otros repartidores y repartidoras ya no pueden verlo.

Dentro de la pestaña "Mis pedidos", el repartidor o repartidora ve los pedidos que ha aceptado.

Para actualizar la lista, un usuario o usuaria debe deslizar para actualizar.

Deslizar para actualizar:

1. En la pestaña "Todos los pedidos": los pedidos que fueron aceptados por otro repartidor o repartidora desaparecen de la lista.

2. En la pestaña "Todos los pedidos": se eliminan los pedidos que han sido cancelados por el usuario o usuaria.

3. En las pestañas "Todos los pedidos" y "Mis pedidos": las tarjetas se ordenan por la fecha de entrega especificada por el usuario o usuaria. Los pedidos atrasados están en la parte superior.

Aquí es cuando se actualiza la lista de pedidos:

1. Cuando un usuario o usuaria desliza para actualizar.

2. Si un usuario o usuaria va a la pestaña "Mis pedidos" en la pantalla de inicio y luego regresa a la pestaña "Todos los pedidos".

3. Si un usuario o usuaria aplica un filtro por estación de metro.

Aquí es cuando no se actualiza la lista de pedidos:

1. Si un usuario o usuaria acepta el pedido, este se mueve a "Mis pedidos", pero el resto de la lista no se actualiza.

Las características de la pantalla "Lista de pedidos":

1. Cuando no hay pedidos, se muestra la pantalla "Sin pedidos". Para actualizar la pantalla, un usuario o usuaria debe deslizar para actualizar.

![](./assets/mobile/no-orders-screen.jpg)

2. Cuando el usuario o usuaria realiza un pedido, aparece una versión corta de la tarjeta de pedido.

3. La lista de pedidos está ordenada por prioridad de entrega: los atrasados están en la parte superior. Un pedido se considera atrasado si no se entregó al cliente antes a las 11:59 p.m. o antes en el día requerido. El marco y la fecha de la tarjeta caducada están resaltados en rojo y la negrita del texto es Media. Esta condición funciona para las listas "Todos los pedidos" y "Mis pedidos".

4. Dentro de la pestaña "Todos los pedidos", hay un filtro para seleccionar una estación de metro. Con este, el repartidor o repartidora puede configurar para qué estaciones quiere ver los pedidos. Al tocar el filtro, se abre una lista que se forma a partir de las estaciones donde existen pedidos. Si hay dos o más pedidos con la misma estación de metro, el nombre de la estación sólo aparece una vez en el filtro: las mismas estaciones no se duplican.

5. La tarjeta de filtro aumenta de tamaño a medida que se agregan estaciones de metro. La tarjeta tiene capacidad para un máximo de 8 estaciones y, a partir de la novena, aparece una barra de desplazamiento.

6. La tarjeta de pedido tiene una versión corta y una completa.

- Campos para la versión corta: "Dirección", "Fecha de entrega" y estación de metro seleccionada.

- Campos para la versión completa: "Dirección", "Fecha de entrega" y estación de metro seleccionada. Se agregan "Nombre", "Apellido", "Teléfono", "Color" y "Comentario". Si el usuario o usuaria no completó el campo "Color", se escribe cualquiera".

![](./assets/mobile/all-orders-screen.jpg)

7. Un usuario o usuaria puede cambiar la versión de la tarjeta tocando la tarjeta. Esto funciona para las pestañas "Todos los pedidos" y "Mis pedidos".

8. Cuando un usuario o usuaria cambia al modo de tarjeta completa, el botón "Aceptar" permanece en su lugar. Las cartas que siguen en la lista se mueven hacia abajo.

9. Para aceptar el pedido, toca el botón "Aceptar"; esto funciona tanto para la versión corta como para la completa de una tarjeta.

10. Al tocar el botón, aparece una notificación con el texto "¿Deseas aceptar el pedido?" y dos botones: "Sí" y "No". Tocar "No" devolverá al usuario o usuaria a la lista de pedidos y el botón "Aceptar" permanecerá activo. Tocar "Sí" confirma la aceptación del pedido.

![](./assets/mobile/desea-aceptar-pedido-popup.jpg)

11. Los usuarios o usuarias no pueden aceptar el pedido de otra persona o un pedido cancelado. Aparece el mensaje "No puedes aceptar el pedido. Ya ha sido aceptado por otro repartidor o repartidora, o el usuario o usuaria lo ha cancelado.”

12. Cuando se acepta el pedido, la tarjeta sale de la lista "Todos los pedidos", con una animación de movimiento hacia arriba. Cuando se acepta el pedido, la tarjeta sale de la lista "Todos los pedidos", con una animación de movimiento hacia arriba.

13. Lógica del punto azul: aparece si hay tarjetas que no han sido visualizadas en la pestaña "Mis pedidos". No hay una transición automática a la pestaña "Mis pedidos".

![](./assets/mobile/my-orders-blue-dot.jpg)

14. La tarjeta aceptada por el repartidor o repartidora se coloca en la pestaña "Mis pedidos". El botón cambia a "Completar". Un usuario o usuaria puede completar el pedido con un toque en el botón "Completar", tanto en la vista de tarjeta corta como en la completa.

![](./assets/mobile/completar-button-on-order-card.jpg)

15. Si un usuario o usuaria hace clic en "Completar", verá la notificación "¿Has completado el pedido?" y dos botones: "Sí" y "No". Tocar "Sí" confirma que el pedido está completo.

![](./assets/mobile/has-completado-pedido-popup.jpg)

16. Cuando se completa el pedido, la tarjeta de pedido se mueve al final de la lista. Si el pedido estaba atrasado, pero luego se completó, la tarjeta no se resalta en rojo.

17. Los pedidos completados se ordenan por el tiempo que tardaron en completarse: cuanto antes se complete el pedido, más abajo estará en la lista.

### Notificación

![](./assets/mobile/notification.jpg)

1. **Una notificación llega cuando quedan 2 horas para completar un pedido. El pedido deberá entregarse el día especificado por el usuario o usuaria antes de las 11:59 p.m. Por ejemplo, en el caso de un pedido para el 8 de mayo, si el repartidor o repartidora no ha entregado el scooter a las 9:59 p.m. el 8 de mayo, recibirá una notificación push.**

2. **La notificación contiene el siguiente mensaje: "2 horas hasta el final del pedido. Se debe completar el pedido "State St 1214". Si no llegas a tiempo, contacta a soporte: 0101".**

3. **Tocar la notificación lleva a la pestaña "Mis pedidos" en la aplicación.**

### Falta de acceso a internet

![](./assets/mobile/no-internet-access.jpg)

1. **Si no hay conexión a Internet, se muestra la ventana emergente "Sin acceso a Internet”. Aparece cuando un usuario o usuaria toca cualquier botón activo en cualquier pantalla, desaparece solo al tocar el botón "Aceptar".**

2. **Cuando un usuario o usuaria toca el botón "Aceptar", la notificación emergente se cierra. Si todavía no hay conexión a Internet, el proceso se repite: tocar cualquier zona activa lleva a la notificación emergente "Sin acceso a Internet".**

## Orientación

La aplicación está en orientación vertical solamente.
