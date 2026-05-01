# 3.48 DEFINIR IMPRESORA FISCAL
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Definir Impresora Fiscal

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Definir Impresora Fiscal** muestra el estado de la conexión entre el sistema y la impresora fiscal o controladora fiscal del punto de venta. Desde aquí podés:

- Verificar si la impresora fiscal está conectada al sistema
- Identificar qué modelo de impresora y qué usuario están asociados a la conexión
- Verificar el estado de la conexión con el botón **Verificar**

---

<img src="imagenes/pantalla_definir_impresora_fiscal.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Definir Impresora Fiscal**

---

## Descripción general de la pantalla

La pantalla muestra información de la conexión activa de la impresora fiscal. Todos los campos son de sólo lectura; se actualizan automáticamente al detectar la conexión.

---

## Información mostrada

| Campo | Descripción |
|---|---|
| **Impresora** | Posición fiscal asignada + Modelo de la impresora fiscal conectada |
| **Usuario** | Usuario del sistema asociado a la conexión activa |
| **ID Caddis** | Identificador único de la conexión entre Caddis y el servicio de facturación. El color del campo indica el estado: **verde** = conectado y activo; **rojo** = sin conexión activa. |

---

## Botón Verificar

Hacé clic en **Verificar** para comprobar el estado actual de la conexión con la impresora fiscal.

Si el campo **ID Caddis** se muestra en **rojo**, significa que no hay una conexión activa. En ese caso, verificá que:
- El servicio de facturación de Caddis esté ejecutándose en la computadora de caja
- La impresora fiscal esté encendida y conectada al equipo
- El equipo de caja esté encendido y en red

---

## Notas importantes

- Esta pantalla es informativa y de uso técnico. Normalmente no requiere intervención del operador habitual.
- La conexión se establece automáticamente al iniciar el servicio de facturación en la computadora de caja.
- Si la impresora está en rojo persistentemente, contactá al soporte técnico.
