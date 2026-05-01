# 5.XX PEDIDOS DE MERCADERÍA — ESTADO
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Pedidos Mercadería Estado

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Pedidos de Mercadería Estado** permite consultar y gestionar el estado de los pedidos de mercadería (**PP** = Presupuesto / **PM** = Pedido de Mercadería) por rango de fechas. Desde aquí podés:

- Filtrar pedidos por fecha, estado y punto de venta
- Aprobar o rechazar pedidos pendientes
- Ver el estado de cada artículo dentro del pedido
- Imprimir comprobantes de pedido

---

<img src="imagenes/pantalla_pedidos_mercaderia_estado.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Pedidos Mercadería Estado**

---

## Formulario

| Campo | Descripción |
|---|---|
| **DESDE** | Fecha de inicio del rango de consulta (por defecto: un mes atrás) |
| **HASTA** | Fecha de fin del rango de consulta (por defecto: hoy) |
| **ESTADO** | Estado de los pedidos a mostrar |
| **PDV** | Punto de venta del pedido. Seleccionando "TODOS" muestra todos los PDV. |

---

## Panel derecho — Grilla de pedidos

Muestra los pedidos del período y estado seleccionados:

| Columna | Descripción |
|---|---|
| Tipo | Tipo de comprobante del pedido |
| Factura Nro | Número del pedido |
| Fecha | Fecha del pedido |
| Solicitante | Cliente o usuario que generó el pedido |
| Movimiento | Órdenes de compra relacionadas con el pedido |
| PDV | Punto de venta del pedido |
| Usuario | Usuario que registró el pedido |

**Acciones disponibles** (varían según el estado seleccionado):
- **Aprobar:** Aprueba el pedido (disponible en estado Rechazado, Anulado o Pendiente)
- **Borrar:** Elimina el pedido (disponible en estado Aprobado o Pendiente)
- **Detalle:** Muestra el estado de cada artículo dentro del pedido
- **Imprimir:** Imprime el comprobante del pedido

---

## Notas importantes

- Los pedidos con tipo **PM** (Pedido de Mercadería) muestran el usuario solicitante en lugar del nombre del cliente.
- La columna **Movimiento** indica las órdenes de compra generadas a partir del pedido y sus facturas asociadas.
- Las acciones disponibles cambian según el estado filtrado: no todos los estados permiten las mismas operaciones.
