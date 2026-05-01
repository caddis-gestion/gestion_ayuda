# 5.15 ARTÍCULOS REMITOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Remitos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Remitos** permite consultar el detalle de un remito de stock específico (ingreso o movimiento). Desde aquí podés:

- Seleccionar el tipo de comprobante y buscar por número
- Ver el listado completo de artículos incluidos en el remito
- Consultar cantidades, precios, puntos de venta y órdenes de compra asociadas

---

<img src="imagenes/pantalla_articulos_remitos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Remitos**

---

## Formulario de búsqueda

| Campo / Botón | Descripción |
|---|---|
| **COMPROBANTE** | Tipo de comprobante a consultar (Remito de ingreso / Remito de movimiento) |
| **REMITO #** | Número del remito a buscar |
| **Buscar** | Carga el detalle del remito en la grilla |

---

## Panel derecho — Detalle del remito

Muestra todos los artículos del remito seleccionado:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Unidades en el remito |
| Transito | Unidades aún en tránsito |
| PrecioU | Precio unitario (con IVA) |
| Total | Importe total |
| Punto de Venta | Depósito de destino |
| Articulo | Descripción |
| Tipo / Grupo / Marca / Variante | Clasificación del artículo |
| OC | Órdenes de compra relacionadas |

La grilla es de solo lectura (no permite modificaciones).

---

## Notas importantes

- Solo se muestran remitos no anulados.
- La columna **OC** muestra las órdenes de compra vinculadas al remito (si las hay).
- Esta pantalla es solo de consulta; para crear o modificar remitos usá las pantallas de **Artículos Ingresos** o **Artículos Movimientos**.
