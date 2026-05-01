# 3.14 VENTAS TOTALES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales y supervisores del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Ventas Totales

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Ventas Totales** es el informe de ventas principal del sistema. Permite analizar las ventas del período agrupadas por diferentes criterios. Desde aquí podés:

- Ver las ventas totales del mes/período filtrado
- Agrupar las ventas por punto de venta, vendedor, artículo, tipo, marca, forma de pago o día
- Ver los importes desglosados: precio lista, descuentos, neto, impuestos, total, costo y margen
- Acceder al detalle de cada factura individual (doble clic en cualquier grupo)
- Filtrar para incluir o excluir remitos y ventas de tiendas virtuales

---

<img src="imagenes/pantalla_ventas_totales.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Ventas Totales**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Filtros de período, agrupación y tipo de ventas
- **Panel derecho:** Grilla con los totales agrupados según el criterio seleccionado

---

## Filtros del panel izquierdo

| Campo | Descripción |
|---|---|
| **DESDE** | Fecha de inicio del período a analizar. Por defecto: el primer día del mes actual. |
| **HASTA** | Fecha de fin del período. Por defecto: hoy. |
| **VER POR** | Criterio de agrupación de las ventas (ver tabla más abajo). |
| **MOSTRAR** | Qué tipos de comprobantes incluir en el análisis (ver tabla más abajo). |
| **TIENDA** | Filtra las ventas de una tienda virtual específica (MercadoLibre, TiendaNube, etc.). Solo activo si el filtro MOSTRAR incluye ventas virtuales. |

---

### Opciones de "VER POR" (agrupación)

| Opción | Cómo agrupa los datos |
|---|---|
| **PUNTO DE VENTA** | Agrupa ventas por local o sucursal |
| **VENDEDOR** | Agrupa ventas por vendedor |
| **ARTICULO** | Agrupa ventas por artículo vendido |
| **TIPO DE ARTICULO** | Agrupa por tipo de artículo (ej.: accesorios, equipos, servicios) |
| **GRUPO DE ARTÍCULOS** | Agrupa por grupo de artículo |
| **MARCA** | Agrupa ventas por marca del artículo |
| **EQUIPOS CON #NSE** | Agrupa ventas de equipos identificados por número de serie |
| **FORMA DE PAGO** | Agrupa ventas por medio de pago utilizado |
| **DIA DE FACTURACION** | Agrupa las ventas por día |
| **TIENDA VIRTUAL** | Agrupa ventas por plataforma de e-commerce (ML, TN, etc.) |
| **TIENDA VIRTUAL \| PDV** | Agrupa combinando plataforma e-commerce con punto de venta |

---

### Opciones de "MOSTRAR" (tipo de comprobantes)

| Opción | Qué incluye |
|---|---|
| **TODO** | Todos los comprobantes (facturas + remitos + ventas virtuales) |
| **SIN REMITOS** | Solo facturas, excluye remitos (R, IR, OV, RM, IRM) |
| **SOLO REMITOS** | Solo remitos |
| **SIN VENTAS VIRTUALES** | Facturas de ventas presenciales, excluye e-commerce |
| **SOLO VENTAS VIRTUALES** | Solo facturas de ventas de tiendas virtuales |

> 💡 El filtro "SIN REMITOS" es el más usado cuando querés analizar solo las ventas facturadas, sin contar los remitos de entrega.

---

## Columnas de la grilla (panel derecho)

| Columna | Descripción |
|---|---|
| **Identificación** | Nombre del PDV, Vendedor, Artículo, etc. según el VER POR elegido |
| **Cantidad** | Total de unidades vendidas |
| **Precio Lista** | Precio original antes de descuentos |
| **Dto Promo** | Descuento por promoción aplicada |
| **Dto General** | Descuento general aplicado |
| **Dto Pago** | Descuento por forma de pago aplicada |
| **Interes** | Interés por cuotas con tarjeta |
| **Precio Neto** | Precio neto (lista − descuentos + intereses) |
| **Impuestos** | IVA + impuesto interno + IIBB |
| **Total** | Total con impuestos (lo que pagó el cliente) |
| **Costo** | Costo de la mercadería vendida |
| **Margen** | Margen de ganancia en porcentaje |

> ⚠️ El margen se calcula como `(Precio Neto - Costo) / Precio Neto`. Solo aparece cuando el costo está cargado en el sistema.

---

## Acción disponible: Ver el detalle de las facturas

Al hacer **doble clic** en cualquier fila de la grilla, se abre una ventana de detalle que muestra todas las facturas individuales del período que conforman ese total. Desde esa ventana también podés ver el detalle de cada factura.

---

## Paso a paso: Consultar las ventas del mes por vendedor

**1.** Verificá que **DESDE** y **HASTA** están en el rango del mes que querés analizar.

**2.** En **VER POR**, seleccioná **VENDEDOR**.

**3.** En **MOSTRAR**, elegí **SIN REMITOS** para ver solo ventas facturadas.

**4.** Actualizá la grilla (el sistema la recarga automáticamente al cambiar los filtros).

**5.** La grilla mostrará una fila por vendedor con los totales del período.

**6.** Para ver el detalle de las facturas de un vendedor específico, hacé doble clic en su fila.

---

## Notas importantes

- **Los datos incluyen Notas de Crédito:** el sistema resta automáticamente las NC de los totales. Los valores de las NC se restan de las cantidades y los importes.
- **Solo aparecen PDVs permitidos:** cada usuario ve solo los puntos de venta a los que tiene acceso.
- **Comprobantes anulados:** los comprobantes con estado de anulación estándar (0 o 8) se incluyen según la configuración del sistema.

---

## Preguntas frecuentes

**¿Por qué el "Precio Lista" es diferente del "Total"?**
El "Precio Lista" es el precio original antes de descuentos e impuestos. El "Total" es lo que realmente pagó el cliente (con descuentos, intereses e impuestos incluidos).

**¿Qué es el "Margen"?**
El margen es el porcentaje de ganancia sobre el precio neto de venta. Solo se calcula correctamente si los costos de los artículos están cargados en el sistema.

**¿Puedo exportar este informe a Excel?**
Sí, la grilla tiene una opción de exportación disponible en la parte superior o inferior. Hacé clic en el ícono de exportación (generalmente un botón de impresora o Excel).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
