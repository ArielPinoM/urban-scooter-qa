# Test Data - Order Form

This document uses equivalence partitioning and boundary value analysis to cover the most important scenarios of the order form. Each field is divided into valid and invalid classes so that representative inputs from each partition are selected. In addition, cases at the limits of the constraints (for example, 2 and 15 characters in the name) are included to verify behavior at values just inside and just outside the limits.

## Form "Para quién es el scooter"

### Field: Name
| Class | Test Data |
| :--- | :--- |
| [Valid] Text 2-15 characters | 2 - Ar<br>3 - Ari<br>5 - Ariel<br>14 - ArielArielArie<br>15 - ArielArielAriel |
| [Valid] Latin alphabet | Ariel |
| [Valid] Spaces | Ariel Ariel |
| [Valid] Hyphens | Ariel-Ariel |
| [Invalid] Text <2 characters | 1 - A |
| [Invalid] Text >15 characters | 16 - ArielArielArielA<br>17 - ArielArielArielAr<br>18 - ArielArielArielAri |
| [Invalid] Empty: 0 characters |
| [Invalid] Periods | Ariel. |
| [Invalid] Commas | Ariel, |
| [Invalid] Special characters | №%@\" |
| [Invalid] Non-Latin characters | 加布里埃爾F加布爾 |
| [Invalid] Numeric characters | 1234567890 |

### Field: Last Name
| Class | Test Data |
| :--- | :--- |
| [Valid] Text 2-15 characters | 2 - Pi<br>3 - Pin<br>5 - PinoP<br>14 - PinoPinoPinoPin<br>15 - PinoPinoPinoPinoPin |
| [Valid] Latin alphabet | Pino |
| [Valid] Spaces | Pino Pino |
| [Valid] Hyphens | Pino-Pino |
| [Invalid] Text <2 characters | 1 - P |
| [Invalid] Text >15 characters | 16 - PinoPinoPinoPino<br>17 - PinoPinoPinoPinoP<br>18 - PinoPinoPinoPinoPi |
| [Invalid] Empty: 0 characters |
| [Invalid] Periods | Pino. |
| [Invalid] Commas | Pino, |
| [Invalid] Special characters | №%@\" |
| [Invalid] Non-Latin characters | 加布里埃爾F加布爾 |
| [Invalid] Numeric characters | 1234567890 |

### Field: Address
| Class | Test Data |
| :--- | :--- |
| [Valid] Text 5-50 characters | 5 - 95501<br>6 - 955011<br>24 - 1 A St, Eureka, CA 95501<br>49 - 350 East 1st Street Apt 205, Los Angeles, CA 9001<br>50 - 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Valid] Latin alphabet | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Valid] Numbers | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Valid] Spaces | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Valid] Hyphens | 100 Universal City Plaza - 0123 |
| [Valid] Periods | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Valid] Commas | 350 East 1st Street Apt. 205, Los Angeles, CA 9001 |
| [Invalid] Text <5 characters | 2 - 1s<br>3 - 1st<br>4 - 9550 |
| [Invalid] Text >50 characters | 51 - 350 East 1st Street Apt. 205, Los Angeles, CAL 9001<br>52 - 350 East 1st Street Apt. 205, Los Angeles, CAL<br>53 - 350 East 1st Street Apt. 2051, Los Angeles, CAL 90012 |
| [Invalid] Empty: 0 characters |
| [Invalid] Special characters | №%@\" |
| [Invalid] Non-Latin characters | 加布里埃爾F加布爾 |

### Field: Metro Station
| Class | Test Data |
| :--- | :--- |
| [Valid] Select one station from the list | 1st Street |
| [Invalid] No selection |

### Field: Phone
| Class | Test Data |
| :--- | :--- |
| [Valid] Text 10-12 characters with "+" at the beginning | 10 - +1234567890<br>11 - +12345678901<br>12 - +123456789012 |
| [Invalid] Text <10 characters | 7 - +1234567<br>8 - +12345678<br>9 - +123456789 |
| [Invalid] Text >12 characters | 13 - +1234567890123<br>14 - +12345678901234<br>15 - +123456789012345 |
| [Invalid] Missing "+" sign | 1234567890 |
| [Invalid] Empty: 0 characters with "+" sign | + |
| [Invalid] Empty: 0 characters without "+" sign |
| [Invalid] "+" sign not at the beginning | 1+234567890 |
| [Invalid] Alphabet | +a234567890 |
| [Invalid] Spaces | + 234567890 |
| [Invalid] Hyphens | +-234567890 |
| [Invalid] Periods | +.234567890 |
| [Invalid] Commas | +,234567890 |
| [Invalid] Special characters | +№%@\"890 |
| [Invalid] Non-Latin characters | +加布爾4567890 |

---

## Form "Alquiler"

### Field: Dropdown Calendar "Fecha de Entrega"
| Class | Test Data |
| :--- | :--- |
| [Valid] Date from the following day onward | Next day<br>2 days later<br>3 days later |
| [Invalid] Current date and earlier | Current date<br>Yesterday<br>2 days before |
| [Invalid] No selection |

### Field: Dropdown List "Periodo de Alquiler"
| Class | Test Data |
| :--- | :--- |
| [Valid] Select rental days | One day |
| [Invalid] No selection |

### Field: Checkbox "Color"
| Class | Test Data |
| :--- | :--- |
| [Valid] Select 1 color | ✓ black |
| [Invalid] Select both colors | ✓ black<br>✓ gray |
| [Invalid] No selection |

### Field: Comment
| Class | Test Data |
| :--- | :--- |
| [Valid] Text 0-24 characters | 0 characters<br>1 character - A<br>12 characters - ArielArielAr<br>23 characters - ArielArielArielArielAri<br>24 characters - ArielArielArielArielArie |
| [Valid] Latin alphabet | ArielArielArielArielArie |
| [Valid] Numbers | 12341234 |
| [Valid] Spaces | Ariel Ariel |
| [Valid] Hyphens | Ariel-Ariel |
| [Valid] Periods | Ariel. |
| [Valid] Commas | Ariel, |
| [Invalid] Text 25 characters and more | 25 characters - ArielArielArielArielAriel<br>26 characters - ArielArielArielArielArielA<br>27 characters - ArielArielArielArielArielAr |
| [Invalid] Special characters | №%@\" |
| [Invalid] Non-Latin characters | 加布里埃爾F加布爾 |