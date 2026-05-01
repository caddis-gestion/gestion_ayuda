# 4.07 FACTURAS DE COMPRA
### Módulo 4 — Compras

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Compras → Facturas de Compra

---
<img src="imagenes/pantalla_facturas_compras.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturas de Compra** es el módulo central para registrar los comprobantes de compra de productos a proveedores. El registro de cada factura permite llevar la cuenta corriente con el proveedor y controlar qué facturas están pendientes de pago. Desde aquí podés:

- Registrar facturas de compra de mercadería, notas de crédito y notas de débito recibidas de proveedores
- Asociar la factura al remito de artículos o equipos ingresados al stock
- Controlar que los importes de la factura coincidan con lo ingresado al stock (semáforo de costos)
- Consultar el historial de facturas registradas por proveedor
- Modificar o borrar comprobantes existentes
- Ver el detalle de artículos de cada compra

---

## ¿Cómo acceder?

**Menú → Compras → Facturas de Compra**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PROVEEDOR** | Proveedor que emitió la factura. Al seleccionarlo se carga la grilla con sus facturas registradas. |
| **TIPO** | Tipo de compra (categoría general). Ej: Mercadería, Gastos, Servicios. |
| **CATEGORIA** | Subcategoría dentro del tipo seleccionado. |
| **RTOS. ARTICULOS** | Remito de artículos del stock asociado a esta factura. Al hacer clic en **BuscarArt** se abre un popup para seleccionar el remito de ingreso de mercadería correspondiente. |
| **RTOS. EQUIPOS** | Remito de equipos con NSE (número de serie) asociado. Solo visible si la empresa usa gestión de equipos con NSE. |
| **FEC. COTBLE** | Fecha contable del comprobante (puede diferir de la fecha de emisión). |
| **FC. FECHA** | Fecha de emisión de la factura del proveedor. |
| **FC. VENCE** | Fecha de vencimiento de la factura (para calcular días de crédito). |
| **FACTURA** | Tipo de comprobante (A, B, C, E, X, NC-A, NC-B, NC-C, ND-A, etc.) y número de factura en formato PPPP-NNNNNNNNN. |
| **MONEDA** | Moneda de la factura (pesos, dólares, etc.). |
| **COTIZACION** | Cotización de la moneda al momento de la compra. Para pesos siempre es 1. |
| **TOTAL** | Total calculado automáticamente a partir de los importes ingresados. |

### Sección: Detalle de Importes

| Campo | Descripción |
|---|---|
| **GRAVADO** | Monto neto gravado (base imponible para IVA). |
| **NO GRAVADO** | Monto no gravado por IVA. |
| **EXENTO** | Monto exento de IVA. |
| **DESCUENTO** | Descuento global sobre la factura. |
| **SUBTOTAL** | Gravado + No Gravado + Exento − Descuento. |
| **IVA 2,5%** | Monto de IVA a tasa 2,5%. |
| **IVA 10,5%** | Monto de IVA a tasa 10,5%. |
| **IVA 21,0%** | Monto de IVA a tasa 21,0%. |
| **IVA 27,0%** | Monto de IVA a tasa 27,0%. |
| **IMP INT** | Impuestos internos. |
| **PERC IVA** | Percepción de IVA retenida por el proveedor. |
| **PERC IIBB 1 y 2** | Percepción de Ingresos Brutos por provincia (hasta 2 provincias). |
| **IMP VARIOS** | Otros impuestos o cargos. |
| **GASTOS** | Gastos de flete, seguro u otros incluidos en la factura. |
| **OBSERVACIONES** | Notas adicionales sobre la factura. |

### Adjunto de imagen / PDF

Se puede adjuntar la imagen escaneada de la factura (JPG/PNG) o el PDF original como comprobante digital. Al hacer clic en el ícono de insertar se selecciona el archivo desde el equipo.

---

## Grilla de compras registradas

La grilla del lado derecho muestra todas las facturas registradas para el proveedor seleccionado, con:

| Columna | Descripción |
|---|---|
| Fecha Contable | Fecha contable de la factura. |
| Factura Fecha | Fecha de emisión. |
| Factura Tipo | Tipo de comprobante (A, B, NC-A, etc.). |
| Factura Numero | Número de factura. |
| Moneda | Divisa del comprobante. |
| Cotización | Tipo de cambio aplicado. |
| Total | Importe total en moneda local. |
| Gravado | Neto gravado. |
| No Gravado | Neto no gravado. |
| ... demás importes | Exento, descuento, IVA 10,5%, 21,0%, 27,0%, etc. |
| Detalle | Observaciones del comprobante. |
| Tipo | Categoría del gasto. |
| Categoría | Subcategoría. |
| Proveedor | Nombre del proveedor. |
| **Semáforo** | Indicador de control de costos: 🟢 verde = importes coinciden con el remito, 🟡 amarillo = diferencia en importes, 🔴 rojo = sin datos de remito asociado. |

---

## Validaciones al guardar

- El **Proveedor**, **Tipo de factura** y **Número de factura** son obligatorios.
- La **Moneda** y **Cotización** deben ser mayores a cero.
- La **Fecha** no puede ser posterior a la fecha actual.
- El **Tipo** y la **Categoría** de compra son obligatorios.
- Para facturas tipo A (responsables inscriptos), el sistema verifica que los montos de IVA sean proporcionales al gravado (validación automática).

---

## Flujo típico — Registro de factura de compra

1. Seleccionar el **Proveedor**
2. Elegir el **Tipo** y la **Categoría** de la compra
3. En **RTOS. ARTICULOS**, hacer clic en **BuscarArt** y seleccionar el remito de ingreso al stock correspondiente
4. Completar **FC. FECHA**, **FC. VENCE** y **FEC. COTBLE**
5. Seleccionar el **Tipo de factura** (A, B, etc.) y escribir el **número**
6. Ingresar los importes: **GRAVADO**, **NO GRAVADO**, **IVA**, percepciones, gastos, etc.
7. Hacer clic en **Guardar** (el sistema valida los importes y pide confirmación)

---

## Notas importantes

- El **semáforo** en verde indica que el importe de la factura coincide con el costo de los artículos ingresados al stock. Si está en amarillo o rojo, hay que revisar la asociación con el remito.
- Para proveedores **Monotributistas** (tipo C), solo aparecen los campos de IMPORTE y DESCUENTO (sin desglose de IVA).
- La cotización es 1 para facturas en pesos. Para facturas en dólares u otras monedas, debe ingresarse el tipo de cambio del día.
- Se puede opcionalmente adjuntar la imagen escaneada de la factura como respaldo digital.

> Relacionado: [**Registro de Compras**](https://ayuda.caddis.com.ar/instructivos/04_COMPRAS_Registro.pdf) (4.05) — consulta del historial de compras por proveedor
