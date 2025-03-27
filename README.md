# js_13
# Roman Numeral Converter

## 📌 Descripción
Este proyecto es una aplicación web desarrollada en JavaScript que convierte números arábigos (decimales) en números romanos. Implementa validaciones de entrada y maneja errores de usuario para garantizar resultados precisos.

## 🚀 Características
- Convierte números del sistema decimal al sistema romano.
- Valida la entrada del usuario y proporciona mensajes de error adecuados.
- Admite números en el rango de 1 a 3999.
- Interfaz interactiva con botón de conversión y validación en tiempo real.

## 🛠️ Tecnologías utilizadas
- **HTML**: Estructura del formulario y botones.
- **CSS**: Estilización de la interfaz.
- **JavaScript**: Lógica de conversión y validación de datos.

## 📖 Funcionamiento
El código utiliza un array de referencia con pares de valores (símbolo romano y su equivalente decimal). Itera sobre la lista, restando valores hasta convertir completamente el número ingresado.

### 🔢 Algoritmo de conversión
1. Se define una lista ordenada de equivalencias entre números romanos y decimales.
2. Se recorre la lista restando el valor correspondiente mientras el número sea mayor o igual a dicho valor.
3. Se agregan los símbolos romanos correspondientes al resultado final.
4. Se retorna la cadena resultante con la conversión completa.

### 🛡️ Validación de entrada
- **Solo números válidos**: Se bloquean valores vacíos o caracteres no numéricos.
- **Rango permitido**: Se restringe la conversión a números entre **1 y 3999**.
- **Mensajes de error**: Se muestran alertas si la entrada es inválida.

## 🎯 Uso
1. Introduce un número decimal en el campo de entrada.
2. Presiona el botón **Convertir** o usa la tecla **Enter**.
3. Si la entrada es válida, se mostrará el número romano equivalente.
4. Si hay un error, aparecerá un mensaje indicando el problema.

## 📝 Código principal
```javascript
const convertToRoman = num => {
  const ref = [
    ['M', 1000], ['CM', 900], ['D', 500], ['CD', 400], ['C', 100],
    ['XC', 90], ['L', 50], ['XL', 40], ['X', 10], ['IX', 9],
    ['V', 5], ['IV', 4], ['I', 1]
  ];
  const res = [];

  ref.forEach(function (arr) {
    while (num >= arr[1]) {
      res.push(arr[0]);
      num -= arr[1];
    }
  });

  return res.join('');
};
```

## 📌 Contribuciones
Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, puedes abrir un _pull request_ o reportar errores en la sección de _issues_.

## 📜 Licencia
Este proyecto está bajo la licencia MIT.


