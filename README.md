# 📊 Dashboard de Desempeño Comercial — Andes Retail Group (2024–2025)

Proyecto de análisis de datos y visualización construido en **Tableau**, que muestra el desempeño comercial de Andes Retail Group a través de dos vistas: una **Overview ejecutiva** y un **Detalle analítico**.

---

## 🧾 Descripción general

Este proyecto responde a dos preguntas de negocio centrales:

1. **¿Cómo ha evolucionado el ingreso total entre 2024 y 2025?** (Vista Overview)
2. **¿Por qué han subido, bajado o se han mantenido los ingresos?** (Vista Detalle)

El dashboard permite a los stakeholders identificar qué regiones, países y categorías generan más ingresos y rentabilidad, además de detectar patrones temporales (como la estacionalidad) que explican las variaciones en ventas.

---

## 🗂️ Fuente de datos

El dataset proviene de un archivo Excel (`Andes_Retail_Group_2024_2025.xlsx`) conectado directamente en Tableau. Contiene las siguientes columnas:

**Preparación de datos realizada:**
- Corrección de tipos de datos en columnas numéricas.
- Formateo de `Fecha_Pedido` al formato de español (Latinoamérica).
- Creación de una columna calculada `Nivel_Venta`, que clasifica cada pedido como **"Venta Alta"** (si `Ingresos` ≥ 1000) o **"Venta Baja"** (si `Ingresos` < 1000).
- Validación de calidad mediante la vista de Perfil de Columna.

---

## 🖥️ Estructura del dashboard

El archivo `.twb` contiene **2 vistas (dashboards)** construidas a partir de **11 hojas de trabajo**:

### Vista 1 — Overview (Resumen Ejecutivo)
Responde a: *¿Cómo ha evolucionado el ingreso total?*

Hojas que la componen:
- **Total Ingresos** — KPI principal de ingresos.
- **Total Unidades Vendidas** — KPI de volumen de ventas.
- **Ingreso Promedio** — KPI de ticket promedio.
- **Ingresos por Region** — gráfico de barras, ingresos agrupados por región.
- **Rentabilidad por Region** — gráfico de barras, diferencia entre ingresos y costos por región.
- **Rentabilidad por Categoria** — gráfico de barras, rentabilidad por categoría de producto.
- **Top 5 Products** — gráfico de tiempo, evolución de los 5 productos más vendidos.

**Filtro principal:** Año (2024–2025).

### Vista 2 — Detailed (Análisis Detallado)
Responde a: *¿Por qué se mueven los ingresos?*

Hojas que la componen:
- **Ingresos Periodo 25-26** — gráfico de líneas, ingresos vs. fecha de pedido, útil para detectar estacionalidad.
- **Ingresos Segmento Cliente** — gráfico de líneas, ingresos por región y segmento de cliente.
- **Unidades Region Segmento** — comparación de unidades vendidas por región y segmento.
- **Tabla** — tabla detallada con: conteo de `ID_Pedido`, conteo único de `ID_Cliente`, `País`, `Unidades_Vendidas`, `Categoría_Producto`, suma de `Ingresos` y rentabilidad.

**Filtros (mínimo 2):** `Fecha_Pedido`, `Región`, `País`, `Categoría_Producto`.

---

## 🔍 Narrativa e insights (Modelo SCQA)

### Vista General
- **Situación:** Andes Retail Group registró sus ingresos anuales durante 2025 y 2026 en todas sus categorías y segmentos de clientes.
- **Complicación:** Se identificó una caída sostenida en los ingresos entre mayo y agosto, en ambos años, afectando a todas las categorías y segmentos.
- **Pregunta:** ¿Qué está causando esta caída recurrente en las ventas?
- **Respuesta:** La caída de ingresos está relacionada con una caída en la cantidad de unidades vendidas.

### Vista Detalle
- **Situación:** La caída de ingresos se deriva de una caída en ventas durante mayo–agosto.
- **Complicación:** Esta caída en unidades vendidas afecta por igual a todos los países y regiones.
- **Pregunta:** ¿Qué está causando esta caída recurrente?
- **Respuesta:** La columna `Estación` revela que estos meses corresponden al invierno. Al repetirse el patrón en 2025 y 2026, se concluye que la caída tiene un comportamiento **estacional**.

### 💬 Mensaje ejecutivo (estilo Slack)

> **📊 Actualización desempeño comercial**
>
> Durante 2024–2025, Andes Retail Group registró ingresos en todas las categorías y segmentos. Los datos muestran una caída sostenida en ventas entre mayo y agosto, que afecta a todas las regiones por igual y coincide con la temporada de invierno, confirmando un patrón estacional.
>
> Próximo paso: evaluar si el catálogo o la estrategia de inventario requieren ajustes específicos para la temporada invernal.

---

## ✅ Estado del proyecto

Proyecto **revisado y aprobado**. Puntos fuertes destacados por el evaluador:
- Conexión de datos sin errores y buena preparación en Power Query.
- KPIs bien definidos, calculados correctamente y con secuencia lógica.
- Insights respaldados por evidencia visual en el dashboard.
- Navegación intuitiva entre pestañas.

**Oportunidades de mejora para futuras iteraciones:**
- Agregar tarjetas (KPIs) adicionales: ganancia total, margen promedio y total de pedidos.
- Incorporar más filtros interactivos (ej. por país).
- Conectar filtros entre pestañas (acciones de filtro cruzadas entre Overview y Detailed).
- Explorar gráficos adicionales segmentados por estación del año.

---

## 🛠️ Herramientas utilizadas

- **Tableau Desktop** — construcción del dashboard (`.twb`).
- **Excel** — fuente de datos original.
- **Jupyter Notebook** — documentación del proceso, planificación y narrativa del proyecto.

---

## 👤 Autor

Jesús — Data Analyst Junior
