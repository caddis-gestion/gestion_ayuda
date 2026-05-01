# 3.11 FACTURAR REMITOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Remitos (Facturar Remitos)

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturar Remitos** permite convertir remitos de entrega en facturas de venta. Desde aquí podés:

- Buscar remitos pendientes de facturación para un cliente específico
- Agrupar uno o más remitos en una sola factura
- Emitir facturas A o B a partir de remitos ya entregados
- Aplicar condiciones de pago (plazos) con intereses automáticos
- Registrar el cobro y emitir el comprobante final

> ℹ️ Un **remito** es un comprobante de entrega de mercadería sin precio. Se usa cuando se entrega el producto antes de cobrar (ventas a cuenta corriente o entregas parciales). Esta pantalla es el paso siguiente: **convertir esas entregas en una factura**.

---

<img src="imagenes/pantalla_remitos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Remitos**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Formulario para seleccionar el cliente, buscar los remitos y configurar la factura
- **Panel derecho:** Grilla con el detalle de los artículos de los remitos seleccionados

---

## Campos del formulario

### Sección: Cliente y Remitos

| Campo/Botón | Descripción |
|---|---|
| **CLIENTE** | Selector del cliente a facturar. Solo muestra clientes que tienen **remitos pendientes de facturación** (remitos tipo R, IR u OV, con precio cero y no generados por canales web). |
| **REMITOS** | Campo de solo lectura que muestra los números de remito seleccionados para facturar. |
| **N° de remito** | Campo de ingreso manual del número de remito. |
| **BuscarRemito** | Botón para buscar y seleccionar remitos pendientes del cliente elegido. Abre un listado con todos los remitos disponibles para ese cliente. |

---

### Sección: Datos de la Factura

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de emisión de la factura. Se completa automáticamente con el día de hoy. |
| **LISTA** | Lista de precios a aplicar en la factura. Al cambiar la lista, los precios en la grilla se recalculan automáticamente. |
| **FACTURA** | Tipo de comprobante a emitir. Disponibles: IA, EA, A, PA, EB, EM, TK, B, IV, X (o EC/NDX para empresas con sistema MTO). |
| **PLAZO** | Condición de pago. El sistema muestra los plazos disponibles junto con el porcentaje de interés configurado (ej.: "30 días — 2%"). Al elegir un plazo con interés, el sistema lo aplica automáticamente al total. |

---

### Sección: Cobro y datos adicionales

| Campo/Botón | Descripción |
|---|---|
| **Voucher** | Permite aplicar un voucher de descuento al total de la factura. |
| **Pagos** | *(Solo para empresas que tienen habilitada esta opción)* Abre la ventana de registro de medios de pago. |
| **Solo Efectivo** | Marca la factura como cobrada exclusivamente en efectivo. |
| **OBSERVACIONES** | Texto libre para agregar notas adicionales a la factura. |

---

## Botones principales

| Botón | Qué hace |
|---|---|
| **Facturar** | Emite la factura a partir de los remitos seleccionados y los envía a AFIP si corresponde. |
| **Cancelar** | Descarta todo lo ingresado y limpia el formulario. |

---

## Paso a paso: Facturar un remito

**Caso típico:** Un cliente tiene uno o más remitos entregados y se va a facturar al fin del mes.

**1. Seleccionar el cliente**
- En el campo **CLIENTE**, buscá y seleccioná al cliente.
- El selector solo muestra clientes con remitos pendientes de facturación.

**2. Buscar los remitos**
- Hacé clic en el botón **BuscarRemito**.
- Se abrirá un listado con todos los remitos pendientes del cliente.
- Seleccioná el o los remitos que querés incluir en la factura.
- Los números de remito se cargan en el campo **REMITOS** y los artículos aparecen en la grilla del panel derecho.

**3. Verificar los datos de la factura**
- Confirmá la **FECHA** (por defecto: hoy).
- Verificá la **LISTA** de precios. Si necesitás cambiarla, los precios se recalcularán automáticamente.
- Seleccioná el tipo de comprobante en **FACTURA** (IA, A, EB, B, etc.).

**4. Configurar el plazo de pago** *(si aplica)*
- En **PLAZO**, elegí la condición de pago acordada con el cliente.
- Si el plazo tiene interés configurado (ej.: "60 días — 3%"), el sistema lo aplicará automáticamente.

**5. Agregar observaciones** *(opcional)*
- Usá el campo **OBSERVACIONES** para notas adicionales.

**6. Registrar el cobro** *(si aplica)*
- Si el pago se realiza en el momento: hacé clic en **Pagos** o tildá **Solo Efectivo**.
- Si es a cuenta corriente: elegí el plazo en **PLAZO** y la factura quedará como deuda del cliente.

**7. Emitir la factura**
- Hacé clic en **Facturar**.
- El sistema convierte los remitos en factura, actualiza los precios y envía a AFIP si corresponde.

---

## Intereses por plazo de pago

Cuando se selecciona un **PLAZO** con interés configurado:

1. El sistema toma el total de los artículos de los remitos
2. Aplica el porcentaje de interés configurado para ese plazo
3. El total de la factura se incrementa automáticamente con el interés

> Ejemplo: Remitos por $100.000, plazo "30 días" con 2% de interés → Factura por $102.000.

Los plazos y sus tasas de interés los configura el administrador del sistema.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| El selector de cliente no muestra algunos clientes | El cliente no tiene remitos pendientes | Verificá si los remitos ya fueron facturados o si son de otro tipo |
| "No se encontraron remitos" | El cliente seleccionado no tiene remitos pendientes | Verificá en la pantalla de búsqueda de remitos (3.12) |
| Los precios en la grilla son cero | El artículo no tiene precio en la lista seleccionada | Cambiá la lista o actualizá el precio del artículo |
| "Elija un comprobante" | No se seleccionó el tipo de factura | Seleccioná el tipo en el campo FACTURA |

---

## Preguntas frecuentes

**¿Puedo incluir remitos de diferentes fechas en una sola factura?**
Sí, podés seleccionar múltiples remitos del mismo cliente (de distintas fechas) y agruparlos en una única factura.

**¿Qué tipos de remito se pueden facturar desde esta pantalla?**
Solo los remitos tipo **R** (Remito), **IR** (Ingreso de Remito) y **OV** (Orden de Venta) que tienen precio cero y no fueron generados por canales de e-commerce.

**¿Qué pasa con el stock al facturar un remito?**
El stock ya fue descontado cuando se emitió el remito. La factura solo genera el comprobante fiscal; no mueve stock nuevamente.

**¿Puedo facturar un remito sin conocer el número?**
Sí. Con el botón **BuscarRemito** podés ver todos los remitos pendientes del cliente seleccionado y elegirlos desde la lista.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
