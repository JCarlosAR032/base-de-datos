#### Tarea 5

![<image>]()

Tenemos una biblioteca que tiene como objetivo la gestión de la información de sus libros y lectores.

La representación de la información dentro de la BBDD es la siguiente:

**TABLA**

Se pide:

1. Comprobar si se cumple la 1ª Forma Normal.
2. Normalizar si no se cumple el apartado 2.
3. Comprobar si se cumple la 2ª Forma Normal.
4. Normalizar si no se cumple el apartado 4.
5. Comprobar si se cumple la 3ª Forma Normal.
6. Normalizar si no se cumple el apartado 5.
7. Indicar claves de todas las tablas resultantes.
8. Genera el diagrama E/R resultante.

#### EJERCICIO 5:

### 1. Comprobar si se cumple la 1ª Forma Normal.

No se cumple la primera forma porque hay atributos multievaluados.

### 2. Pasar a seguda forma si no se cumple la primera.

Lector

| Id_Lector PK | Nombre | Apellidos1 | Apellido2 |
|--------------|--------|------------|-----------|
| 1            | Juan   | Pérez      | Gómez     |
| 2            | Ana    | Ríos       | Terán     |
| 3            | René   | Roca       |           |
| 4            | Luis   | García     | Roque     |

Libro

| CodLibro PK | Id_Lector FK | Titulo            | Editorial    | FechaDev   |
|-------------|--------------|-------------------|--------------|------------|
| 1001        | 1            | Variable compleja | McGraw Hill  | 15/04/2022 |
| 1004        | 2            | Visual Basic 5    | Anaya        | 17/04/2022 |
| 1005        | 3            | Estadística       | McGraw Hill  | 16/04/2022 |
| 1006        | 4            | Oracle University | Oracle Corp. | 20/04/2022 |
| 1007        | 1            | Clipper 5.01      | McGraw Hill  | 18/04/2022 |

Libro_Autor

| CodLibro PK FK1 | Id_Autor PK FK2 |
|-----------------|-----------------|
| 1001            | 1               |
| 1004            | 2               |
| 1005            | 3               |
| 1006            | 4               |
| 1007            | 5               |

Autor

| Id_Autor PK | Nombre  | Apellido    |
|-------------|---------|-------------|
| 1           | Murray  | Spiegel     |
| 2           | E.      | Petroustsos |
| 3           | Nancy   | Greenberg   |
| 4           | Priya   | Nathan      |
| 5           | Ramalho |             |

### 3. Indicar claves de todas las tablas resultantes.

Lector

Libro

Libro_Autor

Autor
