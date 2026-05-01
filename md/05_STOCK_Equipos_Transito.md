# 5.39 EQUIPOS — TRÁNSITO
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Tránsito

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Tránsito** permite gestionar los equipos que están en camino hacia un PDV, permitiendo confirmar su recepción. Desde aquí podés:

- Seleccionar el PDV destino y ver los remitos de tránsito pendientes
- Ver los equipos en tránsito de cada remito (NSE, modelo, PDV de origen, estado)
- Confirmar la recepción de todos los equipos de un remito

---

<img src="imagenes/pantalla_equipos_transito.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Tránsito**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta de destino (donde se recibirán los equipos) |
| **REMITOS** | Lista desplegable con los remitos de tránsito pendientes para el PDV seleccionado. Muestra la fecha, número y PDV de origen |

**Acciones:**
- **Aceptar Todos:** Confirma la recepción de todos los equipos del remito seleccionado

---

## Panel derecho — Grilla de equipos en tránsito

| Columna | Descripción |
|---|---|
| NSE | Número de serie del equipo en tránsito |
| Equipo | Marca y modelo del equipo |
| PDV Origen | PDV desde donde se envió el equipo |
| Estado | Estado actual del equipo en el sistema |

---

## Notas importantes

- Solo se muestran equipos con estado 90 (EN TRÁNSITO) destinados al PDV seleccionado.
- Al usar **Aceptar Todos**, el sistema registra la recepción de todos los equipos del remito y actualiza su estado.
- Si el remito tiene equipos con errores de estado, éstos no aparecerán en la grilla.
