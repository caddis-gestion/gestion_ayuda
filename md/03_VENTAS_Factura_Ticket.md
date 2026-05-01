# 3.04. Facturación por Ticket (POS)

**Ruta de acceso:** Módulo 3 → Ventas y Facturación → Facturación por Ticket (POS)

---

<img src="imagenes/pantalla_factura_ticket.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturación por Ticket (POS)** permite emitir comprobantes de venta en forma rápida desde el punto de venta (POS). Está diseñada para operar con agilidad en mostrador: el vendedor ingresa los artículos por código, aplica pagos y emite el comprobante en un solo flujo. Desde aquí podés:

- Emitir tickets, facturas B, A, X y otros tipos según la configuración del PDV
- Ingresar artículos por código o búsqueda
- Aplicar vouchers y registrar el medio de pago
- Acceder a la lista de artículos más vendidos (si está habilitada)

---

## Descripción general de la pantalla

La pantalla tiene dos paneles:
- **Panel izquierdo:** formulario de cabecera y entrada de artículos
- **Panel derecho:** detalle de los artículos ingresados en la factura

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta desde el cual se emite el comprobante |
| **VENDEDOR** | Vendedor asignado a la venta |
| **CLIENTE** | Cliente al que se emite el comprobante (opcional para tickets) |
| **FACTURA** | Tipo de comprobante. Los disponibles dependen de la empresa: TK, EB, B, IA, EA, EM, A, X (o EC, NDEC, X para monotributistas) |

### Ingreso de artículos

| Campo / Botón | Descripción |
|---|---|
| **Cantidad** | Cantidad del artículo a ingresar (por defecto: 1) |
| **Código** | Código del artículo. Al presionar Enter se ingresa automáticamente |
| **Buscar** | Abre el buscador de artículos con stock |
| **Promos** | Abre el buscador de promociones de venta disponibles |

### Sección "Lo más vendido" (opcional)

Si el parámetro correspondiente está activo, se muestra un panel con botones de acceso rápido a los artículos y promociones más vendidos. Hacé clic en el botón del artículo para agregarlo directamente sin escribir el código.

### Acciones de pago

| Botón | Descripción |
|---|---|
| **Voucher** | Aplica un voucher de descuento a la venta |
| **Pagos** | Abre el popup de medios de pago para registrar el cobro |
| **Solo Efectivo** | Checkbox que indica que el cobro es solo en efectivo (disponible si el PDV tiene caja configurada) |

Al pie del panel izquierdo se muestra la **lista de precios** activa para la venta.

---

## Paso a paso — Emitir un ticket/factura rápida

1. Seleccioná el **PDV** y el **VENDEDOR**
2. Opcionalmente, ingresá el **CLIENTE** (requerido para facturas A o B)
3. Seleccioná el **tipo de comprobante** (FACTURA)
4. Ingresá la **Cantidad** y el **Código** del artículo, luego presioná Enter — o usá **Buscar** para buscarlo
5. Repetí el paso 4 para cada artículo adicional
6. Si corresponde, hacé clic en **Voucher** para aplicar un descuento
7. Hacé clic en **Pagos** para registrar el medio de cobro
8. Confirmá el pago — el sistema emite el comprobante automáticamente

---

## Notas importantes

- Si se cambia el PDV mientras ya hay artículos ingresados, el sistema pregunta si se desean eliminar los datos cargados.
- El tipo de comprobante disponible depende de la configuración del PDV y el tipo de empresa (responsable inscripto vs. monotributista).
- Para clientes finales sin identificación, los tickets (TK) no requieren datos de cliente.
- La lista de precios se determina automáticamente según el cliente y el PDV seleccionados.
