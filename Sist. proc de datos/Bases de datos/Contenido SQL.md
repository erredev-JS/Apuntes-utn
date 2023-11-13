# Resumen sobre Bases de Datos y Subconsultas

## Bases de Datos Relacionales

**Definición:**
- Las **bases de datos relacionales** organizan datos en tablas con filas y columnas.
- **Ejemplo de creación de una tabla:**

```sql
CREATE TABLE Empleados (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    salario DECIMAL(10, 2)
);
```

## Consultas Básicas

**SELECT Statement:**
- **SELECT** se utiliza para recuperar datos de una tabla.
- **Ejemplo de consulta simple:**

```sql
SELECT * FROM Empleados;
```

**WHERE Clause:**
- **WHERE** filtra resultados basados en una condición.
- **Ejemplo de consulta con condición:**

```sql
SELECT * FROM Empleados WHERE salario > 50000;
```

**ORDER BY Clause:**
- **ORDER BY** ordena los resultados.
- **Ejemplo de consulta ordenada:**

```sql
SELECT * FROM Empleados ORDER BY salario DESC;
```

## Operaciones de Modificación

**INSERT Statement:**
- **INSERT INTO** se utiliza para agregar filas a una tabla.
- **Ejemplo de inserción de datos:**

```sql
INSERT INTO Empleados (id, nombre, salario) VALUES (1, 'Juan', 60000);
```

**UPDATE Statement:**
- **UPDATE** modifica datos existentes en una tabla.
- **Ejemplo de actualización de datos:**

```sql
UPDATE Empleados SET salario = 65000 WHERE id = 1;
```

**DELETE Statement:**
- **DELETE FROM** elimina filas de una tabla.
- **Ejemplo de eliminación de datos:**

```sql
DELETE FROM Empleados WHERE id = 1;
```

## Funciones Agregadas

**SUM, AVG, COUNT, MAX, MIN:**
- **SUM, AVG, COUNT, MAX, MIN** son funciones agregadas para realizar cálculos en columnas.
- **Ejemplo de uso de funciones agregadas:**

```sql
SELECT AVG(salario) FROM Empleados;
```

## Joins

**Definición:**
- **Joins** combinan filas de dos o más tablas basándose en una condición.
- **Ejemplo de consulta con INNER JOIN:**

```sql
SELECT Empleados.id, Empleados.nombre, Departamentos.nombre AS departamento
FROM Empleados
INNER JOIN Departamentos ON Empleados.departamento_id = Departamentos.id;
```

## Subconsultas

**Definición:**
- **Subconsultas** son consultas anidadas dentro de otras consultas.
- **Ejemplo de subconsulta en la cláusula WHERE:**

```sql
SELECT nombre FROM Empleados
WHERE departamento_id IN (SELECT id FROM Departamentos WHERE nombre = 'Ventas');
```

**Ejemplo de subconsulta en la cláusula FROM:**

```sql
SELECT nombre, (SELECT COUNT(*) FROM Empleados WHERE departamento_id = Departamentos.id) AS num_empleados
FROM Departamentos;
```

Estos conceptos básicos proporcionan una comprensión sólida de cómo interactuar con bases de datos relacionales, desde la creación de tablas hasta la realización de consultas avanzadas con subconsultas.
