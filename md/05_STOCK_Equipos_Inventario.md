# 5.40 EQUIPOS — INVENTARIO
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Inventario

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Inventario** muestra el inventario completo de equipos (con NSE), incluyendo información de estado, proveedor, remito de ingreso, almacén, costos y facturación. Es una vista de consulta de solo lectura. Desde aquí podés:

- Ver el inventario de equipos del usuario actual
- Consultar el estado, almacén, costo y datos de compra de cada equipo
- Identificar equipos facturados y no facturados

---

<img src="imagenes/pantalla_equipos_inventario.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Inventario**

---

## Grilla de inventario

La pantalla muestra directamente la grilla de equipos sin filtros previos (el filtro se aplica según el usuario):

| Columna | Descripción |
|---|---|
| NSE | Número de serie del equipo (hexadecimal) |
| Equipo Codigo | Código del artículo en el sistema |
| Equipo Tipo | Tipo de artículo |
| Equipo Marca | Marca del equipo |
| Equipo Modelo | Modelo/descripción del equipo |
| Compra Tipo | Tipo de contrato o compra |
| Fecha Ingreso | Fecha en que ingresó al stock |
| Remito | Número de remito de ingreso interno |
| Ultima Fecha | Fecha del último movimiento |
| Factura Proveedor | Número de factura del proveedor |
| Remito Proveedor | Número de remito del proveedor |
| Proveedor | Nombre del proveedor |
| Almacen | Almacén donde se encuentra |
| Documento Asociado | Documento de operadora (solo en integraciones Movistar) |
| Deposito Origen | Depósito de origen del último movimiento |
| Deposito Destino | Depósito de destino del último movimiento |
| Dias | Días desde el ingreso |
| Estado | Estado actual del equipo |
| Facturado | Indica si fue facturado (SI o vacío) |
| Importe Consignado | Precio de consignación |
| Costo | Costo del equipo (el mayor entre costo de reposición y costo de compra) |

---

## Notas importantes

- Esta pantalla muestra el inventario de equipos asociados al usuario que inició sesión.
- Es una pantalla de consulta; para registrar movimientos usá **Equipos Movimientos** o **Equipos Ingresos**.
- Los costos se toman del mayor valor entre Costo Reposición y Costo Compra según la fecha de actualización.
