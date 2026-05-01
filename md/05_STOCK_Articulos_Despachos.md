# 5.31 ARTÍCULOS — DESPACHOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Artículos Despachos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Despachos** permite consultar los movimientos de stock asociados a un número de despacho (número de importación o lote de ingreso). Desde aquí podés:

- Buscar movimientos por número de despacho, remito o artículo
- Registrar un nuevo número de despacho
- Ver el detalle de los movimientos vinculados a cada despacho

---

<img src="imagenes/pantalla_articulos_despachos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Artículos Despachos**

---

## Formulario

| Campo | Descripción |
|---|---|
| **DESPACHO** | Número de despacho a consultar |
| **REMITO** | Número de remito interno asociado |
| **ARTICULO** | Código del artículo |

### Sección NUEVO DESPACHO

| Campo | Descripción |
|---|---|
| **NUEVO** | Número del nuevo despacho a registrar |

---

## Panel derecho — Grilla de movimientos

| Columna | Descripción |
|---|---|
| Fecha | Fecha del movimiento de stock |
| Movimiento | Tipo de movimiento (ingreso, movimiento, devolución, etc.) |
| Remito Interno | Número de remito interno del sistema |
| Remito Proveedor | Número de remito del proveedor |
| Despacho | Número de despacho asociado (en amarillo) |
| Codigo | Código del artículo |
| Cantidad | Cantidad del movimiento (positiva para ingresos, negativa para salidas) |
| Articulo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Variante | Variante del artículo |

---

## Notas importantes

- Si no se ingresa ningún filtro, la grilla no muestra resultados (requiere al menos un criterio).
- El número de despacho identifica lotes de importación y permite rastrear el origen de los artículos.
- La cantidad se muestra positiva para ingresos y negativa para salidas o devoluciones.
