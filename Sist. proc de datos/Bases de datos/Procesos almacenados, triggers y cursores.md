# Resumen sobre Datos Relacionales, Procedimientos Almacenados, Triggers y Cursores

## Datos Relacionales

**Definición:**
- Los **datos relacionales** se organizan en tablas con filas y columnas.
- **Ejemplo de creación de una tabla:**

```sql
CREATE TABLE Empleados (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    salario DECIMAL(10, 2)
);
```

## Procedimientos Almacenados

**Definición:**
- **Procedimientos almacenados** son bloques de código SQL almacenados en la base de datos.
- **Ejemplo de creación de un procedimiento almacenado:**

```sql
DELIMITER //
CREATE PROCEDURE ObtenerEmpleado(IN empleado_id INT)
BEGIN
    SELECT * FROM Empleados WHERE id = empleado_id;
END //
DELIMITER ;
```

## Triggers

**Definición:**
- **Triggers** son acciones automáticas desencadenadas por eventos en la base de datos.
- **Ejemplo de creación de un trigger:**

```sql
CREATE TRIGGER ActualizarSalario
BEFORE UPDATE ON Empleados
FOR EACH ROW
SET NEW.salario = NEW.salario * 1.1;
```

## Cursores

**Definición:**
- **Cursores** permiten procesar filas de resultados de una consulta de manera iterativa.
- **Ejemplo de uso de cursor:**

```sql
DECLARE empleado_id INT;
DECLARE empleado_nombre VARCHAR(50);

DECLARE empleados_cursor CURSOR FOR
    SELECT id, nombre FROM Empleados;

OPEN empleados_cursor;

FETCH empleados_cursor INTO empleado_id, empleado_nombre;

WHILE @@FETCH_STATUS = 0 DO
    -- Procesar datos
    PRINT CONCAT('ID: ', empleado_id, ', Nombre: ', empleado_nombre);
    
    FETCH empleados_cursor INTO empleado_id, empleado_nombre;
END WHILE;

CLOSE empleados_cursor;
```

Estos conceptos son fundamentales en el manejo de bases de datos relacionales, brindando estructura, automatización y control sobre las operaciones realizadas en la base de datos.
