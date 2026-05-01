# 5.34 DEVOLUCIONES — GARANTÍA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Devoluciones Garantía

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Devoluciones Garantía** muestra las devoluciones que están listas para ser enviadas al proveedor como garantía. Permite seleccionar los artículos a remitir y gestionar el envío. Desde aquí podés:

- Filtrar las devoluciones aptas para envío en garantía por proveedor
- Seleccionar los artículos a incluir en el envío al proveedor
- Consultar el detalle de cada devolución

---

<img src="imagenes/pantalla_devoluciones_garantia.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Devoluciones Garantía**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PROVEEDOR** | Filtra las devoluciones por proveedor del artículo |

El filtro se aplica automáticamente al seleccionar el proveedor.

---

## Panel derecho — Grilla de devoluciones para garantía

Solo muestra las devoluciones que cumplen la condición de ser aptas para envío en garantía (según estado):

| Columna | Descripción |
|---|---|
| Checkbox | Permite seleccionar múltiples artículos para el envío |
| Devolucion | Código identificador de la devolución |
| Fecha | Fecha de creación de la devolución |
| Estado | Estado actual |
| Articulo Codigo | Código del artículo |
| Articulo Nombre | Descripción del artículo |
| Articulo Serie | Número de serie del artículo |

Las primeras 4 columnas están fijas para facilitar la navegación.

**Acciones:**
- **Detalle:** Abre el detalle de la devolución seleccionada

---

## Notas importantes

- Solo aparecen aquí las devoluciones cuyo estado las habilita para el envío en garantía al proveedor.
- Usá el checkbox para seleccionar múltiples artículos y procesarlos juntos.
- Los resultados se ordenan por número de lote descendente.
- Para registrar nuevas devoluciones usá **Devoluciones**; para consultar el historial completo usá **Devoluciones Consulta**.
