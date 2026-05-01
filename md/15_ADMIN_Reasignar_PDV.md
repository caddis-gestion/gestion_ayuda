# 15.23 REASIGNAR ACCESOS PDV
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Accesos → Reasignar Accesos PDV

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Reasignar Accesos PDV** permite transferir en bloque todos los puntos de venta asignados a un responsable (supervisor, jefe de ventas o gerente) hacia otro responsable del mismo tipo. Es útil cuando una persona cambia de puesto o deja la empresa y sus PDVs deben pasar a cargo de otro. Desde aquí podés:

- Seleccionar un supervisor, jefe de ventas o gerente actual
- Ver todos los PDVs que tiene asignados
- Reasignarlos en bloque a otra persona del mismo rango

---

## ¿Cómo acceder?

**Menú → Administración → Accesos → Reasignar Accesos PDV**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de responsable a reasignar: **SUPERVISOR**, **JEFE VENTAS** o **GERENTE**. Al seleccionar el tipo, se actualizan los combos ACTUAL y REASIGNAR A. |
| **ACTUAL** | Persona que actualmente tiene asignados los PDVs a reasignar. |
| **REASIGNAR A** | Nueva persona que recibirá la asignación de los PDVs. |

---

## Grilla de PDVs

Muestra todos los puntos de venta asignados actualmente a la persona seleccionada en **ACTUAL**, con:

| Columna | Descripción |
|---|---|
| Puntos de Venta | Nombre del punto de venta o depósito. |
| Supervisor | Supervisor asignado al PDV. |
| Resp. Zonal | Jefe de ventas (Sub-Gerente) asignado al PDV. |
| Gerente | Gerente asignado al PDV. |

---

## Flujo típico — Reasignar PDVs de un supervisor saliente

1. Seleccionar **TIPO = SUPERVISOR**
2. En **ACTUAL**, seleccionar el supervisor saliente
3. La grilla muestra todos sus PDVs asignados
4. En **REASIGNAR A**, seleccionar el nuevo supervisor
5. Guardar — todos los PDVs pasan al nuevo responsable

---

## Notas importantes

- La reasignación es masiva: mueve **todos** los PDVs del responsable seleccionado al nuevo. No permite reasignar PDVs individuales (para eso usar la edición del PDV directamente).
- Se puede reasignar por cualquiera de los tres niveles jerárquicos: Supervisor, Jefe de Ventas o Gerente.
- Esta pantalla es útil especialmente en cambios de estructura organizacional (promociones, renuncias, reestructuraciones de zonas).
