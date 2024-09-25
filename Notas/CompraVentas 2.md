### 1. Crear una consulta que muestre: RFC, nombre completo del cliente (en una sola columna), número de ventas registradas por cliente y monto en ventas registradas por cliente. Se deben mostrar a todos los clientes registrados, hayan o no registrado ventas.

```sql
SELECT
    c.RFC,
    -- Concatenamos el nombre, apellido paterno y apellido materno para formar el nombre completo del cliente
    CONCAT(c.Nombre, ' ', c.ApePaterno, ' ', c.ApeMaterno) AS NombreCompleto,

    -- Contamos el número de ventas registradas para cada cliente
    COUNT(v.NumV) AS NumeroVentas,

    -- Sumamos el monto total de las ventas registradas por cada cliente. Si no hay ventas, se muestra 0 gracias a COALESCE
    COALESCE(SUM(v.Total), 0) AS MontoVentas

FROM
    Clientes c  -- Usamos la tabla Clientes como tabla principal

    -- Hacemos una unión izquierda con la tabla Ventas para asegurarnos de que todos los clientes, incluso los que no tienen ventas, aparezcan en el resultado
    LEFT JOIN Ventas v ON c.RFC = v.Clientes_RFC

-- Agrupamos por RFC y los campos que forman el nombre completo del cliente
GROUP BY
    c.RFC,
    c.Nombre,
    c.ApePaterno,
    c.ApeMaterno;
```

![[Pasted image 20240915191121.png]]
### 2. Crear una vista con la consulta anterior que se llame: “V_ventasXcliente”.
```sql
-- Creación de la vista V_ventasXcliente
CREATE VIEW V_ventasXcliente AS
SELECT 
    c.RFC, 
    -- Concatenamos el nombre, apellido paterno y apellido materno para formar el nombre completo del cliente
    CONCAT(c.Nombre, ' ', c.ApePaterno, ' ', c.ApeMaterno) AS NombreCompleto,
    
    -- Contamos el número de ventas registradas para cada cliente
    COUNT(v.NumV) AS NumeroVentas,
    
    -- Sumamos el monto total de las ventas registradas por cada cliente. Si no hay ventas, se muestra 0 gracias a COALESCE
    COALESCE(SUM(v.Total), 0) AS MontoVentas
    
FROM 
    Clientes c  -- Usamos la tabla Clientes como tabla principal
    
    -- Hacemos una unión izquierda con la tabla Ventas para asegurarnos de que todos los clientes, incluso los que no tienen ventas, aparezcan en el resultado
    LEFT JOIN Ventas v ON c.RFC = v.Clientes_RFC
    
-- Agrupamos por RFC y los campos que forman el nombre completo del cliente
GROUP BY 
    c.RFC, 
    c.Nombre, 
    c.ApePaterno, 
    c.ApeMaterno;


SELECT * FROM V_ventasXcliente;
```

### 3. Con la vista anterior crear una consulta que muestre todos los campos y un campo de puntos acumulados (cada punto se calcula considerando el monto de ventas por cliente entre 100).
```sql
SELECT 
    RFC, 
    NombreCompleto, 
    NumeroVentas, 
    MontoVentas,
    
    -- Calculamos los puntos acumulados dividiendo el monto de ventas entre 100
    MontoVentas / 100 AS PuntosAcumulados
    
FROM 
    V_ventasXcliente;
```
![[Pasted image 20240915191729.png]]

### 4. Crear una consulta que muestre: el código de producto, descripción corta, precio unitario y cantidad total de productos comprados a la fecha. Ordenar de manera descendente según sus compras, es decir primero se mostrará el producto más comprado.
```sql
SELECT 
    p.CodProd AS CodigoProducto, 
    p.DescripC AS DescripcionCorta, 
    p.PrecioV AS PrecioUnitario,
    
    -- Sumamos la cantidad total de productos comprados
    COALESCE(SUM(pc.Cantidad), 0) AS CantidadTotalComprada
    
FROM 
    Productos p
    
    -- Realizamos un LEFT JOIN para incluir todos los productos, incluso los que no han sido comprados
    LEFT JOIN ProductosCompras pc ON p.CodProd = pc.Productos_CodProd
    
-- Agrupamos por el código de producto, descripción y precio
GROUP BY 
    p.CodProd, 
    p.DescripC, 
    p.PrecioV
    
-- Ordenamos de manera descendente por la cantidad total de productos comprados
ORDER BY 
    CantidadTotalComprada DESC;
```
![[Pasted image 20240915192248.png]]

### 5. Crear una consulta que muestre, de los clientes, la colonia y el número de clientes que existen registrados por colonia.

```sql
SELECT Colonia, COUNT(*) AS NumeroClientes
FROM Clientes
GROUP BY Colonia;
```

![[Pasted image 20240917200046.png]]

### 6.  Crear la tabla de Marcas, estará relacionada con Productos, donde un producto pertenece a una marca, pero una marca puede tener diferentes productos.

```sql
-- Crear la tabla Marcas
CREATE TABLE Marcas (
  IdMarca VARCHAR(5) NOT NULL, -- Identificador de la marca
  Descripcion VARCHAR(45) NOT NULL, -- Nombre o descripción de la marca
  Vigente TINYINT(1) DEFAULT 1, -- Indica si la marca está vigente (1 = sí, 0 = no)
  PRIMARY KEY (IdMarca) -- Llave primaria
);

-- Alterar la tabla Productos para relacionarla con Marcas
ALTER TABLE Productos
ADD COLUMN IdMarca VARCHAR(5) NULL, -- Agregar columna para la marca
ADD CONSTRAINT FK_Productos_Marcas FOREIGN KEY (IdMarca) REFERENCES Marcas(IdMarca); -- Relación de llave foránea

```

### 7. La tabla de marcas deberá tener la siguiente información:
  ```sql
-- Insertar los registros en la tabla Marcas
INSERT INTO Marcas (IdMarca, Descripcion, Vigente) VALUES 
('Ps1', 'Quaker', 1),
('Ps2', 'Mafer', 1),
('Ps3', 'Ruffles', 1),
('Ps4', 'Sabritas', 1),
('Ps5', 'Marias', 1),
('Ps6', 'Emperador', 1),
('Ps7', 'Pepsi', 1),
('Fs1', 'CocaCola', 1),
('Fs2', 'DelValle', 1),
('Fs3', 'Fanta', 1);


```
#### Ejercicio 1: Insertar el siguiente registro
```sql
-- Insertar el nuevo registro en la tabla Proveedores
INSERT INTO Proveedores (RFC, NomEmpresa, NombreRepresentante, ApeP_Representante, TelContacto, DiaPedido, DiaEntrega, TipoPago)
VALUES ('TEP961122', 'Cooperativa Pascual', 'Jorge', 'Juarez', 5566771111, 'Lunes', 'Lunes', 'Transferencia');

```
#### Ejercicio 2: Agregar columnas adicionales a la tabla Proveedores (ya resuelto previamente en el ejercicio 7).

```sql
-- Ya se ha ejecutado este comando en el ejercicio 7
ALTER TABLE Proveedores
ADD COLUMN Calle VARCHAR(20) NULL,
ADD COLUMN Num INT NULL,
ADD COLUMN CP INT NULL,
ADD COLUMN Colonia VARCHAR(20) NULL,
ADD COLUMN Alcaldia VARCHAR(20) NULL,
ADD COLUMN Estado VARCHAR(20) NULL;
```
#### Ejercicio 3: Completar los datos de los proveedores según la información proporcionada.
```sql
-- Actualizar los datos de los proveedores
UPDATE Proveedores
SET Calle = 'Recreo', Num = 156, CP = 08620, Colonia = 'Barrio de los Reyes', Alcaldia = 'Iztacalco', Estado = 'CDMX'
WHERE RFC = 'TEP961122';

UPDATE Proveedores
SET Calle = 'Ignacio Zaragoza', Num = 885, CP = 08500, Colonia = 'Agricola Oriental', Alcaldia = 'Iztacalco', Estado = 'CDMX'
WHERE RFC = 'CCF911030';

UPDATE Proveedores
SET Calle = 'Porfirio Díaz', Num = 16, CP = 57460, Colonia = 'Juarez', Alcaldia = 'Pantitlan', Estado = 'Edo. México'
WHERE RFC = 'CPC650101';

```
#### Ejercicio 4: Insertar productos en la tabla Productos.
```sql
-- Insertar los nuevos productos en la tabla Productos
INSERT INTO Productos (CodProd, DescripL, DescripC, PrecioV, Existencias, StockMin, StockMax, Oferta)
VALUES 
(21, 'Boing de 250 ml sabor manzana', 'Boing ¼ Manzana', 10, 0, 0, 150, 0),
(22, 'Boing de 250 ml sabor mango', 'Boing ¼ Mango', 10, 0, 0, 150, 0);

```
#### Ejercicio 5: Insertar la compra en la tabla **Compras** y **Productos Compras**.
Insertar la compra:

```sql
-- Insertar la compra en la tabla Compras
INSERT INTO Compras (NumC, FechaHoraP, FechaHoraE, TipoPago, Subtotal, IVA, Total, Proveedores_RFC)
VALUES (990088, SYSDATE(), SYSDATE(), 'Efectivo', 1000, 160, 1160, NULL);
```

Insertar productos:
```sql
-- Insertar los productos de la compra en la tabla ProductosCompras
INSERT INTO ProductosCompras (Compras_NumC, Productos_CodProd, Cantidad, PrecioC, Subtotal)
VALUES 
(990088, 21, 100, 5, 500),
(990088, 22, 100, 5, 500);
```

#### Ejercicio 6: Crear una consulta que muestre por **alcaldía** el número de proveedores registrados.

```sql
-- Mostrar por alcaldía el número de proveedores registrados
SELECT Alcaldia, COUNT(*) AS NumeroProveedores
FROM Proveedores
GROUP BY Alcaldia;
```
![[Pasted image 20240917202152.png]]
#### Ejercicio 7: Crear una consulta que muestre el valor constante "Sin alcaldía registrada" y el número de proveedores que no tienen alcaldía registrada.

```sql
-- Mostrar proveedores sin alcaldía registrada
SELECT 'Sin alcaldía registrada' AS Alcaldia, COUNT(*) AS NumeroProveedores
FROM Proveedores
WHERE Alcaldia IS NULL;
```

![[Pasted image 20240917202224.png]]

#### Ejercicio 8: Crear una consulta que utilice las dos consultas anteriores y el comando `UNION`.

```sql
-- Unión de proveedores por alcaldía y sin alcaldía registrada
SELECT Alcaldia, COUNT(*) AS NumeroProveedores
FROM Proveedores
WHERE Alcaldia IS NOT NULL
GROUP BY Alcaldia
UNION
SELECT 'Sin alcaldía registrada' AS Alcaldia, COUNT(*) AS NumeroProveedores
FROM Proveedores
WHERE Alcaldia IS NULL;
```
![[Pasted image 20240917202253.png]]
#### Ejercicio 9: Crear una consulta que muestre el nombre de la empresa, el nombre del representante (en una sola columna), y el monto total registrado en compras a cada proveedor.

```sql
-- Mostrar el nombre de la empresa, representante y monto total de compras por proveedor
SELECT p.NomEmpresa, 
       CONCAT(p.NombreRepresentante, ' ', p.ApeP_Representante) AS NombreRepresentante, 
       COALESCE(SUM(c.Total), 0) AS MontoTotalCompras
FROM Proveedores p
LEFT JOIN Compras c ON p.RFC = c.Proveedores_RFC
GROUP BY p.NomEmpresa, p.NombreRepresentante, p.ApeP_Representante;
```

![[Pasted image 20240917202342.png]]

### Ejercicio 10: Crear una consulta que muestre los valores constantes "Sin empresa", "Sin representante" y el monto total en compras registradas sin proveedor.

```sql
-- Mostrar los registros de compras sin proveedor
SELECT 'Sin empresa' AS NomEmpresa, 'Sin representante' AS NombreRepresentante, 
       COALESCE(SUM(c.Total), 0) AS MontoTotalCompras
FROM Compras c
WHERE c.Proveedores_RFC IS NULL;
```


![[Pasted image 20240917202405.png]]