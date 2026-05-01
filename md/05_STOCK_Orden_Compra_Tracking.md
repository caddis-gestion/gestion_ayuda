# 5.XX ORDEN DE COMPRA TRACKING
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Orden de Compra Tracking

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Orden de Compra Tracking** permite registrar y seguir el estado de importación de artículos asociados a órdenes de compra: facturas del proveedor, número de tracking, ubicación y transporte. Desde aquí podés:

- Asociar facturas de proveedor a una orden de compra
- Registrar el tracking, la ubicación y el transporte de los artículos
- Importar datos de tracking desde un archivo
- Imprimir la orden de compra y generar etiquetas de estado

---

<img src="imagenes/pantalla_orden_compra_tracking.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Orden de Compra Tracking**

---

## Formulario

| Campo | Descripción |
|---|---|
| **ORDEN DE COMPRA** | Selector de órdenes de compra en estado Pendiente o Enviado |
| **FACTURA** | Tipo y número de factura del proveedor a asociar |
| **ARTICULO** | Artículo de la orden a ingresar |

**Botón Ingresar Artículos:** Registra los artículos con la factura y datos de tracking ingresados.

### Sección IMPORTAR

Permite cargar o actualizar datos de tracking de múltiples artículos desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y actualiza los registros de tracking de la orden activa. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **10 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Id** | ID interno del registro de tracking (para actualizar uno existente). Dejar vacío para crear nuevo. | Entero o vacío |
| **Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Cantidad** | Cantidad de unidades. Negativo para eliminar el registro. | Entero positivo o negativo |
| **Importe** | Precio unitario del artículo | Decimal (punto como separador) |
| **Factura Tipo** | Tipo de comprobante del proveedor | A, B, C, etc. |
| **Factura Nro** | Número de factura en formato PDV-NRO (ej: 0001-00001234) | Texto con guión en posición 5 |
| **Factura Fecha** | Fecha de la factura | DD/MM/YYYY o número de serie Excel |
| **Id Tracking** | Número de guía o seguimiento | Texto libre |
| **Ubicacion** | Ubicación del artículo en el depósito | Texto libre |
| **Transporte** | Nombre del transporte | Debe existir en la tabla de transportes |

#### Validaciones del sistema

- Filas con **Cantidad < 0** sin **Id** asignado → error, se cancela la importación.
- Datos duplicados en la combinación Codigo + Factura + Tracking + Ubicación → error con detalle.
- **Factura Nro** debe tener un guión en la posición 5 (ej: `0001-00001234`); las filas con formato incorrecto se descartan.
- **Transporte** debe coincidir exactamente con un nombre de la tabla de transportes.
- **Fecha** se convierte automáticamente desde número de serie Excel o formato DD/MM/YYYY.

#### Qué hace el sistema al importar

- **Cantidad > 0**: inserta o actualiza el registro de tracking para esa factura y artículo.
- **Cantidad ≤ 0**: elimina el registro de tracking identificado por el **Id**.

---

## Panel derecho — Grilla de tracking

Muestra el detalle de los artículos registrados para la orden de compra seleccionada:

| Columna | Descripción |
|---|---|
| Id | Identificador del registro |
| Codigo | Código del artículo |
| Cantidad | Cantidad de unidades |
| Precio Unitario Compra | Precio de compra por unidad |
| Precio Unitario Factura | Precio de factura por unidad |
| Monto Total Factura | Total de la factura |
| Factura Tipo | Tipo de comprobante |
| Factura Nro | Número de comprobante |
| Factura Fecha | Fecha del comprobante |
| Tracking | Número de tracking del envío |
| Ubicacion | Ubicación física del artículo |
| Transporte | Empresa de transporte |
| OC | Número de orden de compra |
| Ingreso Articulos | Fecha de ingreso de los artículos |
| Articulo | Descripción del artículo |
| Variante | Variante del artículo |
| Error | Indicador de error en el registro (resaltado) |

**Acciones disponibles:**
- **Checkbox:** Seleccionar registros para operaciones en lote
- **Modificar:** Editar los datos del registro (tracking, ubicación, transporte, etc.)
- **Imprimir:** Imprime la orden de compra
- **Etiqueta:** Genera etiqueta con el estado de tracking
- **Borrar:** Elimina el registro

---

## Notas importantes

- Solo se muestran órdenes de compra en estado **Pendiente** o **Enviado**.
- Los registros con errores se resaltan en la grilla para facilitar su identificación y corrección.
- Usá la importación para cargar masivamente datos de tracking cuando recibís la información del proveedor o transportista.
