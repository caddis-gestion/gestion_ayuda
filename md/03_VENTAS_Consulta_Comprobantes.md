# 3.30 CONSULTA COMPROBANTES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Consulta Comprobantes

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Consulta Comprobantes** permite buscar cualquier comprobante del sistema (facturas, tickets, notas de crédito, presupuestos, órdenes de compra, etc.) por tipo y número para ver su detalle completo. Desde aquí podés:

- Buscar un comprobante por tipo y número
- Ver el detalle completo: artículos, importes, formas de pago
- Consultar si el comprobante fue anulado o si fue facturado (en caso de presupuestos)
- Ver los comprobantes asociados (notas de crédito, remitos, etc.)
- Verificar el estado en AFIP (para comprobantes electrónicos)
- Imprimir las garantías de los equipos incluidos en la factura

---

<img src="imagenes/pantalla_consulta_comprobantes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Consulta Comprobantes**

También se puede acceder directamente desde otras pantallas haciendo doble clic en un comprobante de la grilla (se abre en una ventana emergente).

---

## Descripción general de la pantalla

La pantalla tiene un único panel con toda la información del comprobante buscado, organizada en secciones.

---

## Sección de búsqueda

| Campo | Descripción |
|---|---|
| **FACTURA** | Selector de tipo de comprobante (TK, B, A, C, NC, PP, OC, etc.) + campo de número |
| **Buscar** | Botón para buscar el comprobante |
| **AFIP** | Botón para consultar el estado del comprobante en AFIP (sólo para comprobantes electrónicos) |

---

## Datos del comprobante encontrado

Una vez encontrado el comprobante, se muestran sus datos de cabecera (todos en modo lectura):

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de emisión del comprobante. Si está anulado, se muestra la leyenda **ANULADO** en rojo. Si fue reemplazado (convertido), se muestra **FACTURADO** en amarillo. |
| **CLIENTE / PROVEEDOR** | Nombre y CUIT del cliente (o proveedor, en caso de Orden de Compra) |
| **PDV** | Punto de venta que emitió el comprobante |
| **VENDEDOR** | Vendedor asignado al comprobante |
| **OBSERV.** | Observaciones registradas al momento de la emisión |
| **Garantías** | Botón que aparece si el comprobante tiene garantías registradas. Permite imprimirlas. |

---

## Grilla de artículos

Muestra todos los artículos incluidos en el comprobante:

| Columna | Descripción |
|---|---|
| Código | Código del artículo |
| Artículo | Descripción. Para equipos con NSE: muestra el número de serie + descripción del equipo. |
| Cantidad | Cantidad facturada |
| Importe | Importe total del ítem |
| Tipo | Tipo de artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Variante | Variante del artículo (si aplica) |

> Para presupuestos (PP, PM) y órdenes de compra (OC), la grilla de artículos no muestra importes, sólo cantidades.

---

## Grilla de pago

Muestra las formas de pago utilizadas en el comprobante (sólo para facturas y tickets, no para presupuestos ni OC):

| Columna | Descripción |
|---|---|
| Tipo Pago | Medio de pago (Efectivo, Tarjeta, etc.) |
| Importe | Monto en pesos |
| Divisa | Monto en moneda extranjera (si aplica) |
| Plataforma | Plataforma digital (ej. MercadoPago) |
| Entidad | Banco o tarjeta específica |
| Cuotas | Cantidad de cuotas (para tarjetas) |

---

## Grilla de comprobantes asociados

Muestra los comprobantes relacionados al que se está consultando:

| Columna | Descripción |
|---|---|
| Fecha | Fecha del comprobante asociado |
| Tipo | Tipo (NC, ND, R, IR, etc.) |
| Número | Número del comprobante |
| Estado | Vigente, Anulado, o Facturado |
| Observaciones | Notas del comprobante asociado |

Ejemplos: si se consulta una factura que tiene una nota de crédito, la NC aparece aquí. Si se consulta un presupuesto que fue facturado, la factura aparece aquí.

---

## Pie de pantalla

Muestra el **usuario** que registró el comprobante y la **fecha y hora** de la última actualización.

---

## Notas importantes

- Esta pantalla es **sólo de consulta** — no se puede modificar ningún dato desde aquí.
- Funciona tanto como pantalla independiente como **popup** abierto desde otras pantallas del sistema.
- Para buscar por tipo de comprobante, el selector incluye todos los tipos: TK, B, A, C, M, X, NC, ND, PP, PM, OC, R, IR, OV, etc.
