# Checklist - Pantalla "Realizar Pedido"

## Pruebas de diseño

### Header

#### Logo
41. El logo está presente y se muestra en la posición superior izquierda según Figma.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

42. El logo no está pixelado ni deformado.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

#### Botones del header
43. El botón "Pedir" está presente y en la posición esperada.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

44. El botón "Estado del pedido" está presente y en la posición esperada.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

45. Color de fondo del botón "Pedir" coincide con Figma.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

46. Color de fondo del botón "Estado del pedido" coincide con Figma.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

47. Al hacer hover en "Pedir", el botón muestra el estilo especificado en Figma.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Chrome 85 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1280x720: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

48. Al hacer hover en "Estado del pedido", el botón muestra el estilo especificado en Figma.
    - Chrome 85 o superior, 1920x1080: 🔴 FAILED
    - Chrome 85 o superior, 1280x720: 🔴 FAILED
    - Opera 71 o superior, 1280x720: 🔴 FAILED
    - Opera 71 o superior, 1920x1080: 🔴 FAILED
    - [[US-11]](../bug-reports/US-11.md)

---

# Formulario "Para quién es el scooter"

## Pruebas Funcionales

### Validaciones
49. Si "Nombre" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Nombre correcto".
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

50. Si "Apellido" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un apellido válido".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-12]](../bug-reports/US-12.md)

51. Si "Dirección" está vacía o es inválida, al intentar avanzar se muestra error "Introduce una dirección válida".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-13]](../bug-reports/US-13.md)

52. Si "Estación de metro" está vacía, al intentar avanzar se muestra error "Introduce una estación de metro correcta".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-14]](../bug-reports/US-14.md)

53. Si "Teléfono" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un número de teléfono válido".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-15]](../bug-reports/US-15.md)

### Navegación
54. Si todos los campos están rellenados correctamente, al hacer clic en "Siguiente" se avanza al formulario "Alquiler".
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

55. Si algún campo se marca como inválido, al hacer clic en "Siguiente" se muestra el error correspondiente y no se avanza.
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

## Pruebas de diseño

### Encabezado
56. Si algún campo se marca como inválido, al hacer clic en "Siguiente" se muestra el error correspondiente y no se avanza.
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

### Campos
57. El campo "Nombre" está presente.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

58. El placeholder de "Nombre" coincide con "* Nombre".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

59. "Nombre" inválido se resalta en rojo.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

60. El campo "Apellido" está presente.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

61. El placeholder de "Apellido" coincide con "* Apellido".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

62. "Apellido" inválido se resalta en rojo.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

63. El campo "Dirección" está presente.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

64. El placeholder de "Dirección" coincide con "* Dirección: a dónde llevar el scooter".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

65. "Dirección" inválida se resalta en rojo.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

66. El campo "Estación de metro" está presente.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

67. El placeholder de "Estación de metro" coincide con "* Estación de metro".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

68. El campo "Teléfono" está presente.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

69. El placeholder de "Teléfono" coincide con "Teléfono: el repartidor o repartidora te llamará".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

70. "Teléfono" inválido se resalta en rojo.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

71. Los campos obligatorios están marcados con asterisco.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

### Botón "Siguiente"
72. El botón "Siguiente" está presente en la parte inferior del formulario.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

73. Color de fondo del botón "Siguiente" coincide con Figma.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

74. Al hacer hover en "Siguiente", el botón muestra el estilo especificado en Figma.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

75. Al hacer hover en "Siguiente", el cursor cambia a mano.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

---

# Formulario "Alquiler"

## Pruebas funcionales

### Validaciones de campos

76. Si "Fecha de entrega" se marca como inválido, al hacer clic en "Pedir" se muestra error "Introduce una fecha de entrega correcta".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

77. Si "Periodo de alquiler" se marca como inválido, al hacer clic en "Pedir" se muestra error "Introduce un Periodo de alquiler correcto".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-17]](../bug-reports/US-17.md)

### Botón "Atrás"
78. Al hacer clic en "Atrás" se regresa a la pantalla "Para quién es el scooter".
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

79. Los campos de "Alquiler" conservan la información al regresar después de haber avanzado nuevamente.
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

### Botón "Pedir"
80. Con todos los campos obligatorios correctos, al hacer clic en "Pedir" aparece una ventana emergente "El pedido ha sido realizado".
    - Chrome 85 o superior, 1920x1080
    - Opera 71 o superior, 1920x1080
    - 🔴 FAILED [[US-1]](../bug-reports/US-1.md)

81. La ventana emergente muestra el mensaje "Número de pedido NNNNN. Escríbelo: será útil para darle seguimiento al estado".
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

82. La ventana emergente contiene un botón "Comprueba el estado".
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

83. Al hacer clic en "Comprueba el estado" se redirige a la pantalla "Estado del pedido".
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

84. En la pantalla "Estado del pedido", el campo "Número de pedido" aparece ya completado con el número del pedido recién creado.
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

### Botón "Pedir" (error)
85. Si algún campo obligatorio está vacío o es inválido, al hacer clic en "Pedir" aparece un mensaje de error indicando el campo problemático.
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-18]](../bug-reports/US-18.md)

86. El formulario no se envía hasta que todos los campos obligatorios sean correctos.
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

### Múltiples pedidos
87. Después de realizar un pedido exitosamente, el usuario puede realizar otro pedido.
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

88. Los datos del nuevo pedido no se mezclan con los del anterior.
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

89. Cada pedido genera un número de pedido distinto (visible en la ventana emergente).
    - Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

## Pruebas de diseño

### Encabezado
90. El texto del encabezado coincide con "Alquiler".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

### Campos
91. El campo "Fecha de entrega" está presente.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

92. El placeholder de "Fecha de entrega" coincide con "* Cuándo entregar el scooter".
    - Chrome 85 o superior, 1920x1080: 🔴 FAILED 
    - Opera 71 o superior, 1920x1080: 🔴 FAILED
    - [[US-19]](../bug-reports/US-19.md)

93. Focus en "Fecha de entrega" se resalta en azul.
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

94. "Fecha de entrega" es obligatorio, tiene indicación visual "*".
    - Chrome 85 o superior, 1920x1080: 🟢 PASSED
    - Opera 71 o superior, 1920x1080: 🟢 PASSED
