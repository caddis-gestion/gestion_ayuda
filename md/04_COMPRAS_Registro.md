# 4.05 REGISTRO DE COMPRAS
### Módulo 4 — Compras

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Compras → Registro de Compras

---
<img src="imagenes/pantalla_facturas_compras.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Registro de Compras** permite consultar el historial completo de facturas de compra de productos registradas por proveedor. Es la vista de búsqueda y control del módulo de compras, y su base para gestionar la cuenta corriente con cada proveedor. Desde aquí podés:

- Consultar todas las facturas registradas para un proveedor
- Ver el desglose impositivo de cada compra (gravado, no gravado, IVA, percepciones)
- Controlar si los importes coinciden con los remitos de stock (semáforo)
- Acceder al detalle de artículos de una compra (remito asociado)
- Modificar o borrar compras existentes

---

## ¿Cómo acceder?

**Menú → Compras → Registro de Compras**

---

## Panel de filtros

| Campo | Descripción |
|---|---|
| **PROVEEDOR** | Filtra las compras del proveedor seleccionado. Al cambiarlo, la grilla se actualiza automáticamente. |
| **TIPO** | Opcional. Filtra por categoría general de compra (Mercadería, Gastos, Servicios, etc.). |
| **CATEGORIA** | Opcional. Filtra por subcategoría dentro del tipo seleccionado. |

---

## Grilla de compras

La grilla muestra el historial de facturas registradas con los siguientes datos:

| Columna | Descripción |
|---|---|
| Fecha Contable | Fecha contable asignada al comprobante. |
| Factura Fecha | Fecha de emisión de la factura. |
| Factura Tipo | Tipo de comprobante (A, B, C, NC-A, NC-B, etc.). |
| Factura Número | Número en formato PPPP-NNNNNNNNN. |
| Moneda | Divisa de la factura. |
| Cotización | Tipo de cambio aplicado. |
| Total | Importe total expresado en moneda local. |
| Gravado | Base imponible para IVA. |
| No Gravado | Monto no gravado. |
| Exento | Monto exento de IVA. |
| Descuento | Descuento global. |
| IVA 10,5% | Monto de IVA a tasa reducida. |
| IVA 21,0% | Monto de IVA a tasa general. |
| IVA 27,0% | Monto de IVA a tasa especial. |
| Impuestos Internos | Imp. Internos discriminados. |
| Percepción IVA | Percepción de IVA. |
| Percepción IIBB 1 y 2 | Percepciones de Ingresos Brutos. |
| Impuestos Varios | Otros cargos impositivos. |
| Gastos | Gastos de flete u otros incluidos. |
| Detalle | Observaciones del comprobante. |
| Tipo | Categoría de la compra. |
| Categoría | Subcategoría. |
| Proveedor | Nombre del proveedor. |
| **Semáforo** | Control de costos vs. remito de stock: 🟢 verde = ok, 🟡 amarillo = diferencia de importes, 🔴 rojo = sin remito asociado. |

---

## Acciones disponibles desde la grilla

| Acción | Descripción |
|---|---|
| **Modificar** (✏️) | Abre el formulario de la factura para editar sus datos. |
| **Detalle** (📄) | Abre el detalle de artículos y cantidades del remito asociado a la compra. |
| **Borrar** (🗑️) | Elimina la factura de compra (pide confirmación). |

---

## Detalle de artículos de una compra

Al hacer clic en **Detalle** sobre una compra, se abre un popup que muestra el remito de mercadería vinculado a esa factura, con:

- Código y descripción del artículo
- Costo unitario (en moneda local)
- Porcentaje de descuento
- Cantidad
- Total por artículo

---

## Notas importantes

- La columna **Semáforo** es clave para el control de costos: si una factura no tiene remito asociado (rojo) o los importes no coinciden (amarillo), debe revisarse antes del cierre contable.
- Las compras registradas impactan directamente en el **costo promedio** de los artículos en stock.
- El Registro de Compras es solo para consulta y control; para ingresar nuevas facturas usar [**Facturas de Compra**](https://ayuda.caddis.com.ar/instructivos/04_COMPRAS_Facturas.pdf) (4.07).
