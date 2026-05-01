# 3.31 CUENTA CORRIENTE DE CLIENTES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Cta Cte Clientes

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cuenta Corriente de Clientes** es la principal herramienta de cobro para clientes mayoristas. Permite ver todas las facturas pendientes de pago de un cliente y registrar los cobros imputando los pagos a las facturas correspondientes. Desde aquí podés:

- Ver el **saldo de cuenta corriente** de un cliente en tiempo real
- Consultar las facturas pendientes de cobro y sus importes
- Registrar cobros (en efectivo, cheque, transferencia, etc.) y aplicarlos a facturas específicas
- Ver el detalle de los valores ya cobrados para el recibo en curso
- Consultar el historial completo de la cuenta corriente
- Anular recibos no aprobados

---

<img src="imagenes/pantalla_cta_cte_clientes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Cta Cte Clientes**

---

## Requisito previo — Habilitar cliente para Cta Cte

Para poder facturar a cuenta corriente a un cliente, primero debe estar habilitado con **VENTA CTA CTE = SI** desde la pantalla **Facturación → Clientes → Clientes**.

Esta configuración la realiza el Administrador del sistema antes de comenzar a facturar. Una vez habilitado, al facturar al cliente aparecerá la opción de pago **Cta. Cte.** en el popup **Ingresar Pagos** de la facturación, y mostrará el saldo actual de la cuenta corriente.

> Si el cliente no tiene VENTA CTA CTE = SI, la opción de pago a cuenta corriente no estará disponible al facturar.

---

## Descripción general de la pantalla

La pantalla está dividida en tres zonas:

- **Panel izquierdo:** Formulario del recibo + saldo del cliente
- **Panel derecho superior:** Facturas pendientes de cobro del cliente
- **Panel derecho inferior:** Valores cobrados para el recibo en curso

---

## Panel izquierdo — Datos del recibo

| Campo | Descripción |
|---|---|
| **CLIENTE** | Cliente mayorista a cobrar. Al seleccionarlo se cargan sus facturas pendientes. |
| **RECIBO** | Número de recibo. Se asigna automáticamente al guardar; también puede buscarse un recibo existente. |
| **FECHA** | Fecha del cobro (por defecto: hoy) |
| **IMPORTE** | Total cobrado (se completa automáticamente al ingresar cada cobro) |
| **APLICAR** | Total a imputar a facturas (campo en dorado). Puede diferir del IMPORTE si hay saldo a cuenta. |
| **COTIZACIÓN** | Solo visible en entornos multimoneda. Tipo de cambio para convertir cobros en divisa a pesos. |
| **No emitir ajustes** | Checkbox (solo si multimoneda). Evita que el sistema genere comprobantes de ajuste por diferencia de cambio. |
| **OBSERVACIONES** | Notas del cobro |

### Sección Saldo Cta Cte

Muestra el saldo actual del cliente (en tiempo real, se actualiza al seleccionar el cliente):

| Campo | Descripción |
|---|---|
| **PESOS** | Saldo en pesos (en dorado). Positivo = deuda del cliente. |
| **DIVISA** | Saldo en moneda extranjera (solo si multimoneda) |

### Botones de acción

| Botón | Descripción |
|---|---|
| **Ingresar Cobro** | Abre el popup **Recibo** para registrar los medios de pago (efectivo, cheque, transferencia, etc.) |
| **Ver Cta Cte** | Muestra el historial completo de la cuenta corriente del cliente |
| **Ver Detalle Valores** | Muestra el detalle de los valores cobrados en recibos anteriores |
| **Aplicar** | Aplica los montos ingresados en la columna COBRO a las facturas correspondientes |
| **Actualizar** | Recarga los datos de la pantalla |

---

## Panel derecho superior — Facturas pendientes

Muestra todas las facturas del cliente que tienen saldo pendiente de cobro:

| Columna | Descripción |
|---|---|
| Tipo | Tipo de comprobante (X, NCEA, NCX, etc.) |
| Numero | Número de la factura |
| Fecha | Fecha de emisión |
| Total | Total original de la factura |
| **Pendiente** | Saldo pendiente de cobro (resaltado en amarillo) |
| **Cobro** | Campo editable: monto a aplicar a esta factura en el cobro actual |
| Deuda U$S | Deuda en divisa extranjera (solo si multimoneda) |
| Actualizado | Valor actualizado al tipo de cambio actual (multimoneda) |
| Cotizacion | Tipo de cambio original de la factura (multimoneda) |
| Usuario | Usuario que emitió la factura |

También pueden aparecer filas de **Notas de Crédito** (en negativo) y **Saldo a Cuenta** (recibos anteriores no imputados que actúan como crédito a favor del cliente). Ambos pueden aplicarse a facturas pendientes ingresando el monto en la columna **Cobro**.

---

## Panel derecho inferior — Valores cobrados

Muestra los medios de pago ya ingresados para el recibo en curso (antes de guardar):

| Columna | Descripción |
|---|---|
| Tipo Pago | Medio de pago (Efectivo, Cheque, Transferencia, etc.) |
| Importe | Monto del valor |
| Entidad | Banco o tarjeta (según el medio) |

---

## Popup — Recibo (Ingresar Cobro)

Al hacer clic en **Ingresar Cobro** se abre el popup **Recibo**:

| Campo / Columna | Descripción |
|---|---|
| **TIPO** | Medio de pago: Efectivo, Cheque, Transferencia, etc. |
| Campo importe | Monto del cobro a ingresar |
| **Ingresar** | Agrega el cobro a la grilla del popup |
| Grilla (Tipo Pago / Importe / Entidad) | Lista los medios de pago ingresados en esta sesión |
| Ícono Borrar | Elimina un cobro ingresado antes de aceptar |
| **Aceptar** | Confirma el cobro y lo transfiere a la grilla **Valores Cobrados** de la pantalla principal |

Una vez aceptado, el campo **IMPORTE** del panel izquierdo se actualiza con el total cobrado.

---

## Paso a paso — Registrar un cobro de cuenta corriente

1. Seleccioná el **CLIENTE**
2. Verificá el **Saldo Cta Cte** del cliente
3. En la grilla de **Facturas Pendientes**, ingresá en la columna **Cobro** el monto a aplicar a cada factura
4. Hacé clic en **Ingresar Cobro** para registrar el medio de pago
5. En el popup **Recibo**, seleccioná el tipo de pago, ingresá el importe y hacé clic en **Ingresar**
6. Hacé clic en **Aceptar** — el importe aparece en la grilla **Valores Cobrados**
7. Verificá que los campos **IMPORTE** y **APLICAR** coincidan
8. Completá las **OBSERVACIONES** si es necesario
9. Hacé clic en **Aplicar** para guardar el recibo

El sistema emite un recibo con numeración automática. La pantalla se actualiza mostrando la nueva lista de facturas pendientes con los saldos reducidos.

> Si **IMPORTE** y **APLICAR** no coinciden, la diferencia queda como **Saldo a Cuenta** del cliente (crédito para futuras facturas).

---

## Ver Cta Cte — Historial completo

Al hacer clic en **Ver Cta Cte** se abre una ventana con el historial completo de la cuenta corriente del cliente.

### Filtros

| Campo | Descripción |
|---|---|
| **DESDE / HASTA** | Rango de fechas a consultar |
| **Buscar** | Aplica el filtro y recarga la grilla |

### Grilla del historial

| Columna | Descripción |
|---|---|
| Fecha | Fecha del comprobante |
| Tipo | Tipo de comprobante (X = factura, RC = recibo de cobro, NCX = nota de crédito, NDX = nota de débito, EA = ajuste) |
| Comprobante | Número de comprobante |
| Importe | Importe del movimiento (negativo = cobro o crédito) |
| Actualizado | Valor actualizado al tipo de cambio vigente (multimoneda) |
| Acumulado | Saldo acumulado hasta ese movimiento |
| Divisa | Importe en moneda extranjera (si aplica) |
| Observaciones | Notas del comprobante |
| Usuario | Usuario que registró el movimiento |

**Acciones sobre cada fila:**
- **Ícono Borrar:** Elimina el comprobante — solo disponible si el recibo **no está aprobado**
- **Ícono Copiar:** Copia o consulta el detalle del comprobante
- **Ícono Flecha:** Navega al comprobante de origen

> Para eliminar un recibo primero se deben eliminar sus **aplicaciones** (las imputaciones a facturas). Luego se puede borrar el recibo.

---

## Anulación de un cobro

Para anular un cobro **no aprobado**:

1. Abrí el **Ver Cta Cte** del cliente
2. Ubicá el recibo (tipo RC) a anular
3. Si el recibo tiene aplicaciones a facturas, borrá primero cada aplicación usando el ícono de borrar en la fila correspondiente
4. Una vez sin aplicaciones, borrá el recibo con el ícono de borrar

> Solo se pueden eliminar recibos en estado **no aprobado**. Si el cobro ya fue aprobado, primero debe desaprobarse desde **Cobranza Aprobación**.

---

## Desaprobar un cobro ya aprobado

Si un cobro fue aprobado y necesita anularse:

1. Ir a **Ventas y Facturación → Cobranza → Cobranza Aprobación**
2. Filtrar por **VENTA = CTA CTE**, rango de fechas que contenga el cobro y **APROBADO = SI**
3. Hacer clic en **Buscar**
4. Ubicar el recibo y hacer clic en el ícono del cesto para desaprobarlo
5. Una vez desaprobado, volver a **Cta Cte Clientes** y anular el recibo desde **Ver Cta Cte**

---

## Aprobación de cobros

Todos los cobros registrados en Cta Cte deben ser aprobados por un nivel superior para que se hagan efectivos y la deuda deje de figurar como pendiente.

La aprobación se realiza desde **Ventas y Facturación → Cobranza → Cobranza Aprobación**:

1. Seleccionar **VENTA = CTA CTE**
2. Ingresar el rango de fechas y hacer clic en **Buscar**
3. La grilla muestra los recibos pendientes de aprobación con columnas: Recibo, Fecha, Cliente, Importe, F_Aprobado, Usuario, Observaciones
4. Hacer clic en el ícono de aprobación (tilde) para aprobar cada recibo

> Hasta que el cobro no sea aprobado, la deuda del cliente sigue figurando como pendiente en la cuenta corriente.

---

## Notas importantes

- El campo **APLICAR** puede ser menor al **IMPORTE** cobrado: la diferencia queda como **Saldo a Cuenta** del cliente (crédito para futuras facturas).
- Si el cliente tiene **Saldo a Cuenta** (recibos anteriores no imputados), aparecen como filas en la grilla de facturas y pueden aplicarse ingresando el monto en la columna **Cobro**.
- Las **Notas de Crédito** emitidas al cliente aparecen en la grilla de Facturas Pendientes como filas negativas para ser relacionadas y aplicadas contra las facturas que les dieron origen.
- Para ver el historial completo de la cuenta corriente (no solo las facturas pendientes), usá el botón **Ver Cta Cte**.
- En entornos **multimoneda**, el sistema puede generar ajustes automáticos por diferencia de cotización al imputar pagos en divisa a facturas en pesos (a menos que se marque **No emitir ajustes**).
