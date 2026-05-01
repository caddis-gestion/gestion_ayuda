# 3.69 REASIGNAR VENTAS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Reasignar Ventas

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Reasignar Ventas** permite corregir masivamente las asignaciones de responsables en comprobantes ya emitidos: vendedor, supervisor, jefe de ventas y gerente. Es útil para reorganizaciones comerciales o correcciones después de cambios de estructura. Desde aquí podés:

- Filtrar comprobantes por tipo
- Definir nuevas asignaciones para vendedor, supervisor, subgerente y gerente
- Verificar los comprobantes afectados antes de confirmar

---

<img src="imagenes/pantalla_reasignar_ventas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Reasignar Ventas**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con los criterios de reasignación y una grilla a la derecha con los comprobantes que serán afectados.

---

## Filtro de comprobantes

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de comprobante a reasignar. Incluye todos los tipos de factura, notas de crédito y débito (A, B, C, TK, NCIB, NCIA, NCX, NCP, etc.) |

---

## Sección: Definir Nuevas Asignaciones

Permite especificar qué responsables se reasignarán. Cada fila tiene un selector, un campo de categoría (solo lectura) y un checkbox para activar ese cambio:

| Fila | Descripción |
|---|---|
| **PDV** | Nuevo punto de venta a asignar. El campo de categoría muestra la categoría del PDV. Activar el checkbox para aplicar. |
| **VEND** | Nuevo vendedor. El campo de categoría muestra la categoría del vendedor. Activar el checkbox para aplicar. |
| **SUP** | Nuevo supervisor. El campo de categoría muestra la categoría del supervisor. Activar el checkbox para aplicar. |
| **J.VTAS** | Nuevo jefe de ventas (subgerente). Activar el checkbox para aplicar. |
| **GTE** | Nuevo gerente. Activar el checkbox para aplicar. |

Solo se aplican los cambios cuyo checkbox esté activado.

---

## Grilla de comprobantes afectados

Muestra los comprobantes que serán modificados según los criterios definidos:

| Columna | Descripción |
|---|---|
| Tipo | Tipo de comprobante |
| Factura | Número del comprobante |
| Fecha | Fecha de emisión |
| PDV | Punto de venta actual |
| Vendedor | Vendedor actual |
| VEND_Cat | Categoría del vendedor |
| Supervisor | Supervisor actual |
| SUP_Cat | Categoría del supervisor |
| Subgerente | Subgerente actual |
| SubGte_Cat | Categoría del subgerente |
| Gerente | Gerente actual |
| GTE_Cat | Categoría del gerente |

---

## Notas importantes

- Esta pantalla realiza cambios masivos sobre múltiples comprobantes a la vez. Revisá bien la grilla antes de confirmar.
- Solo se modifican los responsables cuyo checkbox esté marcado; el resto permanece sin cambios.
- La operación afecta los datos de asignación comercial, no los importes ni la validez fiscal del comprobante.
