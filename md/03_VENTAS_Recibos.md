# 3.27 RECIBOS DE COBRO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Cobranza → Recibos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Recibos** permite registrar cobros a cuenta de clientes de cuenta corriente (mayoristas). Se usa cuando un cliente realiza un pago parcial o total de su saldo, generando un **Recibo de Cobro (RC)** que queda vinculado a su cuenta corriente. Desde aquí podés:

- Emitir recibos de cobro para clientes de cuenta corriente
- Registrar el pago con cualquier medio (efectivo, transferencia, cheque, etc.)
- Informar cobros a cuenta de un pedido específico
- Registrar observaciones del cobro

> ℹ️ Esta pantalla es para clientes **mayoristas con cuenta corriente**. Para cobros en ventas al mostrador, el pago se registra directamente en la pantalla de Facturación (3.01).

---

<img src="imagenes/pantalla_recibos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Cobranza → Recibos**

---

## Descripción general de la pantalla

La pantalla tiene un único panel de formulario con todos los campos necesarios para emitir el recibo.

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta desde el cual se emite el recibo |
| **CLIENTE** | Cliente mayorista al que se le emite el recibo. Se busca por nombre o CUIT. |
| **FECHA** | Fecha del cobro. Por defecto: hoy. |
| **RECIBO** | Número de recibo asignado automáticamente por el sistema (formato: 0000-XXXXXXXX). No se puede modificar. |
| **COTIZACIÓN** | Solo visible si el sistema usa multimoneda. Permite registrar cobros en moneda extranjera. |
| **IMPORTE** | Total del recibo (read-only). Se calcula automáticamente al cargar los cobros. |
| **OBSERVACIONES** | Campo libre para detallar el concepto del cobro |

### Botón Cobros

Al hacer clic en **Cobros** se abre un popup donde se ingresan los distintos ítems del pago:

- Tipo de pago (efectivo, cheque, transferencia, tarjeta, etc.)
- Importe por cada medio de pago
- Datos adicionales según el medio (banco, número de comprobante, datos del cheque)

Una vez confirmados los cobros, el **IMPORTE** del formulario principal se actualiza con el total.

---

## Paso a paso — Emitir un recibo de cobro

1. Seleccioná el **PDV**
2. Buscá y seleccioná el **CLIENTE** mayorista
3. Verificá la **FECHA** (por defecto hoy)
4. El campo **RECIBO** se asigna automáticamente
5. Hacé clic en **Cobros** para ingresar el detalle del pago
6. En el popup, seleccioná el tipo de pago e ingresá el importe
7. Confirmá el popup — el **IMPORTE** del formulario se actualiza
8. Ingresá **OBSERVACIONES** si corresponde
9. Guardá el recibo

---

## Notas importantes

- El recibo queda en estado **Pendiente de aprobación** hasta ser aprobado desde la pantalla **Cobranza Aprobación** (3.24).
- El número de recibo se genera automáticamente en secuencia por PDV.
- El recibo queda vinculado a la **cuenta corriente del cliente** y reduce su saldo deudor.
- Si el sistema usa multimoneda, el campo **COTIZACIÓN** permite registrar cobros en moneda extranjera (el sistema convierte al tipo de cambio informado).
