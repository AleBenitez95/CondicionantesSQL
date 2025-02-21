## 🔹 Funciones de Redondeo en SQL

| Función                     | Descripción                                                           | Ejemplo de uso                                         |
|-----------------------------|-----------------------------------------------------------------------|-------------------------------------------------------|
| `TRUNCATE(número, decimales)`| Elimina la parte decimal sin redondear, simplemente corta la cadena decimal. | `SELECT TRUNCATE(123.4567, 2);` → `123.45`            |
| `ROUND(número, decimales)`   | Redondea un número al número de decimales que especifiques.           | `SELECT ROUND(123.4567, 2);` → `123.46`               |
| `CEIL(número)` / `CEILING(número)` | Redondea hacia arriba al siguiente número entero.                     | `SELECT CEIL(123.4567);` → `124`                      |
| `FLOOR(número)`              | Redondea hacia abajo al número entero más cercano.                    | `SELECT FLOOR(123.4567);` → `123`                     |
| `SIGN(número)`               | Devuelve el signo del número: 1 si es positivo, -1 si es negativo, 0 si es cero. | `SELECT SIGN(-56);` → `-1`                            |


