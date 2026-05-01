# 3.60 LIBERAR ENTREGA FACTURA
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Liberar Entrega Factura

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Liberar Entrega Factura** permite autorizar la entrega de mercadería correspondiente a facturas de cuenta corriente. En flujos donde la mercadería no se entrega hasta que el crédito está aprobado, desde aquí podés:

- Consultar las facturas en cuenta corriente de un cliente que están pendientes de liberación para entrega
- Liberar (autorizar) la entrega de la mercadería de una factura específica
- Filtrar por estado de liberación (todas, liberadas, no liberadas)

---

<img src="imagenes/pantalla_liberar_entrega_factura.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Liberar Entrega Factura**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con los filtros y un panel derecho con la grilla de facturas.

---

## Panel izquierdo — Filtros

| Campo | Descripción |
|---|---|
| **CLIENTE** | Cliente mayorista. Al seleccionarlo, la grilla muestra sus facturas en cuenta corriente. |
| **LIBERADAS** | Filtra las facturas por estado de liberación: **TODO** (muestra todas), **NO** (sólo pendientes de liberar), **SI** (sólo las ya liberadas) |

---

## Panel derecho — Grilla de facturas

Muestra las facturas del cliente en cuenta corriente que tienen entrega logística pendiente:

| Columna | Descripción |
|---|---|
| Checkbox | Indica si la factura está liberada para entrega (marcado = liberada) |
| Factura Tipo | Tipo de comprobante |
| Factura Nro | Número de la factura |
| Plazo | Plazo de la condición de cuenta corriente (días) |
| Dias | Cantidad de días transcurridos desde la emisión de la factura |

---

## Cómo liberar una factura

Hacé clic en el **checkbox** de la factura que querés liberar para que el sistema autoriza la entrega de la mercadería.

---

## Notas importantes

- Solo aparecen en la grilla las facturas con pago **en cuenta corriente** (Id_Pago = 4) que no tienen remito logístico asociado.
- La liberación permite que el módulo de logística pueda preparar y despachar la mercadería.
- Este proceso es parte del flujo de crédito y entrega: primero se vende en cta. cte., luego se aprueba el crédito y finalmente se libera la entrega.
