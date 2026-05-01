# 7.13 TV FACTURACIÓN MASIVA
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Facturacion Masiva

---

## ¿Para qué sirve esta pantalla?

**TV Facturación Masiva** permite emitir comprobantes para múltiples ventas de tiendas virtuales en una sola operación. Desde aquí podés:

- Filtrar ventas listas para facturar por estado, envío, tipo de pago y fecha
- Seleccionar el tipo de comprobante y vendedor para toda la lote
- Marcar las ventas a facturar con checkbox y procesar todas juntas

---

<img src="imagenes/pantalla_tv_facturacion_masiva.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Facturacion Masiva**

---

## Panel izquierdo: Configuración y filtros

### Selectores de tienda y cuenta

| Campo | Descripción |
|---|---|
| **TIENDA** | Selector de tienda virtual (banner). |
| **USUARIO** | Cuenta de la tienda. |
| **DEPOSITO** | Punto de venta/depósito desde donde se facturará. |

### Sección Datos de facturación

| Campo | Descripción |
|---|---|
| **FC TIPO** | Tipo de comprobante para toda la lote (B, X, etc.). Visible solo si el parámetro de facturación masiva está activo. |
| **VENDEDOR** | Vendedor asignado. Se filtra por los depósitos del usuario de tienda seleccionado. |

### Sección Filtros de búsqueda

| Campo | Descripción |
|---|---|
| **ESTADO** | Estado de la venta en la tienda. |
| **ENVIO** | Tipo de envío. |
| **PAGO TIPO** | Forma de pago (transferencia, tarjeta, etc.). |
| **DESDE / HASTA** | Rango de fechas. |
| **VER POR** | Ordenar por fecha de CREACION o MODIFICACION. |
| **BUSQUEDA** | ID de venta para filtrar una específica. |

---

## Panel derecho: Grilla de ventas para facturar

| Columna | Descripción |
|---|---|
| **Checkbox** | Marcar las ventas a incluir en la facturación masiva. |
| **Orden** | Número de orden o Pack ID. |
| **Id** | ID de la venta en la tienda. |
| **FechaCreacion** | Fecha de la venta. |
| **Usuario** | Cuenta de la tienda. |
| **Estado** | Estado de la venta. |
| **Total** | Importe total de la venta. |
| **Aprobada** | SI si la venta fue aprobada. |
| **Pago tipo / estado / detalle** | Datos del pago. |
| **Tipo envio / Obs envio / Costo envio** | Datos del envío. |
| **TrackingNumber** | Número de seguimiento. |
| **Cliente / Documento / Telefono / Email** | Datos del comprador. |
| **Fc Tipo / Fc Nro** | Comprobante ya emitido (si tiene). |
| **Fc Subida** | SI si la factura fue subida a la tienda. |
| **Ultimo mensaje** | Error o mensaje del último proceso de facturación. |

### Fila de totales

La grilla muestra una fila de totales con la suma de los importes de las ventas visibles.

---

## Cómo facturar masivamente

1. Seleccioná la **TIENDA**, **USUARIO** y **DEPOSITO**.
2. Si está disponible, seleccioná el **FC TIPO** y **VENDEDOR**.
3. Aplicá los filtros para ver las ventas a facturar.
4. Marcá los **checkboxes** de las ventas a incluir.
5. Ejecutá la facturación (botón de la barra superior).

> 💡 Solo aparecen en la grilla las ventas que cumplen los criterios para ser facturadas (aprobadas, sin factura previa, con datos de cliente válidos).

> ⚠️ Ventas con documento del comprador inválido (muy largo) se filtran automáticamente y no aparecen en la grilla.

---

> 📖 Para facturar una venta individual consultá [**Facturar Ventas**](https://ayuda.caddis.com.ar/instructivos/07_TV_Facturar_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
