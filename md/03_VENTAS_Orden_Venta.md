# 3.13 ORDEN DE VENTA
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Orden de Venta

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Orden de Venta** permite crear pedidos formales antes de emitir la factura. Desde aquí podés:

- Registrar pedidos de clientes con artículos y precios
- Crear órdenes de venta que luego se facturan desde la pantalla de Facturación (3.01)
- Gestionar pedidos con reserva de stock (según configuración)
- Ingresar artículos por código o por número de serie (NSE/IMEI) en forma masiva
- Vincular órdenes de venta a remitos para control de entregas

> ℹ️ Una **Orden de Venta** es un pedido comprometido pero **no facturado todavía**. Para convertirla en factura, accedé desde la pantalla de **Facturación** (3.01) usando el botón **Orden Venta**.

---

<img src="imagenes/pantalla_orden_venta.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Orden de Venta**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Formulario para datos del pedido (cliente, artículos, tipo de comprobante)
- **Panel derecho:** Grilla con los artículos ya ingresados en la orden

> ℹ️ El tipo de comprobante es siempre **OV** (Orden de Venta) y no puede cambiarse. Este comprobante no se envía a AFIP.

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de Venta desde donde se genera la orden. |
| **VENDEDOR** | Vendedor responsable del pedido. |
| **CLIENTE** | Cliente para quien se genera la orden. |

---

### Sección: Ingreso de artículos *(usuarios de gestión)*

Para usuarios con perfil de gestión/administración, la pantalla muestra un panel completo de ingreso de artículos:

| Campo/Botón | Descripción |
|---|---|
| **LISTA** | Lista de precios a aplicar en la orden. |
| **ARTÍCULO** | Código del artículo a ingresar. |
| **Buscar** | Abre una ventana emergente para buscar artículos por nombre, código o categoría. |
| **IMPORTE** | Precio unitario del artículo. Se completa automáticamente al seleccionarlo. |
| **CANTIDAD** | Cantidad solicitada. Presioná **Enter** o hacé clic en **Ingresar** para agregar el artículo. |
| **Ingresar** | Agrega el artículo con el importe y cantidad a la grilla. |
| **Promos** | Abre el buscador de promociones de venta disponibles. |
| **#Series** | Permite ingresar artículos masivamente por NSE (Número de Serie del Equipo / IMEI). |

---

### Sección: Remito *(usuarios sin perfil de gestión)*

Para usuarios sin perfil de gestión, la pantalla muestra solo el campo de remito:

| Campo | Descripción |
|---|---|
| **REMITO N°** | Número de remito a vincular con la orden de venta. Permite asociar una entrega de mercadería a esta orden. |

---

### Sección: Cobro y datos adicionales

| Campo/Botón | Descripción |
|---|---|
| **Voucher** | Permite aplicar un voucher de descuento al total de la orden. |
| **Pagos** | Registra formas de pago (adelanto o seña) sobre la orden de venta. |
| **Solo Efectivo** | Marca el cobro como efectivo con descuento automático. |
| **OBSERVACIONES** | Texto libre para notas del pedido (instrucciones de entrega, plazos, etc.). |

---

## Botones principales

| Botón | Qué hace |
|---|---|
| **Generar OV** (o **Facturar**) | Crea la orden de venta con los artículos ingresados. Genera el comprobante tipo OV. |
| **Cancelar** | Descarta todo lo ingresado y limpia el formulario. |

---

## Paso a paso: Crear una Orden de Venta

**Caso típico:** Un cliente realiza un pedido de artículos que no están en stock inmediato o que se entregarán en otro momento.

**1. Seleccionar PDV, Vendedor y Cliente**
- Elegí el **PDV** desde donde atendés el pedido.
- Seleccioná el **VENDEDOR** responsable.
- Buscá y seleccioná el **CLIENTE**.

**2. Elegir la lista de precios**
- En **LISTA**, seleccioná la lista de precios correspondiente al cliente.

**3. Ingresar los artículos del pedido**
- En **ARTÍCULO**, ingresá el código o buscalo con el botón **Buscar**.
- El precio se completa automáticamente.
- Ingresá la **CANTIDAD** y presioná **Enter** o hacé clic en **Ingresar**.
- El artículo aparece en la grilla.
- Repetí para cada artículo del pedido.
- Si los artículos se identifican por IMEI/NSE, usá el botón **#Series** para ingresarlos masivamente.

**4. Agregar observaciones** *(opcional)*
- Usá **OBSERVACIONES** para anotar instrucciones especiales del cliente (ej.: "Entregar el martes", "Llamar antes de despachar").

**5. Registrar adelanto** *(si el cliente paga una seña)*
- Hacé clic en **Pagos** y registrá el adelanto con el medio de pago correspondiente.

**6. Crear la Orden de Venta**
- Hacé clic en **Generar OV**.
- El sistema crea la orden con un número de comprobante OV (ej.: `OV-000045`).
- Este número se usará luego para facturar la orden.

---

## Paso a paso: Facturar una Orden de Venta existente

Una vez que el cliente confirma o retira el pedido, hay que convertir la OV en factura:

**1.** Accedé a la pantalla de **Facturación** (3.01 → `03_VENTAS_Facturacion.md`).

**2.** Hacé clic en el botón **Orden Venta** del panel izquierdo.

**3.** Buscá y seleccioná la Orden de Venta correspondiente.

**4.** El sistema importará automáticamente el cliente y los artículos de la OV.

**5.** Elegí el tipo de factura (A, B, EB, etc.) y registrá el cobro.

**6.** Hacé clic en **Facturar** para emitir la factura definitiva.

---

## Ingreso masivo por NSE (Número de Serie / IMEI)

Para equipos celulares u otros artículos con número de serie:

**1.** Hacé clic en el botón **#Series**.

**2.** En la ventana que se abre, ingresá (o pegá) los números de serie, uno por línea.

**3.** El sistema buscará cada equipo en el stock y los cargará automáticamente en la grilla.

> ℹ️ Si un NSE no se encuentra en el stock del PDV, el sistema lo informará pero continuará procesando los demás.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Elija un PDV" | Se intentó crear la OV sin seleccionar PDV | Seleccioná el PDV primero |
| "Controle el Artículo" | El campo artículo está vacío | Ingresá o buscá el artículo |
| "Controle la Cantidad" | La cantidad es cero o inválida | Ingresá una cantidad mayor a cero |
| El botón "Orden Venta" no aparece en Facturación | El usuario no tiene perfil de gestión | Consultá con el administrador del sistema |

---

## Preguntas frecuentes

**¿La Orden de Venta reserva el stock?**
Depende de la configuración del sistema. En algunos casos reserva el stock para no venderlo a otros clientes mientras el pedido está pendiente. Consultá con el administrador.

**¿Cuánto tiempo queda válida una OV?**
Las órdenes de venta no vencen automáticamente. Permanecen pendientes hasta que se facturan o se cancelan manualmente.

**¿Puede un operador de caja crear órdenes de venta?**
El acceso y las funciones disponibles dependen del perfil del usuario. Los usuarios sin perfil de gestión ven una versión simplificada de la pantalla.

**¿Cómo sé el número de la OV para facturarla después?**
El sistema asigna automáticamente un número (ej.: OV-000045) al crear la orden. Este número también aparece en el listado de órdenes pendientes accesible desde la pantalla de Facturación.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
