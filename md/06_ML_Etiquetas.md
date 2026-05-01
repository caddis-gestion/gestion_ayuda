# 6.14 ML ETIQUETAS DE ENVÍO
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Etiquetas

---

## ¿Para qué sirve esta pantalla?

**ML Etiquetas** permite consultar y imprimir las etiquetas de envío de MercadoLibre para un conjunto de ventas en un período determinado. Desde aquí podés:

- Filtrar ventas por usuario ML, depósito, rango de fechas y estado de envío
- Ver el listado de ventas con sus datos de tracking, cliente y estado
- Imprimir la etiqueta de envío de una o varias ventas seleccionadas

> ℹ️ Imprimir la etiqueta desde esta pantalla **modifica el estado del envío en ML**. Solo imprimí cuando el paquete esté listo para ser despachado.

---

<img src="imagenes/pantalla_ml_etiquetas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Etiquetas**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda.
- **Panel derecho (grilla):** Listado de ventas con datos de envío. Las primeras 3 columnas son fijas.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio para ver resultados. |
| **DEPOSITO** | Filtra ventas asignadas a un depósito específico. |
| **DESDE** | Fecha de inicio del rango de ventas. |
| **HASTA** | Fecha de fin del rango. |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta en ML |
| **Fecha** | Fecha de la venta |
| **Item** | ID de publicación ML |
| **SKU** | Código del artículo en Caddis |
| **Cantidad** | Unidades vendidas |
| **Importe** | Monto de la venta |
| **Estado** | Estado de la orden |
| **Shipping Tipo** | Tipo de logística del envío |
| **Shipping Estado** | Estado del envío |
| **Shipping Subestado** | Subestado detallado del envío |
| **Shipping Tracking** | ID de seguimiento del envío |
| **Titulo** | Título de la publicación |
| **Cliente** | Nombre del comprador |

---

## Acciones desde la grilla

| Acción | Descripción |
|---|---|
| **Etiqueta** | Imprime la etiqueta de envío de ML para la venta seleccionada |
| **Checkbox** | Selección de ventas para imprimir etiquetas en lote |

### Cómo imprimir una etiqueta

1. Seleccioná el **USUARIO** ML y el rango de fechas.
2. Hacé click en **Buscar** para cargar las ventas.
3. Seleccioná la fila de la venta cuya etiqueta querés imprimir.
4. Hacé click en el botón **Etiqueta**.
5. Confirmá el aviso *"¿Desea imprimir la etiqueta? Esto modifica el estado en Mercado Libre..."*.
6. Se abre el PDF de la etiqueta para imprimir.

### Imprimir etiquetas en lote

1. Marcá el **checkbox** de todas las ventas a imprimir.
2. Hacé click en el botón **Etiqueta** de la barra de la grilla.
3. Confirmá el aviso.
4. Las etiquetas se generan en un único PDF para imprimir.

> ⚠️ Al imprimir la etiqueta el sistema notifica a ML que el paquete está listo para ser retirado por el correo. No imprimas la etiqueta si el paquete no está físicamente armado.

---

> 📖 Para armar el paquete físico antes de imprimir la etiqueta consultá [**Armar Envíos ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Armar_Envios.pdf).
> 📖 Para ver el estado general de preparación y despacho consultá [**Preparar Ítems para Envío**](https://ayuda.caddis.com.ar/instructivos/06_ML_Preparar_Items.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
