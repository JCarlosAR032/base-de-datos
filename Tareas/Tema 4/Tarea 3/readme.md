# Tarea 3: Gestión de INEM

![<image>]()

Tenemos una empresa publica donde los puestos de trabajo, están regulados por el estado, de modo que las condiciones salariales están determinadas por el puesto de trabajo, se ha creado el siguiente esquema relacional: (con el _número de la seguridad social NSS como clave primaria) La representación de la información dentro de la BBDD es la siguiente:

Empleados (NSS, Nombre, puesto, salario, emails)

![<image>](https://github.com/jpexposito/base-datos/blob/main/NORMALIZACION/tareas/tarea3/img/tabla.png)

Se pide:

1. Indicar claves candidatas.
2. Comprobar si se cumple la 1ª Forma Normal.
3. Normalizar si no se cumple el apartado 2.
4. Comprobar si se cumple la 2ª Forma Normal.
5. Normalizar si no se cumple el apartado 4.
6. Comprobar si se cumple la 3ª Forma Normal.
7. Normalizar si no se cumple el apartado 5.
8. Indicar claves candidatas de todas las tablas resultantes.
9. Genera el diagrama E/R resultante.

### Ejercicio 3:

1. Indicar claves candidatas.

- NSS
- Emails

2. Comprobar si se cumple la 1ª Forma Normal.

| NSS | Nombre | Puesto    | Salario | Emails          |
|-----|--------|-----------|---------|-----------------|
| 111 | Pepe   | Jefa Area | 3000    | josep@ecn.es    |
| 111 | Pepe   | Jefa Area | 3000    | jefez@gmail.com |
| 222 | Josu   | Admtivo   | 1500    | jsanchez@ecn.es |
| 333 | Miren  | Admtiva   | 1500    | mlopez@ecn.es   |
| 333 | Miren  | Admtiva   | 1500    | miren@gmail.com |

Empleado_Salario

| NSS | Nombre | Puesto    | Salario |
|-----|--------|-----------|---------|
| 111 | Pepe   | Jefa Area | 3000    |
| 111 | Pepe   | Jefa Area | 3000    |
| 222 | Josu   | Admtivo   | 1500    |
| 333 | Miren  | Admtiva   | 1500    |
| 333 | Miren  | Admtiva   | 1500    |

Empleado_Puesto

| NSS | Nombre | Puesto    |
|-----|--------|-----------|
| 111 | Pepe   | Jefa Area |
| 111 | Pepe   | Jefa Area |
| 222 | Josu   | Admtivo   |
| 333 | Miren  | Admtiva   |
| 333 | Miren  | Admtiva   |

Empleado_Email

| NSS | Emails          |
|-----|-----------------|
| 111 | josep@ecn.es    |
| 111 | jefez@gmail.com |
| 222 | jsanchez@ecn.es |
| 333 | mlopez@ecn.es   |
| 333 | miren@gmail.com |

8. Indicar claves candidatas de todas las tablas resultantes.

- Empleado_Salario
- Empleado_Puesto
- Empleado_Email




