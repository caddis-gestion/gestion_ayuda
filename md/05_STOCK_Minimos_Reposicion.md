# 5.49 MÍNIMOS DE REPOSICIÓN
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Mínimos Reposición

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Mínimos de Reposición** permite definir la cantidad mínima de stock que debe tener cada artículo en cada punto de venta. Cuando el stock cae por debajo de ese mínimo, el sistema puede generar alertas o pedidos de reposición. Desde aquí podés:

- Consultar y editar el mínimo de reposición de cada artículo por PDV
- Filtrar artículos por tipo, grupo, marca, variante y otros criterios
- Importar mínimos de reposición desde un archivo

---

<img src="imagenes/pantalla_minimos_reposicion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Mínimos Reposición**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a consultar/configurar. Al cambiar aplica el filtro automáticamente |
| **ARTICULO** | Código o descripción del artículo |
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **VARIANTE** | Variante del artículo |

### Sección IMPORTAR MÍNIMOS REPOSICIÓN

Permite cargar masivamente los mínimos de reposición de todos los artículos del PDV seleccionado.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y actualiza los mínimos del PDV activo. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **2 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Stk Mínimo** | Cantidad mínima de reposición | Entero positivo |

#### Validaciones del sistema

- El artículo debe existir en el catálogo de Caddis; los que no se encuentran se omiten silenciosamente.
- **Se requiere un PDV seleccionado** en el panel izquierdo antes de importar.

#### Qué hace el sistema al importar

El sistema aplica los mínimos al PDV seleccionado. Si el artículo ya tenía un mínimo configurado, lo reemplaza con el nuevo valor (operación REEMPLAZAR). Si no tenía, lo crea.

---

## Panel derecho — Grilla de mínimos

Muestra los mínimos de reposición configurados para el PDV seleccionado:

| Columna | Descripción |
|---|---|
| Cantidad | Cantidad mínima de reposición (editable, en amarillo) |
| Punto de Venta | Nombre del PDV asociado |
| Codigo | Código del artículo |
| Articulo | Descripción del artículo |
| Tipo | Tipo del artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Variante | Variante del artículo |

La grilla es completamente editable en todas sus filas.

---

## Notas importantes

- Si no se selecciona un PDV, la grilla no muestra resultados.
- Solo se muestran artículos que no sean servicios (artículos físicos).
- Usá la importación para actualizar mínimos de reposición de forma masiva cuando cambian las políticas de stock.
