# Checklist Funcional - Pantalla Estado del Pedido

## Navegación y acceso
- [] Hacer clic en "Estado del pedido" en el encabezado muestra el campo "Número de pedido".
- [] El campo "Número de pedido" acepta entrada de texto.
- [] Presionar Enter con un número válido muestra la información del pedido.
- [] Presionar Enter con un número inválido muestra el mensaje: "No existe tal pedido. ¿Seguro que ese es el número correcto?".
- [] Se puede introducir otro número de pedido después de consultar uno.

## Visualización de datos del pedido
- [] Se muestra el nombre del usuario.
- [] Se muestra el apellido del usuario.
- [] Se muestra la dirección del usuario.
- [] Se muestra la estación del metro.
- [] Se muestra el teléfono del usuario.
- [] Se muestra la fecha de entrega del scooter.
- [] La fecha coincide con la esperada.
- [] Se muestra el periodo del alquiler.
- [] Se muestra el color del scooter.
- [] Se muestra el comentario del usuario.
- [] Si un campo de texto excede una línea, pasa a una segunda línea (regla de truncado/ajuste).


## Cadena de estado (4 estados)
### "El scooter está en el almacén"
- [] Se activa automáticamente al realizar un pedido.

### "El repartidor o repartidora está en camino"
- [] Se activa cuando el repartido confirma que aceptó el pedido.
- [] Muestra el aviso: "El repartidor [Nombre] está en camino".
- [] Si el nombre del repartidor excede una línea, pasa a una segunda línea.

### "El servicio de entrega llegó"
- [] Se activa cuando el repartidor presiona "Completar".

### "Bien, vamos a dar un paseo"
- [] Se activa cuando el repartidor confirma finalización.
- [] Muestra "El alquiler finalizará el <fecha>". 
- [] La fecha se coincide con el cálculo desde la entrega y el número de días de alquiler.
- [] Al finalizar el periodo, el estado cambia a "Periodo de alquiler terminado".
- [] Muestra la leyenda "El repartidor o repartidora recogerá el scooter pronto".

### Reglas de presentación de estados
- [] Solo un estado puede estar activo a la vez.
- [] El estado inactivo está resaltado en negro.
- [] Los estados inactivos están en gris.
- [] Al pasar de un estado al siguiente, el número delante del estado cambia a una marca (check).

## Cancelación de pedido
- [] Al hacer clic en "Cancelar pedido", aparece una ventana emergente con el texto "¿Deseas cancelar el pedido?".
- [] Botón "Atrás" cierra la ventana y vuelve a la pantalla de estado.
- [] Botón "Cancelar" muestra ventana: "El pedido ha sido cancelado. Siéntete libre de volver en cualquier momento :)" y botón "Bien".
- [] Botón "Bien" redirige a la página de inicio.
- [] El botón "Cancelar el pedido" está habilitado solo antes de que el repartidor recoja el pedido.
- [] Una vez que el repartidor tiene el pedido, el botón no es cliqueable.
- [] El pedido cancelado se elimina del sistema y no es visible para el usuario.

## Pedido atrasado
- [] Un pedido no entregado a las 23:59 o antes, del día acordado, cambia a estado "El repartidor o repartidora se demoró".
- [] Muestra mensaje: "No podemos entregar el scooter a tiempo. Para aclarar el estado de tu pedido, llama a soporte: 0101".
- [] El estado y la leyenda aparecen resaltados en rojo.
- [] Si el pedido atrasado se entrega, la cuenta regresiva de alquiler inicia en el momento de la entrega.