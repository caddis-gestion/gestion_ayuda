# 3.23 COBROS — RENDICIÓN DIARIA DE CAJA
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Cobranza → Cobros

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cobros** es donde se registra la rendición diaria de caja. Permite informar al sistema cuánto dinero, qué cupones de tarjeta y qué valores (cheques, transferencias) se recaudaron durante el día en un punto de venta. Desde aquí podés:

- Ver el **saldo pendiente de rendir** del día (facturado menos lo ya rendido)
- Registrar rendiciones por tipo de pago: efectivo, tarjetas, cheques, transferencias, plataformas digitales
- Seleccionar cupones de tarjeta del día para incluirlos en la rendición
- Consultar los **lotes ya cerrados** y su estado (Pendiente de aprobación / Aprobado)
- Imprimir o anular lotes de rendición

> ℹ️ Esta pantalla registra la rendición pero **no la aprueba**. La aprobación se realiza desde la pantalla **Cobranza Aprobación** (3.24).

---

<img src="imagenes/pantalla_cobros.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Cobranza → Cobros**

---

## Descripción general de la pantalla

La pantalla está dividida en tres zonas:

- **Panel izquierdo:** Selección de PDV y fecha, resumen de facturación del día y lotes ya rendidos
- **Panel derecho superior:** Formulario para ingresar cada ítem de la rendición ("Rendición del Día")
- **Panel derecho inferior:** Grilla con los ítems que componen la rendición en curso (aún no guardada como lote)

---

## Panel izquierdo — Filtro y saldos del día

### Campos

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a rendir. Al cambiar, recarga los datos del día. |
| **FECHA** | Fecha a rendir. Por defecto: hoy. Acepta fechas anteriores para rendiciones atrasadas. |

### Indicadores de saldo

Una vez seleccionado el PDV y la fecha, el sistema muestra:

| Indicador | Qué representa |
|---|---|
| **SALDO** | Total facturado del día menos total ya rendido en lotes (en pesos) |
| **SALDO EF** | Lo mismo pero sólo para efectivo |

> Un SALDO en cero indica que toda la facturación del día ya fue rendida.

### Grilla superior — Facturación del día por tipo de pago

Muestra un resumen de todo lo facturado en el día para el PDV seleccionado, agrupado por tipo de pago:

| Columna | Descripción |
|---|---|
| Pago | Tipo de pago (Efectivo, Tarjeta Débito, Tarjeta Crédito, etc.) |
| Pesos | Importe total en pesos para ese tipo |
| Divisa | Importe en moneda extranjera (si aplica, ej. operaciones en USD) |
| Entidad | Nombre del banco o tarjeta |
| Plataforma | Plataforma digital si corresponde (ej. MercadoPago) |

### Indicador RECAUDADO

Muestra el total de los lotes ya cerrados y rendidos para ese día y PDV.

### Grilla inferior — Lotes del día

Lista todos los lotes de rendición ya cerrados para esa fecha y PDV:

| Columna | Descripción |
|---|---|
| Lote | Número de lote de rendición |
| Importe | Total del lote |
| Fecha | Fecha del lote |
| Estado | **Pendiente** (esperando aprobación), **Aprobado**, o **Anulado** |

**Acciones disponibles sobre un lote:**
- **Imprimir:** Imprime la rendición del lote
- **Borrar:** Anula el lote (sólo si está Pendiente)

---

## Panel derecho superior — Rendición del Día

Aquí se ingresan los valores que componen la rendición para generar un nuevo lote.

### Campos

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de la rendición (por defecto la misma del filtro izquierdo) |
| **T PAGO** | Tipo de pago a rendir: Efectivo, Tarjeta Crédito, Tarjeta Débito, Cheque, Transferencia, Compensaciones, etc. |
| **IMPORTE** | Monto a rendir para ese tipo de pago |
| **VENDEDOR** | Selector de vendedor (visible sólo cuando T PAGO = Compensaciones) |
| **BANCO** | Banco donde se depositó o se acredita el importe |
| **COMP#** | Número de comprobante bancario (transferencia, depósito, etc.) |
| **OBSERVACIONES** | Texto libre para registrar aclaraciones |

### Botones

| Botón | Acción |
|---|---|
| **Ingresar rendición** | Agrega el ítem a la grilla inferior (aún no guarda el lote) |
| **Cupones** | Abre el popup de cupones de tarjeta para seleccionar los que se incluyen en la rendición |
| **Guardar** | Cierra la rendición y genera un número de lote. Aparece en la grilla de lotes del panel izquierdo con estado **Pendiente** |

---

## Panel derecho inferior — Ítems de la rendición en curso

Muestra los ítems ya ingresados que formarán el próximo lote al presionar **Guardar**:

| Columna | Descripción |
|---|---|
| Pago | Tipo de pago |
| Importe | Monto del ítem |
| Entidad | Banco o tarjeta |
| Comprobante | Número de comprobante bancario o cupón |
| Observaciones | Notas del ítem |

- **Botón Borrar:** Elimina el ítem de la rendición en curso (antes de guardar)

---

## Popup de Cupones de Tarjeta

Al hacer clic en **Cupones**, se abre una ventana con todos los cupones de tarjeta y plataformas digitales del día para ese PDV que aún no fueron incluidos en una rendición anterior.

| Columna | Descripción |
|---|---|
| Checkbox | Marca o desmarca el cupón para incluirlo |
| Tipo / Factura | Comprobante de origen |
| Fecha | Fecha de la transacción |
| Importe | Importe del cupón |
| Interés | Interés aplicado (si hay) |
| Entidad | Tarjeta o plataforma |
| Promo | Promoción aplicada (si hay) |
| Tarjeta/Referencia | Últimos 4 dígitos de la tarjeta o ID de referencia |
| Cuotas | Cantidad de cuotas |
| Tasa | Tasa de la tarjeta |
| Cupón | Número de cupón |
| Código Aut. | Código de autorización |
| Lote | Lote de tarjeta |

Al cerrar el popup, los cupones seleccionados quedan marcados como incluidos en la rendición en curso.

---

## Paso a paso — Rendir el día

### Rendir efectivo
1. Seleccioná el **PDV** y la **FECHA**
2. En el panel derecho, elegí **T PAGO = Efectivo**
3. Ingresá el **IMPORTE** recaudado en efectivo
4. Hacé clic en **Ingresar rendición**
5. Repetí para otros tipos de pago si es necesario
6. Hacé clic en **Guardar** para cerrar el lote

### Rendir tarjetas
1. Hacé clic en **Cupones** para abrir el popup
2. Seleccioná (con el checkbox) los cupones a incluir
3. Cerrá el popup — los cupones quedan en la rendición en curso
4. (Opcional) Ingresá también efectivo u otros medios
5. Hacé clic en **Guardar**

### Rendir transferencias / cheques
1. Elegí el **T PAGO** correspondiente (Cheque, Transferencia, etc.)
2. Ingresá el **IMPORTE**, el **BANCO** y el **COMP#** del depósito
3. Hacé clic en **Ingresar rendición** y luego **Guardar**

---

## Notas importantes

- El lote guardado queda en estado **Pendiente** hasta que un usuario con perfil habilitado lo apruebe desde la pantalla **Cobranza Aprobación** (3.24).
- Se pueden hacer **múltiples lotes por día** (uno por tipo de pago, o uno general, según la operatoria del negocio).
- El campo **Compensaciones** aparece sólo cuando existen saldos de compensaciones para el vendedor seleccionado.
- Los **Cupones** que se muestran en el popup son sólo los del día seleccionado y del PDV activo, que aún no fueron incluidos en ningún lote anterior.
