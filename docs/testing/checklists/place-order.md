# Checklist - Pantalla "Realizar Pedido"

## Diseño

### Header

#### Logo
El logo está presente y se muestra en la posición superior izquierda según Figma.
Dimensiones del logo coinciden con el diseño (ancho x alto).
El logo no está pixelado ni deformado.

#### Botones del Header
El botón "Pedir" está presente y en la posición esperada.
El botón "Estado del pedido" está presente y en la posición esperada.
Color de fondo del botón "Pedir" coincide con Figma.
Color de fondo del botón "Estado del pedido" coincide con Figma.
Al hacer hover en "Pedir", el botón muestra el estilo especificado en Figma.
Al hacer hover en "Estado del pedido", el botón muestra el estilo especificado en Figma.
Al hacer hover en "Pedir", el cursor cambia a pointer.
Al hacer hover en "Estado del pedido", el cursor cambia a pointer.

#### Encabezado
El logo está presente y se muestra en la posición superior izquierda según Figma.
Dimensiones del logo coinciden con el diseño (ancho x alto).
El logo no está pixelado ni deformado.

### Formulario "Para quién es el scooter"

#### Funcionales
##### Validaciones
Si "Nombre" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Nombre correcto".
Si "Apellido" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Apellido correcto".
Si "Dirección" está vacía o es inválida, al intentar avanzar se muestra error "Introduce un Dirección correcto".
Si "Estación de metro" está vacía o es inválida, al intentar avanzar se muestra error "Introduce un Estación de metro correcto".
Si "Teléfono" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Teléfono correcto".

##### Navegación
Si todos los campos están rellenados correctamente, al hacer clic en "Siguiente" se avanza al formulario "Alquiler".
Si algún campo no está rellenado correctamente, al hacer clic en "Siguiente" se muestra el error correspondiente y no se avanza.

#### Diseño

##### Encabezado
El texto del encabezado coincide con "Para quién es el scooter".

##### Campos
El campo "Nombre" está presente.
El placeholder de "Nombre" coincide con "* Nombre".
"Nombre" inválido se resalta en rojo.
"Nombre" inválido muestra mensaje "Introduce un nombre correcto".
El campo "Apellido" está presente.
El placeholder de "Apellido" coincide con "* Apellido".
"Apellido" inválido se resalta en rojo.
"Apellido" inválido muestra mensaje "Introduce un apellido válido".
El campo "Dirección: a dónde llevar el scooter" está presente.
El placeholder de "Dirección" coincide con "* Dirección: a dónde llevar el scooter".
"Dirección" inválida se resalta en rojo.
"Dirección" inválido muestra mensaje "Introduce una dirección válida".
El campo "Estación de metro" está presente.
El placeholder de "Estación de metro" coincide con "* Estación de metro".
El campo "Teléfono: el repartidor o repartidora llamará" está presente.
El placeholder de "Teléfono" coincide con "Teléfono: el repartidor o repartidora te llamará".
"Teléfono" inválido se resalta en rojo.
"Nombre" inválido muestra mensaje "Introduce un número de teléfono válido".
Todos los campos son obligatorios (marcados con asterisco).

##### Botón "Siguiente"
El botón "Siguiente" está presente en la parte inferior del formulario.
Color de fondo del botón "Siguiente" coincide con Figma.
Al hacer hover en "Siguiente", el botón muestra el estilo especificado en Figma.
Al hacer hover en "Siguiente", el cursor cambia a pointer.

### Formulario "Alquiler"

#### Funcionales

##### Validaciones
Si "Fecha de entrega" está vacío, al hacer clic en "Pedir" se muestra error "Introduce un Fecha de entrega correcto".
Si "Periodo de alquiler" está vacío, al hacer clic en "Pedir" se muestra error "Introduce un Periodo de alquiler correcto".

##### Botón "Atrás"
Al hacer clic en "Atrás" se regresa a la pantalla "Para quién es el scooter".
Los campos de "Alquiler" conservan la información al regresar después de haber avanzado nuevamente.

##### Botón "Pedir"
Con todos los campos obligatorios correctos, al hacer clic en "Pedir" aparece una ventana emergente "El pedido ha sido realizado".
La ventana emergente muestra el mensaje "Número de pedido NNNNN. Escríbelo: será útil para darle seguimiento al estado".
La ventana emergente contiene un botón "Comprueba el estado".
Al hacer clic en "Comprueba el estado" se redirige a la pantalla "Estado del pedido".
En la pantalla "Estado del pedido", el campo "Número de pedido" aparece ya completado con el número del pedido recién creado.

##### Botón "Pedir" (error)
Si algún campo obligatorio está vacío o es inválido, al hacer clic en "Pedir" aparece un mensaje de error indicando el campo problemático.
El formulario no se envía hasta que todos los campos obligatorios sean correctos.

##### Múltiples Pedidos
Después de realizar un pedido exitosamente, el usuario puede realizar otro pedido.
Los datos del nuevo pedido no se mezclan con los del anterior.
Cada pedido genera un número de pedido distinto (visible en la ventana emergente).

#### Diseño

##### Encabezado
El texto del encabezado coincide con "Alquiler".

##### Campos
El campo "Fecha de entrega" está presente.
El placeholder de "Fecha de entrega" coincide con "* Cuándo entregar el scooter".
Focus en "Fecha de entrega" se resalta en azul.
"Fecha de entrega" es obligatorio, tiene indicación visual "*".
El campo "Periodo de alquiler" está presente.
El placeholder de "Periodo de alquiler" coincide con "* Periodo de alquiler".
"Periodo de alquiler" es obligatorio, tiene indicación visual "*".
El campo "Color" está presente.
"El placeholder de ""Color"" coincide con
""
El color del scooter
☐ negro
☐ gris
""."
El campo "Comentario" está presente.
El placeholder de "Comentario" coincide con "Comentario".

##### Botones
El botón "Atrás" está presente en la parte inferior del formulario.
Color de fondo del botón "Atrás" coincide con Figma.
Al hacer hover en "Atrás", el botón muestra el estilo especificado en Figma.
Al hacer hover en "Atrás", el cursor cambia a pointer.
El botón "Pedir" está presente en la parte inferior del formulario.
Color de fondo del botón "Pedir" coincide con Figma.
Al hacer hover en "Pedir", el botón muestra el estilo especificado en Figma.
Al hacer hover en "Pedir", el cursor cambia a pointer.

