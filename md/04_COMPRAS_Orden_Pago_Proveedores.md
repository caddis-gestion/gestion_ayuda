# 4.09 ORDEN DE PAGO A PROVEEDORES
### Módulo 4 — Compras

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Compras → Orden de Pago a Proveedores

---
<img src="imagenes/pantalla_orden_pago_proveedores.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Orden de Pago a Proveedores** permite registrar los pagos realizados a proveedores, asociándolos directamente a las facturas pendientes. A diferencia de la pantalla de Cuenta Corriente, esta vista está orientada específicamente al proceso de pago con cálculo automático de retenciones de IIBB. Desde aquí podés:

- Ver las facturas pendientes de un proveedor y seleccionar cuáles se cancelan
- Registrar los valores del pago (efectivo, cheques, transferencias)
- Calcular automáticamente las retenciones de IIBB aplicables según la provincia
- Generar la Orden de Pago y aplicarla a las facturas

---

## ¿Cómo acceder?

**Menú → Compras → Orden de Pago a Proveedores**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PDV** | Caja / punto de venta desde donde se realiza el pago. |
| **PROVEEDOR** | Proveedor al que se le paga. Al seleccionarlo, la grilla de facturas pendientes se carga automáticamente. |
| **OP Nº** | Número de Orden de Pago (asignado automáticamente por el sistema, solo lectura). |
| **OP FECHA** | Fecha de la orden de pago. |
| **IMPORTE** | Total de los valores ingresados (efectivo, cheques, etc.). Solo lectura. |
| **APLICAR** | Monto total a aplicar sobre las facturas seleccionadas (fondo amarillo). Solo lectura. |
| **OBSERVACIONES** | Texto libre con notas del pago. |

---

## Grilla: Facturas Pendientes

Muestra todas las facturas que aún tienen saldo sin cancelar para el proveedor seleccionado.

| Columna | Descripción |
|---|---|
| Checkbox | Tildando la fila se selecciona la factura para incluirla en el pago. |
| Tipo | Tipo de comprobante (A, B, C, NC, OP). |
| Número | Número de factura. |
| Fecha | Fecha de emisión. |
| Importe | Importe original de la factura. |
| Pendiente | Saldo pendiente (en amarillo). |
| Pago | Monto a aplicar sobre esa factura. |
| Observaciones | Notas. |
| Ret. IIBB (por provincia) | Monto de retención calculado automáticamente para cada provincia configurada (CABA, Buenos Aires, Santa Fe, Tucumán, etc.). |

---

## Panel inferior: Valores ingresados

Muestra en un iframe los valores de pago ya cargados para la orden de pago en curso (similar a la grilla de Valores Pagados de Cta Cte Proveedores).

---

## Botones de acción

| Botón | Descripción |
|---|---|
| **Ingresar Pagos** | Abre el formulario para cargar los valores del pago (efectivo, cheques, transferencias, plataformas de pago). |
| **Cta Cte** | Muestra el estado de cuenta completo del proveedor. |

---

## Flujo típico — Generar una Orden de Pago

1. Seleccionar el **PDV** (caja de origen del pago)
2. Seleccionar el **Proveedor**
3. En la grilla, tildar las facturas que se van a cancelar y completar el monto en la columna **Pago**
4. Revisar las columnas de **Retención IIBB** para validar las retenciones calculadas
5. Hacer clic en **Ingresar Pagos** y cargar los valores (cheque, transferencia, efectivo)
6. Confirmar la Orden de Pago

---

## Diferencia con Cuenta Corriente de Proveedores

Ambas pantallas permiten registrar pagos a proveedores, pero tienen un enfoque distinto:

| Característica | Orden de Pago | Cta Cte Proveedores |
|---|---|---|
| Cálculo retenciones IIBB | Automático por factura | También disponible |
| Gestión de adelantos | No | Sí (botón Adelantos) |
| Vista dedicada a pagos | Sí | Visión integral (facturas + pagos) |

> Relacionado: [**Cuenta Corriente de Proveedores**](https://ayuda.caddis.com.ar/instructivos/04_COMPRAS_Cta_Cte_Proveedores.pdf) (4.08)
