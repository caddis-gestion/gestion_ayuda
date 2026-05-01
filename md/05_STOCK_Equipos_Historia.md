# 5.38 EQUIPOS — HISTORIA DE STOCK
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Historia

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Historia** permite consultar el historial completo de movimientos de un equipo individual, buscándolo por número de serie (NSE o IMEI). Desde aquí podés:

- Ver todos los movimientos de un equipo desde su ingreso hasta su venta o situación actual
- Consultar los datos del equipo (modelo, gama, estado, almacén)
- Ver los comprobantes del proveedor asociados al equipo
- Acceder a las facturas de venta del equipo

---

<img src="imagenes/pantalla_equipos_historia.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Historia**

---

## Formulario — Búsqueda

| Campo | Descripción |
|---|---|
| **SERIE#** | Número de serie (NSE/IMEI) del equipo a consultar |

---

## Panel izquierdo — Datos del equipo

Una vez encontrado el equipo, se muestran dos secciones:

**Datos del equipo:**

| Campo | Descripción |
|---|---|
| MODELO | Marca y modelo del equipo |
| CODIGO | Código interno del artículo |
| GAMA | Gama del equipo |
| ESTADO | Estado actual: ACTIVADO o el estado de stock |
| SAP ID | ID SAP (solo en integraciones con operadoras) |
| TIPO | Tipo de contrato/equipo |
| INGRESO | Fecha de ingreso al stock |
| VENCE | Fecha de vencimiento |
| ALMACEN | Almacén actual |
| BODEGA | Bodega interna |
| FC NRO | Factura de venta emitida (con botón **Buscar**) |
| FACTURADO | Indica si el equipo fue vendido (SI/NO) |

**Comprobantes del proveedor:**

| Campo | Descripción |
|---|---|
| REMITO | Número de remito del proveedor |
| PEDIDO | Número de pedido del proveedor |
| FACTURA | Factura del proveedor (con botón **Buscar**) |
| FC.FECHA | Fecha de la factura del proveedor |
| DOC ASOC | Documento asociado (operadoras) |
| DESPACHO | Número de despacho de importación |

---

## Panel derecho — Historial de movimientos

| Columna | Descripción |
|---|---|
| Id | Identificador del movimiento |
| Movimiento | Tipo de movimiento (ingreso, transferencia, venta, etc.) |
| POS | Punto de venta/depósito de destino |
| Fecha | Fecha del comprobante |
| # Interno | Número del comprobante interno |
| Remito | Número de remito |
| Vendedor | Vendedor involucrado |
| Mov Fecha | Fecha del movimiento |
| Usuario | Usuario que realizó el movimiento |
| Update | Fecha de última actualización |

**Acciones:**
- **Detalle:** Abre el detalle del comprobante del movimiento

---

## Notas importantes

- El sistema busca el historial tanto en la tabla activa como en el historial archivado (si existe).
- El campo **SERIE#** puede ingresarse en formato decimal o hexadecimal; el sistema lo convierte automáticamente.
- Esta pantalla es ideal para rastrear el ciclo de vida completo de un equipo.
