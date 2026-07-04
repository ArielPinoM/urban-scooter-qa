# Datos de Prueba - Formulario de Pedido

Esta documentación usa particiones de equivalencia y análisis de valores límite para cubrir los escenarios más importantes del formulario de pedido. Cada campo se divide en clases válidas e inválidas, de modo que se seleccionan entradas representativas de cada partición. Además, se incluyen casos en los límites de las restricciones (por ejemplo, 2 y 15 caracteres en el nombre) para verificar el comportamiento en valores justo dentro y justo fuera de los límites.

## Formulario "Para quién es el scooter"

### Campo: Nombre
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 2-15 caracteres | 2 - Ar<br>3 - Ari<br>5 - Ariel<br>14 - ArielArielArie<br>15 - ArielArielAriel |
| [Válida] Alfabeto Latino | Ariel |
| [Válida] Espacios | Ariel Ariel |
| [Válida] Guiones | Ariel-Ariel |
| [Inválida] Texto <2 caracteres | 1 - A |
| [Inválida] Texto >15 caracteres | 16 - ArielArielArielA<br>17 - ArielArielArielAr<br>18 - ArielArielArielAri |
| [Inválida] Vacío: 0 caracteres |
| [Inválida] Puntos | Ariel. |
| [Inválida] Comas | Ariel, |
| [Inválida] Caracteres especiales | №%@\" |
| [Inválida] Caracteres de otro lenguaje | 加布里埃爾F加布爾 |
| [Inválida] Caracteres numéricos | 1234567890 |

### Campo: Apellido
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 2-15 caracteres | 2 - Pi<br>3 - Pin<br>5 - PinoP<br>14 - PinoPinoPinoPin<br>15 - PinoPinoPinoPinoPin |
| [Válida] Alfabeto Latino | Pino |
| [Válida] Espacios | Pino Pino |
| [Válida] Guiones | Pino-Pino |
| [Inválida] Texto <2 caracteres | 1 - P |
| [Inválida] Texto >15 caracteres | 16 - PinoPinoPinoPino<br>17 - PinoPinoPinoPinoP<br>18 - PinoPinoPinoPinoPi |
| [Inválida] Vacío: 0 caracteres |
| [Inválida] Puntos | Pino. |
| [Inválida] Comas | Pino, |
| [Inválida] Caracteres especiales | №%@\" |
| [Inválida] Caracteres de otro lenguaje | 加布里埃爾F加布爾 |
| [Inválida] Caracteres numéricos | 1234567890 |

### Campo: Dirección
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 5-50 caracteres | 5 - 95501<br>6 - 955011<br>24 - 1 A St, Eureka, CA 95501<br>49 - 350 East 1st Street Apt 205, Los Angeles, CA 9001<br>50 - 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Válida] Alfabeto Latino | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Válida] Números | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Válida] Espacios | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Válida] Guiones | 100 Universal City Plaza - 0123 |
| [Válida] Puntos | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Válida] Comas | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Inválida] Texto <5 caracteres | 2 - 1s<br>3 - 1st<br>4 - 9550 |
| [Inválida] Texto >50 caracteres | 51 - 350 East 1st Street Apt. 205, Los Angeles, CAL 9001<br>52 - 350 East 1st Street Apt. 205, Los Angeles, CAL<br>53 - 350 East 1st Street Apt. 2051, Los Angeles, CAL 90012 |
| [Inválida] Vacío: 0 caracteres |
| [Inválida] Caracteres especiales | №%@\" |
| [Inválida] Caracteres de otro lenguaje | 加布里埃爾F加布爾 |

### Campo: Estación de Metro
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Selección de alguna estación de la lista | 1st Street |
| [Inválida] Sin selección |

### Campo: Teléfono
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 10-12 caracteres numéricos y símbolo "+" al inicio | 10 - +1234567890<br>11 - +12345678901<br>12 - +123456789012 |
| [Inválida] Texto <10 caracteres | 7 - +1234567<br>8 - +12345678<br>9 - +123456789
| [Inválida] Texto >12 caracteres | 13 - +1234567890123<br>14 - +12345678901234<br>15 - +123456789012345
| [Inválida] Sin el símbolo "+" | 1234567890
| [Inválida] Vacío: 0 caracteres con signo "+" | +
| [Inválida] Vacío: 0 caracteres sin signo "+" |
| [Inválida] Símbolo "+" no inicial | 1+234567890 |
| [Inválida] Alfabeto | +a234567890 |
| [Inválida] Espacios | + 234567890 |
| [Inválida] Guiones | +-234567890 |
| [Inválida] Puntos | +.234567890 |
| [Inválida] Comas | +,234567890 |
| [Inválida] Caracteres especiales | +№%@\"890 |
| [Inválida] Caracteres de otro lenguaje | +加布爾4567890 |

---

## Formulario "Alquiler"

### Campo: Calendario Desplegable "Fecha de Entrega"
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Fecha a partir del día siguiente | Fecha día siguiente<br>Fecha 2 días después<br>Fecha 3 días después |
| [Inválida] Fecha actual y anteriores | Fecha actual<br>Fecha de ayer<br>Fecha de 2 días antes
| [Inválida] Sin selección | 

### Campo: Lista Desplegable "Periodo de Alquiler"
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Selección de días de alquiler | un día |
| [Inválida] Sin selección |

### Campo: Casilla de Verificación "Color"
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Selección de 1 color | ✓ negro |
| [Inválida] Selección de ambos colores | ✓ negro<br>✓ gris |
| [Inválida] Sin selección |

### Campo: Comentario
| Clase | Datos de Prueba | 
| :--- | :--- |
| [Válida] Texto 0-24 caracteres | 0 caracteres<br>1 caracter - A<br>12 caracteres - ArielArielAr<br>23 caracteres - ArielArielArielArielAri<br>24 caracteres - ArielArielArielArielArie |
| [Válida] Alfabeto latino | ArielArielArielArielArie |
| [Válida] Números | 12341234 |
| [Válida] Espacios | Ariel Ariel |
| [Válida] Guiones | Ariel-Ariel |
| [Válida] Puntos | Ariel. |
| [Válida] Comas | Ariel, |
| [Inválida] Texto 25 caracteres y más | 25 caracteres - ArielArielArielArielAriel<br>26 caracteres - ArielArielArielArielArielA<br>27 caracteres - ArielArielArielArielArielAr |
| [Inválida] Caracteres especiales | №%@\" |
| [Inválida] Caracteres de otro lenguaje | 加布里埃爾F加布爾 |