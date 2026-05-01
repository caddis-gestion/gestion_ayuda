# 7.12 TV FACTURAR VENTAS
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Facturar Ventas

---

## ¿Para qué sirve esta pantalla?

**TV Facturar Ventas** permite emitir la factura correspondiente a una venta de tienda virtual de forma individual. Desde aquí podés:

- Buscar una venta por su ID en la tienda
- Seleccionar el punto de venta, vendedor, cliente y tipo de comprobante
- Ver descuentos y recargos que vienen de la venta (cupones, pasarela de pago, envío)
- Emitir factura A, B o X vinculada a la venta

---

<img src="imagenes/pantalla_tv_facturar_ventas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Facturar Ventas**

---

## Panel izquierdo: Formulario de facturación

### Selector de tienda

| Campo | Descripción |
|---|---|
| **TIENDA** | Selector de tienda virtual. Al cambiar, actualiza los datos. |

### Búsqueda de venta

| Campo | Descripción |
|---|---|
| **ORDEN ID** | ID de la venta en la tienda virtual. Ingresá el número y hacé clic en la **lupa** para cargar la venta. |
| **ORDEN NRO** | Número de orden interno *(solo TiendaNube)*. |

### Sección Factura A \| B \| X

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta (depósito) desde el que se factura. Se filtra según la cuenta de la tienda. |
| **FECHA** | Fecha del comprobante. |
| **CAJA-100** | Caja asignada automáticamente (en la mayoría de los casos: CAJA-100). |
| **VENDEDOR** | Vendedor asignado al comprobante. Se filtra por el PDV seleccionado. |
| **CLIENTE** | Cliente para la factura. Se puede buscar o ingresar manualmente. |
| **IVA** | Condición frente al IVA del cliente. |
| **FACTURA** | Tipo de comprobante (A, B, X, etc.) y número. El número puede dejarse en blanco para que lo asigne el sistema. |

### Sección Descuentos / Recargos

Valores informativos provenientes de la venta (solo lectura):

| Campo | Descripción |
|---|---|
| **CUPON: $** | Monto descontado por cupón de la tienda. |
| **F. PAGO: $** | Descuento por forma de pago (ej: descuento de pasarela). |
| **ENVIO: $** | Costo de envío que se suma al total. |

### Observaciones

Campo de texto libre para agregar observaciones al comprobante.

---

## Panel derecho: Detalle de artículos

Muestra los ítems de la venta con sus cantidades y precios. Este detalle se carga automáticamente al buscar la orden.

---

## Cómo facturar una venta

1. Seleccioná la **TIENDA** virtual.
2. En **ORDEN ID**, ingresá el ID de la venta y hacé clic en la **lupa**.
3. Se cargan los datos de la venta y el detalle de artículos en el panel derecho.
4. Seleccioná el **PDV**, **VENDEDOR** y **CLIENTE**.
5. Verificá la condición de **IVA** del cliente.
6. Seleccioná el **tipo de FACTURA** (A, B o X).
7. Revisá los descuentos/recargos informativos.
8. Agregá **OBSERVACIONES** si es necesario.
9. Hacé clic en **Emitir** (o el botón de guardar de la pantalla).

---

> 📖 Para facturar múltiples ventas de una sola vez consultá [**Facturación Masiva**](https://ayuda.caddis.com.ar/instructivos/07_TV_Facturacion_Masiva.pdf).
> 📖 Para ver el listado de ventas consultá [**Ventas de Tienda Virtual**](https://ayuda.caddis.com.ar/instructivos/07_TV_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
