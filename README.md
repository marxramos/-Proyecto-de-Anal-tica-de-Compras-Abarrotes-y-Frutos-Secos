# Proyecto_de_Analitica_de_Compras_Abarrotes_y_Frutos_Secos
## Descripción general
Este proyecto implementa un sistema automatizado de extracción, transformación y análisis de compras, orientado a un negocio de abarrotes y frutos secos. 
El objetivo es centralizar la información de facturas, estructurarla en un modelo analítico y generar KPIs mensuales y comparativos, con un diseño preparado para escalar a mayor volumen de datos.
Actualmente el proyecto cuenta con 1 mes de datos reales, pero la arquitectura fue diseñada con enfoque escalable y modular.
## Arquitectura del sistema
Arquitectura del sistema:
1.- Captura de datos vía Telegram
2.- Orquestación y automatización con Make
3.- Normalización y estructuración usando ChatGPT
4.- Almacenamiento en Google Sheets
5.- Modelado analítico (tablas base y detalle)
6.- Análisis y KPIs mediante QUERY y fórmulas tipo SQL
7.- Visualización en dashboard
## Modelo de datos
### Tabla 1: factura (datos generales)
Contiene información a nivel cabecera de cada factura.
| Campo | Descripcion |
|-------|-------------|
