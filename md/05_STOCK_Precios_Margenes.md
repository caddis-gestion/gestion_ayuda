# 5.48 MARGENES DE VENTA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Precios Márgenes

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Precios Márgenes** permite gestionar el markup (margen de ganancia) de los artículos en una lista de precios. A diferencia de Artículos Precios que edita el precio directo, esta pantalla trabaja con el porcentaje de markup que se aplica al costo para calcular el precio. Desde aquí podés:

- Ver y editar el markup % de cada artículo en una lista de precios
- Aplicar un markup masivo a todos los artículos filtrados
- Regenerar todos los precios en base al costo actual y el markup definido
- Importar márgenes desde un archivo

---

<img src="imagenes/pantalla_precios_margenes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Precios Márgenes**

---

## Formulario

| Campo | Descripción |
|---|---|
| **LISTA** | Lista de precios a gestionar. Botón **Agregar** para agregar artículo |
| **ARTICULO** | Código o descripción del artículo |
| **NEGOCIO** | Línea de negocio a la que pertenece el artículo |
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **PROVEEDOR** | Proveedor del artículo |
| **VER MARKUPS** | Filtra artículos: TODOS / CON MARKUP / SIN MARKUP |

### Sección MODIFICAR MARKUPS

| Campo | Descripción |
|---|---|
| **MARKUP %** | Porcentaje de markup a aplicar a todos los artículos filtrados (botón **Modificar**) |

### Sección REGENERAR TODOS LOS PRECIOS

El botón **Regenerar Precios** recalcula los precios de todos los artículos aplicando el último costo ingresado y el margen definido para cada uno.

### Sección IMPORTAR MARGENES

Permite cargar masivamente los márgenes de una lista de precios desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y actualiza los márgenes de la lista activa. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **2 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Precio Final** | Porcentaje de margen a aplicar | Número positivo, punto como separador decimal. Ej: `25.50` |

> ⚠️ **Importante:** aunque la columna se llama "Precio Final" en el formato de ejemplo, al importar en esta pantalla el valor se interpreta como **porcentaje de margen** (no como precio). Por ejemplo, el valor `25.50` establece un margen del 25,50%.

#### Validaciones del sistema

- El separador decimal **debe ser punto** (no coma). Ej: `25.50`, no `25,50`.
- Los márgenes **deben ser mayores a 0**. Los registros con margen 0 se descartan.
- El artículo debe existir en la lista de precios activa; los que no se encuentran se omiten.

#### Qué hace el sistema al importar

El sistema actualiza el margen de cada artículo en la lista de precios activa. Los precios de venta se recalculan automáticamente en base al nuevo margen y el costo vigente.

---

## Panel derecho — Grilla de márgenes

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| MarkUp % | Porcentaje de markup (editable, en amarillo) |
| Margen % | Porcentaje de margen sobre el precio de venta |
| Precio Vta | Precio de venta con impuestos |
| Costo con Impuestos | Costo total incluyendo IVA e Impuesto Interno |
| Costo sin Impuestos | Costo neto |
| Iva % | Alícuota de IVA |
| Impuesto Interno % | Alícuota de impuesto interno |
| Moneda | Moneda de la lista |
| Articulo | Descripción del artículo |
| Tipo | Tipo del artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |

---

## Notas importantes

- La columna **MarkUp %** es editable directamente en la grilla.
- La diferencia con **Artículos Precios**: aquí se gestiona el margen y se regeneran los precios; allá se edita el precio directamente.
- Solo artículos activos con precio en la lista seleccionada.
