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

# Formulario "Para quién es el scooter"

## Pruebas Funcionales

### Validaciones
49. Si "Nombre" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Nombre correcto".
    - Opera 71 o superior, 1920x1080: 🟢 PASSED

50. Si "Apellido" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Nombre correcto".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-12]](../bug-reports/US-12-md)

51. Si "Dirección" está vacía o es inválido, al intentar avanzar se muestra error "Introduce un dirección correcto".
    - Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-13]](../bug-reports/US-13-md)