# 16.01 VENTAS TOTALES
### Módulo 16 — Reportes

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reportes → Ventas Totales

---

## ¿Para qué sirve esta pantalla?

Reporte de ventas totalizadas por diferentes dimensiones. Permite analizar la performance comercial del período seleccionado agrupando los importes según el criterio elegido: por punto de venta, vendedor, artículo, marca, forma de pago, entre otros.

---

<img src="imagenes/pantalla_ventas_totales.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reportes → Ventas Totales**

---

## Filtros del panel izquierdo

| Campo | Descripción |
|---|---|
| DESDE | Fecha de inicio del período |
| HASTA | Fecha de fin del período |
| VER POR | Dimensión de agrupamiento (ver detalle abajo) |
| MOSTRAR | Qué tipos de comprobantes incluir |
| TIENDA | Filtrar por cuenta de tienda virtual |

---

## Opciones de VER POR

| Opción | Descripción |
|---|---|
| PUNTO DE VENTA | Totales por depósito/PDV |
| VENDEDOR | Totales por vendedor |
| ARTICULO | Totales por artículo |
| TIPO DE ARTICULO | Totales por tipo de artículo |
| GRUPO DE ARTICULOS | Totales por grupo |
| MARCA | Totales por marca |
| EQUIPOS CON #NSE | Totales por modelo de equipo (artículos con número de serie) |
| FORMA DE PAGO | Totales por tipo de pago |
| DIA DE FACTURACION | Totales por día |
| TIENDA VIRTUAL | Totales por tienda virtual |
| TIENDA VIRTUAL \| PDV | Totales por tienda y PDV |

---

## Opciones de MOSTRAR

| Opción | Descripción |
|---|---|
| TODO | Todos los comprobantes |
| SIN REMITOS | Solo facturas (excluye remitos) |
| SOLO REMITOS | Solo remitos |
| SIN VENTAS VIRTUALES | Solo ventas presenciales |
| SOLO VENTAS VIRTUALES | Solo ventas de tiendas virtuales |

---

## Columnas de la grilla

Las columnas varían según la dimensión seleccionada en VER POR.

| Columna | Descripción |
|---|---|
| Dimensión | PDV / Vendedor / Artículo / etc. según selección |
| Cantidad | Unidades vendidas |
| Precio Lista | Precio sin descuentos |
| Dto Promo | Descuento por promoción |
| Dto General | Descuento general |
| Dto Pago | Descuento por forma de pago |
| Interés | Recargo financiero |
| Precio Neto | Precio final antes de impuestos |
| Impuestos | IVA + impuestos internos + IIBB |
| Total | Importe total con impuestos |
| Costo | Costo del artículo |
| Margen | Margen bruto (solo disponible para algunas dimensiones) |

> ℹ️ Para la opción **FORMA DE PAGO**, la grilla muestra solo el Total (el resto de columnas no aplica).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
