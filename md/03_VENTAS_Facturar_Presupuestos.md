# 3.56 FACTURAR PRESUPUESTOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturar Presupuestos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturar Presupuestos** permite convertir un presupuesto aprobado en una factura. Es la continuación del proceso de presupuestación: una vez que el cliente acepta el presupuesto, desde aquí se emite la factura correspondiente con los artículos ya cargados. Desde aquí podés:

- Buscar el presupuesto a facturar
- Seleccionar el PDV, vendedor, cliente y tipo de factura
- Registrar el pago (medio de pago)
- Emitir la factura fiscal

---

<img src="imagenes/pantalla_facturar_presupuestos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturar Presupuestos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de la factura y un panel derecho con el detalle de artículos del presupuesto cargado.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta donde se factura |
| **VENDEDOR** | Vendedor asignado |
| **FECHA** | Fecha de la factura |
| **CLIENTE** | Cliente de la factura |
| **EMITIR EN** | Moneda de facturación + cotización (sólo en entornos multimoneda) |
| **FACTURA** | Tipo de comprobante (TK, A, B, M, X, IV, etc., según el PDV) + número |
| **OBSERVACIONES** | Notas de la factura |

### Búsqueda del presupuesto

| Campo / Botón | Descripción |
|---|---|
| **Presupuesto** | Botón para buscar y seleccionar el presupuesto a facturar |
| **Campo de presupuesto** | Muestra el número del presupuesto seleccionado (sólo lectura) |
| **Botón detalle** | Abre el detalle del presupuesto seleccionado |

### Botones de pago

| Botón | Descripción |
|---|---|
| **Voucher** | Permite aplicar un voucher de descuento al total |
| **Pagos** | Abre el popup para registrar el medio de pago (efectivo, tarjeta, transferencia, etc.) |
| **Solo Efectivo** | Checkbox: marca la venta como pago exclusivo en efectivo |

---

## Panel derecho — Detalle de artículos

Muestra los artículos incluidos en el presupuesto seleccionado (igual al panel de detalle de facturación estándar). Los artículos se cargan automáticamente al seleccionar el presupuesto.

---

## Paso a paso — Facturar un presupuesto

1. Seleccioná el **PDV** y el **VENDEDOR**
2. Verificá la **FECHA**
3. Seleccioná el **CLIENTE**
4. Elegí el tipo de **FACTURA**
5. Hacé clic en **Presupuesto** para buscar y seleccionar el presupuesto — los artículos se cargan en el panel derecho
6. Registrá el pago con **Pagos** (o marcá **Solo Efectivo** si aplica)
7. Agregá **OBSERVACIONES** si es necesario
8. Guardá — se emite la factura y el presupuesto queda marcado como facturado

---

## Notas importantes

- El presupuesto pasa al estado **FACTURADO** una vez emitida la factura desde esta pantalla.
- Los artículos del presupuesto se traspasan automáticamente a la factura; no es necesario ingresarlos de nuevo.
- Si el cliente requiere cambios en los artículos antes de facturar, primero modificá el presupuesto desde **Modificar Presupuesto** (3.60).
