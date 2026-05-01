# 7.20 TV STOCK DE SEGURIDAD
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Stock de Seguridad

---

## ¿Para qué sirve esta pantalla?

**TV Stock de Seguridad** permite definir un stock mínimo de reserva para cada artículo en la tienda virtual. Cuando el stock disponible llega al valor de seguridad, el sistema deja de publicar ese artículo como disponible en la tienda, evitando ventas que no podrían despacharse. Desde aquí podés:

- Consultar y editar el stock de seguridad artículo por artículo
- Importar los valores masivamente desde un archivo Excel

---

<img src="imagenes/pantalla_tv_stock_seguridad.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Stock de Seguridad**

---

## Panel izquierdo: Filtros e importación

### Filtros de artículos

| Campo | Descripción |
|---|---|
| **Tipo / Marca / Grupo** | Filtros estándar para acotar la grilla a un conjunto de artículos. |
| *(otros filtros)* | Según configuración del sistema pueden aparecer filtros adicionales (Proveedor, etc.). |

### Sección IMPORTAR STOCK DE SEGURIDAD

Permite cargar los valores de stock de seguridad para múltiples artículos desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Hacé clic para seleccionar el archivo Excel (.xlsx) desde tu equipo. |
| **Importar** | Procesa el archivo y actualiza los valores de stock de seguridad en el sistema. |

#### Formato del archivo de importación

El archivo debe tener al menos dos columnas:

| Columna | Descripción |
|---|---|
| **Codigo** | SKU del artículo en Caddis (debe existir en el sistema). |
| **Stock Seguridad** | Valor numérico entero. Mínimo: 0. |

> Una vez seleccionado el archivo, hacé clic en **Importar**. El sistema procesa cada fila y actualiza el stock de seguridad del artículo correspondiente. Los artículos no encontrados se omiten.

---

## Panel derecho: Grilla de artículos

| Columna | Descripción |
|---|---|
| **Codigo** | SKU del artículo. |
| **Stock de Seguridad** | Cantidad de reserva (editable directamente, fondo amarillo). Editá el valor y guardá con el ícono o botón correspondiente. |
| **Articulo** | Nombre del artículo. |
| **Tipo** | Tipo de artículo. |
| **Grupo** | Grupo del artículo. |
| **Marca** | Marca del artículo. |
| **Variante** | Descripción de variante (si aplica). |

---

## Edición individual

Podés modificar el stock de seguridad de un artículo directamente en la columna **Stock de Seguridad** (fondo amarillo):

1. Hacé clic en la celda del artículo a modificar.
2. Ingresá el nuevo valor.
3. Guardá el cambio con el ícono de guardado de la fila.

---

## Uso típico

- Para ajustar artículos puntuales: editá la celda amarilla directamente en la grilla.
- Para actualizar muchos artículos a la vez: preparar el Excel con las columnas `Codigo` y `Stock Seguridad`, y usar la sección **IMPORTAR STOCK DE SEGURIDAD**.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
