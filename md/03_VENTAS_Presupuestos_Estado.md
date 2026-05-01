# 3.08 ESTADO DE PRESUPUESTOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Estado de Presupuestos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Estado de Presupuestos** permite consultar todos los presupuestos activos del sistema (pendientes de facturar). Desde aquí podés:

- Ver todos los presupuestos que aún no han sido convertidos en factura
- Consultar el estado de un presupuesto específico por número, CUIT o artículo
- Ver si un presupuesto está pendiente de facturar o ya fue parcialmente facturado
- Imprimir el comprobante de presupuesto
- Ver el detalle de un presupuesto específico

> ℹ️ Esta pantalla muestra solo los presupuestos **activos** (en estado diferente a "Completo" o "Rechazado" y no anulados). Los presupuestos ya facturados no aparecen en este listado.

---

<img src="imagenes/pantalla_presupuestos_estado.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Estado de Presupuestos**

---

## Descripción general de la pantalla

La pantalla tiene un campo de búsqueda y una grilla con todos los presupuestos activos que coinciden con el criterio de búsqueda.

---

## Campo de búsqueda

| Campo | Descripción |
|---|---|
| **Buscar** | Ingresá cualquiera de los siguientes valores para filtrar: número de presupuesto, CUIT/DNI del cliente, o código de artículo. El sistema buscará presupuestos que coincidan con cualquiera de estos criterios. |

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Fecha** | Fecha de creación del presupuesto |
| **Presupuesto** | Número del comprobante de presupuesto (ej.: PP-00001234) |
| **Documento Nro** | CUIT o DNI del cliente |
| **Cliente** | Nombre del cliente |
| **Estado** | Estado actual del presupuesto (Pendiente, Parcial, En proceso, etc.) |
| **Importe** | Monto total del presupuesto |
| **Pendiente Facturar** | SI / NO — indica si el presupuesto todavía tiene artículos pendientes de facturar |
| **PP Pedido** | Cantidad total pedida en el presupuesto |
| **PP Facturado** | Cantidad ya facturada de ese presupuesto |
| **PP Pendiente** | Cantidad que todavía falta facturar |
| **Facturar** | *(Solo si el sistema de reserva y aprobación está habilitado)* Indica si el presupuesto fue aprobado para facturar |
| **Usuario** | Usuario que creó el presupuesto |

---

## Acciones disponibles

| Acción | Cómo activarla | Qué hace |
|---|---|---|
| **Ver detalle** | Doble clic en la fila | Abre el detalle completo del presupuesto seleccionado |
| **Imprimir** | Botón de impresión en la fila | Imprime el comprobante de presupuesto |

---

## Paso a paso: Consultar el estado de un presupuesto

**1.** Ingresá en el campo de búsqueda:
   - El número del presupuesto (ej.: `PP-00001234`), o
   - El CUIT del cliente (ej.: `20-12345678-9`), o
   - El código de un artículo incluido en el presupuesto

**2.** El sistema filtra y muestra los presupuestos que coinciden.

**3.** Revisá las columnas **PP Facturado** y **PP Pendiente** para ver cuánto de ese presupuesto ya se facturó y cuánto queda pendiente.

**4.** Si querés ver el detalle completo, hacé doble clic en la fila del presupuesto.

---

## Preguntas frecuentes

**¿Por qué no aparece un presupuesto que creé?**
Los presupuestos con estado "Completo" (100% facturados) o "Rechazado", y los anulados, no aparecen en esta pantalla. Consultá el historial completo en la pantalla de Presupuestos (3.07).

**¿Qué significa el estado "Parcial"?**
Significa que el presupuesto fue facturado parcialmente: algunos artículos ya se facturaron pero otros están pendientes.

**¿Desde aquí puedo facturar el presupuesto?**
No directamente. Para facturarlo, accedé a la pantalla de **Facturación** (3.01) o **Facturar Presupuestos** (3.09) y buscá el presupuesto por número.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
