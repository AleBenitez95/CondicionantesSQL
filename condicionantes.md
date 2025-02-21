## 🔹 Condiciones Lógicas y de Comparación  

| Operador       | Descripción                          | Ejemplo                 |
|---------------|----------------------------------|-------------------------|
| `=`          | Igual                            | `precio = 100`         |
| `<>` o `!=`  | Distinto de                      | `precio <> 100`        |
| `>`          | Mayor que                        | `precio > 100`         |
| `<`          | Menor que                        | `precio < 100`         |
| `>=`         | Mayor o igual que                | `precio >= 100`        |
| `<=`         | Menor o igual que                | `precio <= 100`        |
| `BETWEEN`    | Rango (incluye extremos)        | `precio BETWEEN 50 AND 150` |
| `IN (...)`   | Coincidencia en una lista       | `id_fabricante IN (1, 3, 5)` |
| `NOT IN (...)` | No está en la lista           | `id_fabricante NOT IN (1, 3, 5)` |
| `LIKE 'patrón'` | Búsqueda con comodines (%)   | `nombre LIKE 'Samsung%'` |
| `IS NULL`    | Es nulo                         | `descuento IS NULL`    |
| `IS NOT NULL` | No es nulo                     | `descuento IS NOT NULL` |

---

## 🔹 Operadores Lógicos  

| Operador | Descripción | Ejemplo |
|----------|------------|---------|
| `AND` | Ambas condiciones deben cumplirse | `precio > 100 AND id_fabricante = 2` |
| `OR` | Al menos una condición debe cumplirse | `precio < 50 OR id_fabricante = 4` |
| `NOT` | Niega la condición | `NOT precio > 500` |

---

## 🔹 Condiciones en Funciones de Agregación (HAVING)  

| Ejemplo | Descripción |
|---------|------------|
| `HAVING COUNT(*) > 5` | Filtra grupos con más de 5 elementos |
| `HAVING SUM(precio) > 1000` | Filtra grupos con suma mayor a 1000 |
| `HAVING AVG(precio) < 200` | Filtra grupos con promedio menor a 200 |

---

## 🔹 Condiciones en `CASE` (Expresiones Condicionales)  

| Cláusula | Descripción | Ejemplo |
|----------|------------|---------|
| `CASE` | Evalúa condiciones y devuelve valores personalizados |  
| `WHEN ... THEN` | Evalúa una condición | `WHEN precio < 100 THEN 'Barato'` |
| `ELSE` | Devuelve un valor por defecto si ninguna condición se cumple | `ELSE 'Caro'` |
| `END` | Finaliza la expresión `CASE` | `END AS "Categoría de Precio"` |

sql
SELECT nombre, precio,
    CASE 
        WHEN precio < 100 THEN 'Barato'
        WHEN precio BETWEEN 100 AND 500 THEN 'Moderado'
        ELSE 'Caro'
    END AS "Categoría de Precio"
FROM producto; ´



## 🔹 Condiciones en Restricciones de Integridad  

| Restricción     | Descripción                               | Ejemplo                                             |
|-----------------|-------------------------------------------|-----------------------------------------------------|
| `PRIMARY KEY`   | Identificador único                      | `id INT PRIMARY KEY`                               |
| `FOREIGN KEY`   | Clave foránea                             | `id_fabricante INT REFERENCES fabricante(id_fabricante)` |
| `UNIQUE`         | No permite valores duplicados             | `nombre VARCHAR(100) UNIQUE`                        |
| `CHECK`          | Valida condiciones en los datos           | `precio CHECK (precio > 0)`                         |
| `NOT NULL`       | No permite valores nulos                  | `nombre VARCHAR(100) NOT NULL`                      |

---

## 🔹 Condiciones en `JOIN` (Condiciones de Unión)  

| Tipo de `JOIN`  | Descripción                                         | Ejemplo                                                                 |
|-----------------|-----------------------------------------------------|-------------------------------------------------------------------------|
| `INNER JOIN`    | Coincidencias en ambas tablas                       | `SELECT * FROM producto p INNER JOIN fabricante f ON p.id_fabricante = f.id_fabricante` |
| `LEFT JOIN`     | Todos los registros de la primera tabla y coincidencias de la segunda | `SELECT * FROM producto p LEFT JOIN fabricante f ON p.id_fabricante = f.id_fabricante` |
| `RIGHT JOIN`    | Todos los registros de la segunda tabla y coincidencias de la primera | `SELECT * FROM producto p RIGHT JOIN fabricante f ON p.id_fabricante = f.id_fabricante` |
| `FULL JOIN`     | Todos los registros de ambas tablas                 | `SELECT * FROM producto p FULL JOIN fabricante f ON p.id_fabricante = f.id_fabricante` |

