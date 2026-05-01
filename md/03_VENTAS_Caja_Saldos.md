# 3.26 CAJA SALDOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Caja → Caja Saldos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Caja Saldos** es el mayor de caja del sistema. Muestra todos los movimientos de dinero de un punto de venta en un período, con un saldo acumulado en tiempo real. Incluye ventas, cobros de cuenta corriente, órdenes de pago y movimientos manuales de caja. Desde aquí podés:

- Ver el saldo de caja por tipo de pago (efectivo, tarjeta, cheque, etc.)
- Consultar el detalle de cada transacción: facturas, recibos, órdenes de pago y movimientos de caja
- Filtrar por PDV, caja individual, tipo de pago y rango de fechas
- Ver el **saldo inicial** (todo lo acumulado antes del período consultado)
- Acceder al detalle de cada comprobante

---

<img src="imagenes/pantalla_caja_saldos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Caja → Caja Saldos**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Filtros de consulta
- **Panel derecho:** Grilla de movimientos con saldo acumulado

---

## Panel izquierdo — Filtros

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a consultar |
| **CAJA** | Caja individual dentro del PDV. Opciones: TODO, CAJA 000 (sin asignación), cajas numeradas por usuario, CAJA 100 (MercadoLibre) |
| **PAGO** | Tipo de pago: TODO, Efectivo, Tarjeta Crédito, Tarjeta Débito, Cheque, Transferencia, etc. |
| **DESDE** | Fecha de inicio del período (por defecto: hace 1 mes) |
| **HASTA** | Fecha de fin del período (por defecto: hoy) |

---

## Panel derecho — Grilla de movimientos

La grilla muestra todos los movimientos del período seleccionado ordenados cronológicamente, comenzando con el **saldo inicial**:

| Columna | Descripción |
|---|---|
| Fecha | Fecha del movimiento |
| Importe | Monto del movimiento (positivo = ingreso, negativo = egreso) |
| **Acumulado** | Saldo corriente hasta ese movimiento (resaltado en amarillo) |
| Pago Tipo | Tipo de pago del movimiento |
| Tipo | Tipo de comprobante: TK, B, A, C, RCC, OPP, MTO, etc. |
| Comprobante | Número del comprobante |
| Detalle | Cliente o nombre asociado al movimiento |
| PDV | Punto de venta |
| Caja | Número de caja |
| Usuario | Usuario que registró el movimiento |
| Observaciones | Notas del movimiento |

### Primera fila — Saldo inicial

La primera fila muestra el **saldo inicial**: todo el dinero acumulado en esa caja/PDV/tipo de pago antes de la fecha de inicio del filtro. Sirve como punto de partida para el cálculo del acumulado.

### Tipos de comprobante en la grilla

| Tipo | Origen |
|---|---|
| TK, B, A, C, M, X, etc. | Ventas (facturas y tickets) |
| RCC | Recibo de cobro de cuenta corriente |
| OPP | Orden de pago a proveedor (egreso, importe negativo) |
| MTO | Movimiento manual de caja (ingreso o egreso) |

### Botón Detalle

Al hacer doble clic en una fila de factura, se abre el comprobante completo en una ventana emergente.

---

## Casos de uso frecuentes

### Ver el saldo de efectivo de un PDV hoy
1. Seleccioná el **PDV**
2. En **PAGO** elegí Efectivo
3. Poné **DESDE** y **HASTA** = fecha de hoy
4. El primer registro muestra el saldo inicial (efectivo acumulado de días anteriores)
5. El último registro del acumulado es el saldo actual

### Reconciliar los movimientos de una caja
1. Seleccioná el **PDV** y la **CAJA** específica
2. Ingresá el rango de fechas del período a reconciliar
3. Dejá **PAGO = TODO** para ver todos los tipos

### Verificar un comprobante específico
1. Ingresá el PDV y las fechas
2. Buscá en la columna Comprobante o usá el filtro de fecha acotado
3. Hacé doble clic en la fila para ver el detalle

---

## Notas importantes

- La columna **Acumulado** (en amarillo) siempre refleja el saldo running desde el inicio del período, incluyendo el saldo inicial.
- Los egresos (Órdenes de Pago) se muestran con **importe negativo** y reducen el acumulado.
- Al filtrar por **CAJA específica**, el saldo inicial sólo considera los movimientos de esa caja (no de todo el PDV).
- Esta pantalla es de **sólo consulta** — no se pueden modificar movimientos desde aquí.
