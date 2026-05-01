# 3.68 REASIGNAR VENDEDOR
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Reasignar Vendedor

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Reasignar Vendedor** permite corregir el vendedor asignado en facturas ya emitidas. Es útil cuando una venta fue registrada con el vendedor incorrecto. Desde aquí podés:

- Filtrar facturas por punto de venta y rango de fechas
- Ver el listado de comprobantes con su vendedor actual
- Modificar el vendedor asignado en cada comprobante

---

<img src="imagenes/pantalla_reasignar_vendedor.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Reasignar Vendedor**

---

## Descripción general de la pantalla

La pantalla tiene un panel superior con los filtros de búsqueda y una grilla inferior con los comprobantes encontrados.

---

## Filtros de búsqueda

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta del que se quieren ver las facturas |
| **DESDE** | Fecha de inicio del período a consultar |
| **HASTA** | Fecha de fin del período a consultar |

---

## Grilla de comprobantes

Muestra las facturas que coinciden con los filtros aplicados:

| Columna | Descripción |
|---|---|
| Fecha | Fecha de emisión del comprobante |
| Tipo | Tipo de comprobante (A, B, C, TK, etc.) |
| Factura | Número del comprobante |
| Cliente | Nombre del cliente |
| Vendedor | Nombre del vendedor asignado actualmente (resaltado en amarillo) |
| Punto de Venta | Nombre del punto de venta |

**Acciones disponibles:**
- **Modificar:** Permite cambiar el vendedor asignado al comprobante seleccionado

---

## Cómo reasignar un vendedor

1. Seleccioná el **PDV** y el rango de fechas (**DESDE** / **HASTA**)
2. La grilla se cargará con los comprobantes del período
3. Hacé clic en **Modificar** en la fila del comprobante a corregir
4. Seleccioná el nuevo vendedor y confirmá el cambio

---

## Notas importantes

- La columna **Vendedor** aparece resaltada en amarillo para facilitar su identificación.
- Solo se muestran comprobantes no anulados (Anulado = 0 u 8).
- Esta pantalla modifica únicamente el vendedor del encabezado del comprobante, no afecta comisiones ni totales.
