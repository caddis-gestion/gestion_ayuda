# 3.09 PRESUPUESTOS PENDIENTES DE FACTURAR
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Presupuestos Pendientes de Facturar

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Presupuestos Pendientes de Facturar** (también llamada **Presupuestos Reservados**) permite gestionar los presupuestos que tienen stock reservado y están en espera de facturación. Desde aquí podés:

- Ver presupuestos con stock reservado y artículos pendientes de entregar
- Filtrar por fecha, cliente, remito de ingreso o artículo específico
- Aprobar presupuestos para que puedan ser facturados
- Anular una aprobación si el presupuesto todavía no debe facturarse
- Ver el estado detallado de cada presupuesto y su orden de compra vinculada

> ℹ️ Esta pantalla está especialmente diseñada para flujos donde el stock se reserva al momento de generar el presupuesto y se factura cuando el stock está disponible para entrega.

---

<img src="imagenes/pantalla_presupuestos_pendientes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Presupuestos Pendientes de Facturar**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Filtros para acotar la búsqueda
- **Panel derecho:** Grilla con los presupuestos pendientes que cumplen los filtros

---

## Filtros del panel izquierdo

| Campo | Descripción |
|---|---|
| **DESDE** | Fecha de inicio del período a consultar. Por defecto: un mes atrás. |
| **HASTA** | Fecha de fin del período. Por defecto: hoy. |
| **CLIENTE** | Filtra por cliente específico. |
| **INGRESO** | Número de ingreso/remito de entrada de mercadería. Permite ver qué presupuestos están esperando un ingreso específico. |
| **ARTICULO** | Filtra por artículo. El selector muestra solo artículos que tienen cantidades pendientes en el período seleccionado. |

---

## Columnas de la grilla (panel derecho)

| Columna | Descripción |
|---|---|
| **Fecha PP** | Fecha de creación del presupuesto |
| **OC** | Número de Orden de Compra relacionada (si existe) |
| **PP** | Número del presupuesto |
| **PP Reservado** | Cantidad de ese artículo reservada para el presupuesto |
| **Cliente** | Nombre del cliente |
| **PP Estado** | Estado actual del presupuesto |
| **Facturar** | SI / vacío — indica si el presupuesto fue aprobado para facturar |

---

## Acciones disponibles por fila

| Acción | Qué hace |
|---|---|
| **Ver detalle** | Muestra el detalle completo del presupuesto (doble clic) |
| **Imprimir** | Imprime el comprobante de presupuesto |
| **Aprobar** | Marca el presupuesto como "aprobado para facturar" (activa la columna Facturar = SI) |
| **Borrar** | Anula la aprobación de facturación (vuelve el presupuesto a estado pendiente) |

---

## Paso a paso: Aprobar un presupuesto para facturar

**Caso típico:** El stock llegó y el presupuesto puede facturarse.

**1.** Buscá el presupuesto usando los filtros (por cliente, artículo o ingreso de mercadería).

**2.** En la grilla, ubicá el presupuesto correspondiente.

**3.** Hacé clic en el botón **Aprobar** de esa fila.

**4.** La columna **Facturar** pasará a mostrar "SI".

**5.** El presupuesto ahora está disponible para ser facturado desde la pantalla de **Facturación** (3.01).

---

## Preguntas frecuentes

**¿Qué diferencia hay entre esta pantalla y Estado de Presupuestos (3.08)?**
- **Estado de Presupuestos** (3.08): muestra todos los presupuestos activos, sin distinción de si tienen stock reservado.
- **Presupuestos Pendientes** (3.09): muestra solo presupuestos con **stock reservado** que están esperando ser facturados. Es más específico para entornos con reserva de stock.

**¿Qué es la "Orden de Compra relacionada" (OC)?**
En algunos flujos, cuando se crea un presupuesto con artículos sin stock, se genera automáticamente una Orden de Compra para proveedor. Esta columna muestra el número de esa OC para hacer el seguimiento.

**¿Si apruebo un presupuesto, se factura automáticamente?**
No. La aprobación es una marca que habilita al operador a facturar ese presupuesto. La facturación sigue siendo manual desde la pantalla de Facturación.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
