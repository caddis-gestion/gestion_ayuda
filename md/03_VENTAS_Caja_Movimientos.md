# 3.28 CAJA MOVIMIENTOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Caja → Caja Movimientos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Caja Movimientos** permite registrar ingresos y egresos manuales de caja que no provienen de una venta ni de un cobro. Se usa para situaciones como gastos en efectivo, adelantos, fondo de caja, viáticos, etc. Desde aquí podés:

- Registrar ingresos de caja (fondos recibidos)
- Registrar egresos de caja (gastos o pagos menores)
- Consultar el historial de movimientos manuales por fecha y PDV
- Modificar o borrar movimientos ya registrados
- Exportar el detalle a PDF

> ℹ️ Los movimientos manuales de caja se identifican con el tipo **MTO** en el **Caja Saldos** (3.26). Afectan el saldo de caja.

---

<img src="imagenes/pantalla_caja_movimientos.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Caja → Caja Movimientos**

---

## Configuración previa

Antes de operar con cajas es necesario configurar dos cosas:

### 1. Cantidad de cajas por PDV — PDV Parámetros

Desde **Administración → PDV Parámetros**, en el campo **CAJAS** se define cuántas cajas tendrá cada Punto de Venta. Guardar para confirmar.

### 2. Asignar cajero — ABM / Accesos / Cajeros

Desde **Administración → Accesos → Cajeros**, se vincula cada usuario con su PDV y su número de caja. Cada usuario puede tener **una única caja** en **un único punto de venta**.

| Campo | Descripción |
|---|---|
| **USUARIO** | Usuario del sistema a asignar como cajero |
| **PDV** | Punto de venta al que pertenece |
| **CAJA** | Número de caja asignada |

---

## Tipos de movimientos de caja

Existen dos tipos de eventos que generan movimientos en la caja:

| Tipo | Descripción |
|---|---|
| **Comprobantes** | Facturas, notas de crédito y otros comprobantes emitidos. Se generan automáticamente al facturar. |
| **Movimientos manuales** | Ingresos y egresos registrados manualmente desde esta pantalla (extracciones, pagos, fondos, etc.) |

Los movimientos manuales deben asociarse a un **concepto** que debe estar previamente creado en **Caja Conceptos**.

**Ejemplos de movimientos manuales:**
- Envío de dinero a otra sucursal
- Pago de alquiler
- Gastos de envíos
- Adelanto de sueldos

---

## Control de acceso por usuario

Cada usuario **solo puede ver y operar su propia caja**. No tiene acceso a los movimientos ni al saldo de las cajas de otros usuarios.

### Transferencia entre cajas

Para transferir dinero de una caja a otra, **ambos cajeros deben registrar el movimiento**:

1. El cajero que envía registra un **EGRESO**
2. El cajero que recibe registra un **INGRESO**

> ⚠️ Si solo uno de los dos registra el movimiento, el sistema lo interpretará como una **extracción** y el saldo quedará descuadrado.

---

## Descripción general de la pantalla

La pantalla tiene dos zonas en el panel izquierdo (formulario de carga y filtro de consulta) y una grilla en el panel derecho.

---

## Panel izquierdo — Formulario de nuevo movimiento

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta al que pertenece el movimiento |
| **FECHA** | Fecha del movimiento. Por defecto: hoy. |
| **MOVIMIENTO** | Tipo: **INGRESO** (entrada de dinero) o **EGRESO** (salida de dinero) |
| **CONCEPTO** | Concepto del movimiento (lista configurable: gastos, adelantos, fondos, etc.) |
| **TIPO** | Medio de pago: Efectivo, Transferencia, etc. (solo los habilitados para caja) |
| **IMPORTE** | Monto del movimiento |
| **OBSERVACIONES** | Descripción libre del movimiento |

### Sección MOSTRAR (filtro de consulta)

| Campo | Descripción |
|---|---|
| **DESDE** | Fecha de inicio para ver movimientos en la grilla (por defecto: primero del mes) |
| **HASTA** | Fecha de fin (por defecto: hoy) |

---

## Panel derecho — Grilla de movimientos

Muestra todos los movimientos manuales de caja del período seleccionado para el PDV activo:

| Columna | Descripción |
|---|---|
| Fecha | Fecha del movimiento |
| Comprobante | Número generado automáticamente (formato: I/E-XXXXXXXX) |
| Pago Tipo | Medio de pago utilizado |
| Concepto | Concepto del movimiento |
| Importe | Monto (en pesos) |
| Divisa | Monto en moneda extranjera (solo si aplica) |
| Usuario | Quien registró el movimiento |
| PDV | Punto de venta |
| Caja | Número de caja |

**Acciones disponibles:**
- **Modificar:** Permite editar el movimiento
- **Borrar:** Elimina el movimiento (lo marca como anulado)

**Botón PDF:** Exporta la grilla actual a PDF.

---

## Paso a paso — Registrar un egreso de caja

1. Seleccioná el **PDV**
2. Ingresá la **FECHA** del movimiento
3. Seleccioná **MOVIMIENTO = EGRESO**
4. Elegí el **CONCEPTO** correspondiente (ej. "Gastos varios")
5. Seleccioná el **TIPO** de dinero (generalmente Efectivo)
6. Ingresá el **IMPORTE**
7. Agregá una **OBSERVACIÓN** descriptiva (ej. "Compra de útiles de oficina")
8. Guardá el registro

> El movimiento aparecerá en la grilla y quedará registrado en el **Caja Saldos** como tipo MTO con importe negativo.

---

## Pantalla relacionada — Caja Saldos

Desde **Ventas y Facturación → Facturación → Caja → Caja Saldos** se puede controlar todos los movimientos existentes en las cajas, incluyendo tanto los comprobantes como los movimientos manuales.

### Filtros

| Campo | Descripción |
|---|---|
| **POS** | Punto de venta a consultar |
| **CAJA** | Número de caja (y usuario asignado) |
| **PAGO** | Medio de pago a filtrar (o TODO para ver todos) |
| **DESDE** | Fecha de inicio del período |
| **HASTA** | Fecha de fin del período |

**Botón Actualizar:** Recalcula y refresca la grilla con los filtros aplicados.

### Grilla

| Columna | Descripción |
|---|---|
| Fecha | Fecha del movimiento |
| Importe | Importe del movimiento (negativo para egresos) |
| Acumulado | Saldo acumulado hasta ese movimiento |
| Pago Tipo | Medio de pago |
| Tipo | Tipo de movimiento (RCC, MTO, NCEB, etc.) |
| Comprob ante | Número de comprobante asociado |
| Detalle | Descripción del movimiento o cliente/proveedor |
| PDV | Punto de venta |
| Caja | Número de caja |
| Usuario | Usuario que registró el movimiento |

> La primera fila muestra el **Saldo inicial** del período seleccionado, y al pie de la grilla figura el **saldo total** acumulado.

---

## Notas importantes

- Los conceptos disponibles en el selector **CONCEPTO** se configuran desde **Caja Conceptos**.
- Un EGRESO reduce el saldo de caja; un INGRESO lo aumenta.
- Los movimientos registrados aquí **no generan comprobante fiscal** ni afectan el stock.
- Cada usuario **solo ve su propia caja**; no puede acceder a las cajas de otros usuarios.
- Para transferencias entre cajas, **ambos cajeros deben registrar su parte** (egreso + ingreso); de lo contrario el sistema lo trata como una extracción.
