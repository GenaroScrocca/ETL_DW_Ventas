# ETL Data Warehouse – Análisis de Ventas

Proyecto de **Data Engineering end-to-end** que construye un **Data Warehouse de ventas** utilizando un pipeline ETL y un modelo dimensional diseñado para análisis de negocio.

El proyecto extrae datos transaccionales de ventas, los transforma mediante procesos ETL, los carga en un **Data Warehouse con esquema estrella**, y finalmente permite analizarlos mediante dashboards en Power BI.

---

# Descripción del proyecto

Este proyecto simula un flujo de trabajo típico de **ingeniería de datos**:

1. Extracción de datos de ventas desde tablas fuente
2. Transformación y limpieza de datos mediante procesos ETL
3. Carga de los datos en un **Data Warehouse**
4. Modelado mediante **Star Schema**
5. Análisis y visualización en Power BI

El objetivo es permitir el análisis de desempeño de ventas mediante **KPIs, tendencias y segmentaciones**.

---

# Arquitectura

Datos fuente → ETL (SSIS) → Data Warehouse (SQL Server) → Dashboard (Power BI)

Componentes principales:

* SQL Server
* SSIS (SQL Server Integration Services)
* Modelado de Data Warehouse
* Dashboards en Power BI

---

# Diseño del Data Warehouse

El Data Warehouse fue modelado utilizando un **esquema estrella (Star Schema)**.

En este tipo de modelo:

* Una **tabla de hechos (Fact Table)** almacena eventos medibles, como ventas.
* Varias **tablas de dimensiones (Dimension Tables)** contienen información descriptiva para análisis.

### Tablas de hechos

Contienen los eventos principales del negocio, como:

* Transacciones de ventas
* Métricas agregadas de ventas

### Tablas de dimensiones

Las dimensiones permiten analizar la información desde distintos puntos de vista:

* Producto
* Fecha
* Cliente
* Región
* Canal de venta

Este modelo permite responder preguntas como:

* Ventas por producto
* Ventas por región
* Tendencias mensuales de ingresos
* Rendimiento por segmento

---

# Pipeline ETL

El pipeline ETL fue implementado utilizando **SSIS** e incluye:

* Data Flow Tasks
* Lookup Transformation
* Merge / Merge Join
* Derived Column
* Conditional Split

Estos procesos se encargan de:

* Limpieza de datos
* Transformación de datos
* Carga de dimensiones
* Carga de tablas de hechos

---

# Capa de Business Intelligence

El Data Warehouse alimenta un **dashboard de Power BI** donde se analizan los datos mediante:

* KPIs de ventas
* Gráficos de tendencias
* Segmentación por producto y región
* Medidas creadas con DAX

Los dashboards se actualizan automáticamente cuando el pipeline ETL procesa nuevos datos.

---

# Tecnologías utilizadas

* SQL Server
* SSIS
* Power BI
* SQL
* Data Warehousing
* Modelado dimensional

---

# Conceptos de ingeniería de datos aplicados

Este proyecto demuestra la implementación práctica de:

* Pipelines ETL
* Modelado dimensional
* Diseño Star Schema
* Tablas de hechos y dimensiones
* Transformación de datos
* Integración con herramientas de Business Intelligence

---

# Autor

**Genaro Scrocca**

Estudiante de Ingeniería Informática.

Intereses principales:

* Data Engineering
* Cloud y plataformas de datos
* Data Warehousing
* Analítica de datos
