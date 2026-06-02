# 📊 Proyecto de Business Intelligence con Power BI

## Análisis Estratégico del Mercado Airbnb

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi\&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-ETL-purple)
![DAX](https://img.shields.io/badge/DAX-Analytics-green)
![Data Modeling](https://img.shields.io/badge/Data-Modeling-blue)
![Business Intelligence](https://img.shields.io/badge/Business-Intelligence-orange)

---

# 📖 Descripción del Proyecto

Este proyecto consiste en el desarrollo de una solución de **Business Intelligence en Power BI** para analizar el comportamiento del mercado Airbnb en diferentes ciudades.

La solución abarca todo el ciclo analítico, desde la preparación y transformación de los datos mediante **Power Query**, pasando por el diseño de un modelo de datos optimizado para análisis multidimensional, hasta la creación de dashboards interactivos orientados a la toma de decisiones.

El objetivo principal es transformar grandes volúmenes de datos en información visual y comprensible que permita detectar tendencias, identificar oportunidades de negocio y generar insights accionables.

---

# 🎯 Objetivos del Proyecto

El proyecto fue desarrollado siguiendo cuatro objetivos fundamentales:

## 1. Carga y Transformación de Datos mediante Power Query

Preparar los datos para su explotación analítica mediante procesos de limpieza, normalización y transformación.

### Actividades realizadas

* Importación de datos.
* Conversión de tipos de datos.
* Eliminación de registros inconsistentes.
* Gestión de valores nulos.
* Normalización de categorías.
* Creación de columnas calculadas.
* Preparación de jerarquías geográficas.

---

## 2. Modelado de Datos para Análisis Multidimensional

Diseñar una estructura eficiente que permita realizar análisis desde diferentes perspectivas.

### Objetivos del modelado

* Mejorar el rendimiento del dashboard.
* Facilitar la navegación de la información.
* Crear relaciones lógicas entre entidades.
* Permitir análisis temporales, geográficos y económicos.

### Modelo implementado

```text
                    Dim_Fecha
                         |
                         |
                         v

Dim_Ciudad ---- Fact_Airbnb ---- Dim_Host
                         |
                         |
                         v

                  Dim_Ubicacion
```

### Dimensiones principales

#### Dimensión Temporal

Permite análisis por:

* Año
* Trimestre
* Mes
* Día

#### Dimensión Geográfica

Permite análisis por:

* Ciudad
* Distrito
* Barrio

#### Dimensión de Anfitriones

Permite segmentar:

* Particulares
* Profesionales
* Empresas

---

## 3. Desarrollo de Dashboards Interactivos en Power BI

Diseñar una experiencia visual intuitiva que facilite el análisis y la exploración de los datos.

### Principios de diseño aplicados

* Simplicidad visual.
* Jerarquía de información.
* Interactividad.
* Consistencia gráfica.
* Storytelling con datos.

### Funcionalidades implementadas

* Filtros dinámicos.
* Segmentadores interactivos.
* Drill Down.
* Navegación por jerarquías.
* Tooltips personalizados.

---

## 4. Obtención de Insights para la Toma de Decisiones

Convertir datos en conocimiento útil para usuarios de negocio.

### Áreas analizadas

#### Mercado

* Comparativa de precios entre ciudades.
* Distribución de la oferta.

#### Demanda

* Evolución temporal de reseñas.
* Actividad de los alojamientos.

#### Ocupación

* Disponibilidad anual.
* Niveles medios de ocupación.

#### Geografía

* Concentración territorial de alojamientos.
* Identificación de zonas estratégicas.

---

# 🏗️ Arquitectura de la Solución

El flujo de trabajo desarrollado sigue una arquitectura típica de Business Intelligence.

```text
Dataset Airbnb
        ↓
Power Query
        ↓
Limpieza y Transformación
        ↓
Modelo Relacional
        ↓
Medidas DAX
        ↓
Dashboard Power BI
        ↓
Insights de Negocio
```

---

# ⚙️ Fase 1: Preparación y Transformación de Datos

La fase inicial estuvo centrada en garantizar la calidad de los datos antes de su explotación analítica.

## Transformaciones realizadas

### Limpieza

* Eliminación de registros duplicados.
* Corrección de inconsistencias.
* Validación de campos obligatorios.

### Conversión de datos

* Fechas.
* Variables numéricas.
* Categorías.

### Estandarización

* Ciudades.
* Distritos.
* Tipos de alojamiento.

### Creación de atributos derivados

* Indicadores de ocupación.
* Segmentación de anfitriones.
* Clasificación territorial.

---

# 🏛️ Fase 2: Modelado de Datos

Una vez transformados los datos, se construyó un modelo optimizado para análisis multidimensional.

## Beneficios del modelo

### Rendimiento

Reduce tiempos de carga y cálculo.

### Escalabilidad

Permite incorporar nuevas fuentes de información.

### Flexibilidad Analítica

Facilita análisis desde múltiples perspectivas.

---

# 📊 Fase 3: Desarrollo del Dashboard

El dashboard está organizado en tres áreas de análisis.

---

# Página 1 — Visión Ejecutiva

## Objetivo

Ofrecer una visión general del mercado.

### KPIs

* Precio Medio.
* Disponibilidad Media.
* Total de Reseñas.
* Total de Alojamientos.

### Visualizaciones

* Tarjetas KPI.
* Gráficos temporales/Demanda
* Comparativas por ciudad.

---

# Página 2 — Oferta y Segmentación

## Objetivo

Analizar la estructura del mercado.

### Visualizaciones

#### Distribución de Anfitriones

Clasificación entre:

* Particulares.
* Profesionales.
* Empresas.

#### Tipología de Alojamientos

* Vivienda completa.
* Habitación privada.
* Habitación compartida.

#### Distribución Territorial

Treemap por:

* Ciudad.
* Distrito.
* Barrio.

---

# Página 3 — Análisis Geográfico y Correlacional

## Objetivo

Detectar patrones espaciales y relaciones entre variables.

### Mapa Interactivo

Representación geográfica de alojamientos mediante coordenadas.

### Análisis de Correlación

Relación entre:

* Precio.
* Número de reseñas.

Este análisis permite identificar:

* Alojamientos premium.
* Alojamientos de alta demanda.
* Posibles oportunidades de inversión.

---

# 📐 Medidas DAX Implementadas

## Precio Medio

```DAX
Precio Medio =
AVERAGE(all_cities_airbnb[price_eur])
```

Calcula el precio medio por alojamiento.

---

## Total Alojamientos

```DAX
Total Alojamientos =
COUNTROWS(all_cities_airbnb)
```

Calcula el número total de anuncios disponibles.

---

## Disponibilidad Media

```DAX
Disponibilidad Media =
AVERAGE(all_cities_airbnb[availability_365])
```

Mide la disponibilidad promedio de los alojamientos.

---

## Total Reseñas

```DAX
Total Reseñas =
SUM(all_cities_airbnb[number_of_reviews])
```

Indica el nivel de actividad y demanda.

---

# 📈 Insights Obtenidos

El análisis permitió identificar:

### Tendencias de Mercado

* Diferencias significativas de precios entre ciudades.
* Mercados con mayor potencial económico.

### Patrones de Demanda

* Zonas con mayor actividad turística.
* Alojamientos con mayor interacción de usuarios.

### Distribución Territorial

* Concentración de oferta en determinadas áreas urbanas.
* Identificación de zonas estratégicas para inversión.

### Segmentación Empresarial

* Diferencias entre particulares y operadores profesionales.
* Mercados altamente profesionalizados.

---

# 🛠️ Tecnologías Utilizadas

| Tecnología       | Función                  |
| ---------------- | ------------------------ |
| Power BI Desktop | Desarrollo del dashboard |
| Power Query      | Transformación de datos  |
| DAX              | Creación de métricas     |
| Excel            | Validación de resultados |
| GitHub           | Control de versiones     |

---

# 📁 Estructura del Repositorio

```text
Dashboard_Analytics_en_Power_BI_Grupo_4/
│
├── assets/
│   ├── lila_theme
│   ├── marron_theme
│
├── documents/
│   ├── Dashboard_PowerBI_Grupo4.pdf
│   ├── Informe_ejecutivo_airbnb.pdf
│
├── images/
│   ├── 1_KPIs-y-Analisis-Temporal_Demanda
│   ├── 2_Analisis-de-Oferta-y-Negocio
│   ├── 3_Mapas-y Analisis-Avanzados
│
├── proyecto_power_bi.pbix
│
├── .gitignore
├── LICENSE
└── README.md
```
---

# 🚀 Mejoras Futuras

* Predicción de precios mediante Machine Learning.
* Forecast de demanda turística.
* Automatización mediante Power BI Service.
* Integración de nuevas fuentes de datos.
* Actualización en tiempo real.

---

# 👨‍💻 Autores

## Manuel Macarro de la Osa
## Irene Condado Alcantarilla
## Ana Paula Montiel


Proyecto desarrollado para demostrar competencias en transformación de datos, modelado analítico y desarrollo de soluciones de Business Intelligence con Power BI orientadas a la toma de decisiones empresariales.
