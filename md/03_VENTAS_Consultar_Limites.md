# 3.44 CONSULTAR LÍMITES DE CRÉDITOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Consultar Límites de Creditos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Consultar Límites de Créditos** permite ver el estado de los límites de crédito asignados a clientes y puntos de venta, incluyendo la deuda actual y el saldo disponible. Desde aquí podés:

- Buscar un cliente o PDV por nombre, CUIT o código
- Filtrar por zona, tipo de PDV o PDV específico
- Filtrar por cliente mayorista
- Ver el límite asignado, la deuda actual y el saldo disponible

> Esta pantalla es sólo de consulta — no permite modificar límites.

---

<img src="imagenes/pantalla_consultar_limites.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Consultar Límites de Creditos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con los filtros de búsqueda y un panel derecho con la grilla de resultados.

---

## Panel izquierdo — Filtros

### Filtro por búsqueda libre

| Campo / Botón | Descripción |
|---|---|
| **CLIENTE/POS/CUIT** | Campo de texto libre para buscar por nombre de cliente, nombre de PDV o CUIT |
| **Buscar** | Ejecuta la búsqueda |

### Filtro por depósito

| Campo | Descripción |
|---|---|
| **ZONA** | Filtra por zona geográfica |
| **TIPO PDV** | Filtra por tipo de punto de venta |
| **PDV** | Filtra por un punto de venta específico |

### Filtro por cliente

| Campo | Descripción |
|---|---|
| **CLIENTE** | Selecciona un cliente mayorista específico |

---

## Panel derecho — Grilla de límites

Muestra los registros de límites de crédito que coinciden con los filtros aplicados:

| Columna | Descripción |
|---|---|
| CUIT\|PDV | CUIT asociado al límite (puede ser de un PDV o de un cliente) |
| Limite | Límite de crédito asignado en pesos |
| **Saldo** | Saldo disponible (Límite menos deuda total). Puede ser negativo si se superó el límite. |
| PDV | Nombre del punto de venta asociado al CUIT (si aplica) |
| Deuda PDV | Deuda del PDV (facturas pendientes de stock + cobranza pendiente) |
| Cliente | Nombre del cliente asociado al CUIT (si aplica) |
| Deuda Cliente | Deuda del cliente en cuenta corriente |

---

## Notas importantes

- El **Saldo** se calcula como: Límite − (Deuda PDV + Deuda Cliente).
- Un saldo negativo indica que el límite de crédito fue superado.
- Para **configurar o modificar** los límites de crédito, usá la pantalla **Límites de Créditos** (acceso desde el menú según permisos).
- Solo aparecen en la grilla los registros con límite mayor a 0.
