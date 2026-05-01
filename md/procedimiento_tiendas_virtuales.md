# Procedimiento: Integración Caddis — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Operadores y administradores que gestionan ventas de tiendas virtuales desde Caddis

---

## ¿De qué trata este procedimiento?

Este documento describe el flujo completo de trabajo para operar la integración entre Caddis y las tiendas virtuales: desde la configuración inicial de la cuenta hasta la facturación y el despacho de envíos.

Las tiendas virtuales soportadas incluyen **TiendaNube**, **Shopify**, **WooCommerce**, **VTEX** y **MercadoLibre Global Selling**. La integración permite que Caddis y la tienda estén sincronizados en cuanto a **stock**, **precios**, **publicaciones** y **ventas**, sin necesidad de operar en el panel de la tienda para las tareas diarias.

> ℹ️ Para MercadoLibre Argentina (cuenta local) existe un procedimiento específico. Consultá [**Integración Caddis — MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/procedimiento_mercadolibre.pdf).

---

## Circuito completo

```
[1. CONFIGURACIÓN]         Alta de cuenta → Depósitos virtuales → Vincular API → Listas de precios
         │
         ▼
[2. PUBLICACIONES]         Publicar artículos → Controlar stock y precios → Excepciones
         │
         ▼
[3. VENTAS DIARIAS]        Actualizar ventas → Emitir remitos
         │
         ▼
[4. PREPARACIÓN ENVÍO]     Preparar ítems → Armar paquetes → Entregar al transporte
         │
         ▼
[5. FACTURACIÓN]           Facturar masivamente → Facturar individualmente → Subir factura
```

---

## Paso 1: Configuración inicial (una sola vez)

### 1.1 Dar de alta la cuenta en Caddis

Antes de operar, la cuenta de la tienda virtual debe ser creada en Caddis.

**Pantalla:** [**TV Accesos**](https://ayuda.caddis.com.ar/instructivos/07_TV_Accesos.pdf)
**Menú:** Tiendas Virtuales → TV Accesos

<img src="imagenes/procedimiento_tv_acceso.png" style="width:auto; height:auto; max-width:100%; max-height:500px; display:block; margin:0 auto;">

| Paso | Acción |
|---|---|
| 1 | Ir a **TV Accesos** |
| 2 | Hacer click en el botón **Crear acceso** |
| 3 | En el campo **TIENDA** seleccionar el tipo de tienda (TiendaNube, Shopify, WooCommerce, etc.) |
| 4 | Completar los datos de acceso requeridos por la tienda seleccionada (URL, nickname, token, etc.) |
| 5 | Configurar los parámetros específicos de la tienda (variación máxima de precios, etc.) |
| 6 | Hacer click en **Guardar** |

> ℹ️ Shopify solo admite una cuenta por empresa. Si se intenta configurar más de una, el sistema lo avisa.

---

### 1.2 Configurar los depósitos virtuales

Cada cuenta de tienda virtual debe tener asociados los depósitos (puntos de venta) desde donde se atenderán los pedidos.

**Pantalla:** [**TV Depósitos Virtuales**](https://ayuda.caddis.com.ar/instructivos/07_TV_Depositos_Virtuales.pdf)
**Menú:** Tiendas Virtuales → TV Depósitos Virtuales

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Agregar los depósitos físicos (PDV) en el **orden de prioridad** deseado |
| 3 | Configurar **Remito Automático** (SI/NO): si está activo, el remito se emite automáticamente al registrar la venta |
| 4 | Configurar **Altera Stock** (SI/NO): si está activo, el remito afecta el stock del depósito |
| 5 | Guardar los cambios |

#### Prioridad de depósitos

El sistema consulta el stock disponible siguiendo el **orden en que fueron ingresados** los depósitos (prioridad 1 primero, prioridad 2 segundo, etc.). Esto permite, por ejemplo, atender pedidos desde el depósito central y, si no hay stock allí, utilizar el de una sucursal secundaria.

---

### 1.3 Vincular la cuenta con la API de la tienda

Cada tienda virtual requiere una autorización específica para conectarse con Caddis. El proceso varía según la plataforma:

#### TiendaNube

**Pantalla:** [**TV TiendaNube Login**](https://ayuda.caddis.com.ar/instructivos/07_TV_TiendaNube_Login.pdf)
**Menú:** Tiendas Virtuales → TV Tiendanube Login

| Paso | Acción |
|---|---|
| 1 | Ir a **TV TiendaNube Login** |
| 2 | Localizar la cuenta en la sección **Cuentas habilitadas para integración** |
| 3 | Hacer click en **Integrar** |
| 4 | Se abre una ventana popup con el login de TiendaNube |
| 5 | Ingresar las credenciales de administrador y autorizar |
| 6 | La cuenta pasa a la sección **Cuentas integradas** |

#### Shopify

**Pantalla:** [**TV Shopify Login**](https://ayuda.caddis.com.ar/instructivos/07_TV_Shopify_Login.pdf)
**Menú:** Tiendas Virtuales → TV Shopify Login

| Paso | Acción |
|---|---|
| 1 | Ir a **TV Shopify Login** |
| 2 | Hacer click en **Integrar** |
| 3 | Se abre una ventana popup de Shopify |
| 4 | Ingresar las credenciales de administrador y autorizar |
| 5 | La cuenta pasa a la sección **Cuentas integradas** |

#### MercadoLibre Global Selling

**Pantalla:** [**TV ML GS Login**](https://ayuda.caddis.com.ar/instructivos/07_TV_MercadoLibre_GS_Login.pdf)
**Menú:** Tiendas Virtuales → TV Mercado Libre GS Login

| Paso | Acción |
|---|---|
| 1 | Ir a **TV ML GS Login** |
| 2 | Localizar la cuenta en la sección **Cuentas habilitadas para integración** |
| 3 | Hacer click en **Integrar** |
| 4 | Se abre una ventana popup con el login de MercadoLibre |
| 5 | Ingresar las credenciales de la cuenta ML y autorizar |
| 6 | Hacer click en **Refrescar pantalla** si la cuenta no aparece inmediatamente |

> ⚠️ Los tokens de autorización tienen vigencia limitada. Si vence, la sincronización deja de funcionar. En ese caso, ir a la pantalla de login correspondiente, desvincular y volver a integrar la cuenta.

---

### 1.4 Configurar listas de precios

Permite asignar qué lista de precios de Caddis se usará para calcular el precio publicado en cada cuenta de tienda virtual.

**Pantalla:** [**TV Listas de Precios**](https://ayuda.caddis.com.ar/instructivos/07_TV_Listas_de_Precios.pdf)
**Menú:** Tiendas Virtuales → TV Listas de Precios

> ℹ️ Esta configuración aplica para TiendaNube, Shopify, WooCommerce y similares. MercadoLibre y MercadoPago tienen su propia configuración de listas en el Módulo 6.

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** de la tienda |
| 2 | Asignar la lista de precios de Caddis correspondiente |
| 3 | Guardar los cambios |

---

## Paso 2: Gestión de publicaciones

### 2.1 Publicar artículos en la tienda

La primera vez que un artículo se publica en una tienda virtual, debe hacerse en forma individual o masiva desde las pantallas de publicación.

#### Publicación masiva

**Pantalla:** [**TV Publicar**](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar.pdf)
**Menú:** Tiendas Virtuales → TV Publicar

Permite seleccionar uno o varios artículos del catálogo de Caddis y publicarlos en la tienda en una sola operación.

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Buscar y seleccionar los artículos a publicar (filtros por marca, grupo, tipo, etc.) |
| 3 | Hacer click en **Publicar** |

#### Publicación individual

**Pantalla:** [**TV Publicar Artículo**](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar_Articulo.pdf)
**Menú:** Tiendas Virtuales → TV Publicar Articulo

Permite configurar todos los parámetros de publicación de un artículo (título, descripción, EAN, tipo, condición, logística, garantía, categoría, atributos, precio y stock) antes de publicarlo.

| Paso | Acción |
|---|---|
| 1 | Buscar el artículo por SKU o nombre |
| 2 | Seleccionar el **USUARIO** de la tienda |
| 3 | Completar **TITULO WEB** y **DESCRIPCION WEB** |
| 4 | Para ML: seleccionar TIPO, CONDICION, LOGISTICA, GARANTIA y buscar la CATEGORIA |
| 5 | Completar los atributos obligatorios (indicados con ⚠️) |
| 6 | Verificar STOCK y PRECIO |
| 7 | Hacer click en **Publicar como ACTIVO** o **Publicar como INACTIVO** |

#### Agregar variantes a un producto existente

**Pantalla:** [**TV Publicar Variante**](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar_Variante.pdf)
**Menú:** Tiendas Virtuales → TV Publicar Variante

Cuando un artículo de Caddis debe agregarse como nueva variante de un producto ya publicado (ej: mismo modelo en distinto color), se usa esta pantalla en lugar de crear una publicación nueva.

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** de la tienda |
| 2 | El sistema carga el producto virtual asociado |
| 3 | Buscar el artículo de Caddis a agregar como variante |
| 4 | Verificar stock, dimensiones y fotos |
| 5 | Completar los atributos de la variante (ej: color, capacidad) |
| 6 | Hacer click en **Publicar** |

---

### 2.2 Controlar y actualizar publicaciones

**Pantalla:** [**TV Publicaciones**](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicaciones.pdf)
**Menú:** Tiendas Virtuales → TV Publicaciones

Panel central de seguimiento de todas las publicaciones activas en la tienda. Muestra para cada artículo el stock y precio publicado en la tienda versus el calculado por Caddis.

#### Controlar el stock disponible

La grilla muestra la diferencia entre el stock en la tienda y el stock que Caddis calcula. Si difieren, ejecutar la actualización de stock:

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Revisar la columna de stock disponible versus stock en tienda |
| 3 | Si hay diferencias, hacer click en **Actualizar Stock Masivamente** y confirmar |

#### Controlar y actualizar precios

La grilla también compara el precio publicado en la tienda con el precio calculado por Caddis según la lista configurada. Para actualizar los precios:

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Revisar las diferencias de precio en la grilla |
| 3 | Hacer click en **Actualizar Precios Masivamente** y confirmar |

#### Control de variación máxima de precio

Antes de enviar un cambio de precio a la tienda, el sistema verifica que la diferencia entre el precio actual publicado y el nuevo precio de Caddis no supere el porcentaje configurado como **Variación máxima de precios** en [**TV Accesos**](https://ayuda.caddis.com.ar/instructivos/07_TV_Accesos.pdf). Si la diferencia supera ese umbral, el sistema no ejecuta la solicitud de modificación.

Este control existe para proteger contra errores de carga accidentales — por ejemplo, ingresar una coma en lugar de un punto en un importe.

> ℹ️ Si un precio legítimamente cambió en forma significativa y el sistema no lo actualiza, verificar que el porcentaje de variación máxima configurado en TV Accesos sea suficiente para cubrir ese cambio.

---

### 2.3 Configurar stock de seguridad y excepciones

#### Stock de seguridad

**Pantalla:** [**TV Stock Seguridad**](https://ayuda.caddis.com.ar/instructivos/07_TV_Stock_Seguridad.pdf)
**Menú:** Tiendas Virtuales → TV Stock Seguridad

Permite reservar una cantidad mínima de cada artículo que no se publicará en la tienda virtual. El stock de seguridad se descuenta del stock disponible a la hora de calcular qué cantidad informar a la tienda.

```
Stock publicado = Stock físico − Stock Seguridad − Remitos Pendientes
```

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Ingresar el **SKU** del artículo y la cantidad de **Stock Seguridad** |
| 3 | Hacer click en **Guardar** |
| 4 | También se puede importar masivamente desde un archivo Excel usando el ícono de carga |

#### Excepciones de stock

**Pantalla:** [**TV Stock Excepciones**](https://ayuda.caddis.com.ar/instructivos/07_TV_Stock_Excepciones.pdf)
**Menú:** Tiendas Virtuales → TV Stock Excepciones

Permite suspender temporalmente la sincronización de stock de un artículo específico durante un período determinado. Útil cuando se necesita mantener el stock publicado tal cual está, sin que el proceso automático lo modifique.

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Ingresar el **SKU** del artículo |
| 3 | Completar la **fecha y hora de expiración** de la excepción |
| 4 | Opcionalmente, ingresar una **observación** con el motivo |
| 5 | Hacer click en **Exceptuar** |

> ⚠️ Mientras la excepción esté activa, el sistema no sincronizará el stock de ese artículo. Una vez vencida, la sincronización automática se reanuda.

---

## Paso 3: Actualizar ventas y emitir remitos

**Pantalla:** [**TV Ventas**](https://ayuda.caddis.com.ar/instructivos/07_TV_Ventas.pdf)
**Menú:** Tiendas Virtuales → TV Ventas

El sistema ejecuta automáticamente un proceso periódico que descarga las ventas nuevas desde la tienda virtual y emite los remitos correspondientes. En condiciones normales **no es necesario intervenir manualmente** en este paso.

Si por algún motivo un remito no pudo emitirse, la venta aparecerá en la grilla con indicación de error. Ante cualquier venta con error de remito, resolver el problema antes de continuar con la facturación (el remito es requisito previo para facturar).

### 3.1 Actualizar ventas manualmente (uso excepcional)

Para forzar una sincronización inmediata de ventas fuera del ciclo automático:

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Completar **DESDE** y **HASTA** con el período deseado |
| 3 | Hacer click en **Actualizar Ventas** y confirmar |
| 4 | El proceso corre en segundo plano |

### 3.2 Emitir remitos manualmente (uso excepcional)

Para reintentar la emisión de remitos pendientes:

| Paso | Acción |
|---|---|
| 1 | En TV Ventas, seleccionar la **TIENDA**, el **USUARIO** y el período |
| 2 | Hacer click en **Emitir Remitos** y confirmar |
| 3 | El proceso corre en segundo plano |

### 3.3 Consultar el detalle de una venta

Para ver los datos completos de una venta, corregir datos de facturación o asociar una factura manualmente:

**Pantalla:** [**TV Consultar Venta**](https://ayuda.caddis.com.ar/instructivos/07_TV_Consultar_Venta.pdf)
**Acceso:** TV Ventas → seleccionar la venta → botón **Modificar**

Desde esta ventana se puede editar el SKU de un ítem no identificado, modificar datos fiscales del comprador y ver el estado completo del envío y el reclamo asociado.

### 3.4 Anular un remito

Si un remito fue generado por error, se puede anular desde:

**Pantalla:** [**TV Anular Remito**](https://ayuda.caddis.com.ar/instructivos/07_TV_Anular_Remito.pdf)
**Menú:** Tiendas Virtuales → TV Anular Remito

> ⚠️ La anulación de un remito es irreversible. Verificar el número antes de confirmar. Al anularlo, el stock vuelve al depósito.

---

## Paso 4: Preparación y despacho de envíos

### 4.1 Preparar los ítems del pedido

**Pantalla:** [**TV Preparar Items**](https://ayuda.caddis.com.ar/instructivos/07_TV_Preparar_Items.pdf)
**Menú:** Tiendas Virtuales → TV Preparar Items

Lista los pedidos pendientes de preparación en el depósito. Permite filtrar por zona geográfica o por artículo para organizar el picking.

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Aplicar filtros de zona o artículo si corresponde |
| 3 | Identificar los pedidos a preparar y separar los artículos físicamente |

---

### 4.2 Armar los paquetes físicos

**Pantalla:** [**TV Armar Envíos**](https://ayuda.caddis.com.ar/instructivos/07_TV_Armar_Envios.pdf)
**Menú:** Tiendas Virtuales → TV Armar Envios

| Paso | Acción |
|---|---|
| 1 | Ingresar el número de **REMITO** de la venta y presionar Enter |
| 2 | Para cada artículo: ingresar el código (o escanear), el NSE si tiene número de serie, y la cantidad |
| 3 | Seleccionar el **tipo de transporte** para el envío |
| 4 | Hacer click en **Ingresar** para agregar el artículo al paquete |
| 5 | El paquete armado queda registrado en el sistema |

---

### 4.3 Registrar la entrega al transporte

**Pantalla:** [**TV Entrega a Transporte**](https://ayuda.caddis.com.ar/instructivos/07_TV_Entrega_Transporte.pdf)
**Menú:** Tiendas Virtuales → TV Entrega a Transporte

Registra el momento en que los paquetes son entregados al servicio de transporte. Hay tres modalidades:

| Modalidad | Descripción |
|---|---|
| **CLIENTE** | El comprador retira el paquete personalmente en el local |
| **TRANSPORTE** | El paquete es despachado a través de un servicio de transporte o correo |
| **COLECTA** | El transporte pasa a retirar los paquetes al depósito |

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA** y el **USUARIO** |
| 2 | Seleccionar la modalidad de entrega (CLIENTE / TRANSPORTE / COLECTA) |
| 3 | Seleccionar los envíos a despachar |
| 4 | Confirmar la entrega |

### 4.4 Controlar el estado de los despachos

**Pantalla:** [**TV Control Entrega Transporte**](https://ayuda.caddis.com.ar/instructivos/07_TV_Control_Entrega_Transporte.pdf)
**Menú:** Tiendas Virtuales → TV Control Entrega Transporte

Muestra el historial de envíos entregados al transporte en los últimos 30 días. Permite auditar que cada venta tenga su envío correctamente despachado y detectar ítems pendientes.

---

## Paso 5: Facturación

### 5.1 Facturación masiva (recomendado para el día a día)

Emite las facturas de un lote de ventas en una sola operación.

**Pantalla:** [**TV Facturación Masiva**](https://ayuda.caddis.com.ar/instructivos/07_TV_Facturacion_Masiva.pdf)
**Menú:** Tiendas Virtuales → TV Facturación Masiva

| Paso | Acción |
|---|---|
| 1 | Seleccionar la **TIENDA**, el **USUARIO**, el **DEPOSITO** y el **VENDEDOR** |
| 2 | Completar **DESDE** y **HASTA** con el período a facturar |
| 3 | Seleccionar el **TIPO FC** de comprobante (EA, EB, EC, A, B) |
| 4 | Verificar la **FECHA** del comprobante |
| 5 | Hacer click en **Buscar** para cargar las ventas a facturar |
| 6 | Revisar la grilla; marcar las ventas con el checkbox (o seleccionar todas) |
| 7 | Hacer click en **Facturar** y confirmar |
| 8 | Revisar la columna **Error** para detectar ventas que no pudieron facturarse |

> ℹ️ Solo se facturan ventas que ya tienen remito y no tienen factura emitida.

---

### 5.2 Facturación individual (para casos especiales)

Para facturar una venta puntual o corregir una que falló en la masiva:

**Pantalla:** [**TV Facturar Ventas**](https://ayuda.caddis.com.ar/instructivos/07_TV_Facturar_Ventas.pdf)
**Acceso:** TV Ventas → seleccionar la venta → botón **Facturar**

| Paso | Acción |
|---|---|
| 1 | Acceder a TV Ventas y seleccionar la venta |
| 2 | Hacer click en **Facturar** |
| 3 | Verificar **PDV**, **VENDEDOR**, **CLIENTE**, **IVA** y **TIPO** de comprobante |
| 4 | Hacer click en **Guardar/Emitir** |

---

### 5.3 Subir la factura a la tienda virtual

Una vez emitida la factura electrónica, puede subirse a la tienda para que el comprador la reciba.

**Acceso:** TV Ventas → seleccionar la venta → botón **Subir FC** (o desde TV Consultar Venta, sección **Comprobante asociado**)

> ℹ️ Solo se pueden subir facturas electrónicas (tipos EA, EB o EC). Si el tipo de comprobante es diferente, la factura deberá enviarse al comprador en forma manual.

---

## Resumen del flujo diario

| Tarea | Pantalla | Cuándo |
|---|---|---|
| Actualizar ventas | TV Ventas | Al inicio del día o varias veces al día |
| Emitir remitos | TV Ventas | Luego de actualizar ventas |
| Preparar pedidos | TV Preparar Items | A medida que ingresan ventas |
| Armar paquetes | TV Armar Envíos | Luego de preparar los ítems |
| Entregar al transporte | TV Entrega a Transporte | Al despachar los paquetes |
| Facturar ventas | TV Facturación Masiva | Una o dos veces por día |
| Subir facturas | TV Ventas / TV Consultar Venta | Luego de facturar |
| Controlar publicaciones | TV Publicaciones | Luego de recibir mercadería o procesar ventas |
| Revisar despachos | TV Control Entrega Transporte | Diariamente |

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa probable | Solución |
|---|---|---|
| Las ventas no se sincronizan | Token de la tienda vencido | Ir a la pantalla de login correspondiente (TiendaNube / Shopify / ML GS) → Desvincular y volver a integrar |
| Artículo sin SKU identificado (fondo rojo) | El código del artículo en la tienda no existe en Caddis | Desde TV Consultar Venta, asignar el SKU correcto manualmente |
| El precio no se actualiza en la tienda | Variación máxima de precio superada | Verificar en TV Accesos el porcentaje de variación configurado; si el cambio es legítimo, aumentar el umbral temporalmente |
| Error al emitir remito | Datos de la venta incompletos o artículo sin stock en el depósito | Revisar el error en la columna Error de TV Ventas; corregir el dato y reintentar **Emitir Remitos** |
| Venta sin remito al intentar facturar | El remito no fue emitido | Ejecutar **Emitir Remitos** desde TV Ventas primero |
| Error de facturación masiva en una venta | Cliente sin documento o tipo de factura incorrecto | Corregir datos desde TV Consultar Venta → Datos de facturación; reintentar factura individual |
| Stock publicado no coincide con Caddis | Sincronización automática no completada | Ejecutar **Actualizar Stock Masivamente** desde TV Publicaciones |

---

## Pantallas del módulo Tiendas Virtuales

| # | Pantalla | Descripción |
|---|---|---|
| 7.01 | [TV Accesos](https://ayuda.caddis.com.ar/instructivos/07_TV_Accesos.pdf) | Alta y configuración de cuentas de tiendas virtuales |
| 7.02 | [TV ML GS Login](https://ayuda.caddis.com.ar/instructivos/07_TV_MercadoLibre_GS_Login.pdf) | Vinculación de cuentas ML Global Selling |
| 7.03 | [TV TiendaNube Login](https://ayuda.caddis.com.ar/instructivos/07_TV_TiendaNube_Login.pdf) | Vinculación de cuentas TiendaNube |
| 7.04 | [TV Shopify Login](https://ayuda.caddis.com.ar/instructivos/07_TV_Shopify_Login.pdf) | Vinculación de cuenta Shopify |
| 7.05 | [TV Depósitos Virtuales](https://ayuda.caddis.com.ar/instructivos/07_TV_Depositos_Virtuales.pdf) | Configuración de depósitos físicos por cuenta de tienda |
| 7.06 | [TV Publicaciones](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicaciones.pdf) | Panel de publicaciones: stock, precio y estado por artículo |
| 7.07 | [TV Publicar](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar.pdf) | Publicación masiva de artículos en la tienda |
| 7.08 | [TV Publicar Artículo](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar_Articulo.pdf) | Publicación individual con configuración completa |
| 7.09 | [TV Publicar Variante](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar_Variante.pdf) | Agregar variantes a un producto ya publicado |
| 7.10 | [TV Consultar Venta](https://ayuda.caddis.com.ar/instructivos/07_TV_Consultar_Venta.pdf) | Detalle completo de una venta individual |
| 7.11 | [TV Ventas](https://ayuda.caddis.com.ar/instructivos/07_TV_Ventas.pdf) | Listado de ventas: remitos, etiquetas, facturación |
| 7.12 | [TV Facturar Ventas](https://ayuda.caddis.com.ar/instructivos/07_TV_Facturar_Ventas.pdf) | Facturación individual de una venta |
| 7.13 | [TV Facturación Masiva](https://ayuda.caddis.com.ar/instructivos/07_TV_Facturacion_Masiva.pdf) | Facturación masiva de ventas del período |
| 7.14 | [TV Listas de Precios](https://ayuda.caddis.com.ar/instructivos/07_TV_Listas_de_Precios.pdf) | Asignación de listas de precios por cuenta |
| 7.15 | [TV Stock Seguridad](https://ayuda.caddis.com.ar/instructivos/07_TV_Stock_Seguridad.pdf) | Reserva de stock mínimo por artículo y tienda |
| 7.16 | [TV Preparar Items](https://ayuda.caddis.com.ar/instructivos/07_TV_Preparar_Items.pdf) | Preparación operativa de pedidos en el depósito |
| 7.17 | [TV Control Entrega Transporte](https://ayuda.caddis.com.ar/instructivos/07_TV_Control_Entrega_Transporte.pdf) | Historial de envíos entregados al transporte |
| 7.18 | [TV Anular Remito](https://ayuda.caddis.com.ar/instructivos/07_TV_Anular_Remito.pdf) | Anulación de remitos generados por error |
| 7.19 | [TV Armar Envíos](https://ayuda.caddis.com.ar/instructivos/07_TV_Armar_Envios.pdf) | Armado físico de paquetes con NSE y tipo de transporte |
| 7.20 | [TV Entrega a Transporte](https://ayuda.caddis.com.ar/instructivos/07_TV_Entrega_Transporte.pdf) | Registro de entrega al transporte (cliente/correo/colecta) |
| 7.21 | [TV Stock Excepciones](https://ayuda.caddis.com.ar/instructivos/07_TV_Stock_Excepciones.pdf) | Suspensión temporal de sincronización de stock por artículo |

---
