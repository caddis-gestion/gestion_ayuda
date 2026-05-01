# 5.01 ARMAR ENVÍOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Armar Envíos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Armar Envíos** permite preparar los paquetes que se van a despachar a los clientes. Se asocia cada artículo (o NSE) a un comprobante de venta y se definen los items que van en cada envío. Desde aquí podés:

- Buscar el comprobante de venta a despachar
- Ingresar artículos o números de serie (NSE) al envío
- Seleccionar el tipo de entrega (transporte)
- Consultar los envíos ya armados
- Imprimir el remito de venta o la etiqueta de envío

---

<img src="imagenes/pantalla_armar_envios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Armar Envíos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de preparación, y un panel derecho dividido en dos: arriba el detalle del comprobante y abajo los items ya preparados para el envío.

---

## Panel izquierdo

| Campo / Botón | Descripción |
|---|---|
| **COMPROBANTE** | Número del remito o factura a despachar (solo lectura) |
| **Buscar** | Abre el buscador para seleccionar un comprobante |
| **Artículo / NSE** | Código del artículo o número de serie a agregar al envío |
| **Cantidad** | Cantidad a incluir |
| **Ingresar** | Agrega el ítem al envío actual (también con Enter) |

### Sección TIPO DE ENTREGA

Si hay transportes configurados, aparecen botones por cada opción de entrega disponible (ej. Mercado Envíos, transporte propio, mostrador). Seleccioná el tipo de entrega antes de confirmar.

### Sección ENVIOS ARMADOS

Grilla con los últimos 100 envíos armados:

| Columna | Descripción |
|---|---|
| Envío | Número de envío |
| Comprobante | Tipo y número del comprobante asociado |
| Items | Cantidad de ítems en el envío |
| Fecha | Fecha de creación |
| Cliente | Nombre del cliente |

**Acciones:**
- **Imprimir** remito de venta
- **Etiqueta** para envío de Mercado Libre

---

## Panel derecho — Detalle del comprobante

Muestra los artículos que contiene el comprobante seleccionado (Comprobante, Cantidad, Código, Producto). Permite modificar.

## Panel derecho inferior — Ítems preparados para envío

Muestra los artículos ya asignados al envío actual (Remito, Cantidad, Código, Producto). Permite borrar ítems del envío.

---

## Notas importantes

- Cada envío queda registrado con un número de envío único.
- Si el sistema tiene integración con Mercado Libre, el botón de etiqueta genera la etiqueta de MercadoEnvíos.
- El comprobante debe existir previamente (factura o remito de venta ya emitido).
