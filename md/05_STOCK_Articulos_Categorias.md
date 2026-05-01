# 5.06 ARTÍCULOS CATEGORÍAS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Categorias

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Categorías** permite administrar las categorías jerárquicas de artículos. Las categorías se usan para clasificar los productos en árbol (padre → hijo → nieto). Desde aquí podés:

- Crear nuevas categorías
- Asignar una categoría padre (hasta 4 niveles de jerarquía)
- Modificar o eliminar categorías existentes

---

<img src="imagenes/pantalla_articulos_categorias.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Categorias**

---

## Formulario

| Campo | Descripción |
|---|---|
| **CATEGORIA** | Nombre de la categoría (máximo 50 caracteres) |
| **PADRE** | Categoría padre en la jerarquía. Dejar vacío si es una categoría de primer nivel. |

---

## Grilla de categorías

| Columna | Descripción |
|---|---|
| Id | Código interno |
| Categoria | Nombre de la categoría |
| Padre (×3) | Categorías ancestro en la jerarquía (hasta 4 niveles) |

**Acciones:**
- **Modificar:** Edita el nombre o padre de la categoría
- **Borrar:** Elimina la categoría

---

## Notas importantes

- La jerarquía de categorías permite hasta 4 niveles (padre, abuelo, bisabuelo, tatarabuelo).
- No elimines categorías que estén asignadas a artículos activos.
