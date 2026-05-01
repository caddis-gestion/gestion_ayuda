# 3.03 FACTURA DE AJUSTE
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Factura de Ajuste

---

## ¿Para qué sirve esta pantalla?

La **Factura de Ajuste** permite emitir notas de crédito o notas de débito sobre una factura existente, ajustando un **importe libre** en lugar de devolver artículos específicos. Desde aquí podés:

- Emitir una Nota de Crédito de ajuste (descuento posterior sobre una venta)
- Emitir una Nota de Débito de ajuste (cargo adicional sobre una venta)
- Ajustar diferencias de precio, gastos adicionales o correcciones de importe
- Vincular el ajuste a la factura original para una correcta trazabilidad fiscal

> ℹ️ **Diferencia clave con Nota de Crédito (3.06):** La Nota de Crédito trabaja con los artículos de la factura original (devuelve unidades y ajusta stock). La Factura de Ajuste trabaja con un **importe y concepto libre**, sin devolver artículos ni afectar el stock.

---

<img src="imagenes/pantalla_factura_ajuste.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Factura de Ajuste**

---

## Descripción general de la pantalla

La pantalla es similar a la de Nota de Crédito, pero con dos campos adicionales exclusivos:

- **Panel izquierdo:** Formulario para buscar la factura original, elegir el tipo de ajuste, e ingresar el concepto e importe del ajuste
- **Panel derecho:** Grilla con los datos de ajuste

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **FACTURA** | Tipo y número de la factura original sobre la que se realiza el ajuste. Buscala con el ícono de lupa. |
| **PDV** | Punto de Venta. Se completa automáticamente con los datos de la factura original. |
| **VENDEDOR** | Vendedor de la operación. Se completa automáticamente. |
| **FECHA** | Fecha del comprobante de ajuste. Por defecto es el día de hoy. |
| **CLIENTE** | Cliente de la factura original. Se completa automáticamente. |
| **TIPO** | Tipo de comprobante a emitir (NC o ND). Se sugiere automáticamente según la factura original, pero puede cambiarse para elegir entre nota de crédito o débito. |
| **CONCEPTO** | Texto libre que describe el motivo del ajuste (ej.: "Diferencia de precio", "Gasto de flete", "Descuento por daño"). |
| **IMPORTE** | Importe del ajuste (sin IVA o con IVA según configuración). |

---

### Tipos de comprobante disponibles según la factura original

| Tipo de factura original | NC disponibles | ND disponibles |
|---|---|---|
| **A / IA** | NCA, NCEA | NDA, NDEA |
| **B / IB** | NCB, NCEB | NDB, NDEB |
| **C** | NCC | NDC |
| **M / IM** | NCM, NCEM | NDM, NDEM |
| **PA** | NCPA | NDPA |
| **X** | NCX | NDX |

> 💡 El sistema sugiere el tipo correcto automáticamente. La diferencia entre NC y ND es el sentido del ajuste:
> - **Nota de Crédito (NC):** a favor del cliente (reduce lo que debe / acredita un saldo)
> - **Nota de Débito (ND):** a favor de la empresa (aumenta lo que debe el cliente / cargo adicional)

---

## Alertas del sistema

| Alerta | Significado |
|---|---|
| **"La factura tiene más de 30 días"** | La factura original fue emitida hace más de 30 días. Se puede continuar, pero conviene verificar si es correcto realizar el ajuste. |

---

## Paso a paso: Emitir una Factura de Ajuste

**Caso típico:** Se acordó un descuento posterior con el cliente sobre una factura ya emitida.

**1. Buscar la factura original**
- En el campo **FACTURA**, seleccioná el tipo e ingresá el número.
- Hacé clic en la lupa o presioná Enter.
- El sistema cargará automáticamente los datos del cliente, PDV y vendedor.

**2. Elegir el tipo de comprobante**
- En el campo **TIPO**, verificá si el sistema sugirió NC o ND.
- Si necesitás cambiar (ej.: querés emitir una ND en lugar de una NC), seleccioná el tipo correcto.

**3. Ingresar el concepto**
- En el campo **CONCEPTO**, escribí una descripción clara del motivo del ajuste.
- Ejemplo: "Descuento por pago anticipado", "Cargo por reentrega", "Corrección de precio".

**4. Ingresar el importe**
- En el campo **IMPORTE**, ingresá el monto del ajuste.

**5. Emitir el comprobante**
- Hacé clic en **Emitir** (o **Facturar**).
- El sistema registra el ajuste, lo envía a AFIP si corresponde y genera el comprobante.

---

## Nota de Crédito vs. Factura de Ajuste: cuándo usar cada una

| Situación | Herramienta a usar |
|---|---|
| El cliente devuelve artículos físicamente | **Nota de Crédito** (3.06) |
| Se acuerda un descuento posterior sobre el precio | **Factura de Ajuste** (3.03) — emitir NC |
| Se cobra un cargo adicional no incluido en la factura original | **Factura de Ajuste** (3.03) — emitir ND |
| Se corrije una diferencia de precio sin devolver mercadería | **Factura de Ajuste** (3.03) — emitir NC o ND según corresponda |
| Se anula completamente una factura | **Nota de Crédito** (3.06) por el total |

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "No se encontró la factura" | El tipo o número de factura no existe | Verificá tipo y número de la factura |
| "Controle el Importe" | El importe es cero o negativo | Ingresá un importe válido mayor a cero |
| "Controle el Concepto" | El campo concepto está vacío | Ingresá una descripción del motivo del ajuste |

---

## Preguntas frecuentes

**¿La Factura de Ajuste afecta el stock?**
No. A diferencia de la Nota de Crédito, la Factura de Ajuste solo ajusta el importe de la factura y no mueve artículos del stock.

**¿Puedo emitir múltiples ajustes sobre la misma factura?**
Sí, se pueden emitir varios comprobantes de ajuste sobre la misma factura original.

**¿El ajuste se envía a AFIP?**
Sí, si el tipo de comprobante elegido es electrónico (NCEA, NCEB, NDEA, NDEB, etc.), se envía automáticamente a AFIP.

**¿Qué importe debo ingresar, con o sin IVA?**
Depende de la configuración del sistema. Consultá con el administrador si el importe a ingresar debe incluir o no el IVA.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
