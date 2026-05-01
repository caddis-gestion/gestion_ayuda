# 4.08 CUENTA CORRIENTE DE PROVEEDORES
### Módulo 4 — Compras

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Compras → Cuenta Corriente de Proveedores

---

<img src="imagenes/pantalla_cta_cte_proveedores.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Cuenta Corriente de Proveedores** permite ver y gestionar la deuda pendiente con cada proveedor y aplicar pagos a sus facturas. Desde aquí podés:

- Consultar las facturas pendientes de pago de un proveedor
- Registrar una nueva Orden de Pago e imputarla a facturas específicas
- Realizar pagos parciales o dejar el saldo a cuenta para futuros pagos
- Ver el historial completo de compras y pagos del proveedor
- Eliminar Órdenes de Pago no aplicadas
- Gestionar adelantos (saldos a cuenta)

---

## ¿Cómo acceder?

**Menú → Compras → Cuenta Corriente de Proveedores**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PROVEEDOR** | Proveedor al que se le realizará el pago. Al seleccionarlo, la grilla de Facturas Pendientes se actualiza automáticamente. |
| **OP Nº** | Número de la Orden de Pago generada. Solo lectura; el sistema lo asigna automáticamente. |
| **OP FECHA** | Fecha de la orden de pago. Por defecto, la fecha actual. |
| **IMPORTE** | Importe total de los valores ingresados (cheques, efectivo, transferencias) para esta orden de pago. Solo lectura; se completa automáticamente al ingresar el pago. |
| **APLICAR** | Monto total a descontar de las facturas seleccionadas (fondo amarillo). Debe coincidir con IMPORTE para que el pago quede completamente imputado. |
| **OBSERVACIONES** | Notas adicionales sobre el pago. |

### Botones de acción

| Botón | Descripción |
|---|---|
| **Orden de Pago** | Abre el popup para ingresar los valores del pago (efectivo, cheque, transferencia, etc.) |
| **Cta Cte** | Muestra el historial completo de compras y pagos del proveedor |
| **Adelantos** | Muestra las órdenes de pago a cuenta (adelantos sin factura asignada) disponibles para aplicar |
| **Aplicar** | Aplica los montos ingresados en la columna PAGO a las facturas correspondientes |

---

## Grilla: Facturas Pendientes (superior derecha)

Muestra todas las facturas que aún tienen saldo pendiente con el proveedor seleccionado.

| Columna | Descripción |
|---|---|
| Checkbox | Permite seleccionar las facturas a las que se aplicará el pago |
| Tipo | Tipo de comprobante (A, B, C). Las filas tipo **OP** con importe negativo representan saldos a cuenta (adelantos disponibles). |
| Numero | Número de la factura |
| Fecha | Fecha de emisión |
| Importe | Importe original de la factura |
| **Pendiente** | Saldo pendiente de pago (resaltado en amarillo) |
| **Pago** | Monto del pago a aplicar a esta factura en la operación actual |
| Observaciones | Notas adicionales (ej: "Saldo a Cuenta") |
| Ret. IIBB (por provincia) | Columnas opcionales con las retenciones de IIBB calculadas automáticamente según la provincia configurada |

---

## Grilla: Valores Pagados (inferior derecha)

Muestra los valores ingresados para la orden de pago en curso.

| Columna | Descripción |
|---|---|
| Tipo Pago | Medio de pago (Efectivo, Cheque, Transferencia, etc.) |
| Importe | Monto del valor |
| Banco | Banco o entidad financiera utilizada |
| Chq/Boleta | Número de cheque, boleta de depósito u otro código de referencia |
| Fecha | Fecha del valor |
| Provincia | Provincia de la cuenta (para retenciones de IIBB) |
| Certificado | Número de certificado de retención emitido |

---

## Popup — Orden de Pago

Al hacer clic en **Orden de Pago** se abre el popup para registrar los medios de pago:

| Campo / Columna | Descripción |
|---|---|
| **TIPO** | Medio de pago: Efectivo, Cheque, Transferencia, etc. |
| Campo importe | Monto del valor a ingresar |
| **Ingresar** | Agrega el valor a la grilla del popup |
| Grilla (Tipo Pago / Importe / Entidad) | Lista los medios de pago ingresados en esta sesión |
| Ícono Borrar | Elimina un valor ingresado antes de aceptar |
| **Cheques** | Abre el subpanel para registrar el detalle de cheques (banco, número, fecha, provincia) |
| **Aceptar** | Confirma el ingreso de valores y los transfiere a la grilla **Valores Pagados** de la pantalla principal |

Una vez aceptado, el campo **IMPORTE** del formulario se actualiza con el total ingresado.

---

## Documento generado — Orden de Pago

Al aplicar el pago, el sistema genera automáticamente el comprobante **Orden de Pago** con el siguiente detalle:

- Número de OP y fecha
- Razón social, domicilio y CUIT del emisor
- Proveedor, CUIT y domicilio
- Tabla con: Fecha, Comprobante afectado, Facturado, Saldo, Pago
- Total pagado

Este comprobante puede imprimirse o consultarse desde la pantalla **Cta Cte**.

---

## Paso a paso — Registrar un pago a proveedor

1. Seleccionar el **Proveedor**
2. En la grilla de **Facturas Pendientes**, tildar el checkbox de las facturas a cancelar
3. En la columna **Pago**, ingresar el monto a aplicar a cada factura seleccionada
4. Hacer clic en **Orden de Pago** e ingresar los valores en el popup (cheque, transferencia, efectivo)
5. Hacer clic en **Aceptar** — los valores aparecen en la grilla **Valores Pagados** y el campo IMPORTE se actualiza
6. Verificar que **IMPORTE** y **APLICAR** coincidan
7. Hacer clic en **Aplicar** para confirmar la operación

El sistema genera la Orden de Pago con numeración automática. Las facturas abonadas reducen su saldo **Pendiente**.

> Si el importe pagado supera el total de las facturas seleccionadas, la diferencia queda como **Saldo a Cuenta** (tipo OP negativo en la grilla de Facturas Pendientes) y puede aplicarse a futuros pagos.

---

## Cta Cte — Historial completo del proveedor

Al hacer clic en **Cta Cte** se abre una ventana con el historial completo de compras y pagos del proveedor.

### Filtros

| Campo | Descripción |
|---|---|
| **DESDE / HASTA** | Rango de fechas a consultar |
| **Buscar** | Aplica el filtro y recarga la grilla |

### Grilla del historial

| Columna | Descripción |
|---|---|
| Fecha | Fecha del comprobante |
| Tipo | Tipo de comprobante (vacío = factura, OP = Orden de Pago) |
| Nro | Número de comprobante |
| Importe | Importe del movimiento (negativo = pago realizado) |
| Acumulado | Saldo acumulado hasta ese movimiento |
| Observaciones | Notas del comprobante |

**Acciones sobre cada fila:**
- **Ícono Borrar:** Elimina la OP — solo si no tiene aplicaciones asociadas
- **Ícono Copiar:** Consulta o copia el comprobante
- **Ícono Detalle (flecha):** Abre el detalle de aplicaciones de la Orden de Pago

---

## Eliminar una Orden de Pago

Para eliminar una Orden de Pago ya registrada:

1. Hacer clic en **Cta Cte** para abrir el historial del proveedor
2. Ubicar la fila de la OP a eliminar (tipo **OP**)
3. Hacer clic en el **ícono Detalle** de esa fila — se abre la ventana **Orden Pago XXXX** con las aplicaciones asociadas

   | Columna | Descripción |
   |---|---|
   | Aplicacion | Número de la aplicación |
   | Fecha | Fecha de la aplicación |
   | Importe | Importe aplicado |
   | Fc_Asociada | Número de la factura a la que fue imputada |
   | Observaciones | Notas |

4. Eliminar cada aplicación haciendo clic en el **ícono Borrar** de cada fila
5. Una vez eliminadas todas las aplicaciones, cerrar la ventana
6. En la grilla del historial, hacer clic en el **ícono Borrar** de la fila de la OP para eliminarla

> No es posible eliminar una OP que tenga aplicaciones pendientes. Primero deben borrarse todas las aplicaciones.

---

## Informe — Cuenta Corriente con Proveedores

Desde el módulo de **Informes** del sistema existe el informe **Cta Cte Proveedores**, que permite obtener un detalle completo de toda la historia de compras y pagos con cada proveedor.

### Filtros del informe

| Campo | Descripción |
|---|---|
| **PROVEEDOR** | Proveedor específico a consultar (dejar vacío para todos) |
| **DESDE / HASTA** | Rango de fechas |
| **VISTA** | **DETALLE**: muestra todas las facturas y pagos del proveedor / **TOTALES**: muestra un resumen por proveedor |

### Formatos de salida

PTL, XLS, TXT, PDF

### Contenido del informe (vista TOTALES)

| Columna | Descripción |
|---|---|
| Cliente (Proveedor) | Nombre del proveedor |
| CUIT | CUIT del proveedor |
| Importe | Saldo actual de la cuenta corriente |
| Ultimos_Movimientos | Fechas de la última factura y el último pago registrados |

La vista **DETALLE** muestra el desglose completo de cada factura y cada pago efectuado al proveedor.

---

## Notas importantes

- Las **retenciones de IIBB** se calculan automáticamente según la configuración de tasas por provincia para el proveedor. Las columnas de retención aparecen solo si existen tasas configuradas.
- Si el pago supera el monto de las facturas seleccionadas, la diferencia queda como **saldo a cuenta** (tipo OP negativo en la grilla) para aplicar en futuros pagos.
- El campo **APLICAR** (fondo amarillo) refleja el total que se descontará de las facturas; debe coincidir con el total de valores ingresados en la Orden de Pago.
- Para eliminar una OP es obligatorio eliminar primero todas sus aplicaciones desde el ícono Detalle en la pantalla Cta Cte.

> Relacionado: [**Orden de Pago a Proveedores**](https://ayuda.caddis.com.ar/instructivos/04_COMPRAS_Orden_Pago_Proveedores.pdf) (4.09) — vista dedicada a ingresar y gestionar órdenes de pago
