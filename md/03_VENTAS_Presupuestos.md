# 3.07 PRESUPUESTOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Presupuestos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Presupuestos** permite crear cotizaciones formales para clientes sin emitir una factura. Desde aquí podés:

- Generar presupuestos con artículos y precios para enviar a clientes
- Vincular un presupuesto existente para facturarlo directamente
- Emitir comprobantes de tipo Presupuesto A o B
- Registrar adelantos sobre presupuestos (señas parciales)
- Facturar presupuestos en moneda extranjera (si está habilitado)

> ℹ️ Un presupuesto **no afecta el stock** ni genera una factura hasta que se convierte en venta. Para facturar un presupuesto ya creado, usá la pantalla **Facturar Presupuestos** (3.07 complementaria, accedida desde el botón PRESUPUESTO).

---

<img src="imagenes/pantalla_presupuestos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Presupuestos**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Formulario con los datos del presupuesto (cliente, artículos, tipo de comprobante)
- **Panel derecho:** Grilla con el detalle de artículos ingresados en el presupuesto

---

## Campos del formulario

### Sección: Datos principales

| Campo | Descripción |
|---|---|
| **PDV** | Punto de Venta desde donde se genera el presupuesto. |
| **VENDEDOR** | Vendedor responsable del presupuesto. Se filtra según el PDV. |
| **FECHA** | Fecha del presupuesto. Se completa automáticamente con el día de hoy. |
| **CLIENTE** | Cliente para quien se genera el presupuesto. Al seleccionarlo, el sistema asigna el tipo de comprobante correspondiente. |
| **EMITIR EN** | *(Opcional)* Moneda en que se emite el presupuesto (ARS o dólares). Solo aparece si la empresa tiene habilitada la facturación en divisas. Incluye un campo de **cotización** del día. |
| **FACTURA** | Tipo de comprobante de presupuesto: **PA** (Presupuesto A) o **PB** (Presupuesto B), según el IVA del cliente. |

---

### Sección: Presupuesto previo

| Campo/Botón | Descripción |
|---|---|
| **PRESUPUESTO** | Botón para importar los artículos de un presupuesto existente. Al hacer clic, se abre un buscador de presupuestos por número. |
| **Campo de número** | Número del presupuesto a importar (se completa al buscarlo). |
| **Botón detalle** | Abre el detalle del presupuesto seleccionado para verificar los artículos antes de importarlo. |

> 💡 Si el cliente ya tiene un presupuesto creado, podés importarlo haciendo clic en **PRESUPUESTO** y buscarlo para no tener que ingresar los artículos nuevamente.

---

### Sección: Ingreso de artículos

Los artículos se ingresan de la misma forma que en la pantalla de Facturación (3.01):

| Campo/Botón | Descripción |
|---|---|
| **ARTÍCULO** | Código del artículo. Podés tipear el código o usar **Buscar** para buscarlo por nombre. |
| **IMPORTE** | Precio unitario del artículo. Se completa automáticamente. |
| **CANTIDAD** | Cantidad a presupuestar. Presioná **Enter** para agregar el artículo. |
| **Buscar** | Abre una ventana para buscar artículos en el stock del PDV. |
| **Promos** | Abre el buscador de promociones de venta disponibles. |
| **Ingresar** | Agrega el artículo con el importe y cantidad al presupuesto. |

---

### Sección: Datos adicionales y cobro

| Campo/Botón | Descripción |
|---|---|
| **MATRÍCULA** | *(Solo para algunos clientes específicos)* Campo especial visible solo para usuarios de soporte técnico. |
| **OBSERVACIONES** | Texto libre para agregar notas, condiciones especiales o instrucciones del presupuesto. |
| **Voucher** | Permite aplicar un voucher de descuento al total del presupuesto. |
| **Pagos** | Permite registrar un adelanto o seña sobre el presupuesto. |
| **Solo Efectivo** | Marca el pago como realizado exclusivamente en efectivo. |
| **Tipo IVA (A / B / C)** | *(Solo para comprobantes tipo X en empresas específicas)* Permite elegir la tasa de IVA aplicada. |

---

## Botones principales

| Botón | Qué hace |
|---|---|
| **Presupuestar** | Guarda el presupuesto sin emitir una factura. Genera un comprobante de presupuesto (PA o PB) que puede usarse para facturar más adelante. |
| **Cancelar** | Descarta todo lo ingresado y limpia el formulario. Pide confirmación. |

---

## Paso a paso: Crear un nuevo presupuesto

**Caso típico:** Un cliente consulta el precio de varios artículos y quiere llevarse una cotización.

**1. Seleccionar el Punto de Venta y Vendedor**
- En **PDV**, elegí el local desde donde atendés al cliente.
- En **VENDEDOR**, elegí el vendedor responsable.

**2. Seleccionar el cliente**
- En **CLIENTE**, buscá y seleccioná al cliente.
- El sistema asignará automáticamente el tipo de comprobante (PA para RI, PB para consumidor final).

**3. Verificar la fecha y el tipo de comprobante**
- La **FECHA** se completa con hoy. Modificala si es necesario.
- Verificá que el campo **FACTURA** muestra **PA** o **PB** según corresponda.

**4. Ingresar los artículos**
- En **ARTÍCULO**, ingresá el código o buscá el artículo con el botón **Buscar**.
- Verificá el **IMPORTE** y ajustá si es necesario.
- Ingresá la **CANTIDAD** y presioná **Enter** o hacé clic en **Ingresar**.
- El artículo aparece en la grilla del panel derecho.
- Repetí para cada artículo.

**5. Agregar observaciones** *(opcional)*
- En **OBSERVACIONES**, anotá condiciones especiales, validez del presupuesto, etc.
- Ejemplo: "Precio válido por 7 días", "Incluye instalación", "Sujeto a disponibilidad de stock".

**6. Guardar el presupuesto**
- Hacé clic en **Presupuestar**.
- El sistema genera un presupuesto con número de comprobante (PA o PB).
- Podés imprimirlo o enviarlo al cliente.

---

## Paso a paso: Importar y facturar un presupuesto existente

Cuando el cliente confirma el presupuesto y quiere comprar:

**1. Abrí la pantalla de Presupuestos** (o bien la pantalla de **Facturar Presupuestos** 3.09 desde el menú).

**2. Hacé clic en el botón PRESUPUESTO.**

**3. En el buscador, ingresá el número del presupuesto** o buscá por cliente.

**4. Seleccioná el presupuesto y hacé clic para importarlo.**

**5. El sistema cargará automáticamente el cliente y todos los artículos del presupuesto en la grilla.**

**6. Verificá que todo sea correcto** (precios, cantidades, tipo de comprobante).

**7. Seleccioná el tipo de comprobante final** (cambiar de PA/PB a una factura real si corresponde).

**8. Registrá el cobro con Pagos** o tildá Solo Efectivo.

**9. Hacé clic en Facturar** para emitir la factura definitiva.

---

## Presupuesto en moneda extranjera *(si está habilitado)*

Si la empresa tiene habilitada la facturación en divisas, aparece el campo **EMITIR EN** con las opciones:
- **ARS:** pesos argentinos (por defecto)
- **USD:** dólares estadounidenses

Al elegir USD, debés ingresar la **cotización del día** en el campo correspondiente. Los precios de los artículos se mostrarán en la moneda seleccionada.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Elija un PDV" | Se intentó guardar sin seleccionar el PDV | Seleccioná el PDV primero |
| "Controle el Artículo" | El campo artículo está vacío | Ingresá o buscá el código del artículo |
| "Controle la Cantidad" | La cantidad es cero o inválida | Ingresá una cantidad mayor a cero |
| "No se encontró el presupuesto" | El número de presupuesto no existe | Verificá el número o buscá por cliente |

---

## Preguntas frecuentes

**¿Un presupuesto afecta el stock?**
No. El presupuesto es solo una cotización. El stock no se reserva ni se modifica hasta que se factura.

**¿Cuánto tiempo es válido un presupuesto?**
El sistema no vence los presupuestos automáticamente. La validez temporal (ej.: "válido por 7 días") es informativa y puede indicarse en el campo Observaciones.

**¿Puedo modificar un presupuesto ya creado?**
Dependiendo de la configuración del sistema, es posible modificarlo antes de facturarlo. Consultá con el administrador.

**¿Cuál es la diferencia entre PA y PB?**
- **PA (Presupuesto A):** para clientes con IVA Responsable Inscripto.
- **PB (Presupuesto B):** para clientes consumidores finales o monotributistas.

**¿Puedo registrar una seña sobre un presupuesto?**
Sí, usando el botón **Pagos** podés registrar un pago parcial (adelanto/seña) sobre el presupuesto antes de facturarlo.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
