# FACTURACIÓN MINORISTA
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturación Minorista** es donde se realizan todas las ventas del negocio. Desde aquí podés:

- Emitir facturas, tickets, remitos y comprobantes de venta
- Ingresar los artículos vendidos uno a uno o en forma masiva
- Registrar el cobro con distintas formas de pago
- Aplicar descuentos, vouchers y promociones automáticamente
- Enviar la factura a ARCA/AFIP de forma electrónica

---

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación**

---

## Descripción general de la pantalla

![Pantalla Facturación](imagenes/pantalla_facturacion.png)

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Formulario de datos de la factura (cliente, artículos, formas de pago)
- **Panel derecho:** Grilla con el detalle de los artículos ya ingresados en la factura actual

---

## Campos del formulario

### Sección: Datos principales

| Campo | Descripción |
|---|---|
| **PDV** | Punto de Venta desde donde se emite la factura. Determina qué artículos están disponibles y qué comprobantes se pueden usar. **Si se cambia el PDV con artículos ya ingresados, se cancelará la factura actual.** |
| **VENDEDOR** | Vendedor que realiza la venta. Se filtra automáticamente según el PDV seleccionado. |
| **FECHA** | Fecha de emisión del comprobante. Se completa automáticamente con la fecha del día. |
| **CAJA** | Caja asociada a la factura (si el PDV tiene caja configurada). |
| **CLIENTE** | Cliente al que se le emite la factura. Si no se elige uno, se usará "Consumidor Final". Al cambiar el cliente se reinicia la factura completa. |
| **EMITIR EN** | Moneda en que se emite la factura (ARS o dólares). Solo aparece si la empresa tiene habilitada la facturación en divisas. Incluye un campo de **cotización** del día. |
| **FACTURA** | Tipo de comprobante (ver tabla más abajo) y número de factura. El número se completa automáticamente, pero puede editarse manualmente si es necesario. |

---

### Tipos de comprobante disponibles

Los comprobantes disponibles dependen de la configuración del PDV y del cliente. Los más comunes son:

| Código | Nombre | Cuándo se usa |
|---|---|---|
| **TK** | Ticket | Venta rápida a consumidor final (sin datos fiscales) |
| **A** | Factura A | Cliente con IVA Responsable Inscripto (RI) |
| **B** | Factura B | Cliente con IVA Consumidor Final o Monotributista |
| **EA** | Factura A (Electrónica) | Igual que A, pero emitida por AFIP electrónicamente |
| **EB** | Factura B (Electrónica) | Igual que B, pero emitida por AFIP electrónicamente |
| **EE** | Factura E | Para exportaciones |
| **EM** | Factura M | Para ciertas categorías fiscales especiales |
| **PA** | Presupuesto A | Presupuesto para cliente RI |
| **PB** | Presupuesto B | Presupuesto para consumidor final |
| **RM** | Remito T3 (Movistar) | Para distribuidores de Movistar, requiere datos de activación |
| **IRM** | Remito IRM (Movistar) | Variante del remito Movistar |
| **M** | Factura M | Régimen especial |
| **X** | Comprobante Interno | Para movimientos internos o sin facturación fiscal |
| **P** | Pedido | Para generar pedidos sin facturar |
| **IV** | Factura Interna | Para uso interno |
| **RC** | Recibo de Seña | Se habilita cuando hay una seña registrada |
| **NDEA / NDEB / NDPA / NDPB / NDX** | Notas de Débito | Para ajustes a favor de la empresa |

> 💡 El sistema sugiere automáticamente el tipo de comprobante correcto según el IVA del cliente al momento de seleccionarlo.

---

### Sección: Ingreso de artículos

| Campo | Descripción |
|---|---|
| **LISTA** | Lista de precios a aplicar. Se asigna automáticamente según el cliente o el PDV. **Si se cambia la lista, se cancelará la factura actual.** |
| **ARTÍCULO** | Código del artículo a ingresar. Podés tipear el código directamente o usar el botón **Buscar** para buscarlo por nombre o categoría. |
| **IMPORTE** | Precio unitario del artículo (con IVA incluido). Se completa automáticamente al buscar el artículo. En algunos casos puede estar bloqueado para edición según la configuración. |
| **CANTIDAD** | Cantidad a vender. Podés presionar **Enter** para confirmar el ingreso del artículo. |

#### Botones de ingreso de artículos

| Botón | Qué hace |
|---|---|
| **Buscar** | Abre una ventana para buscar artículos en el stock del PDV por nombre, código o categoría. |
| **Ingresar** (o tecla Enter) | Agrega el artículo con el importe y la cantidad indicados a la factura. |
| **Multiple** | Permite ingresar varios artículos a la vez. Se abre una ventana donde podés pegar una lista con el formato: `CODIGO;CANTIDAD` (uno por línea). |
| **#Series** | Permite ingresar artículos masivamente por NSE (Número de Serie del Equipo / IMEI). Igual que Múltiple pero por número de serie. |
| **Promos** | Abre un buscador de promociones de venta disponibles (combos de artículos con precio especial). |
| **Orden Venta** | Importa los artículos desde una Orden de Venta previamente creada. Solo visible en el menú de gestión. |
| **Reparaciones** | Vincula la factura a una reparación del módulo de Service. Solo visible si el módulo de reparaciones está habilitado. |

---

### Sección: Cobro

| Campo/Botón | Descripción |
|---|---|
| **Voucher** | Permite aplicar un voucher de descuento o gift card al total de la factura. |
| **Pagos** | Abre la ventana de registro de medios de pago (efectivo, tarjeta, transferencia, etc.). **Debe usarse antes de facturar.** |
| **Solo Efectivo** | Casilla que marca la factura como cobrada exclusivamente en efectivo. Al tildarla se aplica automáticamente el descuento por pago en efectivo configurado. Solo aparece si el PDV tiene caja asociada. |
| **MercadoPago** | Busca cobros realizados a través del terminal de MercadoPago y los vincula a la factura. Solo aparece si el PDV tiene MercadoPago configurado. |
| **Clover** | Busca cobros realizados en el terminal Clover y los vincula a la factura. Solo aparece si el PDV tiene Clover configurado. |

---

### Sección: Datos adicionales

| Campo | Descripción |
|---|---|
| **MATRÍCULA** | Campo especial para algunos clientes específicos. Solo visible para usuarios de soporte técnico. |
| **OBSERVACIONES** | Texto libre para agregar notas internas o instrucciones de entrega. En comprobantes Movistar (RM/IRM), este campo registra automáticamente los datos de activación. |
| **Tipo IVA (A / B / C)** | Solo aparece para comprobantes tipo X cuando está habilitado. Permite elegir la tasa de IVA aplicada: Tipo A (tasa completa), Tipo B (tasa reducida), Tipo C (sin IVA). |

---

## Botones principales de la pantalla

Estos botones generalmente aparecen en la parte inferior del panel de detalles (grilla derecha):

| Botón | Qué hace |
|---|---|
| **Facturar** | Emite el comprobante y lo envía a AFIP si corresponde. **Antes de facturar debe haberse registrado el pago** (con el botón Pagos o tildando Solo Efectivo). |
| **Cancelar** | Descarta todos los datos ingresados y limpia el formulario para iniciar una nueva factura. Pide confirmación antes de ejecutarse. |

---

## Información que muestra el sistema automáticamente

- **Próximo Remito T3:** Si el tipo de comprobante es RM o IRM, el sistema muestra el número del próximo remito a emitir (útil para operadores de Movistar).
- **Descuentos automáticos:** El sistema aplica descuentos por cliente, por cantidad y por voucher de forma automática al agregar artículos.
- **Alerta de certificado AFIP:** Si el certificado electrónico está por vencer, el sistema muestra un banner de advertencia con el enlace para actualizarlo.

---

## Paso a paso: Cómo emitir una factura estándar

**Caso típico:** Venta de un artículo a un cliente registrado, cobrado en efectivo.

**1. Seleccionar el Punto de Venta**
- En el campo **PDV**, elegí el local o caja desde donde estás vendiendo.
- Si es la primera vez en el día, el sistema puede recordar el último PDV usado.

**2. Seleccionar el Vendedor**
- Elegí el vendedor responsable de la venta en el campo **VENDEDOR**.

**3. Verificar la fecha**
- La **FECHA** se completa sola con el día de hoy. Modificala solo si es necesario.

**4. Seleccionar el cliente**
- Escribí el nombre o código del cliente en el campo **CLIENTE** y elegilo de la lista.
- El sistema asignará automáticamente el tipo de comprobante (A, B, etc.) según el IVA del cliente.
- Si es una venta sin datos fiscales, podés dejar "Consumidor Final".

**5. Verificar el tipo de comprobante**
- Confirmá que el campo **FACTURA** muestra el tipo correcto (ej.: Factura B para consumidor final).

**6. Ingresar el artículo**
- Escribí el código del artículo en el campo **ARTÍCULO** o hacé clic en **Buscar** para buscarlo.
- El precio se completa automáticamente.
- Ingresá la **CANTIDAD** y presioná **Enter** o hacé clic en **Ingresar**.
- El artículo aparecerá en la grilla del panel derecho.
- Repetí este paso para cada artículo adicional.

**7. Registrar el cobro**
- Hacé clic en el botón **Pagos** para abrir la ventana de cobro.
- Seleccioná el **tipo de pago** (efectivo, tarjeta de débito, tarjeta de crédito, transferencia, etc.) y completá los campos que aparezcan según el tipo elegido.
- Si el tipo de pago tiene descuento configurado (ej.: efectivo), el sistema lo aplica automáticamente.
- Hacé clic en **Ingresar** para registrar ese medio de pago. El sistema actualiza el saldo pendiente.
- Si la venta se cobra en varios medios (cobro mixto), podés seguir agregando pagos hasta cubrir el total.
- Cuando todos los pagos estén ingresados, hacé clic en **Guardar** para cerrar la ventana y volver a la factura.
- Si el cobro es únicamente en efectivo, podés tildar **Solo Efectivo** directamente en la pantalla principal sin necesidad de abrir la ventana de Pagos.
- Para ver el detalle completo de cada tipo de pago, cobros mixtos e intereses por cuotas, consultá la sección **"La ventana de Pagos en detalle"** más abajo.

**8. Emitir la factura**
- Hacé clic en **Facturar**.
- El sistema enviará el comprobante a AFIP (si es electrónico) y lo registrará.
- Se abrirá la vista previa o se imprimirá automáticamente según la configuración.

---

## Paso a paso: Ingreso múltiple de artículos

Útil cuando tenés que cargar varios artículos de un listado o planilla.

**1.** Hacé clic en el botón **Multiple**.

**2.** En la ventana que se abre, ingresá los artículos en el siguiente formato, uno por línea:
```
CODIGO_ARTICULO;CANTIDAD
```
Ejemplo:
```
ART001;3
ART002;1
ART005;2
```

**3.** Hacé clic en **Aceptar**. El sistema ingresará todos los artículos de la lista automáticamente.

> ⚠️ Si algún artículo no existe o tiene algún problema, el sistema mostrará un mensaje de error indicando cuál fue el artículo con problemas. Los demás se ingresarán igual.

---

## Paso a paso: Ingreso por NSE (Número de Serie / IMEI)

Para equipos celulares u otros artículos que se identifican por número de serie.

**1.** Hacé clic en el botón **#Series**.

**2.** En la ventana que se abre, pegá la lista de números de serie (NSE/IMEI), uno por línea.

**3.** Hacé clic en **Aceptar**. El sistema buscará cada equipo en el stock y los ingresará automáticamente.

> 💡 Si un NSE no se encuentra en el stock del PDV, el sistema te informará pero seguirá cargando los demás.

---

## Paso a paso: Aplicar un Voucher de descuento

Los vouchers son códigos de descuento configurables que el sistema aplica automáticamente al total de la factura. Pueden otorgar un descuento porcentual (ej.: 10% de descuento) o un descuento de importe fijo (ej.: $5.000 de descuento).

> 📖 Para aprender a crear y administrar vouchers antes de usarlos, consultá [**Vouchers Individuales**](https://ayuda.caddis.com.ar/instructivos/01_ARTICULOS_ABM_Vouchers.pdf).

**1.** Ingresá los artículos en la factura normalmente.

**2.** Hacé clic en el botón **Voucher**.

**3.** En la ventana que aparece, ingresá el **Alias** del voucher (el código corto que fue asignado al crearlo).

**4.** El sistema verificará si el voucher es válido y aplicará el descuento automáticamente en la grilla de artículos.

> ⚠️ Los vouchers tienen fecha de vencimiento. Si el voucher está vencido o ya fue utilizado (y no es multiuso), el sistema lo informará con un mensaje de error.

> ⚠️ Los descuentos automáticos por forma de pago (efectivo, tarjeta de débito, etc.) **no se aplican** cuando ya hay un voucher de descuento activo en la factura.

> 💡 Un voucher configurado como **Multiuso** puede aplicarse en múltiples facturas. Un voucher de uso único queda marcado como "utilizado" después de la primera vez que se usa.

---

## Paso a paso: Emitir y aplicar una Gift Card

Una **Gift Card** es un voucher de saldo prepago que funciona en dos etapas: primero se **emite** facturando un artículo especial, y luego el cliente la **usa como forma de pago** al momento de comprar.

> 📖 Para aprender a crear los artículos Gift Card antes de emitirlas, consultá [**ABM Artículos — Crear un artículo Gift Card**](https://ayuda.caddis.com.ar/instructivos/01_ARTICULOS_ABM_Articulos.pdf).

### Etapa 1 — Emitir la Gift Card

La Gift Card es un **artículo de tipo Servicio** (SERVICIO = SI, IVA = 0) que no afecta el stock. Debe estar configurado previamente con tipo **GIFT-CARD** y precio definido en la lista correspondiente.

**1.** Abrí una nueva factura con cualquier comprobante estándar: **EB, EA, B, A o X** según corresponda al cliente.

**2.** Seleccioná el artículo Gift Card de la denominación que el cliente desea (ej.: "GIFT-CARD $500") e ingresalo en la factura.

**3.** Registrá el cobro con el medio de pago que el cliente elige (efectivo, tarjeta, transferencia, etc.) y hacé clic en **Facturar**.

**4.** El sistema emite el comprobante con su número (ej.: `X-00001234`). Ese número es el "código" de la Gift Card. Entregale el comprobante al cliente — lo necesitará para usarla.

> 💡 Al emitir con comprobantes **EB, EA, B, A o X**, el sistema incluye automáticamente la imagen simbólica de la Gift Card en el comprobante impreso. Con otros tipos de comprobante el artículo figura igualmente, pero sin la imagen.

> 💡 El importe de la Gift Card quedará disponible para ser descontado en una compra futura. El sistema lo reconoce por el tipo y número del comprobante.

---

### Etapa 2 — Aplicar la Gift Card como forma de pago

Cuando el cliente quiera usar su Gift Card para pagar una compra:

**1.** Ingresá los artículos en la factura normalmente.

**2.** Hacé clic en el botón **Pagos** para abrir la ventana de cobro.

**3.** En el campo **TIPO**, seleccioná **Gift Card**.

**4.** Aparecerán dos campos:
   - **FC Tipo:** seleccioná el tipo de comprobante de la Gift Card (EB, EA, B, A o X, según cuál se emitió)
   - **FC Nro:** ingresá el número del comprobante (ej.: `00001234`)

**5.** El sistema buscará el comprobante original y cargará automáticamente el importe disponible en el campo **Pagar**.

**6.** Hacé clic en **Ingresar** para registrar el pago.

> ⚠️ El sistema aplica el **100% del valor** de la Gift Card. Al emitir la factura queda marcada como **"utilizada"** y no puede volver a usarse.

> ⚠️ Si el sistema muestra **"Inexistente"**, el número de comprobante no existe o está mal ingresado. Verificá el número con el cliente.

> ⚠️ Si el sistema muestra **"Ya utilizada"**, la Gift Card ya fue aplicada en una compra anterior y no puede reutilizarse.

> 💡 Si el valor de la Gift Card no cubre el total de la factura, podés agregar otro medio de pago para completar el cobro (ver sección **Pagos mixtos**).

---

## Paso a paso: Aplicar una Promoción de Artículos

Las **Promociones de Artículos** son combos preconfigurados que agrupan uno o más artículos o equipos con precios especiales o descuentos. Al aplicarlas, el sistema agrega automáticamente todos los ítems de la promoción con sus condiciones de precio, sin necesidad de ingresar cada artículo por separado.

> ⚠️ Algunas promociones están condicionadas a una **forma de pago específica** (ej.: solo con tarjeta de crédito Visa). El sistema validará este requisito al momento de facturar y no permitirá emitir el comprobante si el pago no cumple la condición.

> 📖 Para aprender a crear y configurar promociones antes de usarlas en facturación, consultá [**Promociones de Artículos**](https://ayuda.caddis.com.ar/instructivos/01_ARTICULOS_ABM_Promos.pdf).

**1. Seleccionar el cliente y el PDV**
- Antes de aplicar la promoción, asegurate de tener el cliente y el punto de venta seleccionados.

**2. Abrir el buscador de promociones**
- Hacé clic en el botón **Promos**.
- Se abrirá una ventana emergente con el buscador de promociones disponibles.

**3. Buscar la promoción**
- Ingresá el código o parte del nombre de la promoción en el buscador.
- Seleccioná la promoción correcta de la lista de resultados.

**4. Confirmar la selección**
- Al seleccionar la promoción, el sistema cargará automáticamente todos los artículos del combo en la grilla de la factura con sus precios o descuentos configurados.

**5. Verificar los artículos cargados**
- Confirmá que todos los ítems de la promoción aparecen en la grilla con las cantidades y precios correctos.

**6. Registrar el pago con la forma requerida**
- Si la promoción tiene una **forma de pago requerida** (ej.: solo con Visa crédito), registrá el pago con ese medio en la ventana de **Pagos**.
- El sistema verificará que el pago coincide con el requisito de la promoción. Si no coincide, no permitirá emitir la factura e informará con un mensaje de error.

**7. Emitir la factura**
- Hacé clic en **Facturar**.

> 💡 Si la promoción tiene artículos de **cualquier equipo con NSE**, el sistema requerirá que ingreses los equipos del stock por número de serie. Podés usar el botón **#Series** para cargarlos masivamente.

---

## Paso a paso: Facturar una Reparación

Cuando el módulo de reparaciones está habilitado, el botón **Reparaciones** permite tanto cobrar la seña inicial como facturar la reparación terminada. Hay dos procedimientos distintos según el momento:

---

### Caso A — Facturar la seña

La seña se registra al momento del ingreso del equipo desde [**Nueva Reparación**](https://ayuda.caddis.com.ar/instructivos/12_REP_Nueva_Reparacion.pdf). Para emitir el recibo:

**1.** Abrí una nueva factura en Facturación.

**2.** Hacé clic en el botón **Reparaciones**. El buscador mostrará las señas aún no facturadas (identificadas como **SENIA** en la columna Op_Tipo).

**3.** Seleccioná la seña correspondiente. El sistema preguntará automáticamente: *"¿Emitir comprobante RC?"*. Hacé clic en **Aceptar** — el tipo de comprobante cambia a **RC (Recibo)** automáticamente.

**4.** Registrá el cobro con el botón **Pagos** (generalmente Efectivo).

**5.** Hacé clic en **Facturar**. El sistema emite el PDF del recibo.

> 💡 Al final del día, las señas cobradas se rinden desde **Cierre de Caja Diario** junto con el resto de los comprobantes emitidos.

---

### Caso B — Facturar la reparación terminada

Cuando el equipo está listo y la orden tiene estado **REPARACION TERMINADA**:

**1.** Abrí una nueva factura en Facturación.

**2.** Hacé clic en el botón **Reparaciones**. El buscador mostrará las órdenes listas para facturar (identificadas como **REPA** en la columna Op_Tipo).

**3.** Seleccioná la orden. El sistema preguntará el tipo de comprobante a emitir (habitualmente **X** para reparaciones). Confirmá.

**4.** El sistema cargará automáticamente el cliente y los artículos de reparación (repuestos y mano de obra).

**5.** Registrá el cobro con el botón **Pagos**:
   - Si el cliente pagó una seña previamente, en la lista de tipos de pago aparecerá la opción **Seña** con el importe disponible — seleccionala para descontarla del total.
   - Agregá los medios de pago restantes hasta cubrir el total.

**6.** Hacé clic en **Facturar**. El sistema emite el comprobante.

**7.** Una vez facturada, registrá la entrega física del equipo desde [**Entrega a Cliente**](https://ayuda.caddis.com.ar/instructivos/12_REP_Entrega_Cliente.pdf).

---

## Paso a paso: Facturar desde una Orden de Venta

**1.** Hacé clic en el botón **Orden Venta**.

**2.** En la ventana que se abre, buscá y seleccioná la orden de venta a facturar.

**3.** El sistema importará automáticamente el cliente y los artículos de la orden.

**4.** Verificá los datos, registrá el cobro y hacé clic en **Facturar**.

---

## Paso a paso: Comprobante Movistar (RM / IRM)

Para distribuidores de Movistar que emiten remitos T3.

**1.** Seleccioná el tipo de comprobante **RM** o **IRM** en el campo **FACTURA**.

**2.** Ingresá los equipos (por artículo o por NSE con el botón **#Series**).

**3.** Al hacer clic en **Facturar**, el sistema abrirá automáticamente una ventana para ingresar los datos de activación (número de orden Movistar, etc.).

**4.** Completá los datos de activación y confirmá para emitir el remito.

> 💡 El sistema muestra el **número del próximo remito T3** en la parte inferior del formulario para que puedas verificarlo antes de emitir.

---

## Cobro con terminales de pago

### MercadoPago

**1.** El cliente realiza el pago desde la app o terminal de MercadoPago.

**2.** Una vez confirmado el pago en el terminal, hacé clic en el botón **MercadoPago** en la pantalla de facturación.

**3.** El sistema buscará automáticamente el cobro y lo vinculará a la factura actual.

**4.** Hacé clic en **Facturar** para emitir el comprobante.

### Clover

**1.** El cliente realiza el pago en la terminal Clover.

**2.** Una vez confirmado el pago, hacé clic en el botón **Clover** en la pantalla de facturación.

**3.** El sistema buscará y vinculará el cobro automáticamente.

**4.** Hacé clic en **Facturar** para emitir el comprobante.

---

## La ventana de Pagos en detalle

Al hacer clic en **Pagos** se abre una ventana emergente dividida en dos áreas:

- **Izquierda:** formulario para ingresar un nuevo medio de pago
- **Derecha:** lista de pagos ya registrados para esa factura, con el **SALDO** pendiente y el **TOTAL PAGOS** acumulado

### Cómo registrar un pago

1. Seleccioná el **TIPO** de pago en la lista desplegable
2. Completá los campos adicionales que aparecen según el tipo elegido (ver tabla más abajo)
3. Verificá el importe en el campo **Pagar** (se precarga con el saldo pendiente)
4. Hacé clic en **Ingresar** o presioná **Enter**
5. El pago queda registrado en la lista de la derecha y el saldo se actualiza
6. Si la venta se cobra en múltiples medios, repetí los pasos anteriores hasta cubrir el total
7. Cuando todos los pagos estén cargados, hacé clic en **Guardar** para cerrar la ventana

> ⚠️ Si cerrás la ventana sin hacer clic en **Guardar**, los pagos no quedarán confirmados en la factura.

> 💡 Podés eliminar cualquier pago ya ingresado haciendo clic en el botón **Borrar** que aparece en cada línea de la lista de la derecha.

---

### Tipos de pago y campos requeridos

| Tipo de pago | Campos adicionales requeridos |
|---|---|
| **Efectivo** | Solo el importe. Puede aplicar descuento automático. |
| **Tarjeta de débito** | Tarjeta, Terminal, N° de tarjeta, N° de cupón, Fecha del cupón, Código de autorización, N° de lote |
| **Tarjeta de crédito** | Tarjeta, Promoción, Terminal, N° de tarjeta, N° de cupón, Fecha del cupón, Código de autorización, N° de lote |
| **Cuenta corriente** | Condición de pago (plazo). Solo disponible para clientes con venta en cuenta corriente habilitada |
| **Cheque propio** | Banco, N° de cheque, Fecha de vencimiento |
| **Cheque de terceros** | Banco, N° de cheque, Fecha de vencimiento |
| **Depósito bancario** | Banco, N° de comprobante, Fecha |
| **Transferencia bancaria** | Banco, N° de comprobante, Fecha |
| **Gift Card** | Tipo de comprobante y número de la gift card a aplicar |
| **Seña** | N° del recibo de seña (comprobante RC previamente emitido) |
| **Dólares** | Cotización del día y monto en dólares (el sistema convierte automáticamente a pesos) |
| **Crédito personal** | Entidad financiera, N° de referencia, Fecha |
| **Marketplace** | Plataforma (MercadoLibre, TiendaNube, etc.), N° de referencia, Fecha |
| **Billetera virtual** | Plataforma (MercadoPago, Ualá, etc.), Fecha y N° de referencia |

> 💡 Los tipos de pago disponibles pueden variar según la empresa, el PDV y el perfil del usuario. Los usuarios sin caja asignada solo pueden cobrar en cuenta corriente (si el cliente la tiene habilitada).

---

### Pagos mixtos (cobro en múltiples medios)

La ventana de Pagos permite registrar **más de un medio de pago** para la misma factura. El sistema descuenta cada pago del saldo y muestra el remanente en tiempo real.

**Ejemplos comunes:**
- $50.000 en efectivo + $30.000 en tarjeta de débito
- Seña previamente abonada (RC) + saldo restante en tarjeta de crédito
- Mitad en transferencia bancaria + mitad en billetera virtual
- Efectivo parcial + cuenta corriente por el resto (clientes mayoristas)

No es necesario que el total de pagos cubra exactamente el monto de la factura antes de hacer clic en **Facturar**, pero sí es recomendable para evitar diferencias en la caja.

---

### Descuentos automáticos por forma de pago

Algunos medios de pago tienen descuentos configurados por el administrador del sistema. Al seleccionarlos, el sistema aplica el descuento automáticamente sobre el importe:

| Tipo de pago | Descuento que puede aplicar |
|---|---|
| Efectivo | Descuento por pago en efectivo |
| Tarjeta de débito | Descuento por débito |
| Depósito bancario | Descuento por depósito |
| Transferencia bancaria | Descuento por transferencia |
| Dólares | Descuento por pago en divisas |
| Billetera virtual | Descuento por billetera |

> 💡 Si el sistema lo permite (según configuración del administrador), el porcentaje de descuento puede modificarse manualmente en el campo **Descuento** antes de confirmar el pago.

> ⚠️ Los descuentos automáticos **no se aplican** si la venta tiene un voucher de descuento ya ingresado, o si ya existe un pago con tarjeta de crédito registrado.

---

### Intereses por cuotas en tarjetas de crédito y débito

Cuando el pago es con **tarjeta de crédito**, el sistema puede aplicar automáticamente el recargo correspondiente según la configuración de tasas. Esto recalcula el importe total de la factura antes de emitirla.

#### Cómo funciona en la ventana de Pagos

Al seleccionar **Tarjeta de crédito** como tipo de pago:

1. Elegís la **Tarjeta** (Visa, Mastercard, Cabal, Naranja, American Express, etc.)
2. Elegís la **Promoción** (contado, 3 cuotas, 6 cuotas, plan Z, etc.)
3. El sistema busca automáticamente la tasa configurada para esa combinación de tarjeta + promoción
4. El **importe total** se recalcula sumando el interés: `Importe + (Importe × Tasa)`
5. La diferencia entre el importe original y el importe final es el **interés** que se le cobra al cliente

#### Ejemplo práctico

Venta por $100.000, cobro con Visa crédito en 6 cuotas con una tasa del 12%:

| Concepto | Monto |
|---|---|
| Importe de la venta | $100.000 |
| Interés (12%) | $12.000 |
| **Total a facturar** | **$112.000** |

El cliente paga $112.000 dividido en 6 cuotas de $18.667 aproximadamente.

---

### Configuración de tasas de tarjetas (para administradores)

Las tasas que aplica el sistema al cobrar con tarjeta se configuran en la pantalla **Tasas de Tarjetas de Crédito** (Módulo 1 → Opción 1.15). Esta pantalla es de uso exclusivo del administrador del sistema.

> 📖 Para el instructivo completo de cómo configurar tasas e intereses por tarjeta, consultá [**Tasas de Tarjetas de Crédito**](https://ayuda.caddis.com.ar/instructivos/01_ARTICULOS_ABM_Tarjetas_Tasas.pdf).

Los campos que se configuran son:

| Campo | Descripción |
|---|---|
| **Plataforma** | Terminal de cobro donde se pasa la tarjeta (Lapos, Clover, MercadoPago, etc.) |
| **Tarjeta** | Marca de la tarjeta (Visa, Mastercard, Cabal, Naranja, etc.) |
| **Promo** | Tipo de promoción (contado, cuotas, plan Z, débito, etc.) |
| **Cuotas** | Cantidad de cuotas. Para tarjetas de débito siempre es **0**. |
| **Tasa** | Porcentaje de interés total **con IVA ya incluido** (ej.: `5.00` = 5%) |
| **Activa** | Si esta tasa está habilitada para usarse en facturas (ACTIVA / INACTIVA) |

> ⚠️ La tasa debe ingresarse como el **porcentaje final con IVA incluido**. Ejemplo: si la tasa financiera neta es 4,13% y el IVA es 21%, la tasa total es 5% → se ingresa `5.00`.

> 💡 Para tarjetas de **débito**, la tasa no puede ser negativa y las cuotas deben ser **0**.

Las tasas pueden importarse masivamente desde un archivo Excel. Al importar, el sistema también requiere que los valores ya incluyan el IVA.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Falta configurar el nombre de su empresa" | El sistema no tiene la razón social de la empresa cargada | Contactar al administrador del sistema |
| "Falta configurar el CUIT de su empresa" | El PDV seleccionado no tiene CUIT asignado | Contactar al administrador del sistema |
| "Falta configurar el domicilio del PDV" | El punto de venta no tiene domicilio registrado | Contactar al administrador del sistema |
| "Falta configurar la fecha de inicio de actividades del PDV" | El PDV no tiene fecha de inicio de actividades | Contactar al administrador del sistema |
| "No se puede eliminar el artículo — Cancele para hacer una nueva Factura" | El artículo ya fue incluido en una factura anterior | Usá **Cancelar** para comenzar una nueva factura |
| "Elija un PDV" | Se intentó ingresar un artículo sin seleccionar el punto de venta | Seleccioná primero el PDV |
| "Controle el Artículo" | El campo artículo está vacío | Ingresá o buscá el código del artículo |
| "Controle la Cantidad" | La cantidad es cero o no es un número válido | Ingresá una cantidad mayor a cero |
| "Controle el Importe" | El precio es cero, negativo o excede el máximo permitido | Verificá el precio del artículo |
| "Ingrese un Item..." | Se intentó abrir Pagos sin artículos en la factura | Ingresá al menos un artículo primero |
| "Debe destildar SOLO EFECTIVO" | Se intentó abrir Pagos con la opción Solo Efectivo tildada | Destildá Solo Efectivo antes de abrir Pagos |
| "Si cambia el Punto de Venta se eliminarán los datos ingresados" | Se intentó cambiar el PDV con artículos ya cargados | Confirmá el cambio (se perderán los datos) o cancelá y terminá la factura actual |
| "Al cambiar de lista se cancela la factura" | Se intentó cambiar la lista de precios con artículos ya cargados | Confirmá el cambio o terminá la factura actual |
| Banner: "Su certificado electrónico de ARCA vencerá el..." | El certificado de facturación electrónica está por vencer | Seguí el enlace del banner o contactá al administrador |

---

## Preguntas frecuentes

**¿Qué pasa si elijo el cliente incorrecto?**
Podés cambiar el cliente haciendo clic en la "X" junto al nombre del cliente (si la factura no tiene artículos). Si ya ingresaste artículos, al cambiar el cliente el sistema te pedirá confirmación y reiniciará la factura.

**¿Puedo modificar el precio de un artículo?**
Depende de la configuración del sistema. En algunos casos el campo **IMPORTE** está bloqueado y no se puede modificar; en otros, está habilitado para editarlo manualmente.

**¿Cómo elimino un artículo que ingresé por error?**
En la grilla del panel derecho, cada artículo tiene un botón de eliminar (ícono de papelera o "X"). Al hacer clic, el sistema te pedirá confirmación. No podés eliminar artículos que ya fueron facturados.

**¿Qué pasa si cierro la pantalla sin facturar?**
La factura queda en estado "borrador" en la tabla temporal. La próxima vez que abras la pantalla, el sistema podría retomar la factura anterior o iniciar una nueva, según la configuración.

**¿Puedo facturar en dólares?**
Sí, si la empresa tiene habilitada la facturación en divisas. En ese caso aparecerá el campo **EMITIR EN** para elegir la moneda y la cotización del día.

**¿Cuándo debo usar el botón Cancelar?**
Cuando querés empezar de cero una nueva factura, descartando todo lo que ingresaste. El sistema te pedirá confirmación antes de borrar los datos.

**¿Qué es el NSE?**
NSE significa "Número de Serie del Equipo" (equivalente al IMEI en celulares). Es un identificador único de cada equipo. Para artículos que requieren NSE, el sistema lo solicitará automáticamente al intentar facturar.

**¿Cómo sé qué tipo de factura usar?**
El sistema lo sugiere automáticamente al seleccionar el cliente, según su condición de IVA. Si hay dudas, consultá con el administrador del sistema.

**¿Por qué no aparece el botón de Reparaciones?**
El botón solo se muestra si el módulo de reparaciones está habilitado en la configuración del sistema.

**¿Por qué no aparecen todos los tipos de comprobante en la lista?**
Los comprobantes disponibles dependen del PDV seleccionado y de la configuración de la empresa. Algunos tipos (como RM para Movistar) solo aparecen si están habilitados para esa empresa.

---

## Referencia rápida de botones y campos

| Elemento | Tipo | Acción / Descripción |
|---|---|---|
| PDV | Lista desplegable | Selecciona el punto de venta |
| VENDEDOR | Lista desplegable | Selecciona el vendedor |
| FECHA | Fecha | Fecha del comprobante (hoy por defecto) |
| CAJA | Lista desplegable | Caja del PDV |
| CLIENTE | Buscador | Selecciona el cliente |
| EMITIR EN | Lista desplegable | Moneda de emisión (ARS/USD) |
| Cotización | Número | Tipo de cambio del día |
| FACTURA (tipo) | Lista desplegable | Tipo de comprobante a emitir |
| FACTURA (número) | Texto | Número de comprobante |
| LISTA | Lista desplegable | Lista de precios |
| ARTÍCULO | Texto | Código del artículo |
| Buscar | Botón | Abre buscador de artículos en stock |
| IMPORTE | Número | Precio unitario con IVA |
| CANTIDAD | Número | Cantidad a vender |
| Ingresar / Enter | Botón/tecla | Agrega artículo a la factura |
| Multiple | Botón | Ingreso masivo de artículos por código |
| #Series | Botón | Ingreso masivo de artículos por NSE |
| Promos | Botón | Busca y aplica promociones de venta |
| Orden Venta | Botón | Importa artículos de una Orden de Venta |
| Reparaciones | Botón | Vincula con una orden de reparación |
| Voucher | Botón | Aplica voucher o gift card de descuento |
| Pagos | Botón | Registra las formas de pago |
| Solo Efectivo | Casilla | Marca cobro en efectivo (aplica descuento automático) |
| MercadoPago | Botón | Vincula cobro del terminal MercadoPago |
| Clover | Botón | Vincula cobro del terminal Clover |
| OBSERVACIONES | Texto libre | Notas adicionales de la venta |
| Tipo IVA | Botones de opción | Solo para tipo X: elige tasa de IVA (A/B/C) |
| Facturar | Botón principal | Emite el comprobante y lo envía a AFIP |
| Cancelar | Botón | Descarta la factura y limpia el formulario |

---

