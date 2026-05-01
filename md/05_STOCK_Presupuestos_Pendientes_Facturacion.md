# 5.XX PRESUPUESTOS PENDIENTES DE FACTURACIÓN
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Presupuestos Pendientes Facturación

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Presupuestos Pendientes de Facturación** permite ver y gestionar los presupuestos que tienen stock reservado y están listos para ser facturados. Desde aquí podés:

- Consultar presupuestos con mercadería ingresada y pendientes de completar
- Aprobar presupuestos para habilitarlos a facturar
- Filtrar por cliente, artículo y número de ingreso

---

<img src="imagenes/pantalla_presupuestos_pendientes_facturacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Presupuestos Pendientes Facturación**

---

## Formulario

| Campo | Descripción |
|---|---|
| **DESDE** | Fecha de inicio del rango de consulta (por defecto: hace un año) |
| **HASTA** | Fecha de fin del rango de consulta (por defecto: hoy) |
| **CLIENTE** | Filtrar por cliente específico |
| **INGRESO** | Número de remito de ingreso asociado |
| **ARTICULO** | Selector de artículos con reserva pendiente en el período. Muestra el código, descripción y cantidad pendiente de cada artículo. Al cambiar aplica el filtro automáticamente. |

---

## Panel derecho — Grilla de presupuestos

Muestra los presupuestos con stock reservado no completados:

| Columna | Descripción |
|---|---|
| Fecha | Fecha del presupuesto |
| OC | Número de orden de compra relacionada |
| PP | Número del presupuesto |
| PP Reservado | Cantidad reservada para el presupuesto |
| Cliente | Nombre del cliente |
| PP Estado | Estado actual del presupuesto |
| Facturar | Indica si el presupuesto está aprobado para facturar (en amarillo) |

**Acciones disponibles:**
- **Aprobar:** Habilita el presupuesto para ser facturado
- **Borrar:** Anula la aprobación de facturación
- **Detalle:** Muestra el estado detallado del presupuesto por artículo
- **Imprimir:** Imprime el comprobante

---

## Notas importantes

- Solo se muestran presupuestos en estado **no Completo**, es decir, que aún tienen artículos pendientes de entrega.
- La columna **Facturar** (en amarillo) indica si el presupuesto fue aprobado para pasar a facturación.
- Un presupuesto debe estar aprobado para que pueda ser seleccionado al momento de facturar.
