# Datos de prueba - Mensajero

## Crear un mensajero `POST /api/v1/courier`

### Campo `login`

Solo letras latinas. La longitud del texto es de 2 a 10 caracteres. `Obligatorio`.

| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 2-10 caracteres latinos | 2 - `Ar`<br>3 - `Ari`<br>5 - `Ariel`<br>9 - `ArielArie`<br>10 - `ArielAriel` |
| [Inválida] Texto <2 caracteres | 1 - `A` |
| [Inválida] Texto >10 caracteres | 11 - `ArielArielA`<br>12 - `ArielArielAr`<br>13 - `ArielArielAri` |
| [Inválida] Vacío: 0 caracteres |
| [Inválida] Omitir campo |
| [Inválida] Caracteres numéricos | `1234567890` |
| [Inválida] Espacios | `Ariel Arie` |
| [Inválida] Guiones | `Ariel-Arie` |
| [Inválida] Puntos | `Ariel.` |
| [Inválida] Comas | `Ariel,` |
| [Inválida] Caracteres especiales | `№%@\"` |
| [Inválida] Caracteres de otro lenguaje | `加布里埃爾F加布爾` |

### Campo `password`

Solo números enteros. La longitud es exactamente de 4 caracteres numéricos. `Obligatorio`.

| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 4 caracteres numéricos | 4 - `1234`|
| [Inválida] Texto <4 caracteres numéricos | 3 - `123`<br>2 - `12` |
| [Inválida] Texto >4 caracteres numéricos | 5 - `12345`<br>6 - `123456`<br>7 - `1234567` |
| [Inválida] Alfabeto Latino | `Arie` |
| [Inválida] Vacío: 0 caracteres |
| [Inválida] Omitir campo |
| [Inválida] Espacios | `12 4` |
| [Inválida] Guiones | `12-4` |
| [Inválida] Puntos | `12.4` |
| [Inválida] Comas | `12,4` |
| [Inválida] Caracteres especiales | `№%@\` |
| [Inválida] Caracteres de otro lenguaje | `加布里埃` |

### Campo `firstName`

Solo letras latinas. La longitud del texto es de 2 a 10 caracteres. `Opcional`.

| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 2-10 caracteres latinos | 2 - `Ar`<br>3 - `Ari`<br>5 - `Ariel`<br>9 - `ArielArie`<br>10 - `ArielAriel` |
| [Válida] Omitir campo |
| [Inválida] Texto <2 caracteres | 1 - `A` |
| [Inválida] Texto >10 caracteres | 11 - `ArielArielA`<br>12 - `ArielArielAr`<br>13 - `ArielArielAri` |
| [Inválida] Vacío: 0 caracteres |
| [Inválida] Caracteres numéricos | `1234567890` |
| [Inválida] Espacios | `Ariel Arie` |
| [Inválida] Guiones | `Ariel-Arie` |
| [Inválida] Puntos | `Ariel.` |
| [Inválida] Comas | `Ariel,` |
| [Inválida] Caracteres especiales | `№%@\"` |
| [Inválida] Caracteres de otro lenguaje | `加布里埃爾F加布爾` |