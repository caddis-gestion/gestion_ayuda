# 6.08 ML VENTAS
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Ventas

---

## ¿Para qué sirve esta pantalla?

**ML Ventas** es el panel de gestión de todas las ventas realizadas a través de MercadoLibre. Desde aquí podés:

- Consultar y filtrar las ventas bajadas desde la API de ML por estado, fecha, logística, depósito y facturación
- Actualizar el listado de ventas sincronizando con la API de ML
- Emitir remitos internos para las ventas del período
- Imprimir etiquetas de envío para despachar paquetes
- Subir comprobantes fiscales (facturas) a la plataforma de ML
- Enviar mensajes al comprador desde el sistema
- Ver el detalle completo de una publicación vinculada a la venta
- Acceder rápidamente a las ventas según su etapa de preparación o despacho

> ℹ️ Esta pantalla muestra ventas ya realizadas. Para gestionar publicaciones activas y stock, consultá [**ML Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicaciones.pdf).

---

<img src="imagenes/pantalla_ml_ventas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Ventas**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda, botones de proceso y accesos rápidos agrupados por etapa logística (Preparar, Despachar, En Tránsito).
- **Panel derecho (grilla):** Listado de ventas con sus datos de envío, facturación, comprador y estado. Las primeras 6 columnas son fijas al hacer scroll horizontal.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre a consultar. **Obligatorio** para ver resultados. |
| **ESTADO** | Estado de la orden de venta en ML (ej: `paid`, `cancelled`). |
| **DEPOSITO** | Filtra ventas asignadas a un depósito/punto de venta específico. |
| **FACTURAS** | `EMITIDAS` — ventas con comprobante fiscal generado. `PENDIENTES` — ventas sin comprobante. Vacío muestra todas. |
| **DESDE** | Fecha de inicio del rango a consultar. |
| **HASTA** | Fecha de fin del rango. |
| **VER POR** | `CREACION` — filtra por fecha en que se generó la venta. `MODIFICACION` — filtra por última actualización. |
| **CANCELADAS** | `SI` incluye ventas canceladas en el resultado. `NO` las oculta. |
| **VENTA** | ID numérico de una venta específica de ML o ID de carrito (cuando el comprador adquirió varios ítems en un solo pedido). Si se completa este campo, se ignoran DESDE y HASTA. |
| **SKU** | Código del artículo en Caddis para filtrar ventas de un producto en particular. |

> 💡 El campo **USUARIO** es obligatorio. Completá DESDE y HASTA para ver el período deseado. El rango máximo para emitir remitos es 31 días.

---

## Botones de proceso

### Actualizar Ventas

Descarga desde la API de MercadoLibre todas las ventas del período seleccionado y las sincroniza en la base de datos de Caddis.

**Cuándo usarlo:** cuando hay ventas recientes que no aparecen en la grilla, o cuando el estado de una venta cambió en ML y no se refleja en el sistema.

**Cómo ejecutarlo:**

1. Seleccioná el **USUARIO** ML.
2. Completá **DESDE** y **HASTA** con el rango de fechas deseado.
3. Elegí **VER POR** (Creación o Modificación).
4. Hacé click en **Actualizar Ventas**.
5. Confirmá el aviso *"Desea actualizar las ventas?"*.
6. El proceso corre en **segundo plano** — podés seguir trabajando mientras sincroniza.

---

### Emitir Remitos

Genera los remitos internos de venta para todas las ventas del período seleccionado que aún no tengan remito emitido.

**Cuándo usarlo:** al final del día o después de procesar un lote de ventas, para registrar las salidas de stock correspondientes a las ventas de ML.

**Cómo ejecutarlo:**

1. Seleccioná el **USUARIO** ML.
2. Completá **DESDE** y **HASTA** (máximo 31 días).
3. Hacé click en **Emitir Remitos**.
4. Confirmá el aviso *"Desea emitir Remitos?"*.
5. El proceso corre en **segundo plano**.

> ⚠️ Si el rango de fechas supera los 31 días el sistema rechazará la solicitud con el mensaje *"Solicitar máximo 31 días por vez"*.

---

## Panel izquierdo: Filtro de Envíos

Permite refinar la grilla por los datos del envío de cada venta. Se puede usar en combinación con los filtros principales.

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de logística del envío (`cross_docking` = colecta, `self_service` = Flex, `fulfillment` = FULL, etc.). |
| **ESTADO** | Estado del envío en ML (ej: `ready_to_ship`, `shipped`, `delivered`). |
| **SUBESTADO** | Subestado del envío, con mayor detalle que el estado (ej: `ready_to_print`, `printed`, `waiting_for_withdrawal`). |

---

## Accesos rápidos por etapa logística

El panel izquierdo incluye botones que aplican automáticamente combinaciones de filtros predefinidas según la etapa en que se encuentra la venta. Son un atajo para filtrar sin configurar manualmente cada campo.

### Ver todas las ventas
Limpia todos los filtros de envío y muestra el total de ventas del período.

---

### PARA PREPARAR

Ventas pagas que están listas para armar y embalar.

| Botón | Filtros aplicados | Descripción |
|---|---|---|
| **Para la colecta** | Logística: `cross_docking` · Subestado: `ready_to_print` | Envíos por colecta con etiqueta lista para imprimir |
| **Mercado Envíos Flex** | Logística: `self_service` · Subestado: `ready_to_print` | Envíos Flex con etiqueta lista para imprimir |
| **Acordar con el comprador** | Logística: `not_specified` · Shipping estado: `to_be_agreed` | Envíos donde hay que coordinar la entrega directamente con el comprador |

---

### PARA DESPACHAR

Ventas ya empaquetadas, listas para entregar al servicio de correo o al centro de ML.

| Botón | Filtros aplicados | Descripción |
|---|---|---|
| **Mercado Envíos Flex** | Logística: `self_service` · Subestado: `printed` | Envíos Flex con etiqueta impresa, listos para despachar |
| **Para la colecta** | Logística: `cross_docking` · Subestado: `ready_for_pickup` | Envíos por colecta esperando al correo |
| **En el centro de almacenamiento** | Shipping estado: `ready_to_ship` · Subestado: `in_warehouse` | Paquetes en el depósito de ML aguardando despacho |

---

### EN TRÁNSITO

Ventas ya despachadas en camino al comprador.

| Botón | Filtros aplicados | Descripción |
|---|---|---|
| **Esperando retiro del comprador** | Subestado: `waiting_for_withdrawal` | El paquete llegó y espera que el comprador lo retire |
| **En camino FULL** | Logística: `fulfillment` · Shipping estado: `shipped` | Envíos FULL en camino gestionados por el depósito de ML |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Venta** | ID único de la venta en MercadoLibre. |
| **Carrito** | ID del carrito o pedido combinado (`pack_id`). Cuando un comprador adquiere varios ítems en un mismo pedido, todas las ventas comparten el mismo ID de carrito. |
| **Fecha** | Fecha de creación de la venta en ML. |
| **Modificado** | Fecha y hora de la última actualización de la venta en ML. |
| **Cantidad** | Cantidad de unidades vendidas. |
| **Cantidad x Bulto** | Unidades físicas incluidas en cada envío según la configuración de la publicación. |
| **Importe** | Monto cobrado al comprador (importe − descuento por cupón). |
| **Estado** | Estado de la orden de venta (ej: `Pagada`, `Cancelada`, `Entregada`). |
| **Shipping Tipo** | Tipo de logística del envío (`Normal`, `Flex`, `FULL`, etc.). |
| **Shipping Estado** | Estado del envío en ML. |
| **Shipping Subestado** | Subestado del envío, con mayor nivel de detalle. |
| **Shipping Tracking** | ID de seguimiento del envío (`shipping_id`). |
| **Item** | ID de la publicación de ML vinculada a la venta. |
| **SKU** | Código del artículo en Caddis. |
| **Titulo** | Título de la publicación en ML. |
| **Cliente** | Nombre del comprador registrado en ML. |
| **Documento** | Tipo y número de documento del comprador (ej: `DNI-12345678`). |
| **Domicilio** | Dirección de entrega del envío. |
| **Cpostal** | Código postal del domicilio de entrega. |
| **Localidad** | Localidad del domicilio de entrega. |
| **Telefono** | Teléfono de contacto del comprador. |
| **Deposito** | Nombre del depósito desde donde se asignó la factura. |
| **Factura Tipo** | Tipo de comprobante fiscal emitido (ej: `EA`, `EB`, `EC`). |
| **Factura Nro** | Número del comprobante fiscal. |
| **Factura Subida** | `SI` si el comprobante fue subido a ML correctamente. Vacío si está pendiente. |
| **Usuario** | Cuenta de MercadoLibre a la que pertenece la venta. |
| **Error** | Último mensaje de error registrado para esa venta (ej: error al subir factura). |

> ℹ️ La grilla se ordena automáticamente mostrando primero las ventas con errores, luego por estado de orden, tipo de logística, estado y subestado del envío, y finalmente por fecha.

---

## Acciones desde la grilla

Seleccioná una fila de la grilla y usá los botones de acción disponibles en la barra de la grilla:

### Mensaje — Comunicación con el comprador

Abre una ventana de mensajería para comunicarte con el comprador directamente desde Caddis, sin salir al portal de ML.

**Cuándo usarlo:** para coordinar una entrega, informar una demora o responder preguntas post-venta.

---

### Detalle — Ver publicación

Abre una ventana con el detalle completo de la publicación vinculada a esa venta (atributos, imágenes, variantes, datos del ítem en ML).

---

### Etiqueta — Imprimir etiqueta de envío

Genera e imprime la etiqueta de envío de MercadoLibre para esa venta.

> ⚠️ Al imprimir la etiqueta, el sistema **modifica el estado del envío en ML** y solicita el retiro del paquete. Confirmá el aviso *"¿Desea imprimir la etiqueta? Esto modifica el estado en Mercado Libre y solicita el retiro del paquete"* solo cuando el paquete esté listo para ser despachado.

**Pasos:**

1. Seleccioná la fila de la venta en la grilla.
2. Hacé click en el botón **Etiqueta**.
3. Confirmá el aviso.
4. Se abre una ventana con el PDF de la etiqueta lista para imprimir.

---

### Aprobar — Subir factura a ML

Sube el comprobante fiscal de esa venta a la plataforma de MercadoLibre.

**Condiciones:**
- La venta debe tener una factura de tipo **EA, EB o EC** (electrónica) generada en Caddis.
- Si la factura ya fue subida (columna **Factura Subida = SI**), el sistema pedirá confirmación adicional antes de volver a subirla.
- Si el tipo de factura es diferente de EA/EB/EC, el sistema mostrará un aviso con el tipo y número para que se controle manualmente.
- Si no hay factura guardada para la venta, el sistema lo informará con un aviso.

**Pasos:**

1. Seleccioná la fila de la venta a facturar.
2. Hacé click en **Aprobar**.
3. Confirmá el aviso *"Desea subir la factura?"*.
4. Si fue exitoso, la columna **Factura Subida** cambia a `SI` automáticamente en la grilla.

---

## Conceptos clave

### Estados de una venta ML

| Estado | Significado |
|---|---|
| `paid` | Venta paga — el comprador pagó |
| `cancelled` | Venta cancelada |
| `delivered` | Entregada al comprador |
| `payment_required` | Pago pendiente |

### Tipos de logística de envío

| Tipo | Nombre visible | Descripción |
|---|---|---|
| `cross_docking` | Colecta | El correo pasa a retirar el paquete del local |
| `self_service` | Mercado Envíos Flex | El vendedor lleva el paquete al correo |
| `fulfillment` | FULL | El stock está en el depósito de ML |
| `not_specified` | Acordar entrega | El envío se coordina directamente con el comprador |

### Subestados de envío más frecuentes

| Subestado | Descripción |
|---|---|
| `ready_to_print` | Etiqueta lista para imprimir |
| `printed` | Etiqueta impresa |
| `ready_for_pickup` | Paquete listo para que pase el correo |
| `in_warehouse` | En el depósito de ML |
| `waiting_for_withdrawal` | Esperando que el comprador retire |

### ¿Qué es el Carrito?

Cuando un comprador adquiere varios artículos en un mismo pedido, ML genera un **ID de carrito** (`pack_id`) que agrupa todas las ventas. En la grilla, cada ítem aparece como una fila separada pero comparte el mismo Carrito. Es útil para identificar y gestionar pedidos múltiples juntos.

### ¿Cuándo se emite el remito?

El remito se genera al ejecutar **Emitir Remitos**. Registra la salida de stock en Caddis y vincula las unidades vendidas a cada ítem del depósito correspondiente. Es necesario emitir el remito antes de poder generar la factura fiscal de la venta.

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| No aparecen ventas | No se seleccionó USUARIO | Elegí una cuenta ML en el campo USUARIO |
| "El proceso ya se encuentra corriendo" | Ya hay un proceso activo del mismo tipo | Esperá a que termine antes de lanzar otro |
| "Solicitar máximo 31 días por vez" | El rango de fechas supera los 31 días | Acotá el período en DESDE y HASTA |
| Columna Error con mensaje de factura | Error al subir el comprobante a ML | Verificá que la factura sea de tipo EA/EB/EC y reintentá con Aprobar |
| Botón Aprobar informa "No hay factura" | La venta no tiene comprobante generado aún | Emitir la factura primero desde ML Facturacion Masiva |
| La columna Factura Subida no cambia a SI | Error en la API de ML | Revisar el mensaje de error en la columna Error |

---

## Preguntas frecuentes

**¿Con qué frecuencia debo actualizar las ventas?**
Depende del volumen de ventas. En días de alta actividad conviene actualizar cada pocas horas. El sistema también puede tener un proceso automático configurado por el administrador.

**¿Puedo emitir remitos de ventas que ya tienen remito?**
No — el proceso solo genera remitos para ventas que aún no lo tienen. Las ventas ya procesadas no se duplican.

**¿Qué diferencia hay entre Actualizar Ventas y Ver todas las ventas?**
- **Actualizar Ventas**: descarga nuevas ventas desde la API de ML y actualiza el estado de las existentes (proceso en segundo plano).
- **Ver todas las ventas**: solo aplica filtros en la grilla ya cargada en pantalla, sin contactar la API.

**¿Por qué algunas ventas no tienen depósito asignado?**
El depósito se asigna cuando se genera la factura de la venta. Si la columna Deposito está vacía, la venta aún no tiene comprobante fiscal emitido.

**¿Puedo filtrar por comprador o nombre de cliente?**
No directamente — la grilla no tiene filtro por nombre de cliente. Podés buscar por **VENTA** (ID de ML) o por **SKU** del artículo vendido.

**¿Qué pasa si imprimo la etiqueta por error?**
Al imprimir la etiqueta se modifica el estado en ML y se solicita el retiro del paquete. Si fue un error, contactá a MercadoLibre para revertir el estado del envío.

---

> 📖 Para gestionar las publicaciones de ML (stock, precio, logística), consultá [**ML Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicaciones.pdf).
> 📖 Para facturar ventas de MercadoLibre en forma masiva, consultá el instructivo de **ML Facturacion Masiva**.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
