# 5.14 ARTÍCULOS RELACIONES
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Relaciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Relaciones** permite definir relaciones de insumo-producto entre artículos: qué insumos se necesitan para producir o transformar un artículo final. Esto se usa en el módulo de producción para controlar el consumo de materias primas. Desde aquí podés:

- Definir el artículo final y su cantidad de producción
- Asociar insumos con su cantidad y unidad de medida
- Activar o desactivar relaciones sin eliminarlas
- Consultar y modificar relaciones existentes

---

<img src="imagenes/pantalla_articulos_relaciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Relaciones**

---

## Sección PRODUCTO FINAL

| Campo | Descripción |
|---|---|
| **PRODUCTO FINAL** | Artículo que se obtiene como resultado (solo editable si es una relación nueva) |
| **DESCRIPCION** | Descripción del artículo final (solo lectura) |
| **CLASE** | Clase del artículo final (solo lectura) |
| **CANTIDAD** | Cantidad del producto final que genera la relación |
| **Unidad** | Unidad de medida del producto final |

---

## Sección RELACIÓN — Insumo

| Campo | Descripción |
|---|---|
| **ESTADO** | Estado de la relación: ACTIVA o INACTIVA |
| **INSUMO** | Artículo insumo que se consume para producir el artículo final |
| **DESCRIPCION** | Descripción del insumo (solo lectura) |
| **CLASE** | Clase del insumo (solo lectura) |
| **CANTIDAD** | Cantidad del insumo necesaria |
| **Unidad** | Unidad de medida del insumo |

---

## Panel derecho — Grilla de relaciones

Muestra todas las relaciones de insumos para el producto final seleccionado:

| Columna | Descripción |
|---|---|
| Estado | ACTIVA o INACTIVA |
| Insumo Codigo | Código del artículo insumo |
| Insumo Clase | Clase del insumo |
| Prod Final Cant | Cantidad del producto final |
| Insumo Cant | Cantidad del insumo |
| Insumo Desc. | Descripción del insumo |

**Acciones:**
- **Modificar:** Edita la relación seleccionada
- **Borrar:** Elimina la relación

---

## Notas importantes

- Las relaciones INACTIVAS no se usan en la producción pero quedan registradas para historial.
- La cantidad y unidad del producto final son compartidas por todas las relaciones del mismo artículo.
