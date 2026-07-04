# Ejecución de pruebas funcionales de la aplicación móvil

## Notificación

| ID | Título | Estado | Reporte de error |
| :--- | :--- | :--- | :--- |
| [TC-MOB-FUNC-001](../../../test-planning/mobile-app/TC-MOB-FUNC-001.md) | Recepción de la notificación push 2 horas antes del plazo. | 🔴 FAILED | [US-31](../../bug-reports/US-31.md) |
| [TC-MOB-FUNC-002](../../../test-planning/mobile-app/TC-MOB-FUNC-002.md) | No se recibe la notificación push 1 hora y 59 minutos antes del plazo. | 🟢 PASSED |
| [TC-MOB-FUNC-003](../../../test-planning/mobile-app/TC-MOB-FUNC-003.md) | No se recibe la notificación push 2 horas y 1 minuto después del plazo | 🟢 PASSED |
| [TC-MOB-FUNC-004](../../../test-planning/mobile-app/TC-MOB-FUNC-004.md) | La notificación incluye la misma dirección del pedido aceptado. | 🟡 SKIPPED | Bloqueado por [US-31](../../bug-reports/US-31.md): sin notificación no se puede verificar el contenido. |
| [TC-MOB-FUNC-005](../../../test-planning/mobile-app/TC-MOB-FUNC-005.md) | Tocar la notificación redirige a la pestaña "Mis pedidos" en la aplicación. | 🟡 SKIPPED | Bloqueado por [US-31](../../bug-reports/US-31.md): sin notificación no se puede verificar el contenido. |
| [TC-MOB-FUNC-006](../../../test-planning/mobile-app/TC-MOB-FUNC-006.md) | No se recibe notificación si el pedido ya fue completado. | 🟢 PASSED |
