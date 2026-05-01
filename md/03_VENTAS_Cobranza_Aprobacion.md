# 3.24 COBRANZA APROBACIÓN
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Cobranza → Cobranza Aprobacion

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cobranza Aprobación** permite que un usuario con perfil habilitado (supervisor, gerente) revise y apruebe los lotes de rendición de caja generados por los cajeros, así como los recibos de cuenta corriente de clientes mayoristas. Desde aquí podés:

- Ver los lotes de rendición pendientes de aprobación
- Aprobar lotes de caja minorista o recibos de cuenta corriente
- Imprimir la rendición de caja o el recibo aprobado
- Anular una aprobación ya realizada (si fuera necesario corregirla)
- Consultar el historial de lotes y recibos ya aprobados

> ℹ️ Los lotes de rendición se generan desde la pantalla **Cobros** (3.23). Esta pantalla sólo los aprueba — no los crea.

---

<img src="imagenes/pantalla_cobranza_aprobacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Cobranza → Cobranza Aprobacion**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda
- **Panel derecho:** Grilla con los lotes o recibos que cumplen el filtro

---

## Panel izquierdo — Filtros

| Campo | Descripción |
|---|---|
| **VENTA** | Tipo de venta: **MINORISTA** (rendiciones de caja) o **CTA CTE** (recibos de cuenta corriente de clientes mayoristas) |
| **PDV** | Punto de venta. Filtra los resultados por local. |
| **PAGO TIPO** | Tipo de pago (Efectivo, Tarjeta, Cheque, etc.). Sólo visible en modo MINORISTA. |
| **DESDE / HASTA** | Rango de fechas a consultar |
| **LOTE** | Número de lote (MINORISTA) o número de recibo (CTA CTE). Si se ingresa, ignora el rango de fechas. |
| **APROBADO** | **NO** → muestra sólo los pendientes de aprobación. **SI** → muestra los ya aprobados. |

Al modificar cualquier filtro, la grilla se actualiza automáticamente.

---

## Panel derecho — Grilla de resultados

### Modo MINORISTA

Muestra los lotes de rendición de caja:

| Columna | Descripción |
|---|---|
| Lote | Número de lote de rendición |
| Fecha | Fecha del lote |
| POS | Punto de venta |
| Pago | Tipo de pago del lote |
| Importe | Total del lote |
| Fecha Aprobación | Cuándo fue aprobado (sólo si ya está aprobado) |
| Entidad | Banco o tarjeta asociada |
| Comprobante | Número de comprobante bancario |
| Usuario | Usuario que aprobó (sólo si ya está aprobado) |
| Observaciones | Notas del lote |

**Acciones disponibles (APROBADO = NO):**
- **Imprimir rendición de caja:** Imprime el detalle del lote para control
- **Aprobar Lote:** Confirma la rendición. El lote pasa a estado Aprobado y se emite el recibo correspondiente.

**Acciones disponibles (APROBADO = SI):**
- **Imprimir recibo:** Imprime el recibo ya emitido
- **Anular aprobación:** Revierte la aprobación y devuelve el lote a estado Pendiente

### Modo CTA CTE

Muestra los recibos de cuenta corriente:

| Columna | Descripción |
|---|---|
| Recibo | Número de recibo |
| Fecha | Fecha del cobro |
| Cliente | Nombre del cliente |
| Importe | Monto cobrado |
| Fecha Aprobación | Cuándo fue aprobado |
| Usuario | Usuario aprobador |
| Observaciones | Notas |

**Acciones disponibles (APROBADO = NO):**
- **Imprimir rendición de caja:** Imprime el recibo para revisión
- **Aprobar Lote:** Aprueba el recibo de cobro

**Acciones disponibles (APROBADO = SI):**
- **Imprimir recibo:** Reimprimir el recibo aprobado
- **Anular aprobación:** Revierte la aprobación

---

## Paso a paso — Aprobar una rendición de caja

1. Seleccioná **VENTA = MINORISTA**
2. Elegí el **PDV** correspondiente (o dejá en blanco para ver todos)
3. Verificá que **APROBADO = NO** para ver los pendientes
4. Revisá la grilla: cada fila es un lote de rendición
5. Hacé clic en **Imprimir rendición de caja** si querés revisar el detalle antes de aprobar
6. Hacé clic en **Aprobar Lote** en la fila correspondiente
7. El lote desaparece de la vista (cambia a estado Aprobado) y se genera el recibo

---

## Notas importantes

- La aprobación genera un comprobante de tipo **RC (Recibo de Cobro)** que queda registrado en el sistema.
- **Anular una aprobación** sólo debe hacerse si hubo un error en la rendición. El lote vuelve a estado Pendiente y puede modificarse.
- El campo **LOTE** permite buscar un lote específico directamente por número, sin necesidad de filtrar por fecha.
- Para los clientes **CTA CTE**, los recibos se generan desde la pantalla **Recibos** (3.25) y se aprueban aquí.
