# 12.08 ARTÍCULOS REPARABLES
### Módulo 12 — Reparaciones

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reparaciones → Articulos Reparables

---

## ¿Para qué sirve esta pantalla?

**Artículos Reparables** define qué artículos del catálogo de Caddis pueden ser recibidos en el servicio técnico. Solo los artículos incluidos en esta lista están disponibles para seleccionar al crear una nueva orden de reparación. Desde aquí podés:

- Agregar artículos reparables de forma individual
- Importar masivamente artículos reparables desde un archivo Excel
- Eliminar artículos de la lista

---

<img src="imagenes/pantalla_articulos_reparables.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reparaciones → Articulos Reparables**

---

## Panel izquierdo

### Filtro de artículos

| Campo | Descripción |
|---|---|
| **ARTÍCULO** | Código del artículo para filtrar la grilla o buscar uno específico para agregar. |

### Sección IMPORTAR

Permite cargar masivamente artículos reparables desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Hacé clic para seleccionar el archivo Excel (.xlsx) desde tu equipo. |
| **Importar** | Procesa el archivo y agrega los artículos a la lista de reparables. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **1 columna**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | Código (SKU) del artículo | Debe existir en el catálogo de Caddis |

> El sistema ignora los artículos cuyo código no existe en el catálogo. Para que un artículo sea importado correctamente, su SKU debe estar cargado previamente en Caddis.

#### Paso a paso para importar

1. Hacé clic en **Formato** para descargar el modelo de Excel con ejemplos de SKU.
2. Completá el archivo con los códigos de los artículos a habilitar.
3. Seleccioná el archivo con el botón de carga.
4. Hacé clic en **Importar**.
5. El sistema agrega los artículos que encontró en el catálogo.

---

## Panel derecho: Grilla de artículos reparables

| Columna | Descripción |
|---|---|
| **Código** | SKU del artículo. |
| **Marca** | Marca del artículo. |
| **Modelo** | Modelo del artículo. |
| **Artículo** | Descripción completa. |
| **Borrar** | Elimina el artículo de la lista de reparables. |

---

## Agregar un artículo individual

1. Ingresá el código del artículo en el campo **ARTÍCULO**.
2. Presioná **Enter**. El sistema agrega el artículo directamente a la grilla.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
