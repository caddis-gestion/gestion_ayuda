# 6.04 ML PREPARAR ÍTEMS
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Preparar Items

---

## ¿Para qué sirve esta pantalla?

**ML Preparar Ítems** es el panel operativo del depósito para preparar los pedidos de MercadoLibre antes del despacho. Desde aquí podés:

- Ver todas las ventas pendientes de preparación con sus datos de envío y comprador
- Filtrar por usuario ML, depósito, zona, artículo, rango de fechas y tipo de envío
- Usar accesos rápidos para ver ventas según su etapa logística (para preparar, para despachar)
- Consultar mensajes del comprador desde la grilla
- Modificar datos de la venta o envío
- Ver totales de ventas seleccionadas

> ℹ️ Esta pantalla está orientada al personal de depósito que arma y despacha los pedidos. Para imprimir etiquetas usá **ML Etiquetas** (6.14). Para armar el paquete con los artículos físicos usá **ML Armar Envíos** (6.13).

---

<img src="imagenes/pantalla_ml_preparar_items.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Preparar Items**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda, filtro de envíos y accesos rápidos por etapa logística.
- **Panel derecho (grilla):** Listado de ventas con todos los datos necesarios para preparar y despachar cada pedido. Las primeras 3 columnas son fijas al hacer scroll horizontal.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre a consultar. Obligatorio para ver resultados. |
| **DEPOSITO** | Filtra ventas asignadas a un depósito o punto de venta específico. |
| **ZONA** | Código postal del comprador. El dropdown se llena con los CPs de las ventas pendientes. Útil para preparar por zona de entrega. |
| **ARTICULO** | Filtra ventas que contengan un artículo específico. El dropdown muestra los artículos de las ventas pendientes. |
| **DESDE** | Fecha de inicio del rango a consultar. |
| **HASTA** | Fecha de fin del rango. |
| **VER POR** | `CREACION` — filtra por fecha de creación de la venta. `MODIFICACION` — filtra por última actualización. |

---

## Filtro de envíos

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de logística (`cross_docking` = colecta, `self_service` = Flex, `fulfillment` = FULL). |
| **ESTADO** | Estado del envío en ML. |
| **SUBESTADO** | Subestado del envío con mayor detalle. |

---

## Accesos rápidos por etapa logística

### PARA PREPARAR

| Botón | Filtros aplicados |
|---|---|
| **Para la colecta** | Logística: `cross_docking` · Subestado: `ready_to_print` |
| **Mercado Envíos Flex** | Logística: `self_service` · Subestado: `ready_to_print` |
| **Acordar con el comprador** | Logística: `not_specified` · Estado envío: `to_be_agreed` |

### PARA DESPACHAR

| Botón | Filtros aplicados |
|---|---|
| **Mercado Envíos Flex** | Logística: `self_service` · Subestado: `printed` |
| **Para la colecta** | Logística: `cross_docking` · Subestado: `ready_for_pickup` |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta en ML |
| **Fecha** | Fecha de creación de la venta |
| **Modificado** | Fecha de última actualización |
| **Cantidad** | Unidades vendidas |
| **Importe** | Monto de la venta |
| **Estado** | Estado de la orden (ej: `paid`) |
| **Shipping Tipo** | Tipo de logística del envío |
| **Shipping Estado** | Estado del envío |
| **Shipping Subestado** | Subestado detallado del envío |
| **Shipping Tracking** | ID de seguimiento |
| **Pack** | ID de carrito (pedidos con varios ítems) |
| **Item** | ID de publicación ML |
| **SKU** | Código del artículo en Caddis |
| **Titulo** | Título de la publicación |
| **Cliente** | Nombre del comprador |
| **Documento** | Tipo y número de documento del comprador |
| **Domicilio** | Dirección de entrega |
| **Cpostal** | Código postal de entrega |
| **Localidad** | Localidad de entrega |
| **Telefono** | Teléfono del comprador |
| **Deposito** | Depósito asignado a la venta |
| **Factura Tipo** | Tipo de comprobante emitido |
| **Factura Numero** | Número del comprobante |
| **Fc Subida** | `SI` si la factura fue subida a ML |
| **Error** | Último mensaje de error registrado |

---

## Acciones desde la grilla

| Acción | Descripción |
|---|---|
| **Mensaje** | Abre la ventana de mensajes con el comprador de esa venta |
| **Modificar** | Permite editar datos de la venta (ej: SKU, datos de envío) |
| **Totales** | Muestra el total acumulado de las filas seleccionadas con el checkbox |

---

## Preguntas frecuentes

**¿Qué diferencia hay entre esta pantalla y ML Ventas?**
ML Preparar Ítems está orientada al trabajo operativo del depósito: muestra las ventas con todos los datos necesarios para armar y despachar. ML Ventas es más completa y permite además actualizar ventas desde la API, emitir remitos y subir facturas.

**¿Puedo filtrar por comprador?**
No directamente. Podés buscar por ID de venta en ML Ventas o filtrar por zona (código postal) para agrupar envíos a una misma área.

---

> 📖 Para imprimir etiquetas de envío consultá [**Etiquetas de Envío ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Etiquetas.pdf).
> 📖 Para armar los paquetes físicos consultá [**Armar Envíos ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Armar_Envios.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
