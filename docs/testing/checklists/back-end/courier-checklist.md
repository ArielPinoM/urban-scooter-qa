# Checklist - Courier

## Create a courier

`POST /api/v1/courier`

### Data validation in request parameters

#### Field `login` - 201 Created and {ok: true}

1. 2 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
2. 3 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
3. 5 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
4. 9 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
5. 10 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED

#### Field `login` - 400 Bad Request

6. 1 Latin character and remaining required fields with valid data.
    - 🔴 FAILED [[US-34]](../../bug-reports/US-34.md)
7. 11 Latin characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-35]](../../bug-reports/US-35.md)
8. 12 Latin characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-36]](../../bug-reports/US-36.md)
9. 13 Latin characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-37]](../../bug-reports/US-37.md)
10. Empty and remaining required fields with valid data.
    - 🟢 PASSED
11. Omit field and remaining required fields with valid data.
    - 🟢 PASSED
12. Numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-38]](../../bug-reports/US-38.md)
13. Characters with spaces and remaining required fields with valid data.
    - 🔴 FAILED [[US-39]](../../bug-reports/US-39.md)
14. Characters with hyphens and remaining required fields with valid data.
    - 🔴 FAILED [[US-40]](../../bug-reports/US-40.md)
15. Characters with periods and remaining required fields with valid data.
    - 🔴 FAILED [[US-41]](../../bug-reports/US-41.md)
16. Characters with commas and remaining required fields with valid data.
    - 🔴 FAILED [[US-42]](../../bug-reports/US-42.md)
17. Special characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-43]](../../bug-reports/US-43.md)
18. Characters from another language and remaining required fields with valid data.
    - 🔴 FAILED [[US-44]](../../bug-reports/US-44.md)

#### Field `password` - 201 Created and {ok: true}

19. 4 numeric characters and remaining required fields with valid data.
    - 🟢 PASSED

#### Field `password` - 400 Bad Request

20. 1 numeric character and remaining required fields with valid data.
    - 🔴 FAILED [[US-45]](../../bug-reports/US-45.md)
21. 2 numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-46]](../../bug-reports/US-46.md)
22. 3 numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-47]](../../bug-reports/US-47.md)
23. 5 numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-48]](../../bug-reports/US-48.md)
24. 6 numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-49]](../../bug-reports/US-49.md)
25. 7 numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-50]](../../bug-reports/US-50.md)
26. Latin alphabet characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-51]](../../bug-reports/US-51.md)
27. Empty and remaining required fields with valid data returns message "Insufficient data to create an account".
    - 🟢 PASSED
28. Omit field and remaining required fields with valid data returns message "Insufficient data to create an account".
    - 🟢 PASSED
29. Numeric characters with spaces and remaining required fields with valid data.
    - 🔴 FAILED [[US-52]](../../bug-reports/US-52.md)
30. Numeric characters with hyphens and remaining required fields with valid data.
    - 🔴 FAILED [[US-53]](../../bug-reports/US-53.md)
31. Numeric characters with periods and remaining required fields with valid data.
    - 🔴 FAILED [[US-54]](../../bug-reports/US-54.md)
32. Numeric characters with commas and remaining required fields with valid data.
    - 🔴 FAILED [[US-55]](../../bug-reports/US-55.md)
33. Special characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-56]](../../bug-reports/US-56.md)
34. Characters from another language and remaining required fields with valid data.
    - 🔴 FAILED [[US-57]](../../bug-reports/US-57.md)

#### Field `firstName` - 201 Created and {ok: true}

35. 2 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
36. 3 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
37. 5 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
38. 9 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
39. 10 Latin characters and remaining required fields with valid data.
    - 🟢 PASSED
40. Empty and remaining required fields with valid data.
    - 🟢 PASSED
41. Omit field and remaining required fields with valid data.
    - 🟢 PASSED

#### Field `firstName` - 400 Bad Request

42. 1 Latin character and remaining required fields with valid data.
    - 🔴 FAILED [[US-58]](../../bug-reports/US-58.md)
43. 11 Latin characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-59]](../../bug-reports/US-59.md)
44. 12 Latin characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-60]](../../bug-reports/US-60.md)
45. 13 Latin characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-61]](../../bug-reports/US-61.md)
46. Numeric characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-62]](../../bug-reports/US-62.md)
47. Characters with spaces and remaining required fields with valid data.
    - 🔴 FAILED [[US-63]](../../bug-reports/US-63.md)
48. Characters with hyphens and remaining required fields with valid data.
    - 🔴 FAILED [[US-64]](../../bug-reports/US-64.md)
49. Characters with periods and remaining required fields with valid data.
    - 🔴 FAILED [[US-65]](../../bug-reports/US-65.md)
50. Characters with commas and remaining required fields with valid data.
    - 🔴 FAILED [[US-66]](../../bug-reports/US-66.md)
51. Special characters and remaining required fields with valid data.
    - 🔴 FAILED [[US-67]](../../bug-reports/US-67.md)
52. Characters from another language and remaining required fields with valid data.
    - 🔴 FAILED [[US-68]](../../bug-reports/US-68.md)

### Request body validation

#### Account created successfully - 201 Created and {ok: true}

53. All required fields valid and firstName valid.		
    - 🟢 PASSED
54. All required fields valid omitting firstName.
    - 🟢 PASSED

#### 400 Bad Request

55. Invalid login field, valid password and omit firstName.
    - 🟢 PASSED
56. Omit login field and firstName, valid password returns message "Insufficient data to create an account".
    - 🟢 PASSED
57. Valid login field, invalid password and omit firstName.
    - 🟢 PASSED
58. Valid login field, omit password and firstName returns message "Insufficient data to create an account".
    - 🟢 PASSED
59. Valid login field, valid password and invalid firstName.
    - 🔴 FAILED [[US-69]](../../bug-reports/US-69.md)

#### 409 Conflict

60. Send request with existing login field returns message "This login is not available".
    - 🟢 PASSED

### Verify Database - Couriers Table

61. Login field matches the one sent.
    - 🟢 PASSED
62. passwordHash field in the table is not plain text password (it is a hash).
    - 🟢 PASSED
63. firstName field matches the one sent.
    - 🟢 PASSED
64. Sending a login that already exists does not create another record.
    - 🟢 PASSED

## Delete a courier

`DELETE /api/v1/courier/:id`

65. Send DELETE /api/v1/courier/:id with existing id returns 200 OK and {ok: true}.
    - 🟢 PASSED
66. Verify in the Couriers table that the record with that id no longer exists.
    - 🟢 PASSED
67. Verify in the Orders table that all orders whose courierId matched the deleted id have been deleted.
    - 🔴 FAILED [[US-70]](../../bug-reports/US-70.md)
68. Omit the id field returns 400 Bad Request and message "Insufficient data to delete the courier".
    - 🔴 FAILED [[US-71]](../../bug-reports/US-71.md)
69. Send a request with a non-existent id returns 404 Not Found and message "No courier with this ID".
    - 🟢 PASSED

## Get an order by its number

`GET /api/v1/orders/track?t=<order_number>`

70. Valid "t" parameter and an order exists with that number returns 200 OK and the response matches the data from the record in the "Orders" table.
    - 🟢 PASSED
71. Omit the parameter returns 400 Bad Request and message "Insufficient data for search".
    - 🟢 PASSED
72. Send the request with a non-existent order number returns 404 Not Found and message "Order not found".
    - 🟢 PASSED