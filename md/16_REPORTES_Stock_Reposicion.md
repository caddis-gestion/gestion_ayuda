# 16.04 STOCK REPOSICIÓN
### Módulo 16 — Reportes

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reportes → Stock Reposicion

---

## ¿Para qué sirve esta pantalla?

Muestra los artículos que tienen stock de reposición definido y requieren ser pedidos, o que tienen pedidos pendientes. Permite controlar el estado de los pedidos de clientes y las órdenes de compra asociadas, facilitando la gestión de reabastecimiento.

Solo muestra artículos con Stock Reposicion > 0 o con OC en tránsito.

---

<img src="imagenes/pantalla_stock_reposicion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reportes → Stock Reposicion**

---

## Filtros

Permite filtrar la lista de artículos por código, tipo, grupo, marca o variante.

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| Código | Código del artículo |
| Artículo | Descripción |
| Cantidad Pedidos | Total de unidades pedidas por clientes (presupuestos activos) |
| Pedidos Internos | Pedidos internos (PM) |
| PP Facturado | Presupuestos ya facturados |
| PP sin Facturar | Presupuestos pendientes de facturar |
| Pedidos con OC | Pedidos que tienen OC asociada |
| Pedidos sin OC | Pedidos sin orden de compra |
| OC Recibida | Unidades recibidas por OC |
| OC Transito | Unidades en OC pendientes de recibir |
| Stock Total | Stock actual en todos los depósitos |
| Stock Repo | Mínimo de reposición configurado |
| Reponer | Cantidad a reponer (Stock Repo - Stock Total - OC Tránsito) — editable |
| Tipo | Tipo de artículo |
| Grupo | Grupo de artículo |
| Marca | Marca |
| Proveedores | Proveedores del artículo |
| Variante | Variante |

> ℹ️ La columna **Reponer** tiene fondo amarillo y es editable. Valores negativos indican que hay stock suficiente y no es necesario reponer.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
