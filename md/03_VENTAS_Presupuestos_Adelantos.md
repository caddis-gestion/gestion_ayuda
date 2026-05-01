# 3.10 ADELANTOS SOBRE PRESUPUESTO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Adelantos de Presupuesto

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Adelantos sobre Presupuesto** permite registrar pagos parciales (señas o adelantos) sobre un presupuesto antes de que se convierta en factura. Desde aquí podés:

- Registrar un adelanto en efectivo, tarjeta u otro medio de pago sobre un presupuesto
- Emitir un recibo de cobro por el adelanto
- Ver el total del presupuesto y el saldo pendiente después del adelanto
- Dejar observaciones sobre el cobro

> ℹ️ Un **adelanto** es un pago parcial a cuenta de un presupuesto que todavía no se facturó. Cuando el cliente retira la mercadería y se emite la factura definitiva, el adelanto se descuenta automáticamente del total a pagar.

---

<img src="imagenes/pantalla_presupuestos_adelantos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Adelantos de Presupuesto**

---

## Descripción general de la pantalla

La pantalla está dividida en dos secciones principales:

- **Datos del presupuesto:** búsqueda del presupuesto y datos del cliente
- **Cobro a cuenta de pedido:** registro del adelanto a cobrar

---

## Sección: Datos del presupuesto

| Campo/Botón | Descripción |
|---|---|
| **PRESUPUESTO** | Número del presupuesto sobre el que se registra el adelanto. Ingresá el número y hacé clic en **Buscar** (lupa) para cargarlo. Si el presupuesto está cancelado, aparecerá un indicador en rojo. |
| **PDV** | Punto de Venta del presupuesto. Se completa automáticamente al buscar el presupuesto. |
| **FECHA** | Fecha del presupuesto. Se completa automáticamente. |
| **CLIENTE** | Nombre del cliente. Se completa automáticamente. |
| **CUIT/DNI** | Documento del cliente. Se completa automáticamente. |

Al buscar el presupuesto, aparece también una **mini-grilla** con los artículos incluidos (Descripción, Cantidad y Total).

---

## Sección: Cobro a cuenta de pedido

| Campo/Botón | Descripción |
|---|---|
| **FECHA** | Fecha del cobro del adelanto (por defecto: hoy). |
| **RECIBO** | Número de recibo generado automáticamente para el adelanto. |
| **COTIZACION** | Cotización de la moneda (si aplica, para presupuestos en moneda extranjera). |
| **TOTAL** | Monto total del presupuesto (solo lectura). |
| **SALDO PENDIENTE** | Saldo que queda por cobrar luego del adelanto (solo lectura). |
| **IMPORTE** | Importe del adelanto a registrar (solo lectura, se actualiza al cobrar). |
| **Cobros** | Botón que abre la ventana de registro de medios de pago para ingresar el adelanto. |
| **OBSERVACIONES** | Texto libre para agregar notas sobre el cobro. |

---

## Botones principales

| Botón | Qué hace |
|---|---|
| **Guardar** (o **Aceptar**) | Registra el adelanto y emite el recibo de cobro. |
| **Cancelar** | Descarta todo y limpia el formulario. |

---

## Paso a paso: Registrar un adelanto sobre un presupuesto

**Caso típico:** Un cliente quiere dejar una seña para reservar su pedido.

**1. Buscar el presupuesto**
- En el campo **PRESUPUESTO**, ingresá el número del presupuesto (ej.: `PP-00001234`).
- Hacé clic en **Buscar** (ícono de lupa).
- El sistema cargará los datos del cliente y el listado de artículos.

**2. Verificar los datos**
- Confirmá que el **CLIENTE** y los artículos son los correctos.
- Verificá el **TOTAL** del presupuesto y el **SALDO PENDIENTE**.

**3. Registrar el cobro**
- Hacé clic en el botón **Cobros**.
- En la ventana que se abre, elegí el tipo de pago (efectivo, tarjeta, transferencia, etc.) y el importe del adelanto.
- Confirmá el pago y cerrá la ventana.
- El campo **IMPORTE** se actualizará con el adelanto registrado.

**4. Agregar observaciones** *(opcional)*
- Usá el campo **OBSERVACIONES** para anotar el motivo del adelanto, condiciones, etc.
- Ejemplo: "Señal 30%, retira el 15/03".

**5. Guardar el adelanto**
- Hacé clic en **Guardar**.
- El sistema emite un recibo de cobro (tipo RC) con el número de recibo asignado.
- El saldo del presupuesto se actualiza automáticamente.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "No se encontró el presupuesto" | El número ingresado no existe o está mal escrito | Verificá el número del presupuesto |
| "CANCELADA" (en rojo) | El presupuesto fue anulado | No se puede registrar adelantos en presupuestos cancelados |
| El IMPORTE queda en cero | No se registró ningún pago en la ventana de Cobros | Usá el botón Cobros para ingresar el pago antes de guardar |

---

## Preguntas frecuentes

**¿Qué recibo se emite al registrar el adelanto?**
El sistema emite un comprobante tipo **RC** (Recibo de Cobro) con el importe del adelanto. Este recibo puede imprimirse y entregarse al cliente como constancia del pago.

**¿El adelanto se descuenta automáticamente al facturar?**
Sí. Al facturar el presupuesto, el sistema reconoce los adelantos registrados y los aplica automáticamente al total a cobrar. El operador puede seleccionar el recibo de seña como medio de pago desde la ventana de Pagos.

**¿Puedo registrar múltiples adelantos sobre el mismo presupuesto?**
Sí, podés registrar varios adelantos parciales sobre el mismo presupuesto. El saldo pendiente se actualiza en cada oportunidad.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
