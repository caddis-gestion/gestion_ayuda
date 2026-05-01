# 16.03 STOCK DE ARTÍCULOS
### Módulo 16 — Reportes

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reportes → Stock de Articulos

---

## ¿Para qué sirve esta pantalla?

Muestra el stock actual de cada artículo desglosado por depósito, en una grilla pivoteada donde cada PDV es una columna. Ideal para ver de un vistazo la distribución de inventario en todos los puntos de venta.

---

<img src="imagenes/pantalla_stock_articulos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reportes → Stock de Articulos**

---

## Filtros

Permite filtrar la lista de artículos por código, tipo, grupo, marca o variante.

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| Código | Código del artículo |
| Artículo | Descripción del artículo |
| Precio Venta | Precio de lista (Lista 1) incluyendo IVA, convertido a moneda base |
| Moneda | Moneda del precio |
| [Columnas de PDV] | Una columna por cada depósito activo, con la cantidad en stock |
| Semáforo | Verde = activo, Rojo = inactivo, Amarillo = oferta, Azul = especial |

> ℹ️ Las primeras 5 columnas son fijas (no se desplazan al hacer scroll horizontal). Las columnas de PDV se agregan dinámicamente según los depósitos configurados.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
