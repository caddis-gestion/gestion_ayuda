# 3.55 FACTURACIÓN X → A|B
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturacion X -> A|B

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturación X → A|B** permite convertir comprobantes de tipo X (comprobantes internos sin información fiscal del cliente) en facturas fiscales tipo A o B. Es útil cuando una venta se realizó sin identificar al cliente y luego se necesita emitir la factura correspondiente. Desde aquí podés:

- Buscar un comprobante X existente
- Asociarlo a un cliente con sus datos fiscales
- Emitir la factura A o B correspondiente

---

<img src="imagenes/pantalla_facturacion_x_a_b.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturacion X -> A|B**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de conversión y un panel derecho con el detalle de artículos del comprobante.

---

## Panel izquierdo — Formulario

### Búsqueda del comprobante X

| Campo / Botón | Descripción |
|---|---|
| **FACTURA** | Selector de tipo (X, NDX, NCX) + número del comprobante X a convertir |
| **Buscar** | Busca el comprobante X y carga sus datos |

### Sección Factura A|B

Permite configurar la nueva factura fiscal a emitir:

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta fiscal desde el que se emite la factura A o B |
| **VENDEDOR** | Vendedor asignado |
| **FECHA** | Fecha de la nueva factura |
| **CLIENTE** | Cliente al que se emite la factura |
| **IVA** | Condición de IVA del cliente (Responsable Inscripto → A; Consumidor Final/Monotributista → B) |
| **FACTURA** | Tipo de comprobante resultante (determinado automáticamente según el PDV y el IVA del cliente) + número |
| **OBSERVACIONES** | Notas de la factura |

**Botón PAGOS:** Aparece si el importe del comprobante X y el de la nueva factura difieren. Permite registrar diferencias de pago.

---

## Panel derecho — Detalle de artículos

Muestra los artículos del comprobante X seleccionado (igual al panel de detalle de facturación estándar).

---

## Paso a paso — Convertir un comprobante X en factura A o B

1. Seleccioná el tipo **X** en el selector de FACTURA e ingresá el número del comprobante
2. Hacé clic en **Buscar** — el sistema carga los datos del comprobante y los artículos en el panel derecho
3. Seleccioná el **PDV** fiscal
4. Seleccioná el **CLIENTE** al que se emite la factura
5. Verificá la condición de **IVA** — determina si se emite A o B
6. Verificá la **FECHA** y el número de **FACTURA**
7. Si hay diferencia de pago, hacé clic en **Pagos** y registrá el medio de pago
8. Guardá — se emite la factura fiscal y el comprobante X queda asociado

---

## Notas importantes

- El tipo de comprobante resultante (A o B) se determina automáticamente según el PDV seleccionado y la condición de IVA del cliente.
- Un comprobante X sólo puede convertirse una vez.
- Esta operación es útil en locales donde primero se cobra con ticket X y luego el cliente solicita la factura.
