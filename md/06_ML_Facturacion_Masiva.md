# 6.12 ML FACTURACIÓN MASIVA
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Facturacion Masiva

---

## ¿Para qué sirve esta pantalla?

**ML Facturación Masiva** permite emitir comprobantes fiscales (facturas) para un lote de ventas de MercadoLibre en una sola operación. Desde aquí podés:

- Seleccionar un conjunto de ventas de ML que ya tienen remito y aún no tienen factura
- Filtrar por usuario ML, depósito, vendedor, rango de fechas, logística y tipo de factura
- Emitir facturas para todas las ventas seleccionadas con un solo click
- Ver el resultado de la facturación masiva con los errores por fila
- Imprimir los comprobantes emitidos
- Consultar el detalle de cada venta antes de facturar

---

<img src="imagenes/pantalla_ml_facturacion_masiva.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Facturacion Masiva**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda y parámetros de facturación.
- **Panel derecho (grilla):** Listado de ventas con todos sus datos, resultados de facturación y errores. Las primeras 3 columnas son fijas.

---

## Panel izquierdo: Filtros y parámetros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio. |
| **DEPOSITO** | Depósito desde donde se emiten las facturas. |
| **VENDEDOR** | Vendedor asignado a las facturas. |
| **DESDE** | Fecha de inicio del rango de ventas a facturar. |
| **HASTA** | Fecha de fin del rango. |
| **LOGISTICA** | Tipo de logística para filtrar (ej: solo ventas FULL, solo colecta). |
| **TIPO FC** | Tipo de comprobante a emitir. Aparece solo si el PDV lo requiere (ej: `EA`, `EB`, `EC`, `A`, `B`). |
| **FECHA** | Fecha del comprobante a generar. Por defecto la fecha del día. |
| **CAJA** | Número de caja (fijo en CAJA-100 para ventas ML, solo lectura). |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta en ML |
| **Fecha** | Fecha de creación de la venta |
| **Pack** | ID de carrito (pedido combinado) |
| **Item** | ID de publicación ML |
| **SKU** | Código del artículo en Caddis |
| **Cantidad** | Unidades vendidas |
| **Importe** | Monto de la venta |
| **Estado** | Estado de la orden |
| **Shipping Tipo** | Tipo de logística |
| **Shipping Estado** | Estado del envío |
| **Shipping Subestado** | Subestado del envío |
| **Shipping Tracking** | ID de seguimiento del envío |
| **Titulo** | Título de la publicación |
| **Cliente** | Nombre del comprador |
| **Documento** | Tipo y número de documento del comprador |
| **Domicilio** | Dirección de entrega |
| **CPostal** | Código postal de entrega |
| **Localidad** | Localidad de entrega |
| **Telefono** | Teléfono del comprador |
| **Deposito** | Depósito asignado |
| **Factura Tipo** | Tipo de comprobante emitido |
| **Factura Numero** | Número del comprobante |
| **Envio_Id** | ID del envío en ML |
| **Error** | Mensaje de error si la facturación falló para esa venta |

---

## Cómo facturar ventas masivamente

1. Seleccioná el **USUARIO** ML.
2. Completá **DEPOSITO**, **VENDEDOR**, **DESDE** y **HASTA**.
3. Elegí el **TIPO FC** de comprobante a emitir.
4. Verificá la **FECHA** del comprobante.
5. Hacé click en **Buscar** para cargar las ventas que cumplen los filtros.
6. Revisá la grilla para confirmar que las ventas son las correctas.
7. Marcá las ventas a facturar con el checkbox (o seleccioná todas).
8. Hacé click en **Facturar** y confirmá el aviso.
9. El sistema emite los comprobantes y muestra los errores en la columna **Error** para las ventas que no pudieron facturarse.

---

## Acciones desde la grilla

| Acción | Descripción |
|---|---|
| **Detalle** | Abre el detalle completo de la venta seleccionada |
| **Imprimir** | Imprime el comprobante de la venta seleccionada |
| **Checkbox** | Selección individual de ventas para incluir en la facturación masiva |

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| Venta con error en columna Error | El cliente no tiene CUIT/DNI cargado | Completar los datos del cliente en ML Ventas → Detalle |
| Venta con error de tipo de factura | El cliente es RI y se intentó emitir EB | Cambiar el TIPO FC a EA y refacturar esa venta individualmente |
| No aparecen ventas | Las ventas no tienen remito emitido | Ejecutar "Emitir Remitos" desde ML Ventas primero |
| Error de AFIP | Servicio de facturación electrónica no disponible | Reintentar más tarde; verificar estado de AFIP |

---

## Preguntas frecuentes

**¿Puedo facturar ventas que ya tienen factura?**
No. La facturación masiva solo procesa ventas sin comprobante emitido. Si una venta ya fue facturada, se omite automáticamente.

**¿Qué pasa si una venta falla en la facturación masiva?**
El proceso continúa con las demás ventas. La venta que falló muestra el motivo en la columna **Error** y puede reintentarse de forma individual desde **ML Facturación** (6.11).

---

> 📖 Para facturar una venta individual consultá [**Facturación desde Ventas ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion.pdf).
> 📖 Para subir las facturas emitidas a ML consultá la sección **Aprobar** en [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
