# Estructura Física de la Base de Datos

## Estructura

Archivos de Datos: Contiene los datos de la bd, compuesto por páginas numeradas.

## Tipos de Páginas

- Páginas de Datos
- Páginas de espacio libre
- Páginas de mapa de ubicaciones de índice
- Páginas de indices

## Archivos de Registros

Recupera datos al completar una copia de respaldo. No contiene páginas sino entradas con datos.

## Data File

Archivos fisicos en los que se almacenan objetos que forman parte de un tablespace

Un tablespace puede estar formado por uno o varios datafiles

Se indica du nombre, su ubicación, tamaño y tablespace.
Indices también son objetos

### Caracteristicas

- No se puede controlar en que datafile se almacenan los datos de un tablespace

## Segments

- Segmentos de TABLE
- Segmentos de INDEX
- Segmentos de ROLLBACK
- Segmentos TEMPORALES

## Extends

Unidad lógica de almacenamiento que está formada por un número determinado de bloques de datos contiguos.
Se crea obligatoriamente una extensión en dicho segmento.
Al llamarlo se solicita una nueva al sistema.

## Data Block

Es el último eslabón dentro de la cadena de almacenamiento. Es la unidad más pequeña.

### Componentes

- Cabecera: Contiene información general sobre el bloque como el tipo de segmento al que pertenece
- Directorio de Tablas: Contiene información acerca de las tablas que tiene datos en el bloque
- Directorio de Filas: Contiene información sobre las filas que se encuentran en cada momento del bloque.
- Espacio Libre: Subzona está reservada para la inserción de nuevas filas en el bloque.
- Datos de Filas: Se almacenan los datos de las tablas po de los indices del bloque.
