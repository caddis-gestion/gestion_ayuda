# 15.33 PUNTAJE POR VENTAS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Comisiones → Puntaje por Ventas

---

## ¿Para qué sirve esta pantalla?

Permite consultar el puntaje acumulado por ventas de un comisionado (vendedor, supervisor, jefe de ventas o gerente) en una liquidación determinada. El sistema muestra un resumen agrupado por tipo de operación con la cantidad de operaciones y los puntos obtenidos en cada grupo.

Esta pantalla es de consulta: no genera ni modifica datos, sino que permite verificar cómo se compone el puntaje de cada integrante del equipo comercial en una liquidación específica.

---

<img src="imagenes/pantalla_admin_puntaje_ventas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Comisiones → Puntaje por Ventas**

---

## Panel izquierdo — Filtros de consulta

| Campo | Descripción |
|---|---|
| LIQUIDACION | Número de liquidación a consultar. Por defecto se muestra la última liquidación registrada. |
| COMISIONADO | Rol del integrante a consultar. Opciones: **VENDEDOR** / **SUPERVISOR** / **JEFE VENTAS** / **GERENTE**. |
| NOMBRE | Nombre del comisionado. Se filtra según el rol seleccionado en el campo anterior. |

> **Tip:** Al cambiar el tipo de comisionado, el campo NOMBRE se actualiza automáticamente para mostrar solo las personas del rol seleccionado.

---

## Grilla derecha — Detalle de puntaje

Muestra el resumen de puntaje del comisionado seleccionado para la liquidación indicada:

| Columna | Descripción |
|---|---|
| Grupo | Tipo de operación o producto (planes, accesorios, liberados, etc.). |
| Operaciones | Cantidad de operaciones realizadas en ese grupo. |
| Puntos | Total de puntos acumulados en ese grupo. |
| **TOTAL** | Fila de totales al pie de la grilla con la suma de operaciones y puntos. |

> **Nota:** Las operaciones observadas (legajos observados) no suman puntos. Los accesorios y equipos liberados acumulan puntos según la configuración de cada artículo.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
