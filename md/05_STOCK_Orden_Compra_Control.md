# 5.21 ORDEN DE COMPRA — CONTROL
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Orden de Compra Control

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Orden de Compra Control** permite consultar el estado detallado de un comprobante de compras o pedidos: Órdenes de Compra (OC), Pedidos/Presupuestos (PP) y Pedidos de Mercadería (PM). Desde aquí podés:

- Buscar un comprobante por tipo y número
- Ver su estado actual (Pendiente, Completo, Aprobado, Anulado)
- Consultar los pedidos, facturas, órdenes de compra y remitos de ingreso relacionados
- Ver el estado de cantidades (pedido, recibido, descartado, pendiente, facturado)

---

<img src="imagenes/pantalla_orden_compra_control.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Orden de Compra Control**

---

## Formulario

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de comprobante: OC (Orden de Compra), PP (Pedido/Presupuesto) o PM (Pedido de Mercadería) |
| **NÚMERO** | Número del comprobante a consultar |
| Botón **Consultar** | Busca el comprobante |
| Botón **Detalle** | Abre el detalle completo del comprobante |
| **ESTADO** (indicador) | Estado actual del comprobante (Completo, Aprobado, Pendiente, ANULADO), en color: verde/amarillo/rojo |
| **RELACIONADA** (indicador) | Muestra la OC relacionada (ARG o USA) cuando corresponde |

---

## Panel de detalle — Orden de Compra (OC)

Al buscar una OC, se muestran tres secciones:

**PEDIDOS Y PRESUPUESTOS** — comprobantes que originaron esta OC:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Cantidad pedida |
| Tipo | Tipo de comprobante origen |
| Nro | Número del comprobante |
| Fecha | Fecha del comprobante |
| Cliente/Usuario | Cliente o usuario que generó el pedido |

**ESTADO DE CANTIDADES** — seguimiento de cantidades por artículo:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Cantidad de la OC |
| Recibido | Cantidad ya recibida |
| Descartado | Cantidad descartada |
| Pendiente | Cantidad aún pendiente de recibir (en amarillo) |
| Facturado | Cantidad ya facturada |
| Articulo | Descripción del artículo |

**REMITOS DE INGRESOS** — ingresos de mercadería contra esta OC:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Cantidad recibida en el remito |
| Fecha | Fecha del remito |
| Remito | Número de remito de ingreso |
| Proveedor | Nombre del proveedor/depósito de origen |

---

## Panel de detalle — Presupuesto (PP)

Al buscar un PP, se muestran cuatro secciones: **FACTURAS**, **ORDENES DE COMPRA**, **ESTADO DE CANTIDADES** y **REMITOS DE INGRESOS**, con columnas equivalentes a las descriptas para OC.

---

## Panel de detalle — Pedido de Mercadería (PM)

Al buscar un PM, se muestran tres secciones: **ORDENES DE COMPRA**, **ESTADO DE CANTIDADES** y **REMITOS DE INGRESOS**.

---

## Notas importantes

- El sistema marca automáticamente una OC como "Completa" cuando todas las cantidades fueron recibidas.
- Los estados se visualizan con color: verde = Completo, amarillo = Aprobado, rojo = otros.
- Usá el botón **Detalle** para ver el comprobante completo con todos sus campos.
