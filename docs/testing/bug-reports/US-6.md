# US-6: El campo "finished" se activa al presionar "Completar" (estado 3); posible inconsistencia con requisitos

# Detalles clave

## Severidad
🔵 Minor

## Prioridad
🟨 Medium

## Entorno
- Opera 132, 1280x720 (Chrome bloqueado por [US-1](./US-1.md))
- Postman 12.16.4
- Api Ez-scooter versión 1.0.0
- Back-end
    - Node.js v12.17.0
- Base de datos PostgreSQL

## Componente
Backend - Lógica de Estados del Pedido

## Descripción

### Vinculación
Bloqueado por [US-5](./US-5.md).

Durante las pruebas de la cadena de estados, se observó que el campo `finished` en la tabla `Orders` cambia a `true` cuando el repartidor presiona **"Completar"** (lo que activa el estado "El servicio de entrega llegó"). Sin embargo, el documento de requisitos del backend indica que *el campo lógico finished se asigna cuando el pedido ha sido enviado,* **(Descripción del contenido de la base de datos > Orders)**.

Se necesita aclarar:
- ¿”Enviado” equivale al momento en que el repartidor presiona “Completar“ (estado 3) o cuando se confirma la finalización (estado 4)?
- Si `finished` debe reflejar la finalización del alquiler (estado 4), entonces está cambiando prematuramente.

**Nota:** Esta verificación se realizó con el bug [US-5](./US-5.md). Es probable que el comportamiento sea el mismo sin duplicados, pero debe confirmarse una vez resuelto.

### Precondiciones
- [US-5](./US-5.md) resuelto.
- Pedido creado y aceptado por el mensajero.

### Pasos para reproducir
1. Aceptar un pedido con un mensajero.
2. Consultar `Orders`: verificar que `finished = false`.
3. Presionar “Completar” (simular vía API o desde la app móvil).
4. Consultar nuevamente `Orders` para el mismo pedido.
5. Contrastar el valor de `finished` con los especificado en los requisitos.


### Resultado esperado (según interpretación de requisitos)
A confirmar. Si “enviado“ = estado 4, `finished` debería seguir siendo `false` tras “Completar“, y pasar a `true` solo al confirmar la finalización. 

### Resultado actual (con [US-5](./US-5.md) presente)
`finished` pasó a `true` inmediatamente después de “Completar“ (estado 3).