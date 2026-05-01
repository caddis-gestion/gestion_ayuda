# 16.10 STOCK DE EQUIPOS TOTALES
### Módulo 16 — Reportes

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reportes → Stock de Equipos Totales

---

## ¿Para qué sirve esta pantalla?

Muestra el stock actual de equipos (celulares y accesorios) disponibles en el sistema, agrupados por artículo y tipo de compra. Permite ver de un vistazo cuántas unidades hay en cada punto de venta, filtrando por PDV y opcionalmente incluyendo SIMs. Es el reporte consolidado de inventario físico de equipos no facturados.

---

<img src="imagenes/pantalla_reportes_stock_equipos_totales.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reportes → Stock de Equipos Totales**

---

## Filtros disponibles

| Filtro | Descripción |
|---|---|
| PDV | Punto de venta (depósito) a consultar. Por defecto muestra todos los PDV permitidos para el usuario. |
| SIMS | Solo visible en menús con prestatarias habilitadas. Permite incluir (SI) o excluir (NO) los artículos de tipo SIM del resultado. |

> Los equipos que se muestran son únicamente los que están activados = NO, con estado activo (1 o 2) o pendiente (90), asignados a un depósito válido y no facturados.

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| Código | Código interno del artículo (Telefono_Codigo) |
| Artículo | Marca y descripción del artículo concatenadas |
| Compra Tipo | Tipo de compra mediante el cual ingresó el equipo al stock |
| Cantidad | Cantidad de unidades disponibles para ese artículo y tipo de compra |
| Tipo | Tipo de artículo (ej: Smartphone, Accesorio) |
| Grupo | Grupo al que pertenece el artículo |
| Marca | Marca del artículo |
| Variante | Variante del artículo (ej: color, capacidad) |

> La grilla muestra totales y detalle. Los resultados se ordenan por marca y descripción del artículo.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
