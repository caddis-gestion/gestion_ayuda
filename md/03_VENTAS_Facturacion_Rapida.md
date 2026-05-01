# 3.02 FACTURACIÓN RÁPIDA (TICKETS)
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación Rápida

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturación Rápida** está diseñada para agilizar las ventas en mostrador de alto volumen, especialmente para tickets y comprobantes sin datos fiscales del cliente. Desde aquí podés:

- Emitir tickets, facturas y comprobantes en forma rápida sin completar datos del cliente
- Ingresar artículos directamente por código sin seleccionar lista de precios
- Aplicar descuentos con vouchers y promociones
- Registrar el cobro con distintas formas de pago
- Acceder rápidamente a los artículos más vendidos con un solo clic

> ℹ️ Para ventas que requieren datos fiscales completos (Factura A, cliente con CUIT, cuenta corriente), usá la pantalla de **Facturación** (3.01 → `03_VENTAS_Facturacion.md`).

---

<img src="imagenes/pantalla_facturacion_rapida.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación Rápida** (aparece también como "Tickets" en el menú)

---

## Descripción general de la pantalla

La pantalla tiene un diseño simplificado respecto a la facturación estándar:

- **Panel izquierdo:** Formulario reducido (PDV, vendedor, cliente, tipo de comprobante e ingreso de artículos)
- **Panel derecho:** Grilla con el detalle de los artículos ya ingresados en el comprobante actual
- **Sección "Lo más vendido"** *(opcional)*: Botones de acceso rápido a los artículos con mayor rotación, si está configurada para el PDV

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de Venta desde donde se emite el comprobante. Se toma automáticamente del último PDV usado (guardado en cookie). |
| **VENDEDOR** | Vendedor que realiza la venta. Se filtra automáticamente según el PDV seleccionado. |
| **CLIENTE** | Cliente al que se emite el comprobante. Opcional: si no se selecciona, el sistema usa "Consumidor Final". |
| **FACTURA** | Tipo de comprobante (ver tabla más abajo). |

> ℹ️ La **FECHA** se completa automáticamente con el día de hoy y no se muestra en el formulario. La **LISTA** de precios se asigna automáticamente y se muestra como referencia en la parte inferior del formulario.

---

### Tipos de comprobante disponibles

Los comprobantes disponibles dependen de la configuración del PDV y de la empresa:

| Código | Nombre | Cuándo se usa |
|---|---|---|
| **TK** | Ticket | Venta rápida a consumidor final (sin datos fiscales) |
| **B** | Factura B | Cliente consumidor final o monotributista |
| **EB** | Factura B (Electrónica) | Igual que B, emitida electrónicamente por AFIP |
| **A** | Factura A | Cliente con IVA Responsable Inscripto |
| **IA** | Factura A (Interna) | Factura A de uso interno |
| **EA** | Factura A (Electrónica) | Igual que A, emitida electrónicamente por AFIP |
| **EM** | Factura M (Electrónica) | Para ciertas categorías fiscales especiales |
| **X** | Comprobante Interno | Para movimientos internos o sin facturación fiscal |
| **EC** | Comprobante Electrónico | Solo para empresas con sistema MTO |
| **NDEC** | Nota de Débito EC | Solo para empresas con sistema MTO |
| **NDX** | Nota de Débito X | Solo para empresas con sistema MTO |

---

## Sección: Ingreso de artículos

| Campo/Botón | Descripción |
|---|---|
| **CANTIDAD** | Cantidad del artículo a ingresar. Se completa antes del código. |
| **CODIGO** | Código del artículo. Al presionar **Enter** se ejecuta automáticamente el ingreso (equivale a hacer clic en **Ingresar**). |
| **Buscar** | Abre una ventana emergente para buscar artículos por nombre, código o categoría en el stock del PDV. |
| **Promos** | Abre un buscador de promociones de venta disponibles (combos con precio especial). |
| **Ingresar** | Agrega el artículo con la cantidad indicada a la grilla del comprobante. |

---

## Sección: Lo más vendido *(opcional)*

Si el PDV tiene habilitada esta sección, aparece una grilla de botones con los artículos de mayor rotación. Al hacer clic en cualquier botón, el artículo se agrega automáticamente al comprobante con cantidad 1.

Esta sección es configurable por el administrador del sistema y puede no aparecer en todos los puntos de venta.

---

## Sección: Cobro

| Campo/Botón | Descripción |
|---|---|
| **Voucher** | Permite aplicar un voucher de descuento o gift card al total del comprobante. |
| **Pagos** | Abre la ventana de registro de medios de pago. Debe usarse antes de emitir. |
| **Solo Efectivo** | Marca el comprobante como cobrado en efectivo con descuento automático por pago en efectivo. Solo aparece si el PDV tiene caja configurada. |

---

## Botones principales

| Botón | Qué hace |
|---|---|
| **Facturar** | Emite el comprobante y lo envía a AFIP si corresponde. Debe haberse registrado el pago previamente (con **Pagos** o tildando **Solo Efectivo**). |
| **Cancelar** | Descarta todo lo ingresado y limpia el formulario. Pide confirmación antes de ejecutarse. |

---

## Paso a paso: Emitir un ticket rápido

**Caso típico:** Venta de mostrador a consumidor final, cobrado en efectivo.

**1. Verificar el PDV y Vendedor**
- El PDV se carga automáticamente. Verificá que es el correcto.
- Seleccioná el vendedor en el campo **VENDEDOR**.

**2. Elegir el tipo de comprobante**
- En el campo **FACTURA**, seleccioná **TK** para ticket o **EB** para Factura B electrónica.
- Si el cliente tiene datos fiscales, seleccionalo en **CLIENTE** (el sistema asignará el tipo automáticamente).

**3. Ingresar los artículos**
- En **CANTIDAD**, ingresá la cantidad del artículo.
- En **CODIGO**, ingresá el código del artículo y presioná **Enter**.
- El artículo aparece en la grilla del panel derecho.
- Repetí para cada artículo adicional.
- Si no sabés el código, hacé clic en **Buscar** para buscarlo por nombre.

**4. Registrar el cobro**
- Si el cobro es en efectivo: tildá **Solo Efectivo** (aplica descuento automático si está configurado).
- Para otros medios de pago: hacé clic en **Pagos**, registrá los medios y hacé clic en **Guardar**.

**5. Emitir el comprobante**
- Hacé clic en **Facturar**.
- El sistema emite el comprobante y lo registra.

---

## Paso a paso: Usar los botones de "Lo más vendido"

Si la sección **Lo más vendido** está visible:

**1.** Asegurate de tener el PDV y vendedor seleccionados.

**2.** Hacé clic directamente en el botón del artículo que querés agregar.

**3.** El artículo se agrega al comprobante con cantidad 1. Si necesitás más unidades, podés modificar la cantidad en la grilla del panel derecho o ingresar el artículo nuevamente con la cantidad deseada.

---

## Diferencias con la pantalla de Facturación estándar (3.01)

| Característica | Facturación Rápida | Facturación Estándar |
|---|---|---|
| Campo FECHA visible | No (automático) | Sí (editable) |
| Campo LISTA visible | No (automático, se muestra como info) | Sí (seleccionable) |
| Campo CAJA | No | Sí (si el PDV tiene caja) |
| Campo ARTÍCULO + IMPORTE separados | No | Sí |
| Botón "Lo más vendido" | Sí (si está configurado) | No |
| Botón "Multiple" (masivo) | No | Sí |
| Botón "Orden Venta" | No | Sí |
| Botón "Reparaciones" | No | Sí |
| Campo OBSERVACIONES | No | Sí |

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Elija un PDV" | Se intentó ingresar artículo sin PDV | Verificá que el PDV esté seleccionado |
| "Controle el Artículo" | El campo código está vacío | Ingresá o buscá el código del artículo |
| "Controle la Cantidad" | La cantidad es cero o inválida | Ingresá una cantidad mayor a cero |
| "Ingrese un Item..." | Se intentó abrir Pagos sin artículos | Ingresá al menos un artículo antes |
| "Al cambiar de lista se cancela la factura" | El PDV cambió implícitamente la lista | Confirmá el cambio o terminá el comprobante actual |

---

## Preguntas frecuentes

**¿Por qué no veo el campo FECHA?**
En la facturación rápida, la fecha se asigna automáticamente al día de hoy para agilizar el proceso. No es necesario ingresarla manualmente.

**¿Puedo emitir Factura A desde esta pantalla?**
Sí, si el PDV tiene habilitado el tipo **A** o **EA**, podés seleccionarlo. Pero necesitarás seleccionar el cliente con los datos fiscales correspondientes en el campo **CLIENTE**.

**¿Cómo sé qué lista de precios se está aplicando?**
En la parte inferior del formulario se muestra el nombre de la lista activa (ej.: "Lista: MINORISTA"). Esta lista se asigna automáticamente según el PDV y el cliente.

**¿Por qué no aparece la sección "Lo más vendido"?**
Esta sección es opcional y se activa por configuración del administrador del sistema para cada PDV. Si no aparece, el PDV no tiene esa función habilitada.

---

## Referencia rápida de botones y campos

| Elemento | Tipo | Acción / Descripción |
|---|---|---|
| PDV | Lista desplegable | Selecciona el punto de venta |
| VENDEDOR | Lista desplegable | Selecciona el vendedor |
| CLIENTE | Buscador | Selecciona el cliente (opcional) |
| FACTURA (tipo) | Lista desplegable | Tipo de comprobante |
| CANTIDAD | Número | Cantidad del artículo |
| CODIGO | Texto | Código del artículo (Enter = Ingresar) |
| Buscar | Botón | Abre buscador de artículos por nombre |
| Promos | Botón | Buscador de promociones de venta |
| Ingresar | Botón | Agrega artículo al comprobante |
| Voucher | Botón | Aplica voucher de descuento |
| Pagos | Botón | Registra formas de pago |
| Solo Efectivo | Casilla | Cobro en efectivo con descuento automático |
| Facturar | Botón principal | Emite el comprobante |
| Cancelar | Botón | Descarta todo y limpia el formulario |

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
