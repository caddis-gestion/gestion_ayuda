# 5.36 EQUIPOS — ASIGNACIÓN
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Asignación

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Asignación** permite asignar unidades de stock de equipos a puntos de venta. Gestiona el stock comprometido para cada PDV antes de la entrega efectiva. Desde aquí podés:

- Consultar o crear una asignación de equipos a un PDV
- Ver el stock físico, asignado, tomado y disponible de un equipo
- Asignar unidades adicionales o anular asignaciones
- Ver el detalle de la asignación por PDV

---

<img src="imagenes/pantalla_equipos_asignacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Asignación**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta para el que se realiza la asignación |
| **FECHA** | Fecha de la asignación |
| **ASIGNACION** | Número de asignación (solo lectura). Botón **Buscar** para localizar una existente, **Anular** para cancelarla |
| **EQUIPO** | Modelo/código de equipo a asignar |
| **STK FISICO** | Stock físico disponible del equipo (solo lectura) |
| **ASIGNADOS** | Cantidad ya comprometida en asignaciones (solo lectura) |
| **TOMADO** | Cantidad tomada/entregada (solo lectura) |
| **DISPONIBLE** | Stock disponible para asignar = Físico − Asignados − Tomado (solo lectura) |
| **ASIGNAR** | Cantidad a asignar | Botón **Ingresar** para confirmar |

---

## Panel derecho — Grilla de asignación

Muestra el detalle de la asignación seleccionada desglosado por PDV y equipo:

| Columna | Descripción |
|---|---|
| Equipo | Marca y modelo del equipo |
| Asignado | Cantidad asignada |
| Entregado | Cantidad ya entregada |
| POS | Nombre del punto de venta |

**Acciones:**
- **Modificar:** Edita la cantidad de la asignación
- **Borrar:** Elimina la asignación

---

## Notas importantes

- Las asignaciones permiten reservar stock para un PDV antes de la entrega efectiva.
- El stock **DISPONIBLE** disminuye al asignar y aumenta al anular o al devolver unidades.
