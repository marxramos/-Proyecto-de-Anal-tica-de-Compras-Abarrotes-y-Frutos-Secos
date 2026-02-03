# Proyecto_de_Automatizacion_de_Facturas_y_analitica_de_datos
## Descripción general
Este proyecto implementa un sistema automatizado de extracción, transformación y análisis de compras, orientado a un negocio de abarrotes y frutos secos. 
El objetivo es centralizar la información de facturas, estructurarla en un modelo analítico y generar KPIs mensuales y comparativos, con un diseño preparado para escalar a mayor volumen de datos.
Actualmente el proyecto cuenta con 1 mes de datos reales, pero la arquitectura fue diseñada con enfoque escalable y modular.
## Arquitectura del sistema
Arquitectura del sistema:
- Captura de datos vía Telegram via imagen o PDF
- Orquestación y automatización con Make
- Normalización y estructuración usando ChatGPT
- Almacenamiento en Google Sheets
- Modelado analítico (tablas base y detalle)
- Análisis y KPIs mediante QUERY y fórmulas tipo SQL
- Visualización en dashboard
## Modelo de datos
### Tabla 1: factura (datos generales)
Contiene información a nivel cabecera de cada factura.
| Campo | Descripcion |
|-------|-------------|
| factura_id | dentificador único de la factura|
| ruc_emisor | RUC del proveedor |
| Proveedor | Nombre del proveedor|
| fecha_factura | Fecha de emision|
| subtotal | Montos sin impuestos |
| igv | Impuesto|
| precio_total | Total de factura|
| timestamp | Hora en que se registra la factura via imagen o pdf|
| usuario | Persona que hace uso de los recursos|
| mes | mes de emision de factura|
| año | año de emision de factura|

La presenta tabla general ayuda a la parte contable donde contrasta y registra cada historia de compra en una fila.

### Tabla 2: items factura (detalle - tabla analítica)
Tabla principal para análisis (nivel producto).
| Campo | Descripción |
|-------|-------------|
| factura_id | Relacion con la tabla factura |
| item | Ítem de la factura |
| descripcion | producto comprado |
| cantidad | Cantidad |
| precio_unitario | Precio por unidad |
| total_item | Total por Ítem |
| fecha_factura | Fecha |
| categoria | Se categorizo en 10 facturas |
| proveedor | Proveedor |
| mes | Mes de la factura numerico |
| año | Año de la factura numerico |

Esta tabla es el minita de informacion puro para el analisis, ya que permite.
- Analisis por categoria
- Comparativo mensuales
- KPIs por proveedor y producto

### KPIs implementados / planificados
- Consumo total del mes
- Variacion VS mes anterior
- Compras por proveedor
- Compras por categoria
- Evolución mensual del gasto
- Top productos por consumo
- Ticket promedio por factura
### Tecnologías utilizadas
- Telegram – Captura inicial de datos
- Make – Automatización y orquestación
- ChatGPT – Normalización y estructuración de datos
- Google Sheets – Almacenamiento y análisis
- QUERY (SQL-like) – Consultas analíticas
- Dashboards – Visualización
### Escalabilidad
El sistema está diseñado para:
- Incorporar nuevos proveedores
- Aumentar volumen de facturas
- Migrar a una base de datos (PostgreSQL / BigQuery)
- Conectarse a herramientas de BI (Looker / Power BI)
### Estado del proyecto
En desarrollo
Datos reales: 1 mes
Objetivo del proyecto: consolidar historico de data  automatizar KPIs mensuales

### Autor
Proyecto desarrollado por: Marx Vladimir Ramos Quispe
Data Analyst / Automatizacion
LinkedIn: www.linkedin.com/in/marxramosquispe
  
