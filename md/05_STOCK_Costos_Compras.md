# 5.29 COSTOS — COMPRAS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Costos Compras

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Costos Compras** permite consultar y actualizar los costos de compra de los artículos a partir de los remitos de ingreso. También permite importar costos masivamente desde un archivo. Desde aquí podés:

- Buscar el costo neto de artículos por remito de ingreso o por artículo
- Editar el costo neto directamente en la grilla
- Importar costos desde un archivo asociado a un remito de ingreso

---

<img src="imagenes/pantalla_costos_compras.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Costos Compras**

---

## Formulario

| Campo | Descripción |
|---|---|
| **REMITO** | Número del remito de ingreso a consultar (con botón **Buscar**) |
| **ARTICULO** | Código del artículo a consultar |
| **MONEDA** | Moneda de costos configurada en el sistema (solo lectura) |

### Sección IMPORTAR COSTOS

Permite cargar masivamente los costos de compra asociados a un remito de ingreso desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y actualiza los costos del remito activo. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **2 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo y en el remito activo |
| **Costo Neto** | Costo de compra **sin IVA** | Decimal, punto como separador. Ej: `3500.00` |

#### Requisito previo

**Es obligatorio tener un remito seleccionado** antes de importar. El sistema asocia los costos a ese remito específico.

#### Validaciones del sistema

- El separador decimal **debe ser punto** (no coma).
- Los registros con **Costo = 0** se omiten.
- El artículo debe existir en el catálogo y en el remito activo; los no encontrados se ignoran silenciosamente.

#### Qué hace el sistema al importar

1. Actualiza el costo unitario (`ArtMov_PrecioU`) en el detalle del remito de ingreso.
2. Actualiza el `Costo_Compras` en la tabla de costos del artículo, **solo si la fecha del remito es igual o posterior** a la última actualización registrada (para no sobreescribir un costo más nuevo con uno más antiguo).

---

## Panel derecho — Grilla de costos de compra

| Columna | Descripción |
|---|---|
| Costo Neto | Costo neto por unidad (editable en la grilla) |
| Cantidad | Cantidad del artículo en el remito |
| Total | Total del costo (Costo Neto × Cantidad) |
| Codigo | Código del artículo |
| Articulo | Descripción del artículo |
| Remito | Número de remito interno |
| RtoProv | Número de remito del proveedor |
| Fecha | Fecha del remito |
| Proveedor | Nombre del proveedor/depósito de origen |

**Acciones:**
- **Imprimir:** Imprime el listado de costos de compra

---

## Notas importantes

- La columna **Costo Neto** es editable directamente en la grilla para ajustar valores si fuera necesario.
- Para ver una consulta hay que ingresar al menos un filtro (remito o artículo); si no se ingresa ninguno, la grilla no muestra resultados.
- La moneda se configura en los parámetros del sistema y no es modificable desde esta pantalla.
