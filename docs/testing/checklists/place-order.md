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
    - [[US-11]](../bug-reports/US-11-md)

---

# Formulario "Para quién es el scooter"

## Pruebas Funcionales

### Validaciones
49. Si "Nombre" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Nombre correcto".
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

50. Si "Apellido" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un apellido válido".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-12]](../bug-reports/US-12-md)

51. Si "Dirección" está vacía o es inválida, al intentar avanzar se muestra error "Introduce una dirección válida".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-13]](../bug-reports/US-13-md)

52. Si "Estación de metro" está vacía, al intentar avanzar se muestra error "Introduce una estación de metro correcta".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-14]](../bug-reports/US-14-md)

53. Si "Teléfono" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un número de teléfono válido".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-15]](../bug-reports/US-15-md)

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