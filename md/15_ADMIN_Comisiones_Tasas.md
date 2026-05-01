# 15.28 COMISIONES — TASAS Y OBJETIVOS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Administración → Comisiones → Comisiones Tasas

---

## ¿Para qué sirve esta pantalla?

Permite configurar los objetivos de venta y las tasas de comisión por categoría de producto. Dependiendo de lo que se seleccione en el campo **DATO**, la pantalla muestra dos modos: uno para definir los objetivos de ventas por categoría y otro para asignar las tasas de comisión que corresponden a cada nivel de objetivo alcanzado.

---

<img src="imagenes/pantalla_comisiones_tasas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Comisiones → Comisiones Tasas**

---

## Panel izquierdo — Filtros principales

| Campo | Descripción |
|---|---|
| CATEGORIA | Tipo de producto al que aplica la configuración |
| DATO | Define qué se edita: **OBJETIVOS** o **TASAS** |

---

## Modo OBJETIVOS

Cuando el campo **DATO** tiene el valor **OBJETIVOS**, la grilla derecha muestra los objetivos de venta configurados para la categoría seleccionada.

### Grilla de objetivos

| Columna | Descripción |
|---|---|
| OBJETIVO 1 | Primer nivel de objetivo de venta |
| OBJETIVO 2 | Segundo nivel de objetivo de venta |
| OBJETIVO 3 | Tercer nivel de objetivo de venta |
| OBJETIVO 4 | Cuarto nivel de objetivo de venta |
| OBJETIVO 5 | Quinto nivel de objetivo de venta |

Desde este modo se pueden **agregar nuevos objetivos** o **eliminar** los existentes según la configuración comercial del negocio.

---

## Modo TASAS

Cuando el campo **DATO** tiene el valor **TASAS**, el panel izquierdo incorpora campos adicionales para modificar tasas de forma masiva, y la grilla derecha muestra las tasas configuradas.

### Campos adicionales en el panel izquierdo (modo TASAS)

| Campo / Botón | Descripción |
|---|---|
| Filtro de artículo | Permite filtrar artículos (disponible si el parámetro **ComisionesTasas** está activo en el sistema) |
| TASA | Valor porcentual de la tasa a aplicar |
| Selector de tasa | Elige a cuál de las 5 tasas se aplica el valor (TASA 1 a TASA 5) |
| Modificar | Aplica la tasa ingresada a todos los artículos que coincidan con el filtro |

### Grilla de tasas — con parámetro ComisionesTasas activo

Muestra las tasas a nivel de artículo individual:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Tasa 1 | Tasa de comisión para el objetivo 1 |
| Tasa 2 | Tasa de comisión para el objetivo 2 |
| Tasa 3 | Tasa de comisión para el objetivo 3 |
| Tasa 4 | Tasa de comisión para el objetivo 4 |
| Tasa 5 | Tasa de comisión para el objetivo 5 |
| Articulo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo de artículo |
| Marca | Marca |
| Variante | Variante del artículo |

### Grilla de tasas — sin parámetro ComisionesTasas

Muestra las tasas agrupadas por tipo de artículo:

| Columna | Descripción |
|---|---|
| Tipo de Artículo | Categoría o tipo al que pertenece |
| Tasa 1 | Tasa de comisión para el objetivo 1 |
| Tasa 2 | Tasa de comisión para el objetivo 2 |
| Tasa 3 | Tasa de comisión para el objetivo 3 |
| Tasa 4 | Tasa de comisión para el objetivo 4 |
| Tasa 5 | Tasa de comisión para el objetivo 5 |

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
