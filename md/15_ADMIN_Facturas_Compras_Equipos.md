# 15.38 FACTURAS COMPRAS EQUIPOS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Proveedores → Facturas Compras Equipos

---

## ¿Para qué sirve esta pantalla?

Permite registrar facturas de compra de equipos (teléfonos) emitidas por la prestataria (operadora telefónica). Cada registro asocia un comprobante de compra (factura, nota de crédito o nota de débito) a un equipo específico identificado por su NSE (número de serie), con todos los importes e impuestos correspondientes.

Esta pantalla se utiliza para llevar el control de los costos de adquisición de equipos por NSE y es independiente del módulo de Compras de productos generales.

---

<img src="imagenes/pantalla_admin_facturas_compras_equipos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Proveedores → Facturas Compras Equipos**

---

## Panel izquierdo — Datos del comprobante

| Campo | Descripción |
|---|---|
| FECHA | Fecha del comprobante de compra. |
| TIPO | Tipo de comprobante. Opciones: **FACTURA** / **NTA. CREDITO** / **NTA. DEBITO**. |
| FACTURA | Número de factura en formato estándar (ej: 0001-00012345). |
| NETO | Importe neto sin IVA (S/IVA). |
| DESCUENTO % | Porcentaje de descuento aplicado sobre el importe neto. |
| IVA % | Tasa de IVA aplicable. Se selecciona de la lista de tasas configuradas para el país. |
| IMP INT % | Porcentaje de impuestos internos. |
| PERC IVA % | Porcentaje de percepción de IVA. |
| PERC IIBB % | Porcentaje de percepción de Ingresos Brutos. Incluye botón **Multiple** para aplicar percepción múltiple. |

### Botones de búsqueda y acción

| Botón | Descripción |
|---|---|
| Buscar | Busca la factura ingresada y carga los equipos asociados. |
| Remito | Busca por número de remito/ingreso de stock en lugar de número de factura. |
| Multiple | Permite distribuir la percepción de IIBB entre múltiples jurisdicciones. |
| Agregar | Registra el comprobante con los datos ingresados. |
| Borrar (grilla) | Elimina una línea de la grilla de equipos antes de confirmar. |

---

## Grilla derecha — Equipos del comprobante

Muestra los equipos incluidos en el comprobante de compra del usuario actual:

| Columna | Descripción |
|---|---|
| NSE | Número de serie (NSE hexadecimal) del equipo. |
| Factura Tipo | Tipo de comprobante (FC, NC, ND). |
| Factura Numero | Número del comprobante. |
| Facura Fecha | Fecha del comprobante. |
| Importe | Importe neto del equipo. |
| Dto | Porcentaje de descuento aplicado. |
| Iva | Tasa de IVA. |
| Impuestos Internos | Porcentaje de impuestos internos. |
| Perc Iva | Porcentaje de percepción IVA. |
| Perc IIBB | Porcentaje de percepción IIBB. |
| Total | Importe total calculado incluyendo todos los impuestos. |
| Equipo | Marca y descripción del equipo asociado al NSE. |
| Código | Código de artículo del equipo. |
| (botones) | Acción disponible: **Borrar** para eliminar la línea. |

> **Nota:** La grilla muestra únicamente los registros del usuario activo en sesión. El campo **Total** se calcula automáticamente como: `Neto × (1 - Descuento) × (1 + IVA + Imp.Int + Perc.IVA + Perc.IIBB)`.

> **Tip:** Para vincular una factura a equipos, ingresá el número de factura en el campo correspondiente y hacé clic en **Buscar**. Si los equipos ingresaron al sistema por remito, usá el botón **Remito** para localizarlos por número de ingreso.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
