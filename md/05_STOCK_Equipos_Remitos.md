# 5.42 EQUIPOS — REMITOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Remitos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Remitos** permite consultar el detalle de un remito de equipos (ingreso o movimiento) por número, listando todos los NSE incluidos y sus datos asociados. Desde aquí podés:

- Buscar un remito por tipo y número
- Ver todos los equipos incluidos en ese remito con sus datos de activación y proveedor
- Imprimir etiquetas o el remito en formato preimpreso

---

<img src="imagenes/pantalla_equipos_remitos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Remitos**

---

## Formulario

| Campo | Descripción |
|---|---|
| **CMPBTE** | Tipo de comprobante (Ingreso de equipos, Movimiento de equipos, etc.) |
| **REMITO#** | Número del remito a consultar (con botón **Buscar**) |

**Acciones:**
- **Etiquetas:** Imprime etiquetas con código de barras de los artículos del remito
- **Remito Preimpreso:** Imprime el detalle en formato preimpreso

---

## Panel derecho — Grilla de equipos del remito

| Columna | Descripción |
|---|---|
| NSE | Número de serie del equipo |
| SAP Id | ID SAP del equipo (solo en integraciones Movistar) |
| Compra Tipo | Tipo de contrato/compra del equipo |
| [campos del equipo] | Marca, modelo y datos adicionales |
| POS | Punto de venta destino del movimiento |
| Pedido | Número de pedido del proveedor |
| Remito Proveedor | Número de remito del proveedor |
| Factura Proveedor | Número de factura del proveedor |
| Vence | Fecha de vencimiento del equipo |
| Linea | Línea telefónica vinculada (si está activado) |
| Activado | Fecha de activación |
| Almacen | Almacén actual |
| Observaciones | Observaciones del equipo |

---

## Notas importantes

- Los tipos de comprobante disponibles dependen del perfil de la empresa (prestataria vs. gestión).
- El remito solo muestra equipos que el usuario actual tiene permiso de ver (según PDV autorizado).
