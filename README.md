# Análisis Comparativo: Power BI vs Tableau

## 1. Objetivo
El propósito de este análisis es crear un **dashboard idéntico** en dos herramientas de Business Intelligence (Power BI y Tableau) usando el dataset **TechStore**, para comparar la **usabilidad**, **rendimiento** y **capacidades** de ambas plataformas, y determinar cuál es más adecuada para el caso de estudio.

## 2. Dataset Utilizado
El dataset está compuesto por cuatro archivos CSV:

- **ventas_techstore.csv:** contiene las ventas históricas de productos, con fecha, cantidad, precio unitario, vendedor y cliente.
- **productos.csv:** catálogo de productos, con categoría, stock y otros atributos.
- **clientes.csv:** información básica de clientes.
- **metas_mensuales.csv:** metas de ventas mensuales para evaluar el desempeño.

---

## 3. Construcción del Dashboard

**Gráficos**
   
- **Gráfico de Líneas:** Ventas por mes

Nota: Teniendo en cuenta que los datos de ventas se limitan a dos meses, se filtraron por mes y dia.




```
Ventas Totales = SUM(ventas_techstore[cantidad])
```
---





**Calculated field:** Se suman las ventas totales.
```
(SUM([ventas_techstore].[Cantidad]))
```

---

- **Gráfico de Barras:** Top 10 productos 



---

- **Gráfico de Pie:** Ventas por categoría



---

 - **Gráfico de Tabla:** Performance de vendedores (ventas, clientes atendidos)



---

# Comparación de herramientas:

Crear el dashboard en Power BI fue un proceso bastante directo. La interfaz es muy intuitiva: cargas los datos, defines relaciones y construyes visualizaciones sin demasiada fricción. DAX ayuda a crear medidas personalizadas de forma sencilla y, con algo de apoyo en documentación o IA, es fácil entender y replicar el código. En general, fue rápido armar el dashboard y el resultado se ve limpio y profesional.

En Tableau, la experiencia es distinta. Es una herramienta que invita más a explorar los datos y probar diferentes visualizaciones. Arrastrar los atributos hacia las columnas y filas también fue bastante intuitivo, las calculated fields son fáciles de entender y conectar tablas es bastante simple con su interfaz interactiva de "Fuente de datos" parecido a SQL. Además, permite crear dashboards muy interactivos gracias a las acciones entre hojas, lo que da un resultado final más dinámico. Sin embargo, el proceso toma más tiempo, ya que cada visual debe construirse en una hoja y luego agregarse manualmente al dashboard. Además, la interfaz me resultó un poco menos intuitiva que la de Power BI.

Además, Power BI tiene una versión de escritorio gratuita, mientras que Tableau requiere una licencia de pago, en conclusión, la experiencia en Power BI fue más rápida y eficiente siendo un poco más intuitiva para alguien inexperto, es ideal si se busca construir un dashboard de forma ágil y sin gastar dinero.
