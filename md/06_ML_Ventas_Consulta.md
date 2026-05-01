# 6.09 ML DETALLE DE VENTA
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Ventana emergente accesible desde ML Ventas

---

## ¿Para qué sirve esta pantalla?

**ML Detalle de Venta** es una ventana emergente que muestra y permite editar el detalle completo de una venta de MercadoLibre. Desde aquí podés:

- Ver todos los datos de la orden: comprador, ítem, importe, factura y estado
- Corregir el SKU vinculado a la venta
- Asociar o ver la factura fiscal de la venta
- Subir el comprobante a ML (FC Subida)
- Controlar los datos de facturación y envío del comprador
- Ver si hay reclamo activo asociado a la venta
- Gestionar el campo de inhabilitación de la venta

---

<img src="imagenes/pantalla_ml_ventas_consulta.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Esta pantalla es una ventana emergente. Se accede desde:
**ML Ventas → seleccionar una venta → botón Detalle (o doble click en la fila)**

---

## Sección: Datos de la venta

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta ML de la venta (solo lectura) |
| **VENTA** | ID de la venta en ML + estado actual (solo lectura) |
| **PACK** | ID de carrito si el comprador compró varios ítems (solo lectura) |
| **CLIENTE** | Nombre del comprador (solo lectura) |
| **FECHA** | Fecha de creación de la venta (solo lectura) |
| **TITULO** | Título de la publicación (editable como área de texto) |
| **ITEM** | ID de la publicación ML (solo lectura) |
| **SKU** | Código del artículo en Caddis — editable. Tiene botón **Buscar** para seleccionar el SKU correcto. |
| **IMPORTE** | Importe de la venta (solo lectura) — se puede ajustar al corregir el SKU |
| **CUPON** | Monto de cupón de descuento aplicado (solo lectura) |
| **TOTAL** | Total a pagar por el comprador (solo lectura) |
| **CANTIDAD** | Unidades vendidas (solo lectura) |

---

### Cómo corregir el SKU vinculado a la venta

El campo **SKU** identifica el artículo de Caddis asociado a la venta de ML. Podés corregirlo en los siguientes casos:

- El SKU fue importado incorrectamente o no se reconoció.
- El cliente solicitó cambiar el producto (por ejemplo, un modelo o color diferente), y se prefiere mantener la venta existente en lugar de cancelarla y generar una nueva.

**Pasos:**

1. Hacé clic en el botón **Buscar** (junto al campo SKU).
2. En la ventana emergente, buscá y seleccioná el artículo correcto.
3. El sistema abre un cuadro de confirmación del importe — verificá el monto y confirmá (o modificalo si corresponde).
4. El sistema actualiza el SKU. Si la venta ya tenía un remito emitido, lo anula automáticamente y emite uno nuevo con el SKU e importe corregidos.

**Restricciones:**

| Situación | Comportamiento |
|---|---|
| Venta con estado **Cancelada** | El botón Buscar no se muestra |
| Venta con factura tipo **EA o EB** (factura fiscal emitida) | El sistema bloquea la modificación: "Venta ya facturada. Primero debe realizar una Nota de Crédito" |
| Venta con remito (R/IR) | El sistema anula el remito anterior y emite uno nuevo automáticamente |
| Sin comprobante previo | Solo actualiza el SKU en la base de datos |

---

## Sección: Factura

| Campo | Descripción |
|---|---|
| **FACTURA tipo** | Tipo de comprobante emitido (ej: EA, EB, EC, A, B) |
| **FACTURA nro** | Número del comprobante |
| **Ver** | Abre el PDF del comprobante para visualizarlo |
| **Asociar** | Permite asociar manualmente un comprobante fiscal existente a esta venta |
| **FC SUBIDA** | `SI`/`NO` + botón **Subir** — indica si el comprobante fue subido a ML y permite subirlo si no se hizo aún |
| **INHABILITADA** | Checkbox — marca la venta como inhabilitada para procesos automáticos |

---

### Cómo ver la factura fiscal asociada

Hacé clic en el botón **Ver** (ícono de lupa/detalle) junto al campo FACTURA. Se abre un popup con el PDF del comprobante.

> Este botón solo funciona si la venta tiene un comprobante asociado (los campos FACTURA tipo y nro están completos).

---

### Cómo asociar una factura fiscal a la venta

Usá esta función cuando la factura fue emitida manualmente y no quedó vinculada automáticamente a la venta de ML.

**Pasos:**

1. Hacé clic en el botón **Asociar** (ícono de lápiz/modificar).
2. Se abre una ventana de búsqueda de comprobantes.
3. Buscá el comprobante por tipo y número, y seleccionalo.
4. El sistema vincula el comprobante a la venta y actualiza los campos FACTURA tipo y nro.

**Restricciones:**

| Situación | Comportamiento |
|---|---|
| Venta con estado **cancelled** | No se permite asociar: "No se puede asociar una factura a una venta cancelada" |
| Venta con estado **invalid** | No se permite asociar: "No se puede asociar una factura a una venta inválida" |

---

### Cómo subir el comprobante a MercadoLibre (FC Subida)

El campo **FC SUBIDA** indica si el comprobante fiscal ya fue enviado a ML (`SI` / `NO`). ML requiere que se adjunte la factura electrónica de cada venta.

**Pasos:**

1. Verificá que la venta tenga un comprobante asociado (FACTURA tipo y nro completos).
2. Hacé clic en el botón **Subir** (ícono de carga).
3. Confirmá el cuadro de diálogo.
4. El sistema sube el comprobante a ML vía API y muestra el resultado.

**Comportamientos:**

| Estado FC SUBIDA | Mensaje de confirmación |
|---|---|
| **NO** (no fue subida aún) | "¿Desea subir la factura?" |
| **SI** (ya fue subida) | "Ya fue subida la factura para esta venta. ¿Desea volver a subirla?" |

Si la operación es exitosa, el campo FC SUBIDA pasa a **SI**. En caso de error, el sistema muestra el mensaje devuelto por la API de ML.

---

### Cómo gestionar la inhabilitación de la venta

El checkbox **INHABILITADA** permite excluir la venta de los procesos automáticos de Caddis (facturación automática, despacho, etc.). Se usa cuando la venta fue gestionada por fuera de ML o requiere tratamiento manual.

**Pasos:**

- **Inhabilitar**: tildá el checkbox → el sistema actualiza el registro y muestra "Venta inhabilitada".
- **Reactivar**: destildá el checkbox → el sistema muestra "Inhabilitación anulada".

> La inhabilitación no cancela la venta en MercadoLibre. Solo la excluye del procesamiento interno de Caddis.

---

## Sección: Datos de facturación del comprador

| Campo | Descripción |
|---|---|
| **DOC. TIPO** | Tipo de documento del comprador (DNI, CUIT, etc.) |
| **DOC. NRO** | Número de documento |
| **NOMBRE** | Nombre completo del comprador |
| **DOMICILIO** | Domicilio fiscal del comprador |
| **C. POSTAL** | Código postal del domicilio fiscal |
| **LOCALIDAD** | Localidad del domicilio fiscal |
| **PROVINCIA** | Provincia |
| **IVA** | Condición frente al IVA (Consumidor Final, Responsable Inscripto, etc.) |

---

## Sección: Datos de envío

| Campo | Descripción |
|---|---|
| **TRACKING** | ID de seguimiento del envío |
| **ESTADO** | Estado del envío |
| **LOGISTICA** | Tipo de logística |
| **ENTREGA** | Tipo de entrega (domicilio, sucursal, etc.) |
| **DOMICILIO** | Dirección de entrega |
| **C. POSTAL** | Código postal de entrega |
| **LOCALIDAD** | Localidad de entrega |
| **PROVINCIA** | Provincia de entrega |
| **TELEFONO** | Teléfono de contacto del comprador |

---

## Sección: Control interno

| Campo | Descripción |
|---|---|
| **ENVIO ARMADO** | Indica si el paquete fue armado en el depósito |
| **PAQUETE** | Identificador del paquete armado |
| **ENTREGA** | Fecha/estado de entrega al comprador |
| **RECEPCION** | Fecha de recepción del paquete por el comprador |

---

## Sección: Logística externa (si aplica)

| Campo | Descripción |
|---|---|
| **ENVIO** | Número de envío en el operador logístico externo |
| **FECHA** | Fecha del envío externo |
| **TRACKING** | Número de seguimiento externo |

---

## Sección: Reclamos (si hay reclamo activo)

Si la venta tiene un reclamo activo en ML, aparece una sección adicional con los datos del reclamo (ID, estado, tipo, descripción, acciones pendientes). Ver [**Reclamos ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Reclamos.pdf) para más detalle.

---

> 📖 Para gestionar el listado completo de ventas consultá [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).
> 📖 Para ver y gestionar reclamos consultá [**Reclamos ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Reclamos.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
