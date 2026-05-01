# 5.30 COSTOS — REPOSICIÓN
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Costos Reposición

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Costos Reposición** permite consultar y actualizar los costos de reposición de los artículos activos. También permite importar costos masivamente desde un archivo. Desde aquí podés:

- Consultar el costo de reposición y el costo de compra de cada artículo
- Editar el costo de reposición directamente en la grilla
- Importar costos de reposición desde un archivo
- Filtrar artículos por código, tipo, grupo, marca u otros criterios

---

<img src="imagenes/pantalla_costos_reposicion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Costos Reposición**

---

## Formulario

| Campo | Descripción |
|---|---|
| **MONEDA** | Moneda de costos configurada en el sistema (solo lectura) |
| **ARTICULO** | Código o descripción del artículo |
| **NEGOCIO** | Línea de negocio a la que pertenece el artículo |
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **PROVEEDOR** | Proveedor del artículo |

### Sección IMPORTAR COSTOS

Permite cargar masivamente los costos de reposición desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y actualiza los costos de reposición. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **2 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Costo Neto** | Costo de reposición **sin IVA** | Decimal, punto como separador. Ej: `3500.00` |

#### Validaciones del sistema

- El separador decimal **debe ser punto** (no coma).
- Los registros con **Costo = 0** se descartan y no modifican el valor actual.
- El artículo debe existir en el catálogo; los no encontrados se omiten.

#### Qué hace el sistema al importar

El sistema actualiza el campo `Costo_Reposicion` en la tabla de costos de cada artículo. Registra el usuario y la fecha de la última actualización.

---

## Panel derecho — Grilla de costos de reposición

| Columna | Descripción |
|---|---|
| Costo Reposicion | Costo de reposición en la moneda del sistema (editable, en amarillo) |
| Fecha | Fecha de última actualización del costo de reposición |
| Costo Compra | Costo de última compra (en amarillo) |
| Fecha | Fecha de última actualización del costo de compra |
| Codigo | Código del artículo |
| Articulo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Proveedores | Proveedores del artículo |

**Acciones:**
- **Detalle:** Abre el detalle completo del artículo

---

## Notas importantes

- La columna **Costo Reposicion** es editable directamente en la grilla (marcada en amarillo).
- Solo se muestran artículos activos.
- Los costos se muestran en la moneda configurada como moneda de costos del sistema, dividida por la cotización correspondiente.
- Usá la importación para actualizar costos de reposición de forma masiva cuando lleguen nuevas listas de precios de proveedores.
