# Test Data - Courier

## Create a courier `POST /api/v1/courier`

### Field `login`

Latin letters only. Text length is 2 to 10 characters. `Required`.

| Class | Test Data | 
| :--- | :--- |
| [Valid] Text 2-10 Latin characters | 2 - `Ar`<br>3 - `Ari`<br>5 - `Ariel`<br>9 - `ArielArie`<br>10 - `ArielAriel` |
| [Invalid] Text <2 characters | 1 - `A` |
| [Invalid] Text >10 characters | 11 - `ArielArielA`<br>12 - `ArielArielAr`<br>13 - `ArielArielAri` |
| [Invalid] Empty: 0 characters |
| [Invalid] Omit field |
| [Invalid] Numeric characters | `1234567890` |
| [Invalid] Spaces | `Ariel Arie` |
| [Invalid] Hyphens | `Ariel-Arie` |
| [Invalid] Periods | `Ariel.` |
| [Invalid] Commas | `Ariel,` |
| [Invalid] Special characters | `№%@\"` |
| [Invalid] Characters from another language | `加布里埃爾F加布爾` |

### Field `password`

Integers only. Length is exactly 4 numeric characters. `Required`.

| Class | Test Data | 
| :--- | :--- |
| [Valid] Text 4 numeric characters | 4 - `1234`|
| [Invalid] Text <4 numeric characters | 3 - `123`<br>2 - `12` |
| [Invalid] Text >4 numeric characters | 5 - `12345`<br>6 - `123456`<br>7 - `1234567` |
| [Invalid] Latin alphabet | `Arie` |
| [Invalid] Empty: 0 characters |
| [Invalid] Omit field |
| [Invalid] Spaces | `12 4` |
| [Invalid] Hyphens | `12-4` |
| [Invalid] Periods | `12.4` |
| [Invalid] Commas | `12,4` |
| [Invalid] Special characters | `№%@\` |
| [Invalid] Characters from another language | `加布里埃` |

### Field `firstName`

Latin letters only. Text length is 2 to 10 characters. `Optional`.

| Class | Test Data | 
| :--- | :--- |
| [Valid] Text 2-10 Latin characters | 2 - `Ar`<br>3 - `Ari`<br>5 - `Ariel`<br>9 - `ArielArie`<br>10 - `ArielAriel` |
| [Valid] Omit field |
| [Invalid] Text <2 characters | 1 - `A` |
| [Invalid] Text >10 characters | 11 - `ArielArielA`<br>12 - `ArielArielAr`<br>13 - `ArielArielAri` |
| [Invalid] Empty: 0 characters |
| [Invalid] Numeric characters | `1234567890` |
| [Invalid] Spaces | `Ariel Arie` |
| [Invalid] Hyphens | `Ariel-Arie` |
| [Invalid] Periods | `Ariel.` |
| [Invalid] Commas | `Ariel,` |
| [Invalid] Special characters | `№%@\"` |
| [Invalid] Characters from another language | `加布里埃爾F加布爾` |