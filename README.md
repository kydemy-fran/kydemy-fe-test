# Test Front-End Kydemy

Ejercicio rápido en tiempo real para entrevista de trabajo front-end.

**Directrices del ejercicio:**
- Durante todo momento describir qué se está haciendo y por qué.
- Se puede buscar, copiar y pegar código de internet.
- Se puede usar cualquier tecnología que se desee. (front-end web) Preferiblemente un framework JS + TypeScript (Vue.js, React, Angular, etc.) En lugar de TypeScript también se puede usar JavaScript ES6 como alternativa.
- Se puede usar cualquier librería de CSS o framework de CSS (tailwind, bulma, bootstrap, etc). También es válido usar CSS vanilla o SCSS, SASS, LESS, etc.

**Se valorará:**
- Pensamiento creativo.
- Experiencia de usuario.
- Gestión correcta de los datos y errores.
- Calidad del HTML y CSS.
- Calidad y sofisticación del código.
- Progreso obtenido durante 30 minutos.
- Opcional: estilos adicionales y animaciones.

# Descripción de alto nivel
Crear una paǵina/componente donde se muestre una lista o placeholder (lista vacía o mensaje, pero sin mostrar ningún dato) y un botón.
Al hacer click al botón vamos a simular una petición a una API para recuperar un listado de Strings.
Hay que validad cuales de esas Strings son DNIs válidos. (sin letra final)
Para los DNIs válidos mostrar la letra asociada al DNI.
Ordenaremos las strings en una sola lista donde los valores estarán ordenados de la siguiente forma:
1. Primero los valores que son DNIs válidos
2. Estos valores válidos se ordenarán por orden alfabético de la Letra del DNI
3. Después los valores no válidos, ordenados de forma desdendente por la longitud de la String.
4. (opcional) Para los valores no válidos, en lugar de mostrar la letra del DNI, se mostrará un botón. Al hacer click en el botón, desaparecerá ese elemento de la lista.

## Detalles y requisitos:
1. Al hacer click al botón, se debe esperar 2 segundos, simulando una carga de datos. Valorar cómo se da feedback al usuario durante la espera.
2. Los elementos no válidos estarán resaltados de alguna forma para identificar que contienen errores.
3. Los datos a utilizar (respuesta de la petición serán los siguientes):
```javascript
const data = ['123ADS23', '12345678', '87654321', '1245', '44587456', '445678912354']
``` 
4. Se considerarán DNIs válidos (en este ejercicio) aquellas Strings que cumplan los siguientes requisitos:
  - Solamente contienen números.
  - La String tiene una longitud de 6 a 8 carácteres.
  - Como se puede ver en los datos, hay tres cadenas válidas y otras tres inválidas.
5. Para calcular la letra del DNI se utiliza el resto de la división del número del DNI entre 23. **(módulo 23)** El resultado es el índice de la letra en el siguiente array:
```javascript
const lettersDNI = ['T', 'R', 'W', 'A', 'G', 'M', 'Y', 'F', 'P', 'D', 'X', 'B', 'N', 'J', 'Z', 'S', 'Q', 'V', 'H', 'L', 'C', 'K', 'E']
```


**¡Suerte!**
