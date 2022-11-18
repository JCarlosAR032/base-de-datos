# Tarea 2: Gestión Escuela de Topografía de Madrid

![<image>](https://www.topografia.upm.es/themes/comun/logos/ETSITopografia.png)

Se ha creado una base de datos para llevar las calificaciones de las asignaturas de los alumnos de primer curso de la Escuela de Topografía de Madrid. La tabla creada tiene los siguientes campos

- DNI varchar (20).
- Apellidos varchar (255).
- Nombre varchar (50).
- Direccion varchar (255).
- Ciudad varchar (50).
- Provincia varchar (50).
- Comunidad varchar (50).
- Codigo integer.
- Asignatura varchar(50).
- Nota double.

Además la información que se aporta es:

- DNI es un identificador único del alumno; lo mismo que {Apellidos, Nombre}.
- Ciudad es el nombre de la ciudad de residencia (único)
- Provincia es el nombre de la provincia de residencia (único)
- Com_Aut es el nombre de la Comunidad Autónoma de residencia (único)
- Codigo es el código de una asignatura (único). Asignatura es el nombre de la asignatura (único)
- Asignatura es el nombre de la asignatura (único)
- Nota es la nota que el alumno ha obtenido en la asignatura
- Codigo, Asignatura y Nota se escriben en el mismo orden en los campos correspondientes

Ejemplo de datos de la tabla:

![<image>](https://github.com/jpexposito/base-datos/blob/main/NORMALIZACION/tareas/tarea2/img/tabla.png)

Se pide:

1. Indicar claves candidatas.
2. Comprobar si se cumple la 1ª Forma Normal.
3. Normalizar si no se cumple el apartado 2.
4. Determinantes sobre las tablas resultado del apartado 3.
5. Indicar claves candidatas de todas las tablas resultantes.

### Ejercicio 2:

###### 1. Indicar claves candidatas:

- DNI
- codigo

###### 2. Comprobar si se cumple la 1ª Forma Normal:

No cumple la primera forma porque tiene valores multievaluados.

###### 3. Normalizar si no se cumple el apartado 2:

- Alumno

| DNI      | Apellidos   | Nombre | Dirección  | Ciudad | Provincia | Com_Aut            |
|----------|-------------|--------|------------|--------|-----------|--------------------|
| 6754567B | Ruiz García | Luis   | Mayor 23   | Madrid | Madrid    | Madrid             |
| 8976345K | Pérez Illán | Marta  | Alcalá 123 | Madrid | Madrid    | Madrid             |
| 5436725H | Juárez Lis  | Ana    | Bailén 45  | Bargas | Toledo    | Castilla La Mancha |

- Codigo_Asignatura_Nota

| código    | Asignatura      | Nota |
|-----------|-----------------|------|
| 125002112 | Base de Datos   | 8    |
| 125001106 | Informática     | 7    |
| 125001105 | Cartografía     | 6    |
| 125002112 | Base de Datos   | 9    |
| 125001104 | Geomática       | 6    |
| 125004208 | Geomorfología   | 5    |
| 125002110 | Topografía y G. | 8    |
| 125002112 | Base de Datos   | 9    |

###### 4. Determinantes sobre las tablas resultado del apartado 3:

- Se crean nuevas tablas segun los datos anteriores.

###### 5. Indicar claves candidatas de todas las tablas resultantes:

- Alumno
- Codigo_Asignatura_Nota
