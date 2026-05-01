# 15.13 MONEDAS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Monedas

---
<img src="imagenes/pantalla_monedas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Monedas** permite gestionar las divisas disponibles en el sistema y mantener actualizada la cotización de cada una. Desde aquí podés:

- Agregar nuevas monedas extranjeras al sistema
- Modificar el alias, símbolo o cotización de una moneda existente
- Mantener actualizado el tipo de cambio para facturas en divisas extranjeras

---

## ¿Cómo acceder?

**Menú → Administración → Monedas**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **MONEDA** | Selector de la moneda base (código estándar: USD, EUR, etc.). |
| **ALIAS** | Nombre personalizado para la moneda dentro del sistema (ej: "Dólar", "Euro"). |
| **SIMBOLO** | Símbolo de la moneda (ej: $, U$S, €). Hasta 3 caracteres. |
| **COTIZACION** | Tipo de cambio respecto a la moneda local. Para la moneda local, siempre es 1. |

---

## Grilla de monedas

Muestra todas las monedas configuradas en el sistema con:

| Columna | Descripción |
|---|---|
| Moneda | Nombre/alias de la moneda. |
| Símbolo | Símbolo de la moneda. |
| Cotización | Tipo de cambio actual. |

---

## Flujo típico — Actualizar cotización del dólar

1. Seleccionar la moneda **USD** en la grilla (clic en Modificar)
2. Actualizar el campo **COTIZACION** con el tipo de cambio del día
3. Guardar los cambios

---

## Notas importantes

- La cotización ingresada se aplica a todas las facturas de compra y venta en esa moneda a partir de ese momento; no modifica comprobantes ya registrados.
- El **SIMBOLO** del peso argentino (`$`) se reemplaza internamente por `S` para evitar conflictos de visualización; esto es normal.
