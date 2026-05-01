# 5.24 ENTREGA EN MOSTRADOR
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Entrega Mostrador

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Entrega en Mostrador** permite gestionar la entrega presencial de órdenes de venta que fueron generadas para retirar en sucursal. Desde aquí podés:

- Consultar las órdenes de venta pendientes de entrega o ya entregadas
- Filtrar por PDV, cliente y período
- Confirmar la entrega de una orden al cliente (marcándola como entregada)
- Consultar el detalle del comprobante

---

<img src="imagenes/pantalla_entrega_mostrador.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Entrega Mostrador**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a consultar |
| **ESTADO** | PENDIENTE (órdenes sin entregar) o ENTREGADO (ya entregadas) |
| **CLIENTE** | Filtra por cliente específico |
| **DESDE** | Fecha de inicio del período |
| **HASTA** | Fecha de fin del período |

---

## Panel derecho — Grilla de órdenes

| Columna | Descripción |
|---|---|
| Fecha | Fecha de la orden de venta |
| Orden | Número de la orden de venta |
| Doc_Nro | Número de documento del cliente (CUIT) |
| Cliente | Nombre del cliente |
| Facturado | Indica si la orden ya fue facturada |

**Acciones:**
- **Aprobar:** Marca la orden como entregada en mostrador
- **Detalle:** Consulta el detalle del comprobante

---

## Notas importantes

- Esta pantalla gestiona exclusivamente las órdenes de venta directas (no las de tiendas online).
- Al aprobar una entrega, el sistema registra la fecha y hora de entrega en el comprobante.
- Para entregas a domicilio con transportistas, usá **Logística Externa**.
