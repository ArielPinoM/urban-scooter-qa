# Execution of mobile application functional tests

## Notification

| ID | Title | Status | Error Report |
| :--- | :--- | :--- | :--- |
| [TC-MOB-FUNC-001](../../../test-planning/mobile-app/TC-MOB-FUNC-001.md) | Reception of push notification 2 hours before the deadline. | 🔴 FAILED | [US-31](../../bug-reports/US-31.md) |
| [TC-MOB-FUNC-002](../../../test-planning/mobile-app/TC-MOB-FUNC-002.md) | Push notification is not received 1 hour and 59 minutes before the deadline. | 🟢 PASSED |
| [TC-MOB-FUNC-003](../../../test-planning/mobile-app/TC-MOB-FUNC-003.md) | Push notification is not received 2 hours and 1 minute after the deadline | 🟢 PASSED |
| [TC-MOB-FUNC-004](../../../test-planning/mobile-app/TC-MOB-FUNC-004.md) | The notification includes the same address as the accepted order. | 🟡 SKIPPED | Blocked by [US-31](../../bug-reports/US-31.md): without notification, content cannot be verified. |
| [TC-MOB-FUNC-005](../../../test-planning/mobile-app/TC-MOB-FUNC-005.md) | Tapping the notification redirects to the "Mis pedidos" tab in the application. | 🟡 SKIPPED | Blocked by [US-31](../../bug-reports/US-31.md): without notification, content cannot be verified. |
| [TC-MOB-FUNC-006](../../../test-planning/mobile-app/TC-MOB-FUNC-006.md) | No notification is received if the order is already completed. | 🟢 PASSED |

## No Internet Access

| ID | Title | Status | Error Report |
| :--- | :--- | :--- | :--- |
| [TC-MOB-FUNC-007](../../../test-planning/mobile-app/TC-MOB-FUNC-007.md) | "Sin acceso a Internet" popup window is displayed when tapping "Iniciar sesión" without internet connection. | 🔴 FAILED | [US-32](../../bug-reports/US-32.md) |
| [TC-MOB-FUNC-008](../../../test-planning/mobile-app/TC-MOB-FUNC-008.md) | "Sin acceso a Internet" popup window is displayed when tapping "Mis pedidos" without internet connection. | 🟢 PASSED |
| [TC-MOB-FUNC-009](../../../test-planning/mobile-app/TC-MOB-FUNC-009.md) | "Sin acceso a Internet" popup window is displayed when tapping to accept an order without internet connection. | 🟢 PASSED |
| [TC-MOB-FUNC-010](../../../test-planning/mobile-app/TC-MOB-FUNC-010.md) | "Sin acceso a Internet" popup window is displayed when completing an order without internet connection. | 🟢 PASSED |
| [TC-MOB-FUNC-011](../../../test-planning/mobile-app/TC-MOB-FUNC-011.md) | Clicking "Aceptar" on the "Sin acceso a Internet" popup window closes the window. | 🟢 PASSED |
| [TC-MOB-FUNC-012](../../../test-planning/mobile-app/TC-MOB-FUNC-012.md) | "Sin acceso a Internet" popup window reappears when tapping any button if there is still no connection.  | 🟢 PASSED |