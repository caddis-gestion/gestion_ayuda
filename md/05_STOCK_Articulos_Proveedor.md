# 5.13 ARTÍCULOS PROVEEDOR
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Proveedor

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Proveedor** permite asociar artículos del catálogo con sus proveedores, registrando el código que usa cada proveedor para identificar ese artículo. Desde aquí podés:

- Vincular un artículo a uno o más proveedores
- Registrar el código interno del proveedor para ese artículo
- Importar asociaciones masivamente desde un archivo
- Eliminar vinculaciones existentes

---

<img src="imagenes/pantalla_articulos_proveedor.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Proveedor**

---

## Formulario

| Campo | Descripción |
|---|---|
| **ARTICULO** | Artículo del catálogo a vincular |
| **PROVEEDOR** | Proveedor al que se asocia el artículo |
| **CODIGO** | Código con el que el proveedor identifica este artículo (máximo 15 caracteres) |

### Sección IMPORTAR

Permite cargar masivamente asociaciones artículo-proveedor desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y actualiza las asociaciones. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **3 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Proveedor Nombre** | Nombre exacto del proveedor | Debe coincidir exactamente con el nombre en Caddis |
| **Proveedor Articulo Codigo** | Código con el que el proveedor identifica este artículo | Texto libre, máximo 15 caracteres |

#### Validaciones del sistema

- El artículo debe existir en el catálogo de Caddis; los no encontrados se omiten.
- El proveedor debe existir en el sistema con el **nombre exacto** indicado; los no encontrados se omiten.

#### Qué hace el sistema al importar

El sistema usa REEMPLAZAR (REPLACE INTO): si ya existe la asociación artículo-proveedor, actualiza el código del proveedor; si no existe, la crea. Al finalizar, actualiza la vista de artículos del sistema.

---

## Panel derecho — Grilla de proveedores del artículo

Muestra los proveedores ya vinculados al artículo seleccionado:

| Columna | Descripción |
|---|---|
| Proveedor | Nombre del proveedor |
| Codigo | Código del artículo en el proveedor |

**Acciones:**
- **Borrar:** Elimina la vinculación artículo-proveedor

---

## Notas importantes

- Un artículo puede tener varios proveedores asociados.
- El código del proveedor es útil para facilitar la comunicación de pedidos y para cruzar datos con remitos o archivos del proveedor.
