# 3.23 CIERRE CAJA DIARIO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Cierre Caja Diario

---

## ¿Para qué sirve esta pantalla?

El **arqueo o cierre de caja** es un procedimiento contable que se realiza al final de la jornada de ventas o al final del turno del cajero. Su finalidad es verificar que el efectivo, los cupones de tarjeta, los cheques y demás comprobantes de pago físicos coincidan con los valores reportados por el sistema en la caja.

Caddis implementa este proceso en dos etapas:

1. **Creación del lote** (esta pantalla): el cajero informa al sistema los importes recaudados por tipo de pago. El sistema genera un número de lote con estado **Pendiente**.
2. **Aprobación** (pantalla **Cobranza Aprobación** — 3.24): el área administrativa verifica físicamente lo recibido contra el lote y lo aprueba.

Desde esta pantalla podés:

- Ver el **saldo pendiente de rendir** del día por PDV
- Registrar rendiciones por tipo de pago: efectivo, tarjetas, cheques, transferencias, plataformas digitales, gastos
- Seleccionar los cupones de tarjeta del día para incluirlos en la rendición
- Consultar los **lotes ya cerrados** y su estado (Pendiente / Aprobado / Anulado)
- Imprimir o anular lotes de rendición

> ℹ️ Esta pantalla registra la rendición pero **no la aprueba**. La aprobación la realiza el área administrativa desde **Cobranza Aprobación** (3.24).

---

<img src="imagenes/pantalla_cobros.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Cierre Caja Diario**

---

## Descripción general de la pantalla

La pantalla está dividida en tres zonas:

- **Panel izquierdo:** Selección de PDV y fecha, resumen de facturación del día y lotes ya rendidos
- **Panel derecho superior:** Formulario "Rendición del Día" para ingresar cada ítem de la rendición
- **Panel derecho inferior:** Grilla con los ítems que componen la rendición en curso (aún no guardada como lote)

**Botones principales:**
- **Nuevo:** Limpia el panel derecho para comenzar una nueva rendición
- **Buscar:** Permite buscar una rendición existente

---

## Panel izquierdo — Filtro y saldos del día

### Campos de filtro

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a rendir. Al cambiar recarga todos los datos del día. |
| **FECHA** | Fecha a rendir. Por defecto: hoy. Acepta fechas anteriores para rendiciones atrasadas. |

### Indicadores de saldo

| Indicador | Qué representa |
|---|---|
| **SALDO** | Total facturado del día menos total ya rendido en lotes (en pesos) |
| **SALDO EF** | Ídem pero solo para efectivo |

> Un SALDO en cero indica que toda la facturación del día ya fue rendida.

### Grilla superior — Facturación del día por tipo de pago

Muestra un resumen de todo lo facturado en el día para el PDV seleccionado, agrupado por tipo de pago:

| Columna | Descripción |
|---|---|
| T.Pago | Tipo de pago (Efectivo, T.Crédito, T.Débito, MktPlaces, etc.) |
| Entidad | Banco o tarjeta |
| Pesos | Importe total en pesos |
| Divisa | Importe en moneda extranjera (si aplica) |

### Cuadro resumen PAGOS / RENDIDO / PENDIENTE / ACUMULADO

Al cierre del día, el panel izquierdo muestra una tabla consolidada con el estado de cada medio de pago:

| Detalle | Pagos | Rendido | Pendiente | Acumulado |
|---|---|---|---|---|
| EFECTIVO | Total facturado | Ya rendido en lotes | Sin rendir | Acum. del período |
| DEBITO | … | … | … | … |
| T.CREDITO | … | … | … | … |
| CHEQUES | … | … | … | … |
| DEP/TRANSF | … | … | … | … |
| CTA CTE | … | … | … | … |
| MARKETPLACES | … | … | … | … |
| OTROS | … | … | … | … |
| **TOTAL** | | | | |
| DOLARES | … | … | … | … |

Esta tabla permite comparar de un vistazo lo facturado contra lo rendido y detectar diferencias por medio de pago.

### Indicador RECAUDADO

Muestra el total acumulado de todos los lotes ya cerrados y rendidos para ese día y PDV.

### Grilla inferior — Lotes del día

Lista todos los lotes de rendición cerrados para esa fecha y PDV:

| Columna | Descripción |
|---|---|
| Lote | Número de lote generado |
| Fecha | Fecha del lote |
| Importe | Total del lote |
| Estado | **Pendiente** (esperando aprobación) / **Aprobado** / **Anulado** |

**Acciones disponibles sobre cada lote:**
- **Imprimir:** Imprime el detalle de la rendición del lote
- **Borrar:** Anula el lote — solo disponible si el lote está en estado **Pendiente**

---

## Panel derecho superior — Rendición del Día

Aquí se ingresan los valores que componen la rendición para generar un nuevo lote.

### Campos

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de la rendición (por defecto la misma del filtro izquierdo) |
| **T PAGO** | Tipo de pago a rendir: Efectivo, Tarjeta Crédito, Tarjeta Débito, Cheque, Transferencia, Gastos, Compensaciones, MercadoPago, etc. |
| **IMPORTE** | Monto a rendir para ese tipo de pago |
| **BANCO** | Banco donde se depositó o se acredita el importe (para transferencias y cheques) |
| **COMP#** | Número de comprobante bancario (transferencia, depósito, etc.) |
| **OBSERVACIONES** | Texto libre para registrar aclaraciones (ej.: "lote cambio de cajera") |
| **VENDEDOR** | Selector de vendedor (visible solo cuando T PAGO = Compensaciones) |

### Botones

| Botón | Acción |
|---|---|
| *(flecha / Ingresar)* | Agrega el ítem a la grilla inferior de la rendición en curso (no guarda el lote todavía) |
| **Tarjetas** | Abre el popup de cupones de tarjeta del día para seleccionar los que se incluyen en la rendición |
| **Guardar** | Cierra la rendición y genera un número de lote. Aparece en la grilla de lotes del panel izquierdo con estado **Pendiente** |

---

## Panel derecho inferior — Ítems de la rendición en curso

Muestra los ítems ya ingresados que formarán el próximo lote al presionar **Guardar**:

| Columna | Descripción |
|---|---|
| Pago | Tipo de pago |
| Importe | Monto del ítem |
| Comprobante | Número de comprobante bancario o cupón |
| Observaciones | Notas del ítem |

- **Botón Borrar (cesto):** Elimina el ítem de la rendición en curso antes de guardar el lote.

---

## Popup de Tarjetas

Al hacer clic en **Tarjetas**, se abre una ventana con todos los cupones de tarjeta y plataformas digitales del día para ese PDV que aún no fueron incluidos en una rendición anterior.

| Columna | Descripción |
|---|---|
| Checkbox | Marca o desmarca el cupón para incluirlo en la rendición |
| Tipo | Tipo de comprobante de origen |
| Factura | Número de factura de origen |
| Fecha | Fecha de la transacción |
| Importe | Importe del cupón |
| Interés | Interés aplicado (si hay) |
| Entidad | Tarjeta o plataforma (VISA, Mastercard, MercadoPago, etc.) |
| Promo | Promoción aplicada (si hay) |
| Tarjeta | Últimos 4 dígitos de la tarjeta |
| Cuotas | Cantidad de cuotas |
| Tasa | Tasa de la tarjeta |
| Cupón | Número de cupón |
| CodAut | Código de autorización |
| Lote | Número de lote de tarjeta |

Al cerrar el popup, los cupones seleccionados quedan incluidos en la rendición en curso.

---

## Paso a paso — Rendir el día

### Rendir efectivo

1. Seleccioná el **PDV** y la **FECHA** en el panel izquierdo.
2. En el panel derecho, elegí **T PAGO = Efectivo**.
3. Ingresá el **IMPORTE** recaudado en efectivo. En **OBSERVACIONES** podés agregar un comentario.
4. Hacé clic en el botón de flecha (**Ingresar**) — el ítem aparece en la grilla inferior.
5. Si hay más tipos de pago, repetí los pasos 2 a 4.
6. Hacé clic en **Guardar** para cerrar el lote.

### Rendir tarjetas

1. Hacé clic en **Tarjetas** para abrir el popup.
2. Seleccioná con el checkbox los cupones del día a incluir.
3. Cerrá el popup — los cupones quedan en la rendición en curso.
4. (Opcional) Ingresá también efectivo u otros medios si los hubiera.
5. Hacé clic en **Guardar**.

### Rendir transferencias / cheques

1. Elegí el **T PAGO** correspondiente (Cheque, Transferencia, etc.).
2. Ingresá el **IMPORTE**, el **BANCO** y el **COMP#** del depósito o cheque.
3. Hacé clic en **Ingresar** y luego **Guardar**.

### Registrar gastos

Si el punto de venta tuvo gastos durante el día (ej.: cambio de cajero, gastos operativos):

1. Elegí **T PAGO = Gastos** (u el tipo correspondiente según configuración).
2. Ingresá el importe y una descripción en **OBSERVACIONES**.
3. Hacé clic en **Ingresar** y luego **Guardar**.

---

## Flujo completo del cierre de caja

| Paso | Responsable | Pantalla | Resultado |
|---|---|---|---|
| 1. Crear lote de rendición | Cajero / Vendedor | **Cierre Caja Diario** (esta pantalla) | Lote generado en estado **Pendiente** |
| 2. Entrega física del dinero y cupones | Cajero → Administración | — | El responsable entrega el efectivo y cupones del día |
| 3. Verificar y aprobar el lote | Administración | **Cobranza Aprobación** (3.24) | Lote cambia a estado **Aprobado** |

---

## Cobranza Aprobación — resumen

El área administrativa compara físicamente lo recibido (efectivo + cupones) con el lote del sistema. Si todo coincide, aprueba el lote desde la pantalla **Cobranza Aprobación** haciendo clic en el ícono de tilde verde.

- Una vez **Aprobado**, el lote ya no puede borrarse desde Cierre Caja Diario.
- Si se necesita editar un lote aprobado, el área administrativa debe primero **desaprobarlo** desde Cobranza Aprobación.

---

## Informe de Cierre de Caja Diario

Desde el módulo de **Informes** del sistema existe el informe **Cierre de Caja Diario**, que consolida por PDV y fecha los importes facturados por cada medio de pago:

| Columna | Descripción |
|---|---|
| POS | Punto de venta |
| Fecha | Fecha de la jornada |
| Facturado | Total facturado en el día |
| Efectivo | Total en efectivo |
| T.Débito | Total en tarjeta débito |
| T.Crédito | Total en tarjeta crédito |
| Cta Cte | Total en cuenta corriente |
| Cheque | Total en cheques |
| Depósito | Total en depósitos/transferencias |
| MktPlaces | Total en plataformas digitales (MercadoPago, etc.) |

Este informe está disponible en formatos PTL, XLS, TXT, PDF y ZIP.

---

## Notas importantes

- Se pueden crear **múltiples lotes por día** (uno por tipo de pago, uno por cajero, o uno general, según la operatoria del negocio). Esto es especialmente útil cuando el local tiene más de un cajero o se realizan cortes intermedios durante la jornada.
- El campo **Compensaciones** aparece solo cuando existen saldos de compensaciones para el vendedor seleccionado.
- Los cupones que se muestran en el popup de Tarjetas son solo los del día seleccionado y del PDV activo que aún no fueron incluidos en ningún lote anterior.
- Un lote en estado **Pendiente** puede borrarse (anularse) desde esta pantalla. Un lote **Aprobado** no puede borrarse hasta que administración lo desapruebe.
