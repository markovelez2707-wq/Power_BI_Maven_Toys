# Maven Toys — Dashboard de Ventas y Rendimiento Retail (Power BI)

Dashboard interactivo desarrollado en **Microsoft Power BI** para analizar el desempeño comercial, la tendencia de unidades vendidas y el crecimiento interanual (YoY) de las tiendas Maven Toys en México.

---

## Vista General y Demostración de Filtros (`Store_Location`)

### 1. Vista General (Sin filtros aplicados)
Panorama completo de ventas con **1.09 millones de unidades vendidas** y **$14.44 millones en ingresos**, desglosado por periodo mensual, categoría de producto y ciudad.

 <img width="1433" height="697" alt="Captura de pantalla 2026-11-24 110024" src="https://github.com/user-attachments/assets/9462a805-651a-4504-b834-2ee6114685b9" />


### 2. Filtro: Airport
Desempeño específico de las sucursales ubicadas en aeropuertos.

 <img width="1318" height="682" alt="Captura de pantalla 2026-11-24 110041" src="https://github.com/user-attachments/assets/9ad90117-a0fc-4ffc-a7e4-f4f7ba3bba47" />


### 3. Filtro: Commercial
Desempeño específico de las sucursales ubicadas en zonas comerciales.

 <img width="1298" height="697" alt="Captura de pantalla 2026-11-24 110054" src="https://github.com/user-attachments/assets/8da20a10-4cba-495a-9dbb-0105be2a8dab" />


### 4. Filtro: Downtown
Desempeño específico de las sucursales ubicadas en zonas centro.

 <img width="1292" height="688" alt="Captura de pantalla 2026-11-24 110107" src="https://github.com/user-attachments/assets/a1c5b33a-13e4-4025-a76e-a3310f03e72b" />


### 5. Filtro: Residential
Desempeño específico de las sucursales ubicadas en zonas residenciales.

 <img width="1302" height="697" alt="Captura de pantalla 2026-11-24 110120" src="https://github.com/user-attachments/assets/76821ac1-d6cf-4ecd-b377-b1f4b624f206" />


---

## Objetivo del Proyecto
Monitorear los indicadores clave de rendimiento (KPIs) del negocio e identificar las ubicaciones, ciudades y categorías de productos con mayor volumen de ventas para apoyar la toma de decisiones comerciales y de inventario.

## Modelado de Datos y Arquitectura
* **Modelo Relacional:** Se conectaron 5 tablas principales (`sales`, `products`, `stores`, `inventory` y una tabla de dimensión de fechas `calendar`) para habilitar filtros temporales precisos y análisis cruzado entre ventas, catálogo y tiendas.
* **Preparación de Datos:** Limpieza y estructuración de costos, precios de venta, registros de transacciones y catálogo de sucursales.

## Medidas DAX e Inteligencia de Tiempo
Se crearon medidas personalizadas en **DAX** para calcular KPIs principales y comparativas entre periodos:
* **KPIs Principales:** Total de Unidades Vendidas (`UNIDADES` — 1.09 mill.), Ingresos Totales (`Ingresos` — $14.44 mill.), Número de Transacciones (`Num_Ventas`) y Unidades por Venta (`Unid_Venta`).
* **Inteligencia de Tiempo (Time Intelligence):** Unidades del mes anterior (`Unid_mes_ant`), Unidades del año anterior (`Unidades_año_ant`), Cambio mensual (`Cambio_vs_mes_ant`) y Crecimiento interanual (`Variación vs año anterior`).
* **Participación:** Porcentaje de contribución de unidades (`% de_unidad`) por tienda y categoría.

## Hallazgos Clave del Análisis
* **Estacionalidad:** El seguimiento por periodo (`202201` – `202302`) evidencia un crecimiento sostenido hacia el cierre de año con un pico máximo de demanda en diciembre (`202212`).
* **Categorías Líderes:** *Art & Crafts*, *Toys* y *Games* concentran el mayor volumen de unidades vendidas y el crecimiento interanual más alto.
* **Plazas Principales:** *Ciudad de México*, *Guadalajara* y *Monterrey* encabezan el volumen de unidades desplazadas a nivel nacional.

## Contenido del Repositorio
* `Maven Toys POWER BI.pbix` — Archivo editable de Power BI Desktop con el modelo relacional y fórmulas DAX completas.
