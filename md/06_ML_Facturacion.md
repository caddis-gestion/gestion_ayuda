# 6.11 ML FACTURACIÓN DESDE VENTAS
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Accesible desde ML Ventas → acción facturar venta individual

---

## ¿Para qué sirve esta pantalla?

**ML Facturación** permite emitir un comprobante fiscal (Factura A o B) para una venta individual de MercadoLibre. Desde aquí podés:

- Emitir factura para una venta de ML que ya tiene remito
- Seleccionar el punto de venta (PDV), vendedor, fecha y tipo de factura
- Completar o verificar los datos del cliente (nombre, documento, IVA)
- Agregar observaciones al comprobante
- Registrar el pago si hay diferencia entre el total de la venta y el pago ya registrado

> ℹ️ Esta pantalla es para facturación **individual** de una venta. Para facturar varias ventas a la vez usá **ML Facturación Masiva** (6.12).

---

<img src="imagenes/pantalla_ml_facturacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Esta pantalla se accede desde:
**ML Ventas → seleccionar una venta → botón Facturar**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Datos de la venta ML y del comprobante a emitir.
- **Panel derecho:** Detalle de los artículos a facturar.

---

## Panel izquierdo: Datos del comprobante

### Venta ML

| Campo | Descripción |
|---|---|
| **VENTA ML** | ID de la venta en MercadoLibre (solo lectura). Tiene botón **Buscar Venta** para cargar los datos y botón **Mensajes** para ver el chat con el comprador. |

### Factura A/B

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta desde donde se emite la factura. Seleccioná el PDV correspondiente. |
| **VENDEDOR** | Vendedor asignado a la factura. Se filtra por el depósito del PDV seleccionado. |
| **FECHA** | Fecha del comprobante. Por defecto la fecha del día. |
| **CAJA** | Número de caja (fijo en CAJA-100 para ventas ML). |
| **CLIENTE** | Cliente de la venta. Se autocompleta desde los datos del comprador en ML. Tiene botón para buscar o crear cliente. |
| **DOC #** | Número de documento del cliente (DNI o CUIT). Solo lectura — se completa desde los datos de ML. |
| **IVA** | Condición frente al IVA del cliente (Consumidor Final, Responsable Inscripto, etc.). |
| **FACTURA** | Tipo de comprobante (ej: EA, EB, EC, A, B, M, X) y número. El número se asigna automáticamente según el PDV. |
| **OBSERVACIONES** | Texto libre para agregar notas al comprobante. |

### Botón Pagos (condicional)

Si el total de la venta difiere del pago ya registrado, aparece el botón **Ingresar Pagos** para registrar la diferencia.

---

## Panel derecho: Detalle de artículos

Muestra el detalle de los artículos incluidos en la venta ML (cargado desde el remito correspondiente):

| Columna | Descripción |
|---|---|
| **Artículo** | Código y descripción del artículo |
| **Cantidad** | Unidades |
| **Precio unitario** | Precio de venta |
| **Subtotal** | Subtotal de la línea |

---

## Cómo facturar una venta de ML

1. Accedé a **ML Ventas** y seleccioná la venta a facturar.
2. Hacé click en **Facturar** (o el acceso desde la grilla).
3. Usá el botón **Buscar Venta** para cargar los datos de la venta en el formulario.
4. Verificá o completá el **PDV**, **VENDEDOR** y **FECHA**.
5. Verificá los datos del **CLIENTE** e **IVA**.
6. Seleccioná el **TIPO** de comprobante (A o B según condición del cliente).
7. Agregá observaciones si es necesario.
8. Revisá el detalle de artículos en el panel derecho.
9. Hacé click en **Guardar** o **Emitir** para generar el comprobante.

> ⚠️ Antes de facturar, la venta debe tener un remito emitido. Si no tiene remito, el sistema lo informará.

---

## Tipos de comprobante más usados

| Tipo | Descripción |
|---|---|
| `EA` | Factura electrónica A |
| `EB` | Factura electrónica B |
| `EC` | Factura electrónica C |
| `A` | Factura A (talonario manual) |
| `B` | Factura B (talonario manual) |

---

> 📖 Para facturar múltiples ventas en lote consultá [**Facturación Masiva ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion_Masiva.pdf).
> 📖 Para subir la factura ya emitida a ML consultá la sección **Aprobar** en [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
