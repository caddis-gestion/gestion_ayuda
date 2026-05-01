# 15.29 ARTÍCULOS — PUNTOS Y TASAS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Administración → Comisiones → Articulos Puntos

---

## ¿Para qué sirve esta pantalla?

Permite configurar los puntos y las tasas de descuento asignados a cada artículo dentro del programa de fidelización del sistema. Se pueden modificar los valores de forma individual directamente en la grilla, o de forma masiva aplicando un valor a todos los artículos que coincidan con un filtro. También permite importar los puntos y tasas desde archivos Excel.

---

<img src="imagenes/pantalla_articulos_puntos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Comisiones → Articulos Puntos**

---

## Panel izquierdo — Filtros y modificación masiva

### Filtro de artículos

Permite acotar los artículos que se muestran en la grilla y sobre los que se aplican las modificaciones masivas:

| Campo | Descripción |
|---|---|
| Código | Código del artículo |
| Negocio | Línea de negocio a la que pertenece el artículo (clasificación propia del catálogo) |
| Tipo | Tipo de artículo |
| Grupo | Grupo de artículo |
| Marca | Marca |
| Proveedor | Proveedor del artículo |

### Modificación masiva de Puntos

| Campo / Botón | Descripción |
|---|---|
| PUNTOS | Valor numérico de puntos a asignar |
| Modificar | Aplica el valor de puntos a todos los artículos que coincidan con el filtro activo |

### Modificación masiva de Tasa

| Campo / Botón | Descripción |
|---|---|
| TASA | Porcentaje de descuento a asignar |
| Modificar | Aplica el porcentaje a todos los artículos que coincidan con el filtro activo |

### Importar Puntos desde Excel

Permite actualizar masivamente los puntos de múltiples artículos desde un archivo Excel.

**Formato del archivo:**

| Columna | Nombre | Descripción | Valores válidos |
|---|---|---|---|
| A | Codigo | Código del artículo | Texto, debe coincidir exactamente con el código en el sistema |
| B | Puntos | Puntos a asignar | Número entero positivo (ej: `25`). No se admiten decimales ni coma como separador |

**Comportamiento:**
- Solo se actualizan los artículos cuyo código coincida con un artículo existente en el sistema.
- Las filas con valor `0` en Puntos se descartan y no modifican el artículo.
- El botón **Ayuda** (ícono carpeta) muestra un ejemplo del formato esperado con datos reales del sistema.

**Validaciones:**
- Si algún valor de Puntos contiene coma (ej: `25,0`), el sistema rechaza toda la importación con el mensaje *"El puntaje debe ingresarse como un valor entero. Ej: 25"*.
- Si algún valor es negativo, se rechaza con el mensaje *"El puntaje debe ser mayor a 0"*.

---

### Importar Tasas desde Excel

Permite actualizar masivamente la tasa de descuento de múltiples artículos desde un archivo Excel.

**Formato del archivo:**

| Columna | Nombre | Descripción | Valores válidos |
|---|---|---|---|
| A | Codigo | Código del artículo | Texto, debe coincidir exactamente con el código en el sistema |
| B | Tasas | Porcentaje de descuento | Número con punto como separador decimal (ej: `25.50`). No se admite coma |

**Comportamiento:**
- Solo se actualizan los artículos cuyo código coincida con un artículo existente en el sistema.
- Las filas con valor `0` en Tasas se descartan y no modifican el artículo.
- El valor se guarda internamente dividido por 100 (ej: `25.50` se almacena como `0.2550`).
- El botón **Ayuda** (ícono carpeta) muestra un ejemplo del formato esperado con datos reales del sistema.

**Validaciones:**
- Si algún valor de Tasas contiene coma (ej: `25,50`), el sistema rechaza toda la importación con el mensaje *"La tasa debe ingresarse solo con punto como separador de decimales. Ej: 25.50"*.
- Si algún valor es negativo, se rechaza con el mensaje *"La tasa debe ser mayor a 0"*.

---

## Grilla derecha — Artículos

Las columnas **Puntos** y **Tasa %** (resaltadas en amarillo) son editables directamente en la grilla. El resto de las columnas son de solo lectura y sirven para identificar el artículo:

| Columna | Descripción |
|---|---|
| Puntos | Puntos asignados al artículo (editable) |
| Tasa % | Tasa de descuento aplicada al artículo (editable) |
| Código | Código identificador del artículo |
| Artículo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo de artículo |
| Marca | Marca |

> **Tip:** Para modificar un artículo puntual, hacé clic directamente sobre la celda **Puntos** o **Tasa %** en la grilla y editá el valor. Para cambios masivos, usá los filtros del panel izquierdo junto con los botones **Modificar**.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
