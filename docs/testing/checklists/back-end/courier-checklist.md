# Checklist - Mensajero

## Crear un mensajero

`POST /api/v1/courier`

### Validación de datos en los parámetros de la solicitud

#### Campo `login` - 201 Created y {ok: true}

1. 2 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
2. 3 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
3. 5 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
4. 9 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
5. 10 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED

#### Campo `login` - 400 Bad Request

6. 1 caracter latino y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-34]](../../bug-reports/US-34.md)
7. 11 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-35]](../../bug-reports/US-35.md)
8. 12 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-36]](../../bug-reports/US-36.md)
9. 13 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-37]](../../bug-reports/US-37.md)
10. Vacío y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
11. Omitir campo y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
12. Caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-38]](../../bug-reports/US-38.md)
13. Caracteres con espacios y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-39]](../../bug-reports/US-39.md)
14. Caracteres con guiones y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-40]](../../bug-reports/US-40.md)
15. Caracteres con puntos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-41]](../../bug-reports/US-41.md)
16. Caracteres con comas y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-42]](../../bug-reports/US-42.md)
17. Caracteres especiales y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-43]](../../bug-reports/US-43.md)
18. Caracteres de otro lenguaje y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-44]](../../bug-reports/US-44.md)

#### Campo `password` - 201 Created y {ok: true}

19. 4 caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED

#### Campo `password` - 400 Bad Request

20. 1 caracter numérico y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-45]](../../bug-reports/US-45.md)
21. 2 caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-46]](../../bug-reports/US-46.md)
22. 3 caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-47]](../../bug-reports/US-47.md)
23. 5 caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-48]](../../bug-reports/US-48.md)
24. 6 caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-49]](../../bug-reports/US-49.md)
25. 7 caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-50]](../../bug-reports/US-50.md)
26. Caracteres del alfabeto latino y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-51]](../../bug-reports/US-51.md)
27. Vacío y el resto de campos obligatorios con datos válidos devuelve mensaje "No hay suficientes datos para crear una cuenta".
    - 🟢 PASSED
28. Omitir campo y el resto de campos obligatorios con datos válidos devuelve mensaje "No hay suficientes datos para crear una cuenta".
    - 🟢 PASSED
29. Caracteres numéricos con espacios y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-52]](../../bug-reports/US-52.md)
30. Caracteres numéricos con guiones y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-53]](../../bug-reports/US-53.md)
31. Caracteres numéricos con puntos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-54]](../../bug-reports/US-54.md)
32. Caracteres numéricos con comas y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-55]](../../bug-reports/US-55.md)
33. Caracteres especiales y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-56]](../../bug-reports/US-56.md)
34. Caracteres de otro lenguaje y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-57]](../../bug-reports/US-57.md)

#### Campo `firstName` - 201 Created y {ok: true}

35. 2 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
36. 3 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
37. 5 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
38. 9 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
39. 10 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
40. Vacío y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED
41. Omitir campo y el resto de campos obligatorios con datos válidos.
    - 🟢 PASSED

#### Campo `firstName` - 400 Bad Request

42. 1 caracter latino y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-58]](../../bug-reports/US-58.md)
43. 11 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-59]](../../bug-reports/US-59.md)
44. 12 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-60]](../../bug-reports/US-60.md)
45. 13 caracteres latinos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-61]](../../bug-reports/US-61.md)
46. Caracteres numéricos y el resto de campos obligatorios con datos válidos.
    - 🔴 FAILED [[US-62]](../../bug-reports/US-62.md)
47. Caracteres con espacios y el resto de campos obligatorios con datos válidos.

48. Caracteres con guiones y el resto de campos obligatorios con datos válidos.
49. Caracteres con puntos y el resto de campos obligatorios con datos válidos.
50. Caracteres con comas y el resto de campos obligatorios con datos válidos.
51. Caracteres especiales y el resto de campos obligatorios con datos válidos.
52. Caracteres de otro lenguaje y el resto de campos obligatorios con datos válidos.

### Validación del body de la solicitud

#### Cuenta creada con éxito - 201 Created y {ok: true}

53. Todos los campos obligatorios válidos y firstName válido.		
54. Todos los campos obligatorios válidos omitiendo firstName		

#### 400 Bad Request

55. Campo login inválido, password válido y omitir firstName.
56. Omitir campo login y firstName, password válido devuelve mensaje "No hay suficientes datos para crear una cuenta".
57. Campo login válido, password inválido y omitir firstName.
58. Campo login válido, omitir password y firstName devuele mensaje "No hay suficientes datos para crear una cuenta".
59. Campo login válido, password válido y firstName inválido.

#### 409 Conflict

60. Enviar solicitud con campo login ya existente devuelve mensaje "Este inicio de sesión no está disponible".

### Verificar Base de Datos - Tabla Couriers

61. El campo login coincide con el enviado.
62. El campo passwordHash en la tabla no es la contraseña en texto plano (es un hash).
63. El campo firstName coincide con el enviado.
64. Enviar un login que ya existe no crea otro registro.

## Eliminar un mensajero

`DELETE /api/v1/courier/:id`

65. Enviar DELETE /api/v1/courier/:id con id existente devuelve 200 OK y {ok: true}.
66. Verificar en la tabla Couriers que el registro con ese id ya no existe.
67. Verificar en la tabla Orders que todos los pedidos cuyo courierId coincidía con el id eliminado han sido borrados.
68. Omitir el campo id devuelve 400 Bad Request y el mensaje "No hay datos suficientes para eliminar el mensajero".
69. Enviar una solicitud con un id no existente devuelve 404 Not Found y el mensaje "No hay un mensajero con esta ID".

## Obtener un pedido por su número

`GET /api/v1/orders/track?t=<numero_pedido>`

70. El parámetro "t" válido y existe un pedido con ese número devuelve 200 OK y la respuesta coincide con los datos del registro en la tabla "Orders".
71. El parámetro "t" inválido devuelve 400 Bad Request.
72. Omitir el parámetro devuelve 400 Bad Request y el mensaje "No hay suficientes datos para la búsqueda".
73. Enviar la solicitud con un número de pedido no existente devuelve 404 Not Found y el mensaje "Pedido no encontrado".