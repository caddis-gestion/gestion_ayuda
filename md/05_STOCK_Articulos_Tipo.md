# 5.07 ARTÍCULOS TIPO
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Tipo

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Tipo** permite administrar los tipos de artículos del catálogo. El tipo es una clasificación fundamental que determina cómo se comporta el artículo en el sistema (si tiene reparación, a qué negocio pertenece, su prefijo de código). Desde aquí podés:

- Crear nuevos tipos de artículo
- Asignar el negocio, prefijo y categoría de garantía extendida
- Indicar si el tipo admite reparaciones
- Modificar o eliminar tipos existentes

---

<img src="imagenes/pantalla_articulos_tipo.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Tipo**

---

## Formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno del tipo (solo lectura, asignado automáticamente) |
| **TIPO** | Nombre del tipo de artículo (máximo 50 caracteres) |
| **PREFIJO** | Prefijo de 3 caracteres que se antepone al código del artículo |
| **NEGOCIO** | Negocio al que pertenece el tipo (ej. Telefonía, Accesorios, Servicios) |
| **REPARACION** | Indica si los artículos de este tipo pueden tener órdenes de reparación (SI / NO) |
| **TIPO GAREX** | Categoría de garantía extendida (Garex) asociada a este tipo |

---

## Grilla de tipos

| Columna | Descripción |
|---|---|
| Codigo | Código del tipo |
| Tipo | Nombre del tipo |
| Prefijo | Prefijo de código |
| Negocio | Negocio asociado |
| Reparación | SI o NO |
| Artículo Garex | Categoría de garantía extendida (grupo y tipo Garex) |

**Acciones:**
- **Modificar:** Edita el tipo seleccionado
- **Borrar:** Elimina el tipo (solo tipos con código ≥ 100)

---

## Notas importantes

- Solo se muestran tipos con código ≥ 100 (los menores son tipos del sistema reservados).
- El **PREFIJO** se usa para generar el código automático de nuevos artículos de ese tipo.
- Si **REPARACION = SI**, los artículos de ese tipo aparecen disponibles en el módulo de Reparaciones.
