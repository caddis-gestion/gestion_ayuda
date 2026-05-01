# 7.14 TV PREPARAR ITEMS
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Preparar Items

---

## ¿Para qué sirve esta pantalla?

**TV Preparar Items** muestra el listado de ítems de ventas de tiendas virtuales que están pendientes de preparación para envío. Desde aquí podés:

- Filtrar las ventas por zona de destino, artículo, fecha y tipo de envío
- Identificar qué artículos y cantidades hay que preparar por destino
- Marcar ítems como preparados para el armado del envío

---

<img src="imagenes/pantalla_tv_preparar_items.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Preparar Items**

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **TIENDA** | Selector de tienda virtual (banner). |
| **USUARIO** | Cuenta de la tienda. |
| **ZONA** | Código postal de destino. El desplegable muestra las zonas disponibles con la cantidad de ítems por zona entre paréntesis (ej: *Buenos Aires - Palermo (3)*). |
| **ARTICULO** | Filtrar por artículo específico. El desplegable muestra los artículos con stock pendiente y su cantidad. |
| **DESDE / HASTA** | Rango de fechas de las ventas. |
| **VER POR** | Ordenar por fecha de CREACION o MODIFICACION. |

### Sección FILTRO ENVIOS

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de logística del envío (Correo, Transporte, Colecta, etc.). |

---

## Panel derecho: Grilla de ítems a preparar

| Columna | Descripción |
|---|---|
| **Checkbox** | Seleccionar ítems para marcar como preparados. |
| **Nro. Item** | ID del ítem en la tienda virtual. |
| **Nro. Venta** | ID de la venta en la tienda virtual. |
| **SKU** | Código del artículo en Caddis. |
| **FechaCreacion** | Fecha de la venta. |
| **Usuario** | Cuenta de la tienda. |
| **Estado** | Estado de la venta. |
| **Titulo** | Nombre del artículo. |
| **Cant.** | Cantidad a preparar. |
| **Importe** | Precio del ítem. |
| **Tipo envio** | Tipo de logística. |
| **Costo envio** | Costo del envío. |
| **Destino** | Provincia y localidad de entrega. |
| **Tracking number** | Número de seguimiento (si ya tiene). |
| **Cliente / Documento / Telefono / Email** | Datos del comprador. |
| **Fc Tipo / Fc Nro** | Factura asociada (si tiene). |
| **Fc Subida** | SI si la factura fue subida a la tienda. |

### Acción por fila

| Acción | Descripción |
|---|---|
| **Modificar** | Abre el detalle de la venta para ver o editar información. |

---

## Uso típico

Esta pantalla se usa en el depósito para **planificar la preparación de paquetes**:

1. Filtrá por **ZONA** para agrupar los envíos por destino.
2. O filtrá por **ARTICULO** para ver cuántas unidades de un artículo específico hay que preparar en total.
3. Usá el filtro **TIPO** para separar los envíos por logística (correo vs. colecta, etc.).
4. Una vez preparados los ítems físicamente, procedé al armado de envíos en **TV Armar Envíos** (7.15).

---

> 📖 Para armar los envíos después de preparar consultá [**Armar Envíos**](https://ayuda.caddis.com.ar/instructivos/07_TV_Armar_Envios.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
