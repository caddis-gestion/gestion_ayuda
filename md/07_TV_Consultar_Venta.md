# 7.10 TV CONSULTAR VENTA
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Ventana emergente accesible desde TV Ventas

---

## ¿Para qué sirve esta pantalla?

**TV Consultar Venta** es una ventana de detalle de una venta de tienda virtual. Desde aquí podés:

- Ver todos los datos de la venta, incluyendo estado y comprobante asociado
- Asociar o subir facturas a la venta
- Ver y editar los datos de facturación del comprador
- Ver los datos de envío completos
- Modificar el SKU de un ítem si no fue identificado correctamente
- Ver el control interno del paquete (armado, entrega, recepción)
- Ver los datos de logística externa
- Ver el reclamo asociado (si hubiera)

---

<img src="imagenes/pantalla_tv_ventas_consulta.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Esta pantalla es una ventana emergente. Se accede desde:
**TV Ventas → seleccionar una venta → botón Modificar**

---

## Sección: Datos de la venta virtual

| Campo | Descripción |
|---|---|
| **VENTA** | ID de la venta en la tienda virtual (solo lectura). |
| **PACK** | ID del pack de ventas (si aplica, solo lectura). |
| **ESTADO** | Estado de la venta. Si está cancelada, se muestra en rojo. |
| **FECHA / HORA** | Fecha y hora de la venta. |
| **CLIENTE** | Nombre del comprador (solo lectura). |

### Comprobante asociado

| Campo | Descripción |
|---|---|
| **COMPROBANTE ASOCIADO** | Tipo y número de factura asociada a esta venta. Botón lupa para verla. |
| **ASOCIAR FC** | Permite asociar manualmente una factura existente: seleccioná el tipo y escribí el número, luego hacé clic en el botón **+**. |
| **FC SUBIDA** | Indica si la factura fue subida a la tienda virtual (SI/NO). Si NO fue subida y es electrónica, aparece el botón para subirla. |

---

## Sección: Ítems de la venta

Tabla con los artículos de la venta:

| Columna | Descripción |
|---|---|
| **Titulo** | Nombre del artículo en la tienda virtual. |
| **Cant.** | Cantidad vendida. |
| **Precio** | Precio unitario. |
| **SKU** | Código del artículo en Caddis. Si no fue identificado, el campo tiene fondo rojo. Se puede editar: botón **modificar** para guardar el SKU, botón **buscar** para buscar el artículo. |

---

## Sección: Datos de facturación

Datos fiscales del comprador para la factura. Son editables:

| Campo | Descripción |
|---|---|
| **DOC.TIPO** | DNI o CUIT. |
| **DOC.NRO** | Número de documento. |
| **CLIENTE** | Nombre del comprador para la factura. |
| **CALLE / NUMERO / PISO** | Domicilio de facturación. |
| **C.POSTAL / LOCALIDAD / PROVINCIA** | Domicilio de facturación. |
| **IVA** | Condición frente al IVA del comprador. |

---

## Sección: Datos del envío

| Campo | Descripción |
|---|---|
| **TRACKING** | ID de seguimiento del envío (solo lectura). |
| **ESTADO** | Estado del envío en la tienda (solo lectura). |
| **LOGISTICA** | Tipo de logística del envío (solo lectura). |
| **ENTREGA** | Método de entrega (solo lectura). |
| **CALLE / NUMERO / PISO / CP / LOCALIDAD / PROVINCIA** | Domicilio de entrega (editable). |
| **TELEFONO** | Teléfono del comprador + botón para ingresar datos de entrega. |

---

## Sección: Control interno del paquete

| Campo | Descripción |
|---|---|
| **ENVIO ARMADO** | Número de envío generado en Caddis (SI/NO). |
| **PAQUETE** | Número de empaque. |
| **ENTREGA** | Número de colecta (entrega al transporte). |
| **RECEPCION** | Número de recepción (si se trata de devolución). |

---

## Sección: Logística externa

| Campo | Descripción |
|---|---|
| **ENVIO** | Número de envío externo. |
| **FECHA** | Fecha del envío externo. |
| **TRACKING** | Número de seguimiento externo. |

---

## Sección: Reclamos (si aplica)

Se muestra solo si la venta tiene un reclamo abierto:

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de reclamo. |
| **ETAPA** | Etapa actual del reclamo. |
| **ESTADO** | Estado del reclamo. |
| **RESOLUCION** | Motivo de resolución. |
| **FECHA** | Fecha de la última resolución. |

---

> 📖 Para ver el listado de ventas consultá [**Ventas de Tienda Virtual**](https://ayuda.caddis.com.ar/instructivos/07_TV_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
