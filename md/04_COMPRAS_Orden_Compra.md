# 4.01 ÓRDENES DE COMPRA A PROVEEDORES
### Módulo 4 — Compras

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Compras → Órdenes de Compra a Proveedores

---

<img src="imagenes/pantalla_orden_compra.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Órdenes de Compra** permite generar órdenes de compra para los proveedores a partir de los pedidos de mercadería y presupuestos pendientes. El sistema detecta automáticamente qué artículos tienen stock por reponer y qué proveedor los suministra, consolidando todo en una orden de compra. Desde aquí podés:

- Crear órdenes de compra para un proveedor seleccionado
- Revisar los pedidos y presupuestos pendientes antes de confirmar
- Agregar observaciones a la orden
- Generar la orden con fecha y proveedor asignados

---

## ¿Cómo acceder?

**Menú → Compras → Órdenes de Compra a Proveedores**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de la orden de compra. Por defecto, la fecha actual. |
| **PROVEEDOR** | Selector con los proveedores que tienen artículos con pedidos sin orden de compra. Solo aparecen los proveedores con ítems pendientes. |
| **ACCION** | (Visible solo en entornos con importador USA) Permite elegir entre **COMPRA LOCAL** (registra la compra en el sistema local) o **CREAR EN LLC** (crea la orden en el sistema de la empresa en USA). |
| **OBSERVACIONES** | Campo de texto libre para agregar notas a la orden de compra. |

---

## Botón: Pedidos y Presupuestos

Al hacer clic en **Pedidos y Presupuestos**, el sistema abre la grilla del lado derecho con el detalle de todos los artículos que tienen pedidos pendientes sin orden de compra para el proveedor seleccionado. Desde esta grilla podés revisar las cantidades antes de confirmar la orden.

Una vez revisado el detalle, la orden se genera y queda registrada en el sistema. El estado puede consultarse desde:
- [**Control de Órdenes de Compra**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Orden_Compra_Control.pdf) (4.02)
- [**Estado de Órdenes de Compra**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Orden_Compra_Estado.pdf) (4.03)
- [**Tracking de Órdenes de Compra**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Orden_Compra_Tracking.pdf) (4.04)

---

## Flujo típico

1. Ir a **Compras → Órdenes de Compra a Proveedores**
2. Seleccionar el **Proveedor** del combo (solo aparecen los que tienen artículos pendientes)
3. Verificar la **Fecha** y completar **Observaciones** si es necesario
4. Hacer clic en **Pedidos y Presupuestos** para ver el detalle de artículos
5. Confirmar la generación de la orden

---

## Notas importantes

- Solo aparecen en el combo de **PROVEEDOR** aquellos que tienen artículos con pedidos sin orden de compra asignada. Si el combo está vacío, no hay pedidos pendientes.
- La opción **ACCION** (COMPRA LOCAL / CREAR EN LLC) solo se muestra si la empresa tiene habilitado el módulo de importador USA.
- Una vez creada la orden, se puede hacer seguimiento desde las pantallas de Control, Estado y Tracking de Órdenes de Compra.
