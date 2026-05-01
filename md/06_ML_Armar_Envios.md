# 6.13 ML ARMAR ENVÍOS
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Armar Envios

---

## ¿Para qué sirve esta pantalla?

**ML Armar Envíos** es la pantalla operativa donde el personal de depósito arma físicamente los paquetes de las ventas de MercadoLibre antes del despacho. Desde aquí podés:

- Registrar qué artículos (con su NSE/serie) se incluyen en cada paquete de envío
- Asociar los artículos a un remito de salida
- Consultar los envíos ya armados con sus comprobantes y ventas
- Ver el detalle de cada envío armado
- Imprimir la etiqueta del envío
- Eliminar artículos del paquete si fue un error

---

<img src="imagenes/pantalla_ml_armar_envios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Armar Envios**

---

## Descripción general de la pantalla

La pantalla tiene tres secciones principales:

- **Panel izquierdo superior:** Búsqueda de remito e ingreso de artículos al paquete.
- **Panel izquierdo inferior:** Grilla de envíos ya armados.
- **Panel derecho:** Detalle del comprobante seleccionado (arriba) y artículos preparados para envío (abajo).

---

## Panel izquierdo superior: Ingresar artículos

| Campo | Descripción |
|---|---|
| **REMITO** | Número del remito de la venta ML. Ingresá el número y presioná Enter para cargar los datos. |
| **ARTICULO** | Código o nombre del artículo a incluir en el paquete. |
| **NSE** | Número de serie del equipo (si aplica). |
| **CANTIDAD** | Cantidad de unidades a incluir. |
| **Ingresar** | Botón para agregar el artículo al paquete del envío. |

---

## Panel izquierdo inferior: Envíos armados

Muestra los envíos que ya fueron armados (paquetes preparados).

| Columna | Descripción |
|---|---|
| **Envio** | ID del envío en ML |
| **Comprobante** | Número del remito asociado |
| **Venta** | ID de la venta en ML |
| **Items** | Cantidad de artículos en el paquete |
| **Fecha** | Fecha en que se armó el paquete |
| **Cliente** | Nombre del comprador |
| **Imprimir** | Botón para imprimir el comprobante del paquete |
| **Etiqueta** | Botón para imprimir la etiqueta de envío ML |

---

## Panel derecho superior: Detalle del comprobante

Muestra los artículos del remito seleccionado en el panel de envíos armados.

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta |
| **Item** | ID de publicación ML |
| **Cantidad** | Unidades en el remito |
| **Codigo** | Código del artículo en Caddis |
| **Producto** | Nombre del artículo |
| **Modificar** | Botón para editar datos del ítem |

---

## Panel derecho inferior: Ítems preparados para envío

Muestra los artículos que ya fueron ingresados al paquete actual (en preparación).

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta |
| **Item** | ID de publicación ML |
| **Cantidad** | Unidades preparadas |
| **Codigo** | Código del artículo |
| **Producto** | Nombre del artículo |
| **Borrar** | Botón para eliminar el artículo del paquete (si fue un error) |

---

## Cómo armar un paquete paso a paso

1. Ingresá el número de **REMITO** de la venta y presioná Enter.
2. El sistema carga los datos de la venta en pantalla.
3. Para cada artículo a empaquetar:
   - Ingresá el código en **ARTICULO** (o escaneá el código de barras).
   - Si es un equipo con NSE, ingresá el número de serie en **NSE**.
   - Ingresá la **CANTIDAD**.
   - Hacé click en **Ingresar**.
4. El artículo aparece en el panel **Ítems preparados para envío**.
5. Una vez armado el paquete completo, el envío aparece en **Envíos armados**.
6. Desde **Envíos armados**, podés imprimir la etiqueta de envío con el botón **Etiqueta**.

---

> 📖 Para imprimir etiquetas de envío sin armar el paquete consultá [**Etiquetas de Envío ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Etiquetas.pdf).
> 📖 Para ver el estado general de las ventas a preparar consultá [**Preparar Ítems para Envío**](https://ayuda.caddis.com.ar/instructivos/06_ML_Preparar_Items.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
