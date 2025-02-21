## 🔹 Funciones de Cadena en SQL

| Función                           | Descripción                                                                  | Ejemplo de uso                                                       |
|-----------------------------------|------------------------------------------------------------------------------|----------------------------------------------------------------------|
| `CONCAT(cadena1, cadena2)`         | Concatenar dos o más cadenas.                                                 | `SELECT CONCAT('Hola', ' Mundo')` → `'Hola Mundo'`                   |
| `LENGTH(cadena)`                   | Devuelve la longitud de una cadena (número de caracteres).                    | `SELECT LENGTH('Hola Mundo')` → `10`                                 |
| `LOWER(cadena)`                    | Convierte todos los caracteres de la cadena a minúsculas.                    | `SELECT LOWER('Hola Mundo')` → `'hola mundo'`                        |
| `UPPER(cadena)`                    | Convierte todos los caracteres de la cadena a mayúsculas.                    | `SELECT UPPER('Hola Mundo')` → `'HOLA MUNDO'`                        |
| `TRIM(cadena)`                     | Elimina los espacios en blanco al principio y al final de la cadena.         | `SELECT TRIM('  Hola Mundo  ')` → `'Hola Mundo'`                     |
| `LTRIM(cadena)`                    | Elimina los espacios en blanco al principio de la cadena.                    | `SELECT LTRIM('  Hola Mundo')` → `'Hola Mundo'`                      |
| `RTRIM(cadena)`                    | Elimina los espacios en blanco al final de la cadena.                        | `SELECT RTRIM('Hola Mundo  ')` → `'Hola Mundo'`                      |
| `SUBSTR(cadena, inicio, longitud)` | Extrae una subcadena de una cadena a partir de una posición especificada.    | `SELECT SUBSTR('Hola Mundo', 1, 4)` → `'Hola'`                       |
| `INSTR(cadena, subcadena)`         | Devuelve la posición de la primera aparición de una subcadena dentro de la cadena. | `SELECT INSTR('Hola Mundo', 'Mundo')` → `6`                        |
| `REPLACE(cadena, antiguo, nuevo)`  | Reemplaza una subcadena dentro de la cadena por otra subcadena.               | `SELECT REPLACE('Hola Mundo', 'Mundo', 'Universo')` → `'Hola Universo'` |
| `RIGHT(cadena, num_caracteres)`    | Devuelve los últimos N caracteres de una cadena.                             | `SELECT RIGHT('Hola Mundo', 5)` → `'Mundo'`                          |
| `LEFT(cadena, num_caracteres)`     | Devuelve los primeros N caracteres de una cadena.                           | `SELECT LEFT('Hola Mundo', 4)` → `'Hola'`                            |
| `CHARINDEX(subcadena, cadena)`     | Devuelve la posición de la primera aparición de una subcadena.              | `SELECT CHARINDEX('Mundo', 'Hola Mundo')` → `6`                      |
| `REVERSE(cadena)`                  | Devuelve la cadena en orden inverso.                                          | `SELECT REVERSE('Hola Mundo')` → `'odnuM aloH'`                      |
| `ASCII(cadena)`                    | Devuelve el código ASCII del primer carácter de la cadena.                   | `SELECT ASCII('A')` → `65`                                           |
| `CHAR(codigo)`                     | Devuelve el carácter correspondiente al código ASCII proporcionado.          | `SELECT CHAR(65)` → `'A'`                                            |
| `SPACE(num_caracteres)`            | Devuelve una cadena con el número especificado de espacios en blanco.        | `SELECT SPACE(5)` → `'     '`                                        |
