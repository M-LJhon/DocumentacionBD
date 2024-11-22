# 1. Introducción a las Bases de Datos
## 1.1. ¿Qué es una base de datos?
Una base de datos es una estructura digital que utiliza modelos estructurados para organizar los datos. En una base de datos podemos leer, editar y almacenar datos.

![Bases de datos](img/DBI-1.jpg)

## 1.2. Significado de las siglas RDBMS y DBMS.
DBMS significa "Database Management System" (Sistema de Gestión de Bases de Datos), el cual es un software diseñado para gestionar bases de datos relacionales y no relacionales, además de eso nos permite gestionar, almacenar y recuperar datos.

Por otro lado RDBMS significa "Relational Database Management System" (Sistema de Gestión de Bases de Datos Relacionales), es un tipo específico de DBMS que maneja bases de datos relacionales a través del uso de tablas con columnas y filas o tuplas. Entre algunos ejemplos nos encontramos con MySQL, PostgreSQL, Oracle, entre otros.

![RDBMS Y DBMS](/img/DBMS-FEAT.webp)

# 2. Propósito y Aplicaciones de las Bases de Datos
## 2.1. Propósito de una base de datos.
El propósito principal de una base de datos es almacenar, organizar, gestionar y recuperar datos de manera eficiente y estructurada.
## 2.2. ¿Dónde se aplican las bases de datos?
Las bases de datos se aplican en prácticamente todos los sectores y áreas donde se requiera manejar información estructurada para tomar decisiones.

# 3. Tipos de Bases de Datos
## 3.1. Clasificación según estructura (relacionales, no relacionales, jerárquicas, etc.).
Ahora hablaremos de los Tipos de Bases de Datos, Clasificándolas Según Su Estructura, la que define cómo se organiza, almacena y accede a la información.

![TIPOS DE BASES DE DATOS](/img/Types-of-databases.jpg)

- **Bases de Datos Relacionales**: Utilizan tablas para organizar los datos. Cada tabla contiene filas o registros y columnas o también llamadas atributos, y las relaciones entre tablas se definen mediante claves primarias y foráneas.
- **Bases de Datos No Relacionales**: Diseñadas para manejar datos no estructurados o semiestructurados. No utilizan un esquema fijo de tablas, sino estructuras más flexibles como documentos, grafos o pares clave-valor.
- **Bases de Datos Jerárquicas**:  Estructuran los datos en forma de árbol, donde cada nodo tiene un único padre, pero puede tener múltiples hijos.
- **Bases de Datos en Red**: Extienden el modelo jerárquico permitiendo que un nodo tenga múltiples padres. Los datos se representan como grafos.
- **Bases de Datos Orientadas a Objetos**: Los datos se almacenan como objetos, similares a los usados en la programación orientada a objetos.

## 3.2 Clasificación según ubicación o acceso (locales, distribuidas, en la nube).
- **Bases de Datos Locales**: Se encuentran alojadas en un único servidor o equipo que no está conectado directamente a una red externa.
- **Bases de Datos Distribuidas**: Los datos se almacenan en varios nodos (servidores o dispositivos) conectados por una red. Cada nodo puede manejar una parte de la base de datos.
- **Bases de Datos en la Nube**: Se alojan en servidores remotos administrados por proveedores de servicios en la nube. Los usuarios acceden a ellas a través de internet.
# 4. Conceptos Fundamentales
## Abstracción de los datos:
- Representación conceptual de los datos que no incluye muchos detalles 
de cómo se almacenan.
 - Modelo de datos: tipo de abstracción de los datos con que se obtiene 
una representación conceptual.
 - Se oculta los detalles de almacenamiento e implementación.
## Las anomalías en SQL:
Son inconsistencias o irregularidades que ocurren 
en una base de datos y que afectan su funcionamiento normal y la integridad 
de los datos. Suelen ser consecuencia de un diseño deficiente de la base de 
datos y pueden causar problemas 
importantes, como pérdida de datos, redundancia de datos y datos incorrectos.
# 5. Lenguaje de los Datos
## LDD (Lenguaje de Definición de Datos)
1. **Propósito**:
- Define la estructura de la base de datos
- Crea, modifica y elimina objetos de la base de datos
- Establece restricciones y relaciones

2. **Principales comandos**:
- CREATE: Para crear objetos (bases de datos, tablas, índices).
- ALTER: Para modificar objetos existentes.
- DROP: Para eliminar objetos.
- TRUNCATE: Para vaciar el contenido de una tabla.

3. **Operaciones comunes**:
- Definición de tablas y sus columnas.
- Establecimiento de claves primarias y foráneas.
- Creación de índices para optimizar búsquedas.
- Definición de restricciones (CONSTRAINTS).

4. **Aspectos importantes**:
- Los cambios son permanentes.
- Afectan a la estructura, no a los datos.
- Requieren permisos especiales de administración.
- Son críticos para el rendimiento y la integridad de los datos.

## LMD
El LMD (o DML en inglés - Data Manipulation Language) 
es el lenguaje que se utiliza para manipular los datos dentro 
de una base de datos. Sus características principales son:

**Principales comandos**:

- SELECT: Para consultar datos.

- INSERT: Para insertar nuevos registros.

- UPDATE: Para modificar registros existentes.

- DELETE: Para eliminar registros.

**Características importantes**:

Afecta al contenido de las tablas, no a su estructura
Las operaciones pueden ser revertidas (rollback) si se usan dentro de una transacción.
Son las operaciones más frecuentes en una base de datos.


**Operaciones comunes**:

*Consultas simples y complejas*:

- Filtrado de datos (WHERE)

- Ordenamiento (ORDER BY)

- Agrupamiento (GROUP BY)

- Joins entre tablas.

- Subconsultas.

**Aspectos a considerar:**

Rendimiento de las consultas
Integridad de los datos
Concurrencia de usuarios
Transaccionalidad.


# 6. Modelo de los Datos
## 6.1. Modelo Entidad-Relación (MER/DER):
El Modelo Entidad-Relación es una herramienta de modelado que permite representar las entidades relevantes de un sistema de información así como sus interrelaciones y propiedades.

- **Entidades**: Son objetos o conceptos del mundo real que son distinguibles entre sí. Se representan como rectángulos.
- **Atributos**: Son las características o propiedades de las entidades. Pueden ser:
    - Simples o compuestos.
    -  Monovaluados o multivaluados.
    - Derivados.
- **Relaciones**: Representan asociaciones entre entidades.
Se indican con líneas que conectan las entidades
Tienen cardinalidad que indica cuántas instancias de una entidad se relacionan con otra.

**Tipos de cardinalidad**:
- Uno a uno (1:1).
- Uno a muchos (1:N).
- Muchos a muchos (N:M).

## 6.2. Notación gráfica (herramientas geométricas):
![NOTACIONES GEOMETRICAS](/img/erd-chart.jpg "Notación gráfica y Cardinalidades")

## 6.3. Llaves o claves en las bases de datos:

![TIPOS DE LLAVES EN BD](/img/firefox_ZjVMRg9gkt.png)

# 7. Normalización de Bases de Datos
## 7.1. Definición de normalización.
La normalización es un proceso sistemático para organizar y estructurar las bases de datos relacionales, eliminando redundancias y dependencias problemáticas.
## 7.2. Objetivos de la normalización.
Eliminar redundancias y dependencias problemáticas de una base de datos.
## 7.3. Formas normales.
- **1FN**: 
    - Eliminar grupos repetitivos.
    - Cada atributo debe ser atómico (no divisible).
    - Cada columna debe tener un nombre único.
- **2FN**: La Segunda Forma Normal (2FN) se basa en el concepto de dependencia funcional completa, es decir, todos los atributos no clave deben depender de TODA la clave primaria.




