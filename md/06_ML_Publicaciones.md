# ML PUBLICACIONES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Publicaciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **ML Publicaciones** es el panel central de control de las publicaciones de MercadoLibre. Permite visualizar en tiempo real el estado de cada publicación: su stock disponible en Caddis comparado con el stock en ML, el precio de lista de Caddis versus el precio de venta publicado, la logística (FULL o estándar), el tipo de publicación y cualquier error de sincronización.

Desde aquí podés:

- Filtrar publicaciones por usuario ML, estado, logística, marca, ítem o SKU
- Ver el stock disponible calculado por Caddis para cada publicación
- Editar directamente el stock, el precio y la cantidad por bulto de una publicación sin salir de la grilla
- Lanzar procesos masivos: actualizar publicaciones desde ML, enviar stock a ML, enviar precios a ML
- Detectar publicaciones con errores de sincronización (columna **Error**)
- Ver el detalle completo de una publicación con doble click

> ℹ️ Esta pantalla **no genera ventas ni facturas** — es una herramienta de gestión y monitoreo de publicaciones. Las ventas de ML se gestionan desde **ML Ventas** (6.08).

---

<img src="imagenes/pantalla_ml_publicaciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Publicaciones**

---

## Descripción general de la pantalla

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Filtros para acotar la grilla + sección **Procesos** con los botones de actualización masiva.
- **Panel derecho (grilla):** Listado de publicaciones con sus datos de stock, precio, logística y estado. Las primeras 4 columnas son fijas (no se desplazan al hacer scroll horizontal).

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre a consultar. Cada empresa puede tener una o más cuentas vendedoras. **Obligatorio** para ver resultados. |
| **ESTADO** | Filtra por estado de la publicación en ML: `Activa`, `Pausada`, `Cerrada`, `Eliminada`, etc. Por defecto muestra las activas. |
| **LOGISTICA** | Filtra por tipo de envío: vacío (todos), `NO ES FULL` (envío propio o estándar), `ES FULL` (stock en depósito de ML). |
| **EXCEPTUADOS** | Filtra publicaciones según si están exceptuadas del control de stock automático: `SI` (exceptuadas) o `NO` (normales). |
| **CATALOGO** | Filtra por publicaciones de catálogo ML (`SI`) o publicaciones propias (`NO`). |
| **BULTOS** | Filtra por cantidad de unidades por envío: `1 UNIDAD` o `MAS DE 1 UNIDAD`. |
| **MARCA** | Filtra por marca del artículo relacionado en Caddis. |
| **ITEM** | Busca una publicación específica por su ID de MercadoLibre (ej: `MLA12345678`). |
| **SKU** | Busca por el SKU del artículo en Caddis. Acepta también códigos de promociones o artículos compuestos. |

> 💡 Para ver todas las publicaciones, solo completá **USUARIO** y hacé click en **Actualizar** (o presioná Enter en cualquier campo). El resto de los filtros son opcionales.

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Item** | ID único de la publicación en MercadoLibre (ej: `MLA12345678`). |
| **SKU** | Código del artículo o promoción de Caddis vinculado a la publicación. |
| **Variante** | ID de variante dentro de la publicación (cuando la publicación tiene tallas, colores, etc.). |
| **Stock Disponible** | Stock calculado por Caddis que se enviaría a ML: `(Stock Caddis − Stock Seguridad − Remitos Pendientes) / Cantidad por Bulto`. Incluye también stock de promos y artículos compuestos. |
| **Stock MLibre** | ⚡ **Editable** — Stock actualmente publicado en ML. Podés modificarlo directamente en la celda. |
| **Caddis Full** | Stock disponible de Caddis para logística FULL. |
| **MLibre Full** | Stock actualmente publicado en ML para logística FULL. |
| **Stock Seguridad** | Cantidad mínima de stock que Caddis reserva y no envía a ML. |
| **Cantidad por Bulto** | ⚡ **Editable** — Cuántas unidades físicas incluye cada venta de esa publicación (ej: `2` = se vende de a pares). |
| **Remitos Pendientes** | Cantidad reservada en remitos de venta aún no entregados. Doble click para ver el detalle. |
| **Precio Lista Caddis** | Precio de lista calculado por Caddis para ese artículo (incluye IVA, impuesto interno y cotización de moneda). |
| **Precio Venta MLibre** | ⚡ **Editable** — Precio de venta publicado actualmente en ML. |
| **Lista Precios** | Nombre de la lista de precios de Caddis usada para esta cuenta ML. |
| **Tipo Publicacion** | Tipo de publicación en ML (ej: `gold_special`, `gold_pro`, etc.). |
| **Logistica** | Tipo de logística (ej: `FULFILLMENT`, `self_service`, etc.). |
| **Es Flex** | Indica si la publicación tiene habilitada la logística Flex de ML (`SI`/`NO`). |
| **Estado** | Estado actual de la publicación en ML (activa, pausada, cerrada, etc.). |
| **Titulo** | Título de la publicación tal como aparece en MercadoLibre. |
| **Marca** | Marca del artículo en Caddis. |
| **Color** | Atributo color de la variante. |
| **Categoria** | Categoría de ML a la que pertenece la publicación. |
| **Exceptuado** | `SI` si la publicación está excluida del envío automático de stock. |
| **Es Promo** | `SI` si el SKU es una promoción de Caddis (no un artículo individual). |
| **Es Compuesto** | `SI` si el artículo es un kit compuesto por otros artículos en Caddis. |
| **Condicion** | Condición del artículo: `NEW` (nuevo) o `USADO`. |
| **Usuario** | Cuenta ML vendedora a la que pertenece la publicación. |
| **Error** | Mensaje de error de la última sincronización, si la hubo (ej: error de precio, de stock, o de SKU sin relacionar). |

> ⚠️ Si la columna **Error** muestra `Falta relacionar SKU con Caddis [código]`, significa que la publicación no tiene un artículo de Caddis vinculado a ese SKU. Hay que crear o relacionar el artículo antes de poder sincronizar.

---

## Edición directa en la grilla

Tres columnas permiten modificar valores directamente en la celda sin abrir ninguna ventana:

### Editar Stock MLibre

**1.** Hacé click sobre el valor en la columna **Stock MLibre** de la fila deseada.

**2.** Ingresá el nuevo valor de stock.

**3.** El sistema pedirá confirmación *"¿Modifica el Stock?"*. Confirmá con **Aceptar**.

**4.** El sistema llama a la API de MercadoLibre y actualiza el stock inmediatamente.

> 💡 Usá esta opción para correcciones puntuales. Para actualizar masivamente el stock de todas las publicaciones usá el botón **Actualizar Stock Masivamente**.

### Editar Precio Venta MLibre

**1.** Hacé click sobre el valor en la columna **Precio Venta MLibre**.

**2.** Ingresá el nuevo precio.

> ⚠️ No podés ingresar un precio menor al **70% del precio actual**. Si lo intentás el sistema mostrará un aviso y rechazará el cambio.

**3.** Confirmá con *"¿Modifica el Precio?"*.

**4.** El sistema actualiza el precio en MercadoLibre vía API.

### Editar Cantidad por Bulto

**1.** Hacé click sobre el valor en la columna **Cantidad por Bulto**.

**2.** Ingresá el nuevo valor (número entero).

**3.** Confirmá con *"¿Modifica la Cantidad por Bulto?"*.

> ℹ️ La cantidad por bulto afecta el cálculo del **Stock Disponible**: si un artículo se vende de a 2, el stock que llega a ML es la mitad del stock físico de Caddis.

---

## Doble click en la grilla

| Columna | Acción |
|---|---|
| **Stock Disponible** | Abre una ventana con el detalle de stock por variante y depósito, incluyendo stock FULL y estándar. |
| **Remitos Pendientes** | Abre una ventana con el detalle de los remitos de venta pendientes de entrega que afectan ese SKU. |
| **Cualquier otra celda** | Abre el **detalle completo de la publicación** (título, imágenes, atributos, variantes, etc.). |

---

## Procesos masivos

### Actualizar Publicaciones

Descarga desde la API de MercadoLibre la información actualizada de **todas las publicaciones** del usuario seleccionado y las guarda en la base de datos de Caddis (estado, precio, stock, logística, categoría, etc.).

**Cuándo usarlo:** cuando las publicaciones en ML fueron modificadas directamente desde el portal de ML o desde otra herramienta, y Caddis no tiene esa información actualizada.

**Cómo ejecutarlo:**

**1.** Seleccioná el **USUARIO** ML.

**2.** Seleccioná el **ESTADO** de las publicaciones a actualizar (ej: `Activa`).

**3.** Hacé click en **Actualizar Publicaciones**.

**4.** Confirmá el aviso *"Este proceso actualiza todas las publicaciones desde Mercado Libre. El proceso puede tardar varios minutos"*.

**5.** El sistema lanza el proceso en segundo plano y muestra un panel de estado del proceso. Podés seguir trabajando mientras corre.

> ⚠️ Este proceso puede tardar varios minutos dependiendo de la cantidad de publicaciones.

---

### Actualizar Stock Masivamente

Envía a MercadoLibre el stock disponible calculado por Caddis para **todas las publicaciones** del usuario seleccionado (respetando filtros de ítem, SKU y marca si están completados).

**Cuándo usarlo:** luego de ingresar mercadería, procesar ventas o modificar el stock de seguridad, para que ML refleje el stock actualizado.

**Cómo ejecutarlo:**

**1.** Seleccioná el **USUARIO** ML.

**2.** Opcionalmente completá **ITEM**, **SKU** o **MARCA** para limitar el alcance del proceso.

**3.** Hacé click en **Actualizar Stock Masivamente**.

**4.** Confirmá el aviso.

**5.** El proceso corre en segundo plano.

> 💡 Si solo querés actualizar el stock de una publicación puntual, usá la **edición directa en la columna Stock MLibre** en lugar de este proceso masivo.

---

### Actualizar Precios Masivamente

Envía a MercadoLibre el precio calculado por Caddis (según la lista de precios configurada para esa cuenta ML) para todas las publicaciones que coincidan con los filtros activos.

**Cuándo usarlo:** luego de actualizar la lista de precios en Caddis para que los cambios se reflejen en ML automáticamente.

**Cómo ejecutarlo:**

**1.** Seleccioná el **USUARIO** ML.

**2.** Opcionalmente completá filtros de **ITEM**, **SKU** o **MARCA** para limitar el alcance.

**3.** Hacé click en **Actualizar Precios Masivamente**.

**4.** Confirmá el aviso.

**5.** El sistema procesa los precios y muestra el resultado directamente (a diferencia de stock y publicaciones, este proceso no corre en background).

> ⚠️ El precio que se envía a ML se calcula con la lista de precios configurada para esa cuenta. Si querés cambiar la lista de precios, consultá con el administrador del sistema.

---

## Conceptos clave

### ¿Qué es el Stock Disponible calculado por Caddis?

El **Stock Disponible** es lo que Caddis calcula que debería publicarse en ML:

```
Stock Disponible = (Stock Caddis − Stock Seguridad − Remitos Pendientes) ÷ Cantidad por Bulto
                   + Stock de Promo (si el SKU es una promo)
                   + Stock de Artículo Compuesto (si es un kit)
```

Si el valor es menor a cero (por ejemplo, stock de seguridad mayor al stock real), Caddis envía `0` a ML.

### ¿Qué es un artículo Exceptuado?

Un artículo **exceptuado** tiene desactivada la sincronización automática de stock. Caddis no modifica el stock de esa publicación en ML, independientemente de los movimientos internos. Se usa para artículos cuyo stock en ML se gestiona manualmente.

### ¿Qué es logística FULL?

**FULL** (Fulfillment) significa que el stock físico está en un depósito de MercadoLibre, no en el local. ML gestiona el envío directamente. Caddis lleva un seguimiento separado de este stock.

### ¿Qué es "Es Promo" en la grilla?

Cuando el SKU de una publicación corresponde a una **promoción de artículos** de Caddis (definida en ABM Promos), el stock se calcula sumando el stock de todos los artículos incluidos en esa promo. La columna muestra `SI` para identificarlo.

### Columna Error

La columna **Error** muestra el último error registrado en la sincronización de precio o stock de esa publicación:

| Mensaje | Qué significa |
|---|---|
| `Falta relacionar SKU con Caddis [código]` | El SKU de ML no existe como artículo ni como promo en Caddis |
| `Precios: [detalle]` | Error al enviar precio a ML (ej: precio inválido, publicación no modificable) |
| `Stock: [detalle]` | Error al enviar stock a ML (ej: ítem cerrado, token vencido) |

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| No aparecen publicaciones | No se seleccionó un USUARIO | Elegí una cuenta ML en el campo USUARIO |
| Stock Disponible en negativo | Stock Seguridad mayor al stock real | Revisá el stock de seguridad del artículo o reponé stock |
| Columna Error: "Falta relacionar SKU" | El SKU de la publicación no existe en Caddis | Crear el artículo en Caddis con ese código o corregir el SKU en ML |
| Precio no se actualiza en ML | Token de ML vencido | Reconectá la cuenta ML desde el módulo de conexión |
| "El proceso ya se encuentra corriendo" | Hay otro proceso activo del mismo tipo | Esperá a que termine el proceso anterior |
| El precio nuevo es rechazado | Es menor al 70% del precio actual | Revisar si el precio es correcto; si lo es, modificarlo en etapas intermedias |

---

## Preguntas frecuentes

**¿Con qué frecuencia debo actualizar publicaciones?**
El proceso de actualización se puede programar automáticamente (vía cron del servidor). En uso manual, conviene correrlo cuando se realizan cambios masivos de precios o cuando se agregan nuevas publicaciones directamente en ML.

**¿El Stock Disponible se envía automáticamente a ML?**
Sí, existe un proceso automático (cron) que sincroniza el stock periódicamente. El botón **Actualizar Stock Masivamente** es para forzar una actualización inmediata fuera del ciclo automático.

**¿Puedo modificar el precio de solo una publicación?**
Sí. Usá la **edición directa en la columna Precio Venta MLibre** de la grilla para modificar una publicación puntual.

**¿Qué diferencia hay entre "Stock MLibre" y "Stock Disponible"?**
- **Stock MLibre**: lo que actualmente está publicado en ML (el dato viene de la API de ML).
- **Stock Disponible**: lo que Caddis calcula que *debería* estar en ML según el inventario interno.

Si difieren, hay que correr "Actualizar Stock Masivamente" para sincronizarlos.

**¿Por qué algunas publicaciones de catálogo ML aparecen con la columna MLibre Full en rojo?**
Las publicaciones de catálogo (`CATALOGO = SI`) muestran esa columna con resaltado diferente. Es solo visual, no indica un error.

**¿Qué pasa si cierro la ventana mientras corre un proceso?**
Los procesos de Actualizar Publicaciones y Actualizar Stock corren en **segundo plano** en el servidor. Podés cerrar la ventana o navegar a otra pantalla sin interrumpirlos.

---

## Referencia rápida de filtros

| Campo | Tipo | Descripción |
|---|---|---|
| USUARIO | Lista | Cuenta ML vendedora (obligatorio para filtrar) |
| ESTADO | Lista | Estado de la publicación en ML |
| LOGISTICA | Lista | FULL o estándar |
| EXCEPTUADOS | Lista | SI/NO según excepción de stock |
| CATALOGO | Lista | SI/NO según tipo de publicación |
| BULTOS | Lista | Cantidad de unidades por venta |
| MARCA | Buscador | Marca del artículo en Caddis |
| ITEM | Texto | ID de publicación ML |
| SKU | Texto | Código de artículo, promo o kit en Caddis |

---

> 📖 Para aprender a publicar nuevos artículos en MercadoLibre desde Caddis, consultá [**Publicar Artículo en ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicar.pdf).
> 📖 Para gestionar las ventas y facturas de MercadoLibre, consultá [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
