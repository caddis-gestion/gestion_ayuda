# 5.28 COSTOS CONSULTA
### Módulo 5 — Stock y Logística

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Artículos Costos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Costos** permite consultar los costos actuales de los artículos, mostrando tanto el costo de reposición como el costo de última compra. Desde aquí podés:

- Filtrar artículos por código, tipo, grupo, marca, variante u otros criterios
- Ver el costo de reposición y el costo de compra de cada artículo con su fecha de actualización
- Acceder al detalle completo de cada artículo

---

<img src="imagenes/pantalla_articulos_costos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Artículos Costos**

---

## Formulario

Filtros de búsqueda de artículos (solo artículos activos):

| Campo | Descripción |
|---|---|
| **ARTICULO** | Código o descripción del artículo |
| **NEGOCIO** | Línea de negocio a la que pertenece el artículo |
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **PROVEEDOR** | Proveedor del artículo |

---

## Panel derecho — Grilla de costos

| Columna | Descripción |
|---|---|
| Reposicion | Costo de reposición vigente (en moneda configurada) |
| Fecha | Fecha de la última actualización del costo de reposición |
| Cto Compra | Costo de la última compra registrada |
| Fecha | Fecha de la última actualización del costo de compra |
| Codigo | Código del artículo |
| Articulo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Proveedores | Proveedores del artículo |

**Acciones:**
- **Detalle:** Abre el detalle completo del artículo

---

## Circuito de costos y armado de precios

El sistema calcula los precios de venta a partir de los costos y los márgenes definidos para cada artículo. El siguiente diagrama resume el circuito completo:

<img src="imagenes/diagrama_precios_y_costos.png" style="width:auto; height:auto; max-width:100%; display:block;">

### Costo Compras

Al recibir mercadería del proveedor el proceso es:

1. Los artículos se ingresan al stock desde **Artículos Ingresos**, registrando el remito del proveedor. En ese momento se puede indicar el COSTO NETO de cada artículo.
2. Cuando llega la factura del proveedor, se ingresa desde **Facturas Compras** asociándola al remito existente. En esa pantalla se completa el precio unitario de cada artículo.
3. Esa información queda registrada en el sistema como **Costo Compras** y se refleja en la columna **Cto Compra** de esta pantalla.

### Costo de Reposición

El costo de reposición puede actualizarse por dos vías:

| Vía | Descripción |
|---|---|
| **Por Compras** | Se actualiza automáticamente al registrar la factura del proveedor en Facturas Compras |
| **Por Inflación** | Se actualiza manualmente desde la pantalla **Costos por Reposición**, cargando los precios actualizados del proveedor tantas veces como sea necesario para reflejar la inflación |

### El costo más actual

El sistema **toma automáticamente el más reciente** entre el Costo de Reposición y el Costo Compras para calcular los precios de venta. La comparación es por fecha: el que tenga la fecha de actualización más reciente es el que se usa como base.

> Este es el costo que se muestra en la columna **Costo** de la pantalla **Márgenes de Venta** y el que se usa para calcular el MarkUp% y Margen% en **Artículos Precios**.

---

## Pantalla relacionada — Costos por Reposición

Desde **Stock → Costos por Reposición** se pueden actualizar manualmente los costos de reposición de los artículos, sin necesidad de registrar una compra. Es la herramienta para mantener los costos al día cuando hay inflación o cuando el proveedor informa nuevos precios.

### Filtros

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **ARTICULO** | Código o descripción del artículo |

### Grilla

| Columna | Descripción |
|---|---|
| Reposicion | Costo de reposición actual (editable directamente en la grilla) |
| Fecha | Fecha de la última actualización del costo de reposición |
| Cto Compra | Costo de la última compra registrada |
| Fecha | Fecha de la última actualización del costo de compra |
| Codigo | Código del artículo |

### Sección IMPORTAR COSTOS

Permite actualizar costos masivamente desde un archivo:

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo a importar |
| **Importar** (ícono naranja) | Procesa el archivo y actualiza los costos de reposición |
| **?** | Muestra el formato requerido para la importación |

---

## Pantalla relacionada — Márgenes de Venta

Desde **Stock → Márgenes de Venta** se define el porcentaje de margen que el sistema aplica sobre el costo para calcular automáticamente el precio de venta en cada lista de precios.

### Filtros

| Campo | Descripción |
|---|---|
| **LISTA** | Lista de precios a configurar |
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **BUSCAR** | Búsqueda por código o descripción |

### Grilla

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| **Margen %** | Porcentaje de margen de venta (editable, resaltado en amarillo) |
| Costo | Costo más actual del artículo |
| Precio Vta | Precio de venta calculado según el margen |
| Iva % | Alícuota de IVA |
| Moneda | Moneda de la lista |

### Sección MODIFICAR MASIVAMENTE

| Campo | Descripción |
|---|---|
| **MARGEN %** | Nuevo margen a aplicar a todos los artículos filtrados |
| **Modificar** | Aplica el margen a todos los artículos del filtro activo |

> ⚠️ Si el margen de un artículo está en **0**, el sistema **no actualiza su precio** al recalcular, dejando el valor que tiene en ese momento en la lista de precios.

---

## Notas importantes

- Los costos se muestran en la moneda configurada como moneda de costos del sistema.
- El sistema usa el **costo más reciente** entre Reposición y Compra para calcular precios y márgenes.
- Para actualizar costos de reposición manualmente usá **Costos por Reposición**.
- Para consultar los costos actualizados por compras usá **Costos por Compras** (Stock → Costos por Compras).
- Para configurar el margen de venta de cada artículo usá **Márgenes de Venta**.
- Solo se muestran artículos activos.

> Relacionado: [**Artículos Precios**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Precios.pdf) — consulta y edición de precios de venta con costos y márgenes
