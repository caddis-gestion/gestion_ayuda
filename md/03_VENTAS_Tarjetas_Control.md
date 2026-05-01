# 3.17 CONTROL DE TARJETAS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios de administración y caja del sistema
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Control de Tarjetas

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Control de Tarjetas** permite gestionar las liquidaciones de cobros realizados con tarjetas de crédito y débito. Desde aquí podés:

- Registrar la liquidación de cupones de tarjeta cuando el banco acredita el cobro
- Ver los cupones pendientes de liquidar por entidad (banco/tarjeta)
- Consultar la cuenta corriente de tarjetas para cada entidad
- Reconciliar los cobros registrados con los resúmenes de la entidad bancaria
- Llevar el control de los cupones emitidos vs. los liquidados

> ℹ️ Cuando un cliente paga con tarjeta, el sistema registra el cupón como "cobro pendiente de liquidar". Esta pantalla es donde se confirma que el banco efectivamente acreditó ese dinero.

---

<img src="imagenes/pantalla_tarjetas_control.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Control de Tarjetas**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Datos de la liquidación a registrar
- **Panel derecho:** Grilla con los cupones emitidos pendientes de liquidar para la entidad seleccionada

---

## Campos del panel izquierdo

| Campo | Descripción |
|---|---|
| **ENTIDAD** | Tarjeta/banco que procesa el cobro (Visa, Mastercard, Cabal, etc.). Al seleccionar la entidad, la grilla del panel derecho se actualiza automáticamente con los cupones pendientes de esa entidad. |
| **LIQUIDACION** | Número de liquidación asignado por el banco al acreditar el pago. |
| **FECHA** | Fecha de la liquidación del banco. |
| **IMPORTE** | Importe total de los cupones seleccionados para liquidar (solo lectura, se calcula automáticamente). |
| **APLICAR** | Importe total a aplicar en la liquidación (solo lectura, en color dorado). |
| **OBSERVACIONES** | Texto libre para notas sobre la liquidación. |

---

## Botones de acción

| Botón | Qué hace |
|---|---|
| **Cobros** | Abre la ventana de pagos para registrar el cobro de la liquidación. |
| **Cta Cte** | Muestra la cuenta corriente de la entidad seleccionada (historial de liquidaciones). |
| **Pendientes** | Muestra los cupones pendientes de liquidar para la entidad seleccionada. |

---

## Grilla del panel derecho: cupones pendientes

La grilla muestra los cupones de tarjeta emitidos que aún no fueron liquidados por el banco. Al seleccionar los cupones en la grilla y registrar la liquidación, el sistema los marca como liquidados.

Las columnas típicas incluyen: Entidad, Fecha del cupón, Tipo de factura, N° de factura, Tarjeta, Cuotas, N° de cupón, Lote, Importe, Autorización.

---

## Paso a paso: Registrar una liquidación de tarjeta

**Caso típico:** El banco acreditó los cobros con Visa del mes pasado y querés registrarlo en el sistema.

**1. Seleccionar la entidad**
- En el campo **ENTIDAD**, elegí la tarjeta (ej.: Visa).
- La grilla del panel derecho mostrará todos los cupones pendientes de esa entidad.

**2. Seleccionar los cupones a liquidar**
- En la grilla, seleccioná los cupones que están incluidos en esta liquidación.
- El importe total se calcula automáticamente y aparece en el campo **APLICAR**.

**3. Completar los datos de la liquidación**
- Ingresá el **N° de LIQUIDACION** que figura en el resumen del banco.
- Verificá la **FECHA** (fecha en que el banco acreditó el dinero).

**4. Registrar el cobro**
- Hacé clic en **Cobros**.
- El sistema registra la liquidación y los cupones seleccionados quedan marcados como liquidados.

**5. Verificar** *(opcional)*
- Hacé clic en **Cta Cte** para ver el historial de liquidaciones de esa entidad.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| No aparecen cupones en la grilla | La entidad seleccionada no tiene cupones pendientes | Verificá la entidad o el período de búsqueda |
| El IMPORTE no coincide con el resumen del banco | Puede haber diferencias por contracargos o devoluciones | Verificar cupón por cupón antes de liquidar |
| "Este es un cobro no aplicado a ningún cupón" | Se hizo doble clic en una fila sin cupón asociado | Es informativo, no es un error crítico |

---

## Preguntas frecuentes

**¿Qué pasa si el banco acreditó un importe diferente al de los cupones?**
Podés registrar la diferencia como un cobro con ajuste, usando el campo OBSERVACIONES para documentar la discrepancia. Consultá con el administrador del sistema.

**¿Puedo ver el detalle de una factura desde esta pantalla?**
Sí, haciendo doble clic en un cupón de la grilla se abre el comprobante de factura correspondiente.

**¿Qué diferencia hay entre Control de Tarjetas y Liquidaciones de Tarjetas (3.18)?**
- **Control de Tarjetas** (3.17): es donde se *registra* la liquidación y se *controlan* los cupones pendientes.
- **Liquidaciones de Tarjetas** (3.18): es una vista de detalle de los cupones incluidos dentro de una liquidación ya registrada.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
