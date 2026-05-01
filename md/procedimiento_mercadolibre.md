# Procedimiento: Integración Caddis — MercadoLibre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Operadores y administradores que gestionan ventas de MercadoLibre desde Caddis

---

## ¿De qué trata este procedimiento?

Este documento describe el flujo completo de trabajo para operar la integración entre Caddis y MercadoLibre: desde la configuración inicial de la cuenta hasta la facturación, el despacho y la gestión post-venta.

La integración permite que Caddis y ML estén sincronizados en cuanto a **stock**, **precios**, **ventas** y **comprobantes fiscales**, sin necesidad de operar en el portal de ML para las tareas diarias.

---

## Circuito completo

```
[1. CONFIGURACIÓN]         Alta de cuenta en Caddis → Vincular con ML via API → Configurar listas de precios
         │
         ▼
[2. PUBLICACIONES]         Actualizar publicaciones desde ML → Controlar stock y precios
         │
         ▼
[3. VENTAS DIARIAS]        Actualizar ventas → Emitir remitos
         │
         ▼
[4. PREPARACIÓN ENVÍO]     Preparar items → Armar paquetes → Imprimir etiquetas
         │
         ▼
[5. FACTURACIÓN]           Facturar masivamente → Subir facturas a ML
         │
         ▼
[6. COBROS Y POST-VENTA]   Controlar cobros → Gestionar mensajes y reclamos
```

---

## Paso 1: Configuración inicial (una sola vez)

### 1.1 Dar de alta la cuenta en Caddis

Antes de vincular la API, la cuenta de MercadoLibre debe ser creada en Caddis junto con los depósitos desde donde se operará.

**Pantalla:** [**TV Accesos**](https://ayuda.caddis.com.ar/instructivos/07_TV_Accesos.pdf)
**Menú:** E-Commerce → TV Accesos

<img src="imagenes/procedimiento_ml_acceso.png" style="width:auto; height:auto; max-width:100%; max-height:500px; display:block; margin:0 auto;">

| Paso | Acción |
|---|---|
| 1 | Ir a **TV Accesos** |
| 2 | Hacer click en el botón **Crear acceso** |
| 3 | En el campo **TIENDA** seleccionar **MercadoLibre** |
| 4 | En **NICKNAME** ingresar el nombre de usuario de la cuenta en MercadoLibre |
| 5 | En los campos **Depósito 1**, **Depósito 2**, etc., seleccionar los depósitos (puntos de venta) desde donde se atenderán los pedidos de esa cuenta |
| 6 | Hacer click en **Guardar** |

#### Depósitos y prioridad de stock

Se pueden asociar **múltiples depósitos** a una misma cuenta de MercadoLibre. El sistema consultará el stock disponible en cada depósito siguiendo el **orden en que fueron ingresados** (Depósito 1 primero, Depósito 2 segundo, etc.).

> ℹ️ Esto permite, por ejemplo, atender pedidos de ML desde el depósito central y, si no hay stock allí, utilizar el stock de una sucursal secundaria como respaldo, según el orden configurado.

---

### 1.2 Vincular la cuenta de MercadoLibre con la API

Antes de operar, el administrador del sistema debe vincular cada cuenta de ML con Caddis.

**Pantalla:** [**ML Login**](https://ayuda.caddis.com.ar/instructivos/06_ML_Login.pdf)

<img src="imagenes/procedimiento_ml_login.png" style="width:auto; height:auto; max-width:100%; max-height:500px; display:block; margin:0 auto;">
**Menú:** Mercado Libre → ML Login

| Paso | Acción |
|---|---|
| 1 | Ir a **ML Login** |
| 2 | En la sección **Cuentas configuradas**, hacer click en **Integrar cuenta** |
| 3 | El sistema abre la página de autorización de MercadoLibre en el navegador |
| 4 | Iniciar sesión con las credenciales del vendedor en ML |
| 5 | Hacer click en **Autorizar** para otorgar acceso a la aplicación Caddis |
| 6 | ML redirige de vuelta a Caddis; la cuenta queda en la sección **Cuentas integradas** |

> ⚠️ El token de ML tiene vigencia limitada. Si vence, la sincronización deja de funcionar. En ese caso repetir el proceso de integración. La cuenta sigue configurada; solo hay que volver a autorizar.

---

### 1.3 Configurar listas de precios por tipo de publicación

Cada tipo de publicación de ML (Premium, Clásica, Gratuita) puede tener asignada una lista de precios distinta de Caddis. Esta configuración determina qué precio calcula Caddis para enviar a ML.

**Pantalla:** [**ML Listas de Precios**](https://ayuda.caddis.com.ar/instructivos/06_ML_Listas_Precios.pdf)
**Menú:** Mercado Libre → ML Listas Precios

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** ML |
| 2 | Ver la grilla con los tipos de publicación y sus listas asignadas |
| 3 | Seleccionar el tipo a modificar y hacer click en **Modificar** |
| 4 | Asignar la lista de precios de Caddis correspondiente (MarketPlace y/o M-Shop) |
| 5 | Guardar los cambios |

> ℹ️ Si no se configura esta pantalla, el sistema no podrá calcular ni enviar precios a ML automáticamente.

---

## Paso 2: Gestión de publicaciones

### 2.1 Actualizar publicaciones desde ML

**Pantalla:** [**ML Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicaciones.pdf)
**Menú:** Mercado Libre → ML Publicaciones

En condiciones normales **no es necesario presionar el botón "Actualizar Publicaciones"** manualmente. El sistema mantiene las publicaciones sincronizadas mediante dos procesos automáticos:

| Proceso | Descripción |
|---|---|
| **Webhook** | Cada vez que una publicación sufre una modificación en ML (precio, stock, estado, etc.), ML notifica a Caddis en tiempo real y el registro se actualiza de inmediato. |
| **Normalización periódica** | Cada 6 horas el sistema recorre todas las publicaciones de la cuenta y las normaliza, corrigiendo cualquier diferencia que pudiera haber escapado al webhook. |

El botón **Actualizar Publicaciones** está disponible para forzar una actualización inmediata en situaciones excepcionales: por ejemplo, si se realizaron cambios masivos directamente desde el portal de ML y no se quiere esperar al ciclo automático.

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** ML |
| 2 | Seleccionar el **ESTADO** de publicaciones a actualizar (ej: `Activa`) |
| 3 | Hacer click en **Actualizar Publicaciones** y confirmar |
| 4 | El proceso corre en segundo plano; esperar que finalice antes de continuar |

---

### 2.2 Controlar el stock disponible

La grilla de ML Publicaciones muestra, para cada publicación, el stock calculado por Caddis que debería estar en ML:

```
Stock Disponible = (Stock Caddis − Stock Seguridad − Remitos Pendientes) ÷ Cantidad por Bulto
```

| Columna | Qué indica |
|---|---|
| **Stock Disponible** | Lo que Caddis calcula que debería estar publicado en ML |
| **Stock MLibre** | Lo que actualmente está en ML (dato de la API) |
| **Error** | Si hay un problema de sincronización para esa publicación |

#### Remitos pendientes

Los **Remitos Pendientes** en la fórmula son ventas de ML para las cuales, por algún motivo, no se pudo emitir el remito de salida (por ejemplo, un error en el proceso de emisión). Aunque el remito no fue generado, el sistema descuenta esas unidades del stock disponible de forma preventiva, evitando así que se vuelva a vender un artículo que ya fue comprometido en una venta anterior (**prevención de sobreventas**).

> ℹ️ Si la columna **Remitos Pendientes** muestra un valor alto, conviene revisar las ventas sin remito en **ML Ventas** y ejecutar **Emitir Remitos** para normalizarlas.

Si los valores de Stock Disponible y Stock MLibre difieren, ejecutar **Actualizar Stock Masivamente** para sincronizar.

> ℹ️ Existe un proceso automático (cron del servidor) que sincroniza el stock periódicamente. El botón es para forzar una actualización inmediata.

---

### 2.3 Controlar y actualizar precios

**Pantalla:** [**ML Precios**](https://ayuda.caddis.com.ar/instructivos/06_ML_Precios.pdf)
**Menú:** Mercado Libre → ML Precios

La pantalla muestra el precio actual en ML comparado con el precio calculado por Caddis, con un semáforo visual:

| Color | Significado |
|---|---|
| 🟢 Verde | El precio de ML coincide con el de Caddis |
| 🔴 Rojo | Hay diferencia — conviene actualizar |

Para actualizar los precios de todas las publicaciones:

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** ML |
| 2 | Aplicar filtros opcionales (MARCA, ITEM, SKU) para limitar el alcance |
| 3 | Hacer click en **Actualizar Precios Masivamente** y confirmar |

> ⚠️ Solo se actualizan las publicaciones que **NO** estén marcadas como exceptuadas.

#### Control de variación máxima de precio

Antes de enviar un cambio de precio a ML, el sistema verifica que la diferencia entre el precio actual en ML y el nuevo precio de Caddis no supere el porcentaje configurado como **Variación máxima de precios** en [**TV Accesos**](https://ayuda.caddis.com.ar/instructivos/07_TV_Accesos.pdf). Si la diferencia supera ese umbral, el sistema **no ejecuta la solicitud de modificación** a ML para esa publicación.

Este control existe para proteger contra errores de carga accidentales — por ejemplo, ingresar una coma en lugar de un punto en un importe, lo que podría resultar en un precio extremadamente diferente al real.

> ℹ️ Si un precio legítimamente cambió en forma significativa y el sistema no lo está actualizando, verificar que el porcentaje de variación máxima configurado en TV Accesos sea suficiente para cubrir ese cambio.

---

## Paso 3: Actualizar ventas y emitir remitos

**Pantalla:** [**ML Ventas**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf)
**Menú:** Mercado Libre → ML Ventas

En condiciones normales **no es necesario intervenir manualmente** en este paso. El sistema ejecuta automáticamente cada **1 minuto** un proceso que descarga las ventas nuevas desde ML y emite los remitos correspondientes.

Este proceso automático cubre ventas con hasta **7 días de antigüedad**. Si una venta tiene mayor antigüedad y aún no tiene remito, deberá forzarse manualmente usando el botón **Emitir Remitos** (ver sección 3.2).

Si por algún motivo un remito no pudo emitirse, la venta aparecerá **resaltada en rojo** en la grilla de ML Ventas y la última columna (**Error**) mostrará el detalle del problema que impidió la emisión.

> ⚠️ **Requisito previo para facturar:** la venta debe tener remito antes de poder generar la factura. Ante cualquier venta en rojo, resolver el error indicado antes de continuar con la facturación.

### 3.1 Actualizar ventas manualmente (uso excepcional)

El botón **Actualizar Ventas** está disponible para forzar una sincronización inmediata fuera del ciclo automático.

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** ML |
| 2 | Completar **DESDE** y **HASTA** con el período deseado |
| 3 | Hacer click en **Actualizar Ventas** y confirmar |
| 4 | El proceso corre en segundo plano |

---

### 3.2 Emitir remitos manualmente (uso excepcional)

El botón **Emitir Remitos** permite reintentar la emisión de remitos pendientes en forma manual.

| Paso | Acción |
|---|---|
| 1 | En ML Ventas, seleccionar el **USUARIO** y el período (máximo 31 días) |
| 2 | Hacer click en **Emitir Remitos** y confirmar |
| 3 | El proceso corre en segundo plano |

---

## Paso 4: Preparación y despacho de envíos

### 4.1 Identificar pedidos a preparar

**Pantalla:** [**ML Preparar Ítems**](https://ayuda.caddis.com.ar/instructivos/06_ML_Preparar_Items.pdf)
**Menú:** Mercado Libre → ML Preparar Items

Usar los **accesos rápidos** para filtrar ventas según su etapa:

| Botón rápido | Descripción |
|---|---|
| **Para la colecta** (Preparar) | Envíos por colecta con etiqueta lista para imprimir |
| **Mercado Envíos Flex** (Preparar) | Envíos Flex con etiqueta lista para imprimir |
| **Acordar con el comprador** | Envíos que requieren coordinar la entrega directamente |
| **Para la colecta** (Despachar) | Envíos esperando el paso del correo |
| **Mercado Envíos Flex** (Despachar) | Envíos Flex con etiqueta ya impresa, listos para llevar |

---

### 4.2 Armar los paquetes físicos

**Pantalla:** [**ML Armar Envíos**](https://ayuda.caddis.com.ar/instructivos/06_ML_Armar_Envios.pdf)
**Menú:** Mercado Libre → ML Armar Envios

| Paso | Acción |
|---|---|
| 1 | Ingresar el número de **REMITO** de la venta y presionar Enter |
| 2 | Para cada artículo: ingresar el código (o escanear), el NSE si tiene número de serie, y la cantidad |
| 3 | Hacer click en **Ingresar** para agregar al paquete |
| 4 | El paquete armado aparece en **Envíos armados** |
| 5 | Desde allí imprimir la **Etiqueta** cuando el paquete esté listo para despachar |

> ⚠️ Imprimir la etiqueta modifica el estado en ML y solicita el retiro del paquete. Solo hacerlo cuando el paquete esté físicamente armado.

---

### 4.3 Imprimir etiquetas

Para imprimir etiquetas sin pasar por ML Armar Envíos (por ejemplo, ventas FULL que no requieren armado físico):

**Pantalla:** [**ML Etiquetas**](https://ayuda.caddis.com.ar/instructivos/06_ML_Etiquetas.pdf)
**Menú:** Mercado Libre → ML Etiquetas

| Paso | Acción |
|---|---|
| 1 | Seleccionar **USUARIO** y rango de fechas |
| 2 | Hacer click en **Buscar** |
| 3 | Seleccionar la/s venta/s a imprimir |
| 4 | Hacer click en **Etiqueta** y confirmar |

También se puede imprimir la etiqueta directamente desde **ML Ventas** seleccionando la fila y haciendo click en el botón **Etiqueta**.

---

## Paso 5: Facturación

### 5.1 Facturación masiva (recomendado para el día a día)

Emite las facturas de un lote de ventas en una sola operación.

**Pantalla:** [**ML Facturación Masiva**](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion_Masiva.pdf)
**Menú:** Mercado Libre → ML Facturacion Masiva

| Paso | Acción |
|---|---|
| 1 | Seleccionar **USUARIO**, **DEPOSITO**, **VENDEDOR** |
| 2 | Completar **DESDE** y **HASTA** |
| 3 | Seleccionar el **TIPO FC** de comprobante (EA, EB, EC, A, B) |
| 4 | Verificar la **FECHA** del comprobante |
| 5 | Hacer click en **Buscar** para cargar las ventas a facturar |
| 6 | Revisar la grilla; marcar las ventas con el checkbox (o seleccionar todas) |
| 7 | Hacer click en **Facturar** y confirmar |
| 8 | Revisar la columna **Error** para detectar ventas que no pudieron facturarse |

> ℹ️ Solo se facturan ventas que ya tienen remito y no tienen factura emitida. Las que fallaron se pueden reintentar de forma individual desde **ML Facturación**.

---

### 5.2 Facturación individual (para casos especiales)

Para facturar una venta puntual o corregir una que falló en la masiva:

**Pantalla:** [**ML Facturación**](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion.pdf)
**Acceso:** ML Ventas → seleccionar la venta → botón Facturar

| Paso | Acción |
|---|---|
| 1 | Acceder a ML Ventas y seleccionar la venta |
| 2 | Hacer click en **Facturar** |
| 3 | Usar el botón **Buscar Venta** para cargar los datos |
| 4 | Verificar **PDV**, **VENDEDOR**, **CLIENTE**, **IVA** y **TIPO** de comprobante |
| 5 | Hacer click en **Guardar/Emitir** |

---

### 5.3 Subir facturas a MercadoLibre

Una vez emitida la factura, debe subirse al portal de ML para que el comprador la reciba.

**Pantalla:** [**ML Ventas**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf)

| Paso | Acción |
|---|---|
| 1 | En ML Ventas, filtrar con **FACTURAS = EMITIDAS** |
| 2 | Seleccionar la venta cuya factura se quiere subir |
| 3 | Hacer click en **Aprobar** y confirmar |
| 4 | La columna **Factura Subida** cambia a `SI` cuando el proceso es exitoso |

> ℹ️ Solo se pueden subir facturas de tipo **EA, EB o EC** (electrónicas). Si el tipo es diferente, el sistema avisa para control manual.

---

## Paso 6: Cobros y post-venta

### 6.1 Controlar cobros

**Pantalla:** [**ML Cobros**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas_Cobros.pdf)
**Menú:** Mercado Libre → ML Cobros

Permite consultar todos los cobros registrados en ML: pagos regulares, suscripciones y transferencias. Para actualizar la información:

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** ML y el período |
| 2 | Hacer click en **Actualizar Cobros** y confirmar |
| 3 | Revisar la grilla con el detalle de cada cobro |

---

### 6.2 Gestionar reclamos

**Pantalla:** [**ML Reclamos**](https://ayuda.caddis.com.ar/instructivos/06_ML_Reclamos.pdf)
**Menú:** Mercado Libre → ML Reclamos

Muestra todos los reclamos activos y resueltos. Prestar especial atención a:

| Columna | Qué controlar |
|---|---|
| **Afecta Rep.** | `SI` = reclamos que impactan la reputación del vendedor — resolver con prioridad |
| **Accion Oblig.** | Acción que ML requiere del vendedor |
| **Acc. Fecha Lím.** | Fecha límite para tomar la acción — si vence, ML puede resolver en favor del comprador |

> ℹ️ Caddis solo muestra la información de los reclamos. Para responderlos, acceder directamente al portal de MercadoLibre.

---

---

## Resumen del flujo diario

| Tarea | Pantalla | Cuándo |
|---|---|---|
| Actualizar ventas | ML Ventas | Al inicio del día o varias veces al día |
| Emitir remitos | ML Ventas | Luego de actualizar ventas |
| Preparar y despachar pedidos | ML Preparar Items / ML Armar Envíos / ML Etiquetas | A medida que ingresan ventas |
| Facturar ventas | ML Facturación Masiva | Una o dos veces por día |
| Subir facturas a ML | ML Ventas (Aprobar) | Luego de facturar |
| Actualizar stock en ML | ML Publicaciones | Luego de recibir mercadería o procesar ventas |
| Controlar cobros | ML Cobros | Según necesidad contable |
| Monitorear reclamos | ML Reclamos | Diariamente — atender los que afectan reputación |

---

## Acciones automáticas del sistema (cron del servidor)

El servidor puede tener configurados procesos automáticos que corren sin intervención manual:

| Proceso automático | Descripción |
|---|---|
| Sincronización de stock | Envía el stock calculado por Caddis a todas las publicaciones activas periódicamente |
| Actualización de ventas | Baja ventas nuevas desde la API de ML en intervalos regulares |

> ℹ️ Estos procesos automáticos no reemplazan las actualizaciones manuales cuando se necesita información inmediata. Usá los botones de proceso para forzar una sincronización fuera del ciclo automático.

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa probable | Solución |
|---|---|---|
| Las ventas no se sincronizan | Token de ML vencido | Ir a ML Login → Desvincular y volver a integrar la cuenta |
| Publicación con `Error: Falta relacionar SKU` | El SKU de ML no existe en Caddis | Crear el artículo en Caddis con ese código o corregir el SKU en ML |
| El precio no se actualiza en ML | Token vencido o publicación exceptuada | Renovar el token; verificar si la publicación está marcada como exceptuada |
| "Solicitar máximo 31 días" al emitir remitos | El rango de fechas supera 31 días | Acotar el período en DESDE y HASTA |
| Venta sin remito al intentar facturar | Los remitos no fueron emitidos aún | Ejecutar **Emitir Remitos** desde ML Ventas primero |
| Error de facturación masiva en una venta | Cliente sin CUIT/DNI o tipo de factura incorrecto | Corregir datos del cliente; reintentar factura individual desde ML Facturación |
| Factura no se puede subir a ML | Tipo de comprobante no es EA/EB/EC | Emitir factura electrónica; los talonarios manuales no se suben automáticamente |

---

## Pantallas del módulo Mercado Libre

| # | Pantalla | Descripción |
|---|---|---|
| 6.01 | [ML Login](https://ayuda.caddis.com.ar/instructivos/06_ML_Login.pdf) | Vinculación de cuentas ML con Caddis |
| 6.02 | [ML Publicaciones](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicaciones.pdf) | Panel central de publicaciones (stock, precio, estado) |
| 6.03 | [ML Editar Items](https://ayuda.caddis.com.ar/instructivos/06_ML_Editar_Items.pdf) | Edición de datos de publicaciones |
| 6.04 | [ML Preparar Items](https://ayuda.caddis.com.ar/instructivos/06_ML_Preparar_Items.pdf) | Gestión operativa de pedidos a preparar y despachar |
| 6.05 | [ML Empaques](https://ayuda.caddis.com.ar/instructivos/06_ML_Empaques.pdf) | Configuración de empaques de envío |
| 6.06 | [ML Precios](https://ayuda.caddis.com.ar/instructivos/06_ML_Precios.pdf) | Visualización y actualización masiva de precios |
| 6.07 | [ML Promociones](https://ayuda.caddis.com.ar/instructivos/06_ML_Promociones.pdf) | Gestión de promociones de precio en ML |
| 6.08 | [ML Ventas](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf) | Panel completo de ventas (remitos, etiquetas, facturas) |
| 6.09 | [ML Ventas Consulta](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas_Consulta.pdf) | Consulta de detalle de ventas individuales |
| 6.10 | [ML Cobros](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas_Cobros.pdf) | Consulta y gestión de cobros |
| 6.11 | [ML Facturación](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion.pdf) | Facturación individual de una venta |
| 6.12 | [ML Facturación Masiva](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion_Masiva.pdf) | Facturación masiva de ventas del período |
| 6.13 | [ML Armar Envíos](https://ayuda.caddis.com.ar/instructivos/06_ML_Armar_Envios.pdf) | Armado físico de paquetes con NSE |
| 6.14 | [ML Etiquetas](https://ayuda.caddis.com.ar/instructivos/06_ML_Etiquetas.pdf) | Impresión de etiquetas de envío |
| 6.15 | [ML Mensajes](https://ayuda.caddis.com.ar/instructivos/06_ML_Mensajes.pdf) | Mensajería con compradores |
| 6.16 | [ML Suscripciones](https://ayuda.caddis.com.ar/instructivos/06_ML_Suscripciones.pdf) | Gestión de suscripciones periódicas |
| 6.17 | [ML Reclamos](https://ayuda.caddis.com.ar/instructivos/06_ML_Reclamos.pdf) | Consulta y seguimiento de reclamos |
| 6.18 | [ML Precios Mayoristas](https://ayuda.caddis.com.ar/instructivos/06_ML_Precios_Mayoristas.pdf) | Gestión de precios para canal mayorista |
| 6.23 | [ML Listas de Precios](https://ayuda.caddis.com.ar/instructivos/06_ML_Listas_Precios.pdf) | Configuración de listas de precios por tipo de publicación |

---
