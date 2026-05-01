# 3.06 NOTA DE CRÉDITO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Nota de Crédito

---

## ¿Para qué sirve esta pantalla?

La **Nota de Crédito** es el comprobante que se emite para anular total o parcialmente una factura ya emitida o para registrar la devolución de artículos por parte del cliente. Desde aquí podés:

- Cancelar o anular completamente una factura
- Registrar una devolución parcial de mercadería facturada
- Ajustar el stock por artículos devueltos

> ℹ️ **¿Cuándo usar otras pantallas?**
> - Para **variación de precio** (diferencia de importe sin devolver artículos): usá **Factura de Ajuste** (3.03).
> - Para **cambios de mercadería** (el cliente devuelve y se lleva otros artículos): usá **Cambios de Mercadería** (3.XX).

---

<img src="imagenes/pantalla_nota_credito.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Nota de Crédito**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Formulario para buscar la factura original y configurar la nota de crédito.
- **Panel derecho:** Grilla con los artículos de la factura original, donde se ajustan cantidades y se revisan importes.

El flujo de trabajo es: **buscar la factura original → el sistema carga los datos → ajustar cantidades si es devolución parcial → registrar la forma de pago → presionar PROCESAR**.

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **FACTURA** | Tipo de comprobante (ej.: EA, EB, A, B) y número de la factura original. Buscala por número ingresándola directamente, o usá el ícono de **lupa** para buscar por cliente o fecha. El botón **Detalle** permite ver el comprobante original. |
| **PDV** | Punto de Venta. Se completa automáticamente con los datos de la factura buscada. |
| **VENDEDOR** | Vendedor de la operación. Se completa automáticamente. |
| **FECHA** | Fecha de emisión de la nota de crédito. Muestra también la caja activa. Por defecto es el día de hoy. |
| **CLIENTE** | Cliente de la factura original. Se completa automáticamente al buscar la factura. |
| **TIPO** | Tipo de nota de crédito a emitir. El sistema lo sugiere automáticamente según el tipo de factura (ver tabla más abajo). |
| **Observaciones** | Texto libre para registrar el motivo u otras observaciones de la NC. |
| **Pagos** | Botón que abre la ventana de forma de pago. Es obligatorio completarlo antes de procesar, especialmente en devoluciones parciales. |

---

### Tipos de Nota de Crédito según la factura original

| Tipo de factura original | Tipos de NC disponibles |
|---|---|
| **A / IA** | NCA (manual), NCEA (electrónica) |
| **B / IB / TK** | NCB (manual), NCEB (electrónica) |
| **C / IC** | NCC, NCEC |
| **M / IM / EM** | NCM (manual), NCEM (electrónica) |
| **PA** (Presupuesto A) | NCPA |
| **X** | NCX |
| **IV** | NCIV |

> El sistema sugiere el tipo correcto automáticamente. Solo modificá este campo si tenés una razón específica.

---

## Panel derecho — Grilla de artículos

Al buscar la factura, el sistema carga en la grilla todos los artículos del comprobante original descontando las NC previas ya emitidas sobre esa factura.

| Columna | Descripción |
|---|---|
| **CANT** | Cantidad del artículo. En devoluciones parciales aparece un botón para modificarla. |
| **P.UNIT** | Precio unitario del artículo. |
| **DTO** | Porcentaje de descuento aplicado. |
| **IVA** | Alícuota de IVA del artículo. |
| **DESCRIPCION** | Código y descripción del artículo. |
| **IMPORTE** | Importe total de la línea. |
| *(ícono cesto)* | Elimina el artículo de la NC (lo deja fuera de la devolución). |

**Totales al pie de la grilla:**

| Campo | Descripción |
|---|---|
| **Subtotal** | Suma de importes sin IVA |
| **Neto de Impuestos** | Base imponible neta |
| **Total IVA** | IVA total del comprobante |
| **TOTAL** | Importe total de la NC |
| **PAGOS** | Importe registrado en la forma de pago |

---

## Alertas del sistema

| Alerta | Significado | Qué hacer |
|---|---|---|
| **"La factura tiene más de 30 días"** | La factura original fue emitida hace más de 30 días | Confirmar si corresponde continuar |
| **"TIENE GARANTÍAS ASOCIADAS"** | Uno o más artículos tienen garantía registrada | Verificar el impacto de la devolución en la garantía |

---

## Caso 1 — Cancelación total de una factura

Cuando el cliente devuelve todos los productos o cancela la venta, se emite una NC por el total de la factura.

1. En el campo **FACTURA**, seleccioná el tipo e ingresá el número. Podés usar la **lupa** para buscar por cliente o fecha.
2. El sistema carga automáticamente todos los artículos en la grilla con sus cantidades e importes originales.
3. Verificá el **CLIENTE**, **PDV**, **FECHA** y **TIPO** de NC.
4. Sin modificar nada en la grilla, presioná **PROCESAR**.
5. El sistema emite la NC por el total de la factura, actualiza el stock y, si corresponde, envía el comprobante a AFIP.

---

## Caso 2 — Devolución parcial de mercadería

Cuando el cliente devuelve solo algunos artículos o una cantidad menor a la facturada:

1. Buscá la factura original (igual que en el Caso 1).
2. En la grilla, ajustá los artículos según lo que se devuelve:
   - **Para modificar la cantidad:** hacé clic en el número de la columna **CANT** — el sistema abre un campo para ingresar la nueva cantidad.
   - **Para eliminar un artículo de la NC:** presioná el ícono del cesto de basura — la cantidad pasa a cero y el artículo queda excluido.
   - En pantalla deben quedar **solo los artículos y cantidades que efectivamente se devuelven**.
3. Verificá que el **TOTAL** de la grilla refleje el importe correcto de la devolución parcial.
4. Hacé clic en **Pagos** para registrar la forma de pago por el nuevo importe total. Es obligatorio que el importe de pagos coincida con el total de la NC para poder procesar.
5. Presioná **PROCESAR**. El sistema emite la NC parcial y ajusta el stock.

---

## Devolución total vs. parcial — resumen

| Tipo | Qué hacer en la grilla | ¿Ajustar pagos? |
|---|---|---|
| **Total** | No modificar nada — dejar las cantidades originales | Solo si la factura original tenía forma de pago registrada |
| **Parcial** | Modificar cantidades y/o eliminar artículos no devueltos | **Sí, siempre** — el importe de pagos debe coincidir con el nuevo total |

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "No se encontró la factura" | El tipo o número no existe en el sistema | Verificá tipo y número, o usá la búsqueda por lupa |
| "La factura ya tiene una NC completa" | Ya se emitió una NC por el total de esa factura | No se puede volver a acreditar esa factura |
| Los pagos no coinciden con el total | El importe de la forma de pago no coincide con el total de la NC | Revisá el botón Pagos y ajustá el importe |
| El sistema redirige al login | La sesión expiró | Volvé a iniciar sesión y repetí la operación |

---

## Preguntas frecuentes

**¿Puedo emitir más de una NC sobre la misma factura?**
Sí, siempre que quede saldo por acreditar. El sistema descuenta automáticamente las NC previas y solo permite acreditar el saldo restante.

**¿La NC afecta el stock?**
Sí. Al emitir la NC, los artículos devueltos vuelven al stock del PDV correspondiente.

**¿La NC se envía a AFIP?**
Sí, si el tipo de NC es electrónico (NCEA, NCEB, NCEM, etc.) se envía automáticamente a AFIP al procesar.

**¿Qué diferencia hay entre Nota de Crédito y Factura de Ajuste?**
- **Nota de Crédito** (esta pantalla): trabaja con los artículos de la factura, devuelve unidades físicas y ajusta el stock.
- **Factura de Ajuste** (3.03): ajusta un importe libre con un concepto sin devolver artículos ni mover stock. También permite emitir Notas de Débito.

**¿Qué diferencia hay entre Nota de Crédito y Cambios de Mercadería?**
- **Nota de Crédito** (esta pantalla): el cliente solo devuelve artículos.
- **Cambios de Mercadería** (3.XX): el cliente devuelve artículos y al mismo tiempo se lleva otros en reemplazo. El sistema genera la NC y la nueva factura en una sola operación.
