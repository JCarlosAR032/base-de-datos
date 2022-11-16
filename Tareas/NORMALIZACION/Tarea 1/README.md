# Tarea 1


Se ha creado una base de datos con los datos de ciudades y sus aeropuertos. Los campos y los tipos de datos son los que se indican a continuación:
- Ciudad: Nombre de la ciudad (único).
- HabCiudad_M: número de habitantes de la ciudad en millones.
- País: País en el que se encuentra la ciudad.
- HabPais_M: Número de habitantes del país en millones.
- PerteneceUE: campo booleano. TRUE si el país Pertenece a la Unión Europea; FALSE, no pertenece a la Unión Europea.
- CodigoAeropuerto: único.
- NombreAeropuerto: único.
- Distancia_km: distancia del aeropuerto a la ciudad en km.
La representación de la información dentro de la BBDD es la siguiente:

| Ciudad  | HabCiudad_M | País | HabPaís_M | PerteneceUE | codAeropuerto | NombreAeropuerto | Distancia_km |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Madrid  | 3  | España | 45 | Verdadero | MAD | Barajas | 13 |
| Londres  | 13  | Francia | 66 | Verdadero | CDG ORG | Roissy De Gaulle Orly | 23 16|
| Londres  | 8,3  | Gran Bretaña | 60 | Falso | LHT LTN | Heathrow Luton | 28 48|
| Belgrado  | 1,3  | Serbia | 7,5 | Falso | BEG | Nikola Tesla | 12 |
| Viena  | 1,8  | Austria | 8,5 | Verdadero | VIE | Schwechat | 18 |

Se pide:

1. Indicar claves candidatas
2. Comprobar si se cumple la 1ª Forma Normal
3. Normalizar si no se cumple el apartado 2
4. Determinantes sobre las tablas resultado del apartado 3
5. Indicar claves candidatas de todas las tablas resultantes



#### Ejercicio 1:

###### 1. Indicar claves candidatas:

| Ciudad  | codAeropuerto |
| ------------- | ------------- |
| Madrid  | MAD  |
| París  | CDG ORY  |
| Londres  | LHT LTN  |
| Belgrado  | BEG  |
| Viena  | VIE  |

###### 2. Comprobar si se cumple la 1º Forma Normal

-----------------------------------


| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
