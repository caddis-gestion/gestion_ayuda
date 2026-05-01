# 16.11 LISTAS DE PRECIOS
### Módulo 16 — Reportes

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reportes → Listas de Precios

---

## ¿Para qué sirve esta pantalla?

Permite consultar los precios de todos los artículos en cada lista de precios configurada en el sistema. Muestra una grilla donde cada lista de precios es una columna independiente, con el precio final al público (incluido IVA) en la moneda correspondiente a esa lista. Es útil para comparar precios entre listas y verificar la vigencia de los valores cargados.

> Esta pantalla es distinta de la pantalla de gestión de precios del módulo Stock: aquí solo se consultan los precios, no se modifican.

---

<img src="imagenes/pantalla_reportes_listas_precios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reportes → Listas de Precios**

---

## Filtros disponibles

| Filtro | Descripción |
|---|---|
| Buscar artículo | Permite filtrar por código, descripción, tipo, grupo, marca o variante del artículo. Si se deja vacío, muestra todos los artículos. |

> Solo se muestran las listas de precios correspondientes a los PDV (depósitos) a los que tiene acceso el usuario.

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| Código | Código del artículo |
| Artículo | Descripción del artículo |
| [Una columna por lista] | Precio final al público con IVA incluido, redondeado a 4 decimales, en la moneda de esa lista (ej: $ Mayorista, $ Minorista, USD Exportación). El encabezado muestra el símbolo de moneda y el nombre de la lista. |
| Tipo | Tipo de artículo |
| Grupo | Grupo al que pertenece el artículo |
| Marca | Marca del artículo |
| Variante | Variante del artículo (ej: color, capacidad) |

> Las primeras 2 columnas (Código y Artículo) son fijas y no se desplazan al hacer scroll horizontal. Las columnas de listas de precios se generan dinámicamente según las listas configuradas en el sistema.

> Si un artículo no tiene precio cargado en una lista determinada, la celda correspondiente aparece vacía.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
