# 3.25 CHEQUES A DEPOSITAR
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Cobranza → Cheques a Depositar

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cheques a Depositar** permite registrar en el sistema los cheques (y e-cheques) recibidos de clientes que se están depositando en el banco. Desde aquí podés:

- Ver todos los cheques pendientes de depositar que vencen hasta la fecha indicada
- Seleccionar los cheques que se van a depositar en un mismo acto
- Registrar los datos del depósito: banco, cuenta y número de comprobante bancario
- Controlar qué cheques ya fueron depositados y cuáles siguen pendientes

> ℹ️ Los cheques aparecen en esta pantalla cuando fueron registrados como forma de pago en una factura o recibo de cobro de cuenta corriente.

---

<img src="imagenes/pantalla_cheques_depositar.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Cobranza → Cheques a Depositar**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Datos del depósito a registrar y filtro de fecha
- **Panel derecho:** Grilla con los cheques pendientes de depositar

---

## Panel izquierdo — Datos del depósito

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha límite de vencimiento. La grilla muestra sólo los cheques con fecha de cobro hasta este día (salvo que se active "Mostrar todos"). |
| **BANCO** | Banco donde se realiza el depósito |
| **CUENTA** | Número de cuenta bancaria destino |
| **COMP#** | Número de comprobante del depósito bancario (boleta de depósito) |
| **CHEQUES** | Texto informativo (read-only) con los números de cheque seleccionados |
| **IMPORTE** | Total de los cheques seleccionados (read-only, se calcula automáticamente) |
| **OBSERVACIONES** | Notas adicionales sobre el depósito |
| **Mostrar todos los cheques** | Checkbox: si se activa, muestra también los cheques con fecha de cobro futura (no sólo los que vencen hasta hoy) |

---

## Panel derecho — Grilla de cheques pendientes

Muestra todos los cheques y e-cheques recibidos de clientes que aún no fueron depositados:

| Columna | Descripción |
|---|---|
| Checkbox | Marca el cheque para incluirlo en el depósito |
| Fecha | Fecha de cobro del cheque |
| Importe | Monto del cheque |
| Tipo | CHEQUE (físico) o E-CHECK (cheque electrónico) |
| Banco | Banco del cheque |
| Nro | Número del cheque |
| Cliente | Cliente de quien proviene el cheque |

---

## Paso a paso — Registrar un depósito de cheques

1. Controlá la **FECHA** para ver qué cheques vencen hasta ese día
2. (Opcional) Activá **Mostrar todos los cheques** si necesitás depositar uno con fecha futura
3. En la grilla, marcá el **checkbox** de cada cheque a depositar
4. El campo **IMPORTE** se actualiza con la suma total
5. Completá el **BANCO**, la **CUENTA** y el **COMP#** del depósito
6. Añadí **OBSERVACIONES** si es necesario
7. Hacé clic en **Guardar** (o el botón de confirmación disponible)

> El sistema registra el depósito y los cheques seleccionados dejan de aparecer en la grilla de pendientes.

---

## Notas importantes

- Un cheque que ya fue incluido en un depósito anterior **no aparece** en la grilla (se filtra por `cheques_control`).
- El campo **IMPORTE** es sólo informativo — se calcula automáticamente al seleccionar cheques.
- Se pueden depositar cheques de distintos clientes en un mismo comprobante de depósito (un solo trámite bancario).
- Los **e-cheques** (tipo E-CHECK) se procesan de la misma forma que los cheques físicos.
