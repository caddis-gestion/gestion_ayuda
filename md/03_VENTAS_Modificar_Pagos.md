# 3.62 MODIFICAR PAGOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Modificar Pagos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Modificar Pagos** permite consultar y corregir los medios de pago registrados en una factura ya emitida. Es útil cuando hubo un error al cargar el número de autorización de una tarjeta, el número de cupón u otros datos del pago. Desde aquí podés:

- Buscar una factura por tipo y número
- Ver el detalle de los artículos facturados
- Ver y modificar los datos de la forma de pago registrada (especialmente el código de autorización)
- Consultar el estado en AFIP de comprobantes electrónicos

---

<img src="imagenes/pantalla_modificar_pagos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Modificar Pagos**

---

## Descripción general de la pantalla

La pantalla tiene un único panel con secciones de búsqueda, datos del comprobante, grilla de artículos, grilla de forma de pago y pie con el usuario.

---

## Sección de búsqueda

| Campo / Botón | Descripción |
|---|---|
| **FACTURA** | Tipo de comprobante + número de la factura a consultar |
| **Buscar** | Busca la factura e indica el resultado |
| **AFIP** | Consulta el estado del comprobante en AFIP (sólo para electrónicos) |
| **Estado** | Si la factura está cancelada, muestra **CANCELADA** en rojo. Si tiene nota de crédito asociada, muestra el número de NC en amarillo. |

---

## Datos del comprobante (sólo lectura)

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta que emitió la factura |
| **FECHA** | Fecha de la factura |
| **CLIENTE** | Nombre del cliente |
| **CUIT/DNI** | CUIT o DNI del cliente |
| **OBSERV** | Observaciones registradas en la factura |

---

## Grilla DETALLE — Artículos

Muestra los artículos incluidos en la factura:

| Columna | Descripción |
|---|---|
| Articulo | Descripción del artículo (con NSE si aplica) |
| Cantidad | Cantidad facturada |
| Importe | Importe total del ítem |

---

## Grilla FORMA DE PAGO

Muestra los medios de pago de la factura. La columna **CodAut** (Código de Autorización) es editable:

| Columna | Descripción |
|---|---|
| Tipo Pago | Medio de pago (Efectivo, Tarjeta, Cheque, etc.) |
| Pesos | Importe en pesos |
| Divisa | Importe en moneda extranjera (si aplica) |
| Entidad | Banco o tarjeta |
| Cuotas Plazo | Cuotas (tarjetas) o plazo en días (cta. cte.) |
| Tarjeta | Número de tarjeta |
| Cupon | Número de cupón |
| Fecha | Fecha del pago |
| **CodAut** | Código de autorización (editable — principal campo a modificar) |
| Lote | Número de lote |
| Chq/Boleta | Número de cheque o boleta de depósito |
| Gift_Card | Número de gift card |
| Recibo | Número de recibo |

**Acciones disponibles:**
- **Detalle:** Ver el detalle completo del ítem de pago

---

## Pie de pantalla

Muestra el **usuario** que registró el comprobante y la **fecha y hora** de la última actualización.

---

## Notas importantes

- Esta pantalla es principalmente para corregir el **Código de Autorización** de pagos con tarjeta que se ingresó mal al momento de la venta.
- No permite modificar el tipo de pago, los importes ni agregar o quitar medios de pago. Para eso sería necesario anular y rehacer la factura.
- El botón **AFIP** sólo aparece para comprobantes electrónicos (facturas A, B, C electrónicas).
