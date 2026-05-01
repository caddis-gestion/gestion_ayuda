# 5.02 ARTÍCULOS INGRESOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Ingresos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Ingresos** permite registrar el ingreso de mercadería al depósito. Se usa cuando llega una compra de un proveedor o una transferencia de stock. Desde aquí podés:

- Crear un remito de ingreso con los artículos recibidos
- Indicar el proveedor de origen y el depósito de destino
- Ingresar artículos individualmente, en forma múltiple o desde una orden de compra
- Registrar el costo unitario de cada artículo
- Importar el detalle desde un archivo

---

<img src="imagenes/pantalla_articulos_ingresos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Ingresos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario del ingreso y un panel derecho con el detalle de artículos ya ingresados.

---

## Encabezado del remito de ingreso

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha del ingreso |
| **REMITO** | Número de remito (se asigna automáticamente, editable) |
| **ORIGEN** | Proveedor del que proviene la mercadería |
| **DESTINO** | Depósito de destino donde se acredita el stock |
| **OBSERVACIONES** | Notas adicionales sobre el ingreso |

---

## Sección de artículos

| Campo / Botón | Descripción |
|---|---|
| **DESPACHO** | Número de despacho de aduana (si aplica) |
| **ARTICULO** | Búsqueda del artículo a ingresar |
| **COSTO NETO** | Precio de costo neto (sin IVA) del artículo. Se autocompleta si está cargado en el sistema. |
| **CANTIDAD** | Cantidad a ingresar |
| **Ingresar** | Agrega el artículo con el costo y cantidad indicados |
| **Multiple** | Permite ingresar múltiples artículos a la vez |
| **Ordenes Compra** | Busca órdenes de compra pendientes de recepción para importar su detalle |

---

## Sección IMPORTAR

Permite cargar masivamente el detalle de artículos del ingreso desde un archivo Excel, en lugar de ingresarlos uno por uno. Es útil cuando el ingreso incluye muchos artículos o cuando el proveedor entrega un listado en planilla.

### Elementos del área de importación

| Elemento | Descripción |
|---|---|
| **Campo de archivo** | Muestra el nombre del archivo seleccionado. |
| **Ícono de carpeta** | Abre el explorador de archivos para seleccionar el archivo a importar. |
| **Botón Importar** | Procesa e importa el archivo seleccionado. |
| **Botón Formato** | Abre una ventana con el formato de ejemplo del archivo requerido, con datos reales del sistema como referencia. |

---

### Formato del archivo a importar

Presioná **Formato** antes de armar el archivo para ver el modelo exacto con datos del sistema como ejemplo. El archivo debe ser de tipo Excel (`.xls` o `.xlsx`) y contener las siguientes columnas **en este orden**, con encabezado en la primera fila:

| N° | Columna | Tipo | Descripción |
|---|---|---|---|
| 1 | **Codigo** | Texto | Código del artículo en Caddis. Debe existir en el catálogo. |
| 2 | **Cantidad** | Número entero | Unidades a ingresar al depósito. |
| 3 | **Costo** | Número decimal | Costo neto unitario del artículo (sin IVA). |
| 4 | **Despacho** | Texto | Número de despacho de aduana. Dejar vacío si no aplica. |

**Ejemplo de archivo:**

| Codigo | Cantidad | Costo | Despacho |
|---|---|---|---|
| ART001 | 10 | 15000.00 | |
| ART002 | 5 | 8500.50 | 24-001-00123/8 |
| ART003 | 20 | 3200.00 | |

---

### Cómo importar el archivo paso a paso

> ⚠️ El **ORIGEN** (proveedor) y el **DESTINO** (depósito) del encabezado deben estar seleccionados antes de importar. Si alguno está vacío, el sistema mostrará un aviso y no procesará el archivo.

1. Completá los campos **ORIGEN** y **DESTINO** en el encabezado del remito.
2. Hacé click en **Formato** para ver el modelo de columnas requeridas.
3. Prepará el archivo Excel con las columnas: **Codigo / Cantidad / Costo / Despacho** en ese orden, con encabezado en la primera fila.
4. Hacé click en el ícono de carpeta y seleccioná el archivo desde tu equipo.
5. El nombre del archivo aparece en el campo de texto.
6. Hacé click en **Importar**.
7. El sistema procesa el archivo y agrega los artículos al detalle del ingreso. Si hay errores (código inexistente, cantidad inválida), se informan en pantalla para corregirlos.

---

## Panel derecho — Detalle del ingreso

Muestra los artículos ya cargados en el remito de ingreso:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Unidades ingresadas |
| Precio Unitario | Costo unitario (con IVA) |
| Precio Total | Costo total (con IVA) |
| Articulo | Descripción |
| Tipo / Grupo / Marca / Variante | Clasificación del artículo |

**Acciones:**
- **Borrar:** Elimina un artículo del ingreso
- **Detalle:** Ver detalle del ítem

---

## Notas importantes

- El **DESTINO** por defecto es el depósito central (código 1000) si el parámetro `sArtIngreso` está activo.
- El costo se registra neto (sin IVA); el sistema muestra el precio con IVA en la grilla.
- Al usar **Ordenes Compra**, se importan automáticamente los artículos de la orden pendiente seleccionada.
