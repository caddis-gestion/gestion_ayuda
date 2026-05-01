# 3.51 ELIMINAR REMITO T3
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Eliminar Remito T3

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Eliminar Remito T3** permite eliminar remitos de tipo T3 (RM e IRM) que fueron generados por error o que necesitan ser removidos del sistema. Desde aquí podés:

- Seleccionar el tipo de remito (RM o IRM) y su número
- Eliminarlo definitivamente del sistema

> ⚠️ Esta operación es **irreversible**. Verificá bien el número del remito antes de eliminarlo.

---

<img src="imagenes/pantalla_eliminar_remito_t3.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Eliminar Remito T3**

---

## Descripción general de la pantalla

La pantalla tiene un único formulario simple sin panel derecho.

---

## Formulario

| Campo / Botón | Descripción |
|---|---|
| **COMPROBANTE** | Selector del tipo de remito: **RM** (Remito) o **IRM** (Inter-Remito) |
| **Número** | Número del comprobante a eliminar (en formato estándar de factura) |
| **Eliminar** | Ejecuta la eliminación del remito |

---

## Paso a paso — Eliminar un remito T3

1. Seleccioná el tipo en **COMPROBANTE** (RM o IRM)
2. Ingresá el número del remito a eliminar
3. Hacé clic en **Eliminar**
4. Confirmá la operación cuando el sistema lo solicite

---

## Notas importantes

- Solo están disponibles los tipos **RM** (Remito Movistar T3) e **IRM** (Inter-Remito Movistar T3).
- Esta pantalla es de uso específico para la integración con Movistar T3. Para eliminar otros tipos de comprobantes, usá **Control Comprobantes** (3.32).
- La eliminación es permanente y no genera registros de reversión.
