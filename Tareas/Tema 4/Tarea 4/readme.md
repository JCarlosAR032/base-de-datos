# Tarea 4

![<image>](https://th.bing.com/th/id/OIP.YZHVWoI6VFwNa3FBhBBHogHaEK?pid=ImgDet&rs=1)

Se desea crear una base de datos para una pequeña empresa debe contener información acerca de clientes, artículos y pedidos. Hasta el momento se registran los siguientes datos en documentos varios:

- Para cada cliente: Número de cliente (único), Direcciones de envío (varias por cliente), Saldo, Límite de crédito (depende del cliente, pero en ningún caso debe superar los 3.000.000 €), Descuento.

- Para cada artículo: Número de artículo (único), Fábricas que lo distribuyen, Existencias de ese artículo en cada fábrica, Descripción del artículo.

- Para cada pedido: Cada pedido tiene una cabecera y el cuerpo del pedido. La cabecera está formada por el número de cliente, dirección de envío y fecha del pedido. El cuerpo del pedido son varias líneas, en cada línea se especifican el número del artículo pedido y la cantidad.

- Además, se ha determinado que se debe almacenar la información de las fábricas. Sin embargo, dado el uso de distribuidores, se usará: Número de la fábrica (único) y Teléfono de contacto. Y se desean ver cuántos artículos (en total) provee la fábrica. También, por información estratégica, se podría incluir información de fábricas alternativas respecto de las que ya fabrican artículos para esta empresa.

### 1.- Comprobar si se cumple la 1º Forma Normal:

No se cumple la primera forma porque tiene atributos multievaluados.

### 2.- Pasar a 1º Forma:

Cliente

| Número PK | Límite | Saldo |
|-----------|--------|-------|
| 1         | 1000   | 5000  |
| 2         | 2200   | 10000 |
| 3         | 500    | 6000  |

Dirección

| Calle PK | Número_Cliente FK | Número | Ciudad     | Comunidad |
|----------|-------------------|--------|------------|-----------|
| Pilar    | 1                 | 10     | Tacoronte  | Canarias  |
| Rábano   | 1                 | 6      | Getafe     | Madrid    |
| Ramar    | 2                 | 13     | La Orotava | Canarias  |
| Trucha   | 3                 | 44     | Granadilla | Canarias  |
| Almar    | 3                 | 18     | Leganés    | Madrid    |

### Comprobar si se cumple la 2º Forma Normal:

Si esta en 2º Forma.

### Comprobar si se cumple la 3º Forma Normal:

Cliente

| Número PK | Límite | Saldo | Nombre_Calle FK |
|-----------|--------|-------|-----------------|
| 1         | 1000   | 5000  | Pilar           |
| 1         | 1000   | 5000  | Rábano          |
| 2         | 2200   | 10000 | Ramar           |
| 3         | 500    | 6000  | Trucha          |
| 3         | 500    | 6000  | Almar           |

Calle

| Nombre PK | Nombre_Ciudad FK | Número |
|-----------|------------------|--------|
| Pilar     | Tacoronte        | 10     |
| Rábano    | Getafe           | 6      |
| Ramar     | La Orotava       | 13     |
| Trucha    | Granadilla       | 44     |
| Almar     | Leganés          | 18     |

Ciudad

| Nombre PK  | Nombre_Cominidad FK |
|------------|---------------------|
| Tacoronte  | Canarias            |
| Getafe     | Madrid              |
| La Orotava | Canarias            |
| Granadilla | Canarias            |
| Leganés    | Madrid              |

Comunidad

| Nombre PK  | Nombre_Cominidad FK |
|------------|---------------------|
| Tacoronte  | Canarias            |
| Getafe     | Madrid              |
| La Orotava | Canarias            |
| Granadilla | Canarias            |
| Leganés    | Madrid              |

Pedido

| Número PK | Nombre_Calle FK |
|-----------|-----------------|
| 100       | Pilar           |
| 101       | Rábano          |
| 102       | Ramar           |
| 103       | Trucha          |
| 104       | Almar           |

### Indicar claves candidatas de todas las tablas resultantes

Cliente
Calle
Ciudad
Comunidad
Pedido
