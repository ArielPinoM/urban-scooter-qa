# Checklist - "Realizar Pedido" Screen

## Design Tests

### Header

#### Logo
41. The logo is present and displayed in the top left position according to Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

42. The logo is not pixelated or distorted.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

#### Header Buttons
43. The "Pedir" button is present and in the expected position.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

44. The "Estado del pedido" button is present and in the expected position.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

45. Background color of the "Pedir" button matches Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

46. Background color of the "Estado del pedido" button matches Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

47. On hover over "Pedir", the button displays the style specified in Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Chrome 85 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1280x720: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

48. On hover over "Estado del pedido", the button displays the style specified in Figma.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED
- Chrome 85 or higher, 1280x720: 🔴 FAILED
- Opera 71 or higher, 1280x720: 🔴 FAILED
- Opera 71 or higher, 1920x1080: 🔴 FAILED
- [[US-11]](/docs/testing/bug-reports/US-11.md)

---

# Form "Para quién es el scooter"

## Functional Tests

### Validations
49. If "Nombre" is empty or invalid, when attempting to advance, error "Introduce un Nombre correcto" is displayed.
- Opera 71 or higher, 1920x1080: 🟢 PASSED

50. If "Apellido" is empty or invalid, when attempting to advance, error "Introduce un apellido válido" is displayed.
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-12]](/docs/testing/bug-reports/US-12.md)

51. If "Dirección" is empty or invalid, when attempting to advance, error "Introduce una dirección válida" is displayed.
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-13]](/docs/testing/bug-reports/US-13.md)

52. If "Estación de metro" is empty, when attempting to advance, error "Introduce una estación de metro correcta" is displayed.
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-14]](/docs/testing/bug-reports/US-14.md)

53. If "Teléfono" is empty or invalid, when attempting to advance, error "Introduce un número de teléfono válido" is displayed.
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-15]](/docs/testing/bug-reports/US-15.md)

### Navigation
54. If all fields are filled correctly, clicking "Siguiente" advances to the "Alquiler" form.
- Opera 71 or higher, 1920x1080: 🟢 PASSED

55. If any field is marked invalid, clicking "Siguiente" displays the corresponding error and does not advance.
- Opera 71 or higher, 1920x1080: 🟢 PASSED

## Design Tests

### Header
56. If any field is marked invalid, clicking "Siguiente" displays the corresponding error and does not advance.
- Opera 71 or higher, 1920x1080: 🟢 PASSED

### Fields
57. The "Nombre" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

58. The placeholder for "Nombre" matches "* Nombre".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

59. Invalid "Nombre" is highlighted in red.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

60. The "Apellido" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

61. The placeholder for "Apellido" matches "* Apellido".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

62. Invalid "Apellido" is highlighted in red.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

63. The "Dirección" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

64. The placeholder for "Dirección" matches "* Dirección: a dónde llevar el scooter".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

65. Invalid "Dirección" is highlighted in red.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

66. The "Estación de metro" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

67. The placeholder for "Estación de metro" matches "* Estación de metro".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

68. The "Teléfono" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

69. The placeholder for "Teléfono" matches "Teléfono: el repartidor o repartidora te llamará".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

70. Invalid "Teléfono" is highlighted in red.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

71. Required fields are marked with an asterisk.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

### "Siguiente" Button
72. The "Siguiente" button is present at the bottom of the form.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

73. Background color of the "Siguiente" button matches Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

74. On hover over "Siguiente", the button displays the style specified in Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

75. On hover over "Siguiente", the cursor changes to a hand.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

---

# Form "Alquiler"

## Functional Tests

### Field Validations

76. If "Fecha de entrega" is marked invalid, clicking "Pedir" displays error "Introduce una fecha de entrega correcta".
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-16]](/docs/testing/bug-reports/US-16.md)

77. If "Periodo de alquiler" is marked invalid, clicking "Pedir" displays error "Introduce un Periodo de alquiler correcto".
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-17]](/docs/testing/bug-reports/US-17.md)

### "Atrás" Button
78. Clicking "Atrás" returns to the "Who is the scooter for?" screen.
- Opera 71 or higher, 1920x1080: 🟢 PASSED

79. The fields in the "Rental" form retain information when returning after advancing again.
- Opera 71 or higher, 1920x1080: 🟢 PASSED

### "Pedir" Button
80. With all required fields correct, clicking "Pedir" displays a modal "El pedido ha sido realizado".
- Chrome 85 or higher, 1920x1080
- Opera 71 or higher, 1920x1080
- 🔴 FAILED [[US-1]](/docs/testing/bug-reports/US-1.md)

81. The modal displays the message "Número de pedido NNNNN. Escríbelo: será útil para darle seguimiento al estado".
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

82. The modal contains a "Comprueba el estado" button.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

83. Clicking "Comprueba el estado" redirects to the "Order Status" screen.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

84. On the "Order Status" screen, the "Número de pedido" field appears already filled with the number of the newly created order.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

### "Pedir" Button (Error)
85. If any required field is empty or invalid, clicking "Pedir" displays an error message indicating the problematic field.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-18]](/docs/testing/bug-reports/US-18.md)

86. The form is not submitted until all required fields are correct.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🔴 FAILED [[US-16]](/docs/testing/bug-reports/US-16.md)

### Multiple Orders
87. After successfully placing an order, the user can place another order.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

88. The data from the new order does not mix with data from the previous order.
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

89. Each order generates a different order number (visible in the modal).
- Chrome 85 or higher, 1920x1080: 🟡 SKIPPED - Cannot create order [[BUG US-1]](/docs/testing/bug-reports/US-1.md)
- Opera 71 or higher, 1920x1080: 🟢 PASSED

## Design Tests

### Header
90. The header text matches "Alquiler".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

### Fields
91. The "Fecha de entrega" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

92. The placeholder for "Fecha de entrega" matches "* Cuándo entregar el scooter".
- Chrome 85 or higher, 1920x1080: 🔴 FAILED 
- Opera 71 or higher, 1920x1080: 🔴 FAILED
- [[US-19]](/docs/testing/bug-reports/US-19.md)

93. Focus on "Fecha de entrega" is highlighted in blue.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

94. "Fecha de entrega" is required, has visual indication "*".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

95. The "Periodo de alquiler" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

96. The placeholder for "Periodo de alquiler" matches "* Periodo de alquiler".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

97. "Periodo de alquiler" is required, has visual indication "*".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

98. The "Color" field is present.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

99. The placeholder for "Color" matches "El color del scooter ☐ negro ☐ gris".  
- Chrome 85 or higher, 1920x1080: 🟢 PASSED  
- Opera 71 or higher, 1920x1080: 🟢 PASSED  

100. The "Comentario" field is present.  
- Chrome 85 or higher, 1920x1080: 🟢 PASSED  
- Opera 71 or higher, 1920x1080: 🟢 PASSED  

101. The placeholder for "Comentario" matches "Comentario".
- Chrome 85 or higher, 1920x1080: 🟢 PASSED  
- Opera 71 or higher, 1920x1080: 🟢 PASSED  

### Buttons

102. The "Atrás" button is present at the bottom of the form.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

103. Background color of the "Atrás" button matches Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

104. On hover over "Atrás", the button displays the style specified in Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

105. On hover over "Atrás", the cursor changes to a hand.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

106. The "Pedir" button is present at the bottom of the form.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

107. Background color of the "Pedir" button matches Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

108. Background color of the "Pedir" button matches Figma.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED
- Opera 71 or higher, 1920x1080: 🟢 PASSED

108. On hover over "Pedir", the cursor changes to a hand.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 
- Opera 71 or higher, 1920x1080: 🟢 PASSED 

## Data Validation Tests for Fields
Each item verifies:
- The visual signaling of the field (error styling).
- The blocking/permission logic in the flow ("Siguiente" or "Pedir" button).

### Form "Para quién es el scooter"

#### Nombre
109. **VALID** – Length 2 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

110. **VALID** – Length 3 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

111. **VALID** – Length 5 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

112. **VALID** – Length 14 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

113. **VALID** – Length 15 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

114. **INVALID** – Length 1 character.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

115. **INVALID** – Length 16 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

116. **INVALID** – Length 17 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

117. **INVALID** – Length 18 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

118. **INVALID** – Empty: 0 characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

119. **VALID** – Latin alphabet characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

120. **VALID** – Name with spaces
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

121. **VALID** – Name with hyphens
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

122. **INVALID** – Name with periods
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

123. **INVALID** – Name with commas
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

124. **INVALID** – Name with special characters [ №%@\" ]
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

125. **INVALID** – Characters from another language [ 加布里埃爾F加布爾 ]
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

126. **INVALID** – Numbers
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

#### Apellido

127. **VALID** – Length 2 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

128. **VALID** – Length 3 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

129. **VALID** – Length 5 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

130. **VALID** – Length 14 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

131. **VALID** – Length 15 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

132. **INVALID** – Length 1 character.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

133. **INVALID** – Length 16 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-20]](/docs/testing/bug-reports/US-20.md)

134. **INVALID** – Length 17 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-21]](/docs/testing/bug-reports/US-21.md)

135. **INVALID** – Length 18 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-22]](/docs/testing/bug-reports/US-22.md)

136. **INVALID** – Empty: 0 characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

137. **VALID** – Latin alphabet characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

138. **VALID** – Last name with spaces
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

139. **VALID** – Last name with hyphens
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

140. **INVALID** – Last name with periods
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

141. **INVALID** – Last name with commas
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

142. **INVALID** – Last name with special characters [ №%@\" ]
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

143. **INVALID** – Characters from another language [ 加布里埃爾F加布爾 ]
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

144. **INVALID** – Numbers
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

#### Dirección
145. **VALID** – Length 5 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

146. **VALID** – Length 6 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

147. **VALID** – Length 24 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

148. **VALID** – Length 49 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

149. **VALID** – Length 50 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-23]](/docs/testing/bug-reports/US-23.md)

150. **INVALID** – Length 2 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

151. **INVALID** – Length 3 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

152. **INVALID** – Length 4 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

153. **INVALID** – Length 51 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

154. **INVALID** – Length 52 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

155. **INVALID** – Length 53 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

156. **INVALID** – Empty: 0 characters
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-24]](/docs/testing/bug-reports/US-24.md)

157. **VALID** – Latin alphabet characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

158. **VALID** – Numbers
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

159. **VALID** – Address with spaces
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

160. **VALID** – Address with hyphens
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

161. **VALID** – Address with periods
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

162. **VALID** – Address with commas
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

163. **INVALID** – Address with special characters [ №%@\" ]
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

164. **INVALID** – Characters from another language [ 加布里埃爾F加布爾 ]
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

#### Metro Station
165. **VALID** - Selection of any station from the list.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

166. **INVALID** - No selection.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

#### Teléfono

167. **VALID** - Length of 10 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

168. **VALID** - Length of 11 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

169. **VALID** - Length of 12 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

170. **INVALID** - Length of 7 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

171. **INVALID** - Length of 8 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

172. **INVALID** - Length of 9 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

173. **INVALID** - Length of 13 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

174. **INVALID** - Length of 14 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

175. **INVALID** - Length of 15 numeric characters and "+" symbol at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

176. **INVALID** - Without the "+" symbol.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-25]](/docs/testing/bug-reports/US-25.md)

177. **INVALID** - Empty: 0 characters with "+" sign.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

178. **INVALID** - Empty: 0 characters without "+" sign.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

179. **INVALID** - "+" symbol not at the beginning.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

180. **INVALID** - Phone with alphabetic characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

181. **INVALID** - Phone with spaces
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

182. **INVALID** - Phone with hyphens
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

183. **INVALID** - Phone with periods
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

184. **INVALID** - Phone with commas
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

185. **INVALID** - Phone with special characters
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

186. **INVALID** - Phone with characters from another language
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

### Form "Alquiler"

#### Delivery Date

187. **VALID** - Date starting from tomorrow.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

188. **VALID** - Date 2 days later.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

189. **VALID** - Date 3 days later.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

190. **INVALID** - Yesterday's date.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-16]](/docs/testing/bug-reports/US-16.md)

191. **INVALID** - Today's date.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-16]](/docs/testing/bug-reports/US-16.md)

192. **INVALID** - Date 2 days ago.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-16]](/docs/testing/bug-reports/US-16.md)

193. **INVALID** - No delivery date selection.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-16]](/docs/testing/bug-reports/US-16.md)

#### Rental Period

194. **VALID** - Selection of rental days.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

195. **INVALID** - No selection of rental days.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-17]](/docs/testing/bug-reports/US-17.md)

#### Color

196. **VALID** - Selection of one color.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

197. **VALID** - Selection of both colors.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

198. **VALID** - No color selection.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

#### Comment

199. **VALID** - Empty: 0 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

200. **VALID** - Length of 1 character.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

201. **VALID** - Length of 12 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

202. **VALID** - Length of 23 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

203. **VALID** - Length of 24 characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

204. **INVALID** - Length of 25 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-26]](/docs/testing/bug-reports/US-26.md)

205. **INVALID** - Length of 26 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-27]](/docs/testing/bug-reports/US-27.md)

206. **INVALID** - Length of 27 characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-28]](/docs/testing/bug-reports/US-28.md)

207. **VALID** - Comment with Latin alphabet characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

208. **VALID** - Comment with numeric characters.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

209. **VALID** - Comment with spaces.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

210. **VALID** - Comment with hyphens.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

211. **VALID** - Comment with periods.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

212. **VALID** - Comment with commas.
- Chrome 85 or higher, 1920x1080: 🟢 PASSED 

213. **INVALID** - Comment with special characters.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-29]](/docs/testing/bug-reports/US-29.md)

214. **INVALID** - Comment with characters from another language.
- Chrome 85 or higher, 1920x1080: 🔴 FAILED [[US-30]](/docs/testing/bug-reports/US-30.md)