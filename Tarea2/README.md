# Tarea 2 — Dashboard analítico en Power BI

**Curso:** Ingeniería en Ciencias y Sistemas — SEMI2
**Grupo:** SS22S2026_G# <!-- TODO: reemplazar # por el número de grupo -->
**Autor:** <!-- TODO: nombre completo -->
**Fecha de entrega:** <!-- TODO -->

## 1. Descripción del dataset

**Nombre:** Brazilian E-Commerce Public Dataset by Olist
**Fuente:** [Kaggle - olistbr/brazilian-ecommerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

<!-- TODO: 3-5 líneas describiendo de qué trata el dataset, qué periodo cubre,
cuántos registros/tablas tiene y por qué es relevante para el análisis. -->

Tablas utilizadas:

| Tabla | Contenido | Llave |
| --- | --- | --- |
| olist_orders_dataset | Pedidos, fechas y estatus | order_id |
| olist_order_items_dataset | Ítems, precio y flete por pedido | order_id, product_id |
| olist_customers_dataset | Clientes y ubicación | customer_id |
| olist_order_reviews_dataset | Reseñas y puntuación (1-5) | order_id |
| olist_products_dataset | Categoría de producto | product_id |
| product_category_name_translation | Traducción de categorías (PT→EN) | product_category_name |

## 2. Transformaciones realizadas (Power Query)

<!-- TODO: lista real de los pasos aplicados en Power Query, por ejemplo: -->

- Eliminación de columnas no utilizadas (ej. `review_comment_title`, coordenadas no usadas).
- Cambio de tipo de dato en columnas de fecha (`order_purchase_timestamp`, etc.) a Fecha/Hora.
- Eliminación de filas con `order_id` o `customer_id` nulos.
- Creación de columna calculada `Año-Mes` a partir de `order_purchase_timestamp` para análisis de tendencia.
- Combinación (merge) de `olist_products_dataset` con `product_category_name_translation` para obtener el nombre de categoría en inglés.
- Renombrado de columnas para claridad en el modelo.

## 3. Modelo de datos (relaciones)

<!-- TODO: captura del modelo (vista "Modelo" en Power BI) y breve explicación de
las relaciones (cardinalidad 1-a-muchos, tabla de hechos vs. dimensiones). -->

![Modelo de datos](capturas/modelo_relaciones.png)

## 4. Dashboard

![Dashboard](capturas/dashboard.png)

### Visualizaciones incluidas

1. **<!-- TODO: ej. Ventas totales por mes (gráfico de líneas) -->**
2. **<!-- TODO: ej. Ventas por categoría de producto (gráfico de barras) -->**
3. **<!-- TODO: ej. Puntuación promedio de reseñas por estado (mapa/barras) -->**
4. **Segmentador / filtro:** <!-- TODO: ej. filtro por rango de fechas o por estado del pedido -->
5. **Gráfico comparativo:** <!-- TODO: ej. comparación de ventas entre categorías o entre periodos -->

## 5. Interpretación de los KPIs

<!-- TODO: para cada indicador/visualización clave, 2-3 líneas explicando
qué muestra el dato y qué conclusión o decisión de negocio se puede tomar. -->

- **KPI 1 — <!-- nombre -->:** <!-- interpretación -->
- **KPI 2 — <!-- nombre -->:** <!-- interpretación -->
- **KPI 3 — <!-- nombre -->:** <!-- interpretación -->

## 6. Estructura del repositorio

```
SS22S2026_G#/
└── Tarea2/
    ├── README.md
    ├── dashboard.pbix
    ├── dataset/          (opcional: CSVs originales o link de origen)
    └── capturas/          (imágenes usadas en este README)
```
