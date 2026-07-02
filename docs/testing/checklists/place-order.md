# Checklist - Pantalla "Realizar Pedido"

## Pruebas de diseño

### Header

#### Logo
41. El logo está presente y se muestra en la posición superior izquierda según Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

42. El logo no está pixelado ni deformado.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

#### Botones del header
43. El botón "Pedir" está presente y en la posición esperada.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

44. El botón "Estado del pedido" está presente y en la posición esperada.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

45. Color de fondo del botón "Pedir" coincide con Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

46. Color de fondo del botón "Estado del pedido" coincide con Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

47. Al hacer hover en "Pedir", el botón muestra el estilo especificado en Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Chrome 85 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1280x720: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

48. Al hacer hover en "Estado del pedido", el botón muestra el estilo especificado en Figma.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED
- Chrome 85 o superior, 1280x720: 🔴 FAILED
- Opera 71 o superior, 1280x720: 🔴 FAILED
- Opera 71 o superior, 1920x1080: 🔴 FAILED
- [[US-11]](../bug-reports/US-11.md)

---

# Formulario "Para quién es el scooter"

## Pruebas Funcionales

### Validaciones
49. Si "Nombre" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un Nombre correcto".
- Opera 71 o superior, 1920x1080: 🟢 PASSED

50. Si "Apellido" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un apellido válido".
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-12]](../bug-reports/US-12.md)

51. Si "Dirección" está vacía o es inválida, al intentar avanzar se muestra error "Introduce una dirección válida".
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-13]](../bug-reports/US-13.md)

52. Si "Estación de metro" está vacía, al intentar avanzar se muestra error "Introduce una estación de metro correcta".
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-14]](../bug-reports/US-14.md)

53. Si "Teléfono" está vacío o es inválido, al intentar avanzar se muestra error "Introduce un número de teléfono válido".
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-15]](../bug-reports/US-15.md)

### Navegación
54. Si todos los campos están rellenados correctamente, al hacer clic en "Siguiente" se avanza al formulario "Alquiler".
- Opera 71 o superior, 1920x1080: 🟢 PASSED

55. Si algún campo se marca como inválido, al hacer clic en "Siguiente" se muestra el error correspondiente y no se avanza.
- Opera 71 o superior, 1920x1080: 🟢 PASSED

## Pruebas de diseño

### Encabezado
56. Si algún campo se marca como inválido, al hacer clic en "Siguiente" se muestra el error correspondiente y no se avanza.
- Opera 71 o superior, 1920x1080: 🟢 PASSED

### Campos
57. El campo "Nombre" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

58. El placeholder de "Nombre" coincide con "* Nombre".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

59. "Nombre" inválido se resalta en rojo.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

60. El campo "Apellido" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

61. El placeholder de "Apellido" coincide con "* Apellido".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

62. "Apellido" inválido se resalta en rojo.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

63. El campo "Dirección" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

64. El placeholder de "Dirección" coincide con "* Dirección: a dónde llevar el scooter".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

65. "Dirección" inválida se resalta en rojo.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

66. El campo "Estación de metro" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

67. El placeholder de "Estación de metro" coincide con "* Estación de metro".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

68. El campo "Teléfono" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

69. El placeholder de "Teléfono" coincide con "Teléfono: el repartidor o repartidora te llamará".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

70. "Teléfono" inválido se resalta en rojo.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

71. Los campos obligatorios están marcados con asterisco.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

### Botón "Siguiente"
72. El botón "Siguiente" está presente en la parte inferior del formulario.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

73. Color de fondo del botón "Siguiente" coincide con Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

74. Al hacer hover en "Siguiente", el botón muestra el estilo especificado en Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

75. Al hacer hover en "Siguiente", el cursor cambia a mano.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

---

# Formulario "Alquiler"

## Pruebas funcionales

### Validaciones de campos

76. Si "Fecha de entrega" se marca como inválido, al hacer clic en "Pedir" se muestra error "Introduce una fecha de entrega correcta".
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

77. Si "Periodo de alquiler" se marca como inválido, al hacer clic en "Pedir" se muestra error "Introduce un Periodo de alquiler correcto".
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-17]](../bug-reports/US-17.md)

### Botón "Atrás"
78. Al hacer clic en "Atrás" se regresa a la pantalla "Para quién es el scooter".
- Opera 71 o superior, 1920x1080: 🟢 PASSED

79. Los campos de "Alquiler" conservan la información al regresar después de haber avanzado nuevamente.
- Opera 71 o superior, 1920x1080: 🟢 PASSED

### Botón "Pedir"
80. Con todos los campos obligatorios correctos, al hacer clic en "Pedir" aparece una ventana emergente "El pedido ha sido realizado".
- Chrome 85 o superior, 1920x1080
- Opera 71 o superior, 1920x1080
- 🔴 FAILED [[US-1]](../bug-reports/US-1.md)

81. La ventana emergente muestra el mensaje "Número de pedido NNNNN. Escríbelo: será útil para darle seguimiento al estado".
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

82. La ventana emergente contiene un botón "Comprueba el estado".
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

83. Al hacer clic en "Comprueba el estado" se redirige a la pantalla "Estado del pedido".
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

84. En la pantalla "Estado del pedido", el campo "Número de pedido" aparece ya completado con el número del pedido recién creado.
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

### Botón "Pedir" (error)
85. Si algún campo obligatorio está vacío o es inválido, al hacer clic en "Pedir" aparece un mensaje de error indicando el campo problemático.
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-18]](../bug-reports/US-18.md)

86. El formulario no se envía hasta que todos los campos obligatorios sean correctos.
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

### Múltiples pedidos
87. Después de realizar un pedido exitosamente, el usuario puede realizar otro pedido.
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

88. Los datos del nuevo pedido no se mezclan con los del anterior.
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

89. Cada pedido genera un número de pedido distinto (visible en la ventana emergente).
- Chrome 85 o superior, 1920x1080: 🟡 SKIPPED - No se puede crear pedido [[BUG US-1]](../bug-reports/US-1.md)
- Opera 71 o superior, 1920x1080: 🟢 PASSED

## Pruebas de diseño

### Encabezado
90. El texto del encabezado coincide con "Alquiler".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

### Campos
91. El campo "Fecha de entrega" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

92. El placeholder de "Fecha de entrega" coincide con "* Cuándo entregar el scooter".
- Chrome 85 o superior, 1920x1080: 🔴 FAILED 
- Opera 71 o superior, 1920x1080: 🔴 FAILED
- [[US-19]](../bug-reports/US-19.md)

93. Focus en "Fecha de entrega" se resalta en azul.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

94. "Fecha de entrega" es obligatorio, tiene indicación visual "*".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

95. El campo "Periodo de alquiler" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

96. El placeholder de "Periodo de alquiler" coincide con "* Periodo de alquiler".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

97. "Periodo de alquiler" es obligatorio, tiene indicación visual "*".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

98. El campo "Color" está presente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

99. El placeholder de "Color" coincide con "El color del scooter ☐ negro ☐ gris".  
- Chrome 85 o superior, 1920x1080: 🟢 PASSED  
- Opera 71 o superior, 1920x1080: 🟢 PASSED  

100. El campo "Comentario" está presente.  
- Chrome 85 o superior, 1920x1080: 🟢 PASSED  
- Opera 71 o superior, 1920x1080: 🟢 PASSED  

101. El placeholder de "Comentario" coincide con "Comentario".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED  
- Opera 71 o superior, 1920x1080: 🟢 PASSED  

### Botones

102. El botón "Atrás" está presente en la parte inferior del formulario.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

103. Color de fondo del botón "Atrás" coincide con Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

104. Al hacer hover en "Atrás", el botón muestra el estilo especificado en Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

105. Al hacer hover en "Atrás", el cursor cambia a mano.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

106. El botón "Pedir" está presente en la parte inferior del formulario.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

107. Color de fondo del botón "Pedir" coincide con Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

108. Color de fondo del botón "Pedir" coincide con Figma.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED
- Opera 71 o superior, 1920x1080: 🟢 PASSED

108. Al hacer hover en "Pedir", el cursor cambia a mano.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 
- Opera 71 o superior, 1920x1080: 🟢 PASSED 

## Pruebas de validación de datos en los campos
Cada ítem verifica:
- La señalización visual del campo (estilo de error).
- La lógica de bloqueo/permiso en el flujo (botón "Siguiente" o "Pedir").

### Formulario "Para quién es el scooter"

#### Nombre
109. **VÁLIDO** – Longitud 2 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

110. **VÁLIDO** – Longitud 3 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

111. **VÁLIDO** – Longitud 5 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

112. **VÁLIDO** – Longitud 14 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

113. **VÁLIDO** – Longitud 15 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

114. **INVÁLIDO** – Longitud 1 caracter.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

115. **INVÁLIDO** – Longitud 16 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

116. **INVÁLIDO** – Longitud 17 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

117. **INVÁLIDO** – Longitud 18 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

118. **INVÁLIDO** – Vacío: 0 caracteres
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

119. **VÁLIDO** – Caracteres del alfabeto latino
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

120. **VÁLIDO** – Nombre con espacios
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

121. **VÁLIDO** – Nombre con guiones
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

122. **INVÁLIDO** – Nombre con puntos
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

123. **INVÁLIDO** – Nombre con comas
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

124. **INVÁLIDO** – Nombre con caracteres especiales [ №%@\" ]
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

125. **INVÁLIDO** – Caracteres de otro lenguaje [ 加布里埃爾F加布爾 ]
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

126. **INVÁLIDO** – Números
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

#### Apellido

127. **VÁLIDO** – Longitud 2 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

128. **VÁLIDO** – Longitud 3 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

129. **VÁLIDO** – Longitud 5 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

130. **VÁLIDO** – Longitud 14 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

131. **VÁLIDO** – Longitud 15 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

132. **INVÁLIDO** – Longitud 1 caracter.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

133. **INVÁLIDO** – Longitud 16 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-20]](../bug-reports/US-20.md)

134. **INVÁLIDO** – Longitud 17 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-21]](../bug-reports/US-21.md)

135. **INVÁLIDO** – Longitud 18 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-22]](../bug-reports/US-22.md)

136. **INVÁLIDO** – Vacío: 0 caracteres
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

137. **VÁLIDO** – Caracteres del alfabeto latino
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

138. **VÁLIDO** – Apellido con espacios
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

139. **VÁLIDO** – Apellido con guiones
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

140. **INVÁLIDO** – Apellido con puntos
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

141. **INVÁLIDO** – Apellido con comas
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

142. **INVÁLIDO** – Apellido con caracteres especiales [ №%@\" ]
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

143. **INVÁLIDO** – Caracteres de otro lenguaje [ 加布里埃爾F加布爾 ]
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

144. **INVÁLIDO** – Números
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

#### Dirección
145. **VÁLIDO** – Longitud 5 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

146. **VÁLIDO** – Longitud 6 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

147. **VÁLIDO** – Longitud 24 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

148. **VÁLIDO** – Longitud 49 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

149. **VÁLIDO** – Longitud 50 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-23]](../bug-reports/US-23.md)

150. **INVÁLIDO** – Longitud 2 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

151. **INVÁLIDO** – Longitud 3 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

152. **INVÁLIDO** – Longitud 4 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

153. **INVÁLIDO** – Longitud 51 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

154. **INVÁLIDO** – Longitud 52 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

155. **INVÁLIDO** – Longitud 53 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

156. **INVÁLIDO** – Vacío: 0 caracteres
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-24]](../bug-reports/US-24.md)

157. **VÁLIDO** – Caracteres del alfabeto latino
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

158. **VÁLIDO** – Números
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

159. **VÁLIDO** – Dirección con espacios
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

160. **VÁLIDO** – Dirección con guiones
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

161. **VÁLIDO** – Dirección con puntos
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

162. **VÁLIDO** – Dirección con comas
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

163. **INVÁLIDO** – Dirección con caracteres especiales [ №%@\" ]
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

164. **INVÁLIDO** – Caracteres de otro lenguaje [ 加布里埃爾F加布爾 ]
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

#### Estación de Metro
165. **VÁLIDO** - Selección de alguna estación de la lista.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

166. **INVÁLIDO** - Sin selección.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

#### Teléfono

167. **VÁLIDO** - Longitud de 10 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

168. **VÁLIDO** - Longitud de 11 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

169. **VÁLIDO** - Longitud de 12 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

170. **INVÁLIDO** - Longitud de 7 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

171. **INVÁLIDO** - Longitud de 8 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

172. **INVÁLIDO** - Longitud de 9 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

173. **INVÁLIDO** - Longitud de 13 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

174. **INVÁLIDO** - Longitud de 14 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

175. **INVÁLIDO** - Longitud de 15 caracteres numéricos y símbolo "+" al inicio.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

176. **INVÁLIDO** - Sin el símbolo "+".
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-25]](../bug-reports/US-25.md)

177. **INVÁLIDO** - Vacío: 0 caracteres con signo "+".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

178. **INVÁLIDO** - Vacío: 0 caracteres sin signo "+".
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

179. **INVÁLIDO** - Símbolo "+" no inicial.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

180. **INVÁLIDO** - Teléfono con caracteres del alfabeto
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

181. **INVÁLIDO** - Teléfono con espacios
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

182. **INVÁLIDO** - Teléfono con guiones
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

183. **INVÁLIDO** - Teléfono con puntos
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

184. **INVÁLIDO** - Teléfono con comas
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

185. **INVÁLIDO** - Teléfono con caracteres especiales
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

186. **INVÁLIDO** - Teléfono con caracteres de otro lenguaje
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

### Formulario "Alquiler"

#### Fecha de entrega

187. **VÁLIDO** - Fecha a partir del día siguiente.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

188. **VÁLIDO** - Fecha 2 días después.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

189. **VÁLIDO** - Fecha 3 días después.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

190. **INVÁLIDO** - Fecha de ayer.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

191. **INVÁLIDO** - Fecha de hoy.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

192. **INVÁLIDO** - Fecha de 2 días antes.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

193. **INVÁLIDO** - Sin selección de fecha de entrega.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-16]](../bug-reports/US-16.md)

#### Periodo de alquiler

194. **VÁLIDO** - Selección de días de alquiler.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

195. **INVÁLIDO** - Sin selección de días de alquiler.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-17]](../bug-reports/US-17.md)

#### Color

196. **VÁLIDO** - Selección de un color.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

197. **VÁLIDO** - Selección de ambos colores.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

198. **VÁLIDO** - Sin selección de color.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

#### Comentario

199. **VÁLIDO** - Vacío: 0 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

200. **VÁLIDO** - Longitud de 1 caracter.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

201. **VÁLIDO** - Longitud de 12 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

202. **VÁLIDO** - Longitud de 23 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

203. **VÁLIDO** - Longitud de 24 caracteres.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

204. **INVÁLIDO** - Longitud de 25 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-26]](../bug-reports/US-26.md)

205. **INVÁLIDO** - Longitud de 26 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-27]](../bug-reports/US-27.md)

206. **INVÁLIDO** - Longitud de 27 caracteres.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-28]](../bug-reports/US-28.md)

207. **VÁLIDO** - Comentario con caracteres del alfabeto latino.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

208. **VÁLIDO** - Comentario con caracteres numéricos.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

209. **VÁLIDO** - Comentario con espacios.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

210. **VÁLIDO** - Comentario con guiones.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

211. **VÁLIDO** - Comentario con puntos.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

212. **VÁLIDO** - Comentario con comas.
- Chrome 85 o superior, 1920x1080: 🟢 PASSED 

213. **INVÁLIDO** - Comentario con caracteres especiales.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-29]](../bug-reports/US-29.md)

214. **INVÁLIDO** - Comentario con caracteres de otro lenguaje.
- Chrome 85 o superior, 1920x1080: 🔴 FAILED [[US-30]](../bug-reports/US-30.md)