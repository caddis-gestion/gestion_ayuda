# 3.54 FACTURACIÓN ABONOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturacion Abonos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturación Abonos** permite procesar la facturación mensual de los abonos configurados en el sistema. Muestra todos los abonos activos e inactivos con su estado de facturación y permite emitir, imprimir o reenviar las facturas correspondientes. Desde aquí podés:

- Ver todos los abonos y su estado (activo/inactivo, facturado/pendiente)
- Facturar individualmente un abono del período actual
- Imprimir el último comprobante emitido para un abono
- Reenviar por mail el último comprobante de un abono

---

<img src="imagenes/pantalla_facturacion_abonos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturacion Abonos**

---

## Descripción general de la pantalla

La pantalla muestra únicamente una grilla con todos los abonos. No tiene formulario de carga en panel izquierdo.

---

## Grilla de abonos

| Columna | Descripción |
|---|---|
| Estado | ACTIVO o INACTIVO |
| Modo | MANUAL o AUTOMATICO |
| Cliente | Nombre del cliente |
| Empresa | Empresa que factura |
| Importe total | Importe total del abono (con IVA) |
| Tipo FC | Tipo de comprobante a emitir (A, B, C, etc.) |
| Condicion | Condición de pago asignada |
| PDV | Punto de venta de facturación |
| Frecuencia | MENSUAL |
| Inicio | Fecha de inicio del abono |
| Fecha Ultima FC | Fecha de la última factura emitida para este abono |
| Caducidad | Fecha de vencimiento del abono |
| Error | Mensaje del último error de emisión (si lo hubiera) |

**Acciones disponibles:**

| Botón | Descripción |
|---|---|
| **Facturar abono** | Emite la factura del período actual para el abono seleccionado |
| **Imprimir último comprobante** | Imprime el último comprobante emitido |
| **Enviar último comprobante por mail** | Reenvía el último comprobante al cliente por e-mail |

---

## Notas importantes

- Para configurar o modificar un abono, usá la pantalla **Definir Abonos** (3.47).
- La columna **Error** muestra el mensaje de error si la última emisión falló (por ejemplo, por problemas con AFIP o datos incompletos del cliente).
- Los abonos con estado **INACTIVO** no se facturan aunque aparezcan en la grilla.
- La **Fecha Ultima FC** permite verificar si el abono ya fue facturado en el período corriente.
