# 3.05 FACTURACIÓN MÓVIL
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación Móvil

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Facturación Móvil** está diseñada para emitir comprobantes de venta desde dispositivos móviles (tablets, celulares) o desde cualquier navegador con pantalla pequeña. Desde aquí podés:

- Emitir facturas, tickets y comprobantes de venta desde cualquier dispositivo
- Ingresar artículos y registrar cobros con una interfaz adaptada a pantallas táctiles
- Aplicar vouchers y promociones
- Ver el total de la factura en tiempo real antes de emitirla

> ℹ️ Esta pantalla tiene las mismas funciones que la **Facturación estándar** (3.01), pero con un diseño vertical y adaptado para uso táctil. Para ventas desde computadora de escritorio, se recomienda usar la pantalla estándar.

---

<img src="imagenes/pantalla_facturacion_movil.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación Móvil**

---

## Descripción general de la pantalla

La pantalla tiene un diseño vertical (una sección debajo de la otra), optimizado para pantallas táctiles:

1. **Sección COMPROBANTE:** Tipo de comprobante, PDV y vendedor
2. **Sección CLIENTE:** Datos del cliente (nombre, documento/CUIT, email)
3. **Sección ARTÍCULOS:** Ingreso de artículos con promociones y voucher
4. **Sección PAGOS:** Lista de formas de pago registradas con opción de agregar nuevas
5. **Botón EMITIR:** Muestra el total en tiempo real y emite el comprobante al presionarlo

---

## Secciones del formulario

### Sección: COMPROBANTE

| Campo | Descripción |
|---|---|
| **FACTURA (tipo)** | Tipo de comprobante a emitir (TK, EB, EA, A, B, X, etc.). |
| **PDV** | Punto de Venta desde donde se emite el comprobante. |
| **VENDEDOR** | Vendedor responsable de la venta. |

> ℹ️ La **FECHA** se asigna automáticamente al día de hoy (campo oculto, no requiere ingreso manual).

---

### Sección: CLIENTE

| Campo | Descripción |
|---|---|
| **CLIENTE** | Nombre del cliente. Podés buscarlo por nombre o dejarlo vacío para usar "Consumidor Final". |
| **DOC / CUIT** | Documento o CUIT del cliente. Se completa automáticamente al seleccionar el cliente. |
| **EMAIL** | Correo electrónico del cliente para enviar el comprobante. |

---

### Sección: ARTÍCULOS

| Campo/Botón | Descripción |
|---|---|
| **Campo de artículo** | Ingresá el código del artículo o usá el buscador para encontrarlo. |
| **Promos** | Abre el buscador de promociones disponibles para aplicar al comprobante. |
| **Voucher** | Permite ingresar el código de un voucher de descuento. |

> ℹ️ En la versión móvil, los campos de cantidad e importe de cada artículo se gestionan a través de un modal (ventana emergente) que se abre al seleccionar el artículo, en lugar de campos siempre visibles en la pantalla principal.

---

### Sección: PAGOS

Esta sección muestra una tabla con los medios de pago ya registrados para el comprobante actual:

| Columna | Descripción |
|---|---|
| **Tipo** | Tipo de pago ingresado (efectivo, tarjeta, transferencia, etc.) |
| **Importe** | Monto registrado para ese pago |
| **Eliminar** | Botón para quitar ese pago de la lista |

En la parte inferior de la tabla se muestran:
- **Total pagos:** suma de todos los medios de pago registrados
- **Botón "Agregar Pago":** abre el formulario para registrar un nuevo medio de pago

---

### Botón EMITIR

El botón de emisión muestra en tiempo real el **total de la factura**:

```
Facturar  $XX.XX
```

El importe se actualiza automáticamente a medida que se agregan artículos o se aplican descuentos. Al presionarlo, el sistema emite el comprobante y lo envía a AFIP si corresponde.

---

## Paso a paso: Emitir una factura desde el móvil

**1. Elegir el tipo de comprobante**
- En la sección **COMPROBANTE**, seleccioná el tipo (ej.: TK para ticket, EB para Factura B electrónica).
- Elegí el **PDV** y el **VENDEDOR**.

**2. Seleccionar el cliente** *(opcional)*
- En la sección **CLIENTE**, buscá y seleccioná al cliente.
- Si es una venta a consumidor final, podés omitir este paso.

**3. Ingresar los artículos**
- En la sección **ARTÍCULOS**, ingresá el código del artículo o buscalo.
- Se abrirá un modal para ingresar la cantidad. Confirmá.
- El artículo se agrega al comprobante y el total del botón se actualiza.
- Repetí para cada artículo adicional.

**4. Aplicar descuentos** *(opcional)*
- Hacé clic en **Promos** para buscar y aplicar una promoción de venta.
- Hacé clic en **Voucher** e ingresá el código si hay un voucher disponible.

**5. Registrar el cobro**
- En la sección **PAGOS**, hacé clic en **Agregar Pago**.
- Seleccioná el tipo de pago, completá los campos requeridos y confirmá.
- Repetí si el cobro es en múltiples medios de pago.

**6. Emitir**
- Verificá que el total del botón **Facturar** sea correcto.
- Presioná el botón para emitir el comprobante.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Elija un PDV" | Se intentó emitir sin seleccionar PDV | Seleccioná el PDV en la sección COMPROBANTE |
| "Ingrese un Item..." | Se intentó emitir sin artículos | Ingresá al menos un artículo |
| "Controle la Cantidad" | La cantidad es cero o inválida | Revisá la cantidad en el modal del artículo |
| La pantalla no se adapta bien | El navegador no es compatible | Usá Chrome o Edge actualizados |

---

## Preguntas frecuentes

**¿Necesito instalar alguna aplicación?**
No. La Facturación Móvil es una página web que se accede desde el navegador del dispositivo móvil. No requiere instalación.

**¿Funciona sin conexión a internet?**
No. Se requiere conexión a internet para acceder al sistema y para enviar los comprobantes a AFIP.

**¿Puedo imprimir la factura desde el móvil?**
Sí, el sistema puede mostrar el comprobante en PDF para imprimirlo o enviarlo por email desde el dispositivo.

**¿La Facturación Móvil es igual a la estándar en cuanto a funciones fiscales?**
Sí, emite los mismos tipos de comprobantes y los envía a AFIP de igual manera. La diferencia es solo en la interfaz.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
