# Checklist - Mensajero

## Crear un mensajero

`POST /api/v1/courier`

1. Enviar una solicitud con `login`, `password` y `firstName` válidos devuelve un código `201 Created` y `{ok: true}`.

2. Enviar una solicitud sin el campo `login` devuelve `400 Bad Request` y {"message": "No hay suficientes datos para crear una cuenta"}.

3. Enviar una solicitud sin el campo `password` devuelve `400 Bad Request` y "message": "No hay suficientes datos para crear una cuenta".

4. Enviar una solicitud con `login` y `password` válidos sin el campo `firstName`, devuelve un código `201 Created` y `{ok: true}`.

5. Enviar una solicitud con `login` existente devuelve `409 Conflict` y {"message": "Este inicio de sesión no está disponible"}.

6. Verificar en la base de datos que el `login` enviado aparece en la tabla `Couriers` exactamente como se envió.

7. Verificar que el campo `passwordHash` en la tabla `Couriers` no es la contraseña en texto plano (es un hash).

8. Verificar que el campo `firstName` en la tabla `Couriers` coincide con el enviado.

9. Iniciar sesión (`POST /api/v1/courier/login`) con el login y la contraseña correcta devuelve un código `200 OK` y el `id` del repartidor. Esto confirma que el hash se generó correctamente y la verificación funciona.