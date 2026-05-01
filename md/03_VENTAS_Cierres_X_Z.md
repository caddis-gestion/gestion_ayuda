# 3.34 CIERRES X Y Z
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Cierres X y Z

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cierres X y Z** permite emitir los cierres fiscales de la controladora fiscal (o impresora fiscal). Desde aquí podés:

- Emitir un **Cierre X** (cierre parcial, no acumulativo): consulta los totales del día sin cerrar el período fiscal
- Emitir un **Cierre Z** (cierre definitivo del día): cierra el período fiscal diario y acumula los totales en la memoria fiscal
- Emitir **Cierres Z de fechas anteriores** en forma retroactiva (para cerrar períodos que quedaron abiertos)

---

<img src="imagenes/pantalla_cierres_x_z.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Cierres X y Z**

---

## Descripción general de la pantalla

La pantalla tiene dos secciones principales: los botones de cierre del día actual y la sección para cierres Z de fechas anteriores.

---

## Sección principal — Cierres del día

| Botón | Descripción |
|---|---|
| **Cierre X** | Emite un reporte parcial de los totales acumulados hasta el momento. No cierra el día ni afecta la memoria fiscal. Se puede hacer varias veces por día. |
| **Cierre Z** | Emite el cierre definitivo del día. Acumula los totales en la memoria fiscal y cierra el período diario. Se debe hacer una sola vez al final del día. |

> ⚠️ El **Cierre Z** es definitivo e irreversible. Una vez emitido, no se pueden registrar más comprobantes para esa fecha en la controladora fiscal.

---

## Sección — Cierres Z Antiguos

Permite emitir cierres Z de fechas anteriores que quedaron pendientes.

| Campo / Botón | Descripción |
|---|---|
| **DESDE** | Fecha de inicio del rango a cerrar |
| **HASTA** | Fecha de fin del rango a cerrar |
| **CIERRE GLOBAL** | Checkbox: si está activado, emite el cierre Z para todas las fechas del rango de una sola vez |
| **Z Antiguos** | Ejecuta el cierre Z para el rango de fechas indicado |

---

## Notas importantes

- El **Cierre X** es una herramienta de consulta: se puede usar en cualquier momento del día para ver los totales acumulados sin consecuencias.
- El **Cierre Z** debe hacerse una vez por día, generalmente al cierre de la jornada comercial.
- Si se omitió el Cierre Z de un día anterior, usá la sección **Cierres Z Antiguos** para regularizar la situación antes de continuar operando.
- Esta pantalla trabaja directamente con la controladora o impresora fiscal conectada al punto de venta.
