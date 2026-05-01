# 12.06 TRASLADOS DE REPARACIÓN
### Módulo 12 — Reparaciones

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reparaciones → Traslados

---

## ¿Para qué sirve esta pantalla?

**Traslados** registra el movimiento físico de equipos en reparación entre depósitos o hacia el service externo. Permite trasladar múltiples equipos en una sola operación, ingresando los IMEI/NSE de forma masiva. Cada traslado genera un lote identificado por número de movimiento.

---

<img src="imagenes/pantalla_traslados_reparacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reparaciones → Traslados**

---

## Panel izquierdo: Configuración del traslado

| Campo / Botón | Descripción |
|---|---|
| **FECHA** | Fecha del traslado. |
| **DESTINO** | Depósito o service de destino. El desplegable incluye los PDV habilitados más el service central (código 1000). |
| **OBSERVACIONES** | Texto libre para describir el motivo o detalles del traslado. |
| **Múltiple** | Abre una ventana para ingresar masivamente los IMEI/NSE de los equipos a trasladar. |

---

## Panel derecho: Grilla del lote actual

Muestra los equipos ingresados en el traslado en curso.

| Columna | Descripción |
|---|---|
| **Nro. Orden** | Número de la orden de reparación. |
| **Fecha** | Fecha de creación de la orden. |
| **IMEI** | Número de serie del equipo. |
| **Error** | Indica con **X** si el equipo tuvo un error al ser procesado. |
| **Mensaje** | Descripción del error (si aplica). Por ejemplo: IMEI no encontrado, orden ya entregada. |
| **Estado actual** | Estado de la orden de reparación. |
| **Depósito actual** | Depósito de origen del equipo. |
| **Borrar** | Elimina el equipo del lote antes de confirmar el traslado. |

---

## Uso típico

1. Seleccioná la **FECHA** y el **DESTINO**.
2. Ingresá las **OBSERVACIONES** del traslado.
3. Hacé clic en **Múltiple** e ingresá los IMEI de los equipos a trasladar (uno por línea).
4. El sistema procesa cada IMEI y lo muestra en la grilla con el resultado.
5. Revisá la columna **Error** para detectar equipos con problemas y usá **Borrar** si hay alguno incorrecto.
6. Confirmá el traslado. El sistema registra el lote y actualiza la ubicación de cada equipo.

> ⚠️ Los equipos con **Error = X** no serán trasladados. Corregí el problema antes de volver a intentarlo.

---

> 📖 Para ver el historial de todos los traslados de un equipo consultá [**Traslados Historia**](https://ayuda.caddis.com.ar/instructivos/12_REP_Traslados_Historia.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
