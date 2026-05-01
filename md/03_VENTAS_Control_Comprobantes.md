# 3.32 CONTROL COMPROBANTES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Control Comprobantes

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Control Comprobantes** es una herramienta administrativa para gestionar comprobantes en situaciones especiales: liberar bloqueos de facturación, anular comprobantes (emitidos o no emitidos), modificar fechas y eliminar comprobantes. Desde aquí podés:

- Liberar el control de facturación de un PDV (desbloquear el sistema cuando quedó trabado)
- Anular comprobantes emitidos por tipo y número
- Anular rangos de comprobantes no emitidos (talonarios sin usar)
- Modificar la fecha de un comprobante ya emitido
- Eliminar comprobantes del sistema

> ⚠️ Esta pantalla es de uso administrativo. Algunas operaciones están limitadas según el perfil del usuario.

---

<img src="imagenes/pantalla_control_comprobantes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Control Comprobantes**

---

## Descripción general de la pantalla

La pantalla está organizada en secciones verticales, cada una con una función específica de control.

---

## Sección 1 — Liberar Control FC

Permite desbloquear el sistema de facturación de un punto de venta cuando quedó en estado de control activo (por ejemplo, si una factura quedó pendiente sin completarse).

| Campo / Botón | Descripción |
|---|---|
| **PDV** | Punto de venta a desbloquear |
| **Liberar** | Libera el control del PDV seleccionado |
| **Lib Todos** | Libera el control de todos los PDV de una vez |

---

## Sección 2 — Anulación de Comprobantes Emitidos

Permite anular un comprobante que ya fue emitido, identificándolo por tipo y número.

| Campo / Botón | Descripción |
|---|---|
| **Tipo** | Tipo de comprobante a anular (TK, B, A, C, NC, etc.) |
| **Número** | Número del comprobante |
| **Anular** | Ejecuta la anulación del comprobante |

> Los tipos disponibles excluyen comprobantes electrónicos ya autorizados por AFIP (EB, EA, EC, PA, NCEBx, etc.) que no pueden anularse desde aquí.

---

## Sección 3 — Anulación de Comprobantes No Emitidos

Permite anular un rango de números de comprobante que nunca fueron utilizados (talonarios en blanco).

| Campo / Botón | Descripción |
|---|---|
| **FECHA** | Fecha a asignar a la anulación |
| **TIPO** | Tipo de comprobante (TK, IA, B, A, MQ, R, RM, IRM, IV) |
| **DESDE FACTURA** | Número inicial del rango a anular |
| **HASTA FACTURA** | Número final del rango a anular |
| **Anular** | Registra la anulación del rango indicado |

---

## Sección 4 — Modificar Fecha

Permite cambiar la fecha de un comprobante ya emitido.

| Campo / Botón | Descripción |
|---|---|
| **Tipo** | Tipo de comprobante |
| **Número** | Número del comprobante |
| **FECHA** | Nueva fecha a asignar |
| **Modificar** | Aplica el cambio de fecha |

---

## Sección 5 — Eliminar Comprobantes

Permite eliminar un comprobante del sistema de forma definitiva.

| Campo / Botón | Descripción |
|---|---|
| **Tipo** | Tipo de comprobante a eliminar |
| **Número** | Número del comprobante |
| **Eliminar** | Elimina el comprobante |

> **Permisos:** El soporte técnico puede eliminar cualquier tipo de comprobante. Los usuarios regulares sólo pueden eliminar comprobantes de tipo TK, IA, NCIB y NCIA.

---

## Notas importantes

- Las operaciones de anulación y eliminación son **irreversibles** — verificar bien antes de ejecutar.
- La opción **Liberar** se usa cuando el sistema muestra un mensaje de "Control activo" al intentar facturar; resuelve bloqueos causados por facturas incompletas o cierres abruptos.
- La **anulación de no emitidos** se usa para dar de baja números de talonario que quedaron fuera de uso (por ejemplo, al cambiar de talonario o resolver saltos de numeración).
