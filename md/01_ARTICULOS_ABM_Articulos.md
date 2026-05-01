# 1.01. Alta, Baja y Modificación de Artículos

**Ruta de acceso:** Módulo 1 → Artículos → Alta, Baja y Modificación de Artículos

**Artículos → ABM Artículos**

---

## Descripción general de la pantalla

![Pantalla ABM Artículos](imagenes/pantalla_articulos.png)

La pantalla muestra un **formulario central** con todos los campos del artículo, organizado en secciones desplegables. En la parte superior del formulario se encuentran los botones de acción:

| Botón / Control | Descripción |
|---|---|
| **Nuevo** | Limpia el formulario para cargar un artículo nuevo |
| **Guardar** | Graba el artículo actual (nuevo o modificado) |
| **Eliminar** | Elimina el artículo seleccionado |
| **Buscar...** + ícono lupa | Campo para filtrar artículos. Al hacer clic en la lupa, se abre una **ventana emergente** con los resultados de la búsqueda. |
| Ícono Excel | Exporta los resultados de la búsqueda a Excel |

> 💡 La pantalla funciona tanto para **crear** artículos nuevos como para **buscar y editar** artículos existentes. Al ingresar, el formulario está en blanco para crear. Para editar, ingresá el criterio de búsqueda y hacé clic en la **lupa**: se abre una ventana emergente con los resultados. Al seleccionar un artículo, sus datos se cargan en el formulario.

---

## Secciones y campos del formulario

### Datos generales

| Campo | Tipo | Descripción |
|---|---|---|
| **NOMBRE** | Texto (255 car.) | Descripción completa del artículo. Se guarda en mayúsculas automáticamente. Es **obligatorio**. |
| **ESTADO** | Desplegable | Estado del artículo en el catálogo: ACTIVO, INACTIVO, DISCONTINUO o SIN REPOSICION. |
| **SERVICIO** | SI / NO | Indica si el artículo es un servicio (instalación, garantía, etc.). Si es **SI**, el sistema **no controla stock**. |
| **USA NSE** | SI / NO | Si es **SI**, cada unidad del artículo se registra con su propio número de serie (NSE). Aplica a cualquier producto que requiera identificación individual: teléfonos (IMEI), electrodomésticos, equipos de cualquier tipo, etc. |
| **PRECIO LIBRE** | SI / NO | Si es **SI**, el precio puede modificarse al momento de facturar. Útil para artículos con precio variable. |
| **SAP ID** | Texto | Solo visible en entornos Movistar. Código SAP del artículo para la operadora. |

---

### Atributos del artículo

| Campo | Tipo | Descripción |
|---|---|---|
| **PRODUCTO** | Número (solo lectura) | Identificador del **producto** al que pertenece el artículo. Un producto agrupa todas sus variantes. |
| **VARIANTE** | Número (solo lectura) | Identificador único del artículo/variante específica. |
| **CODIGO / SKU** | Texto (20 car.) | Código único del artículo. Fondo rojo en pantalla. Es **obligatorio**. Puede ser ingresado manualmente por el usuario o asignado automáticamente por el sistema según la configuración del Tipo de artículo. |
| **EAN** | Texto (15 car.) | Código de barras estándar (EAN-13 o similar). Permite escaneo con lectora. |
| **MARCA** | Desplegable | Marca del artículo (Apple, Samsung, Motorola, etc.). **Obligatorio.** |
| **MODELO** | Texto (50 car.) | Nombre del modelo. Al completarlo y salir del campo, el sistema busca si ya existe ese modelo y lo vincula automáticamente. |
| **TIPO** | Desplegable | Tipo de artículo (celular, accesorio, servicio, etc.). **Obligatorio.** Al cambiar el tipo, se actualizan los atributos dinámicos disponibles. |
| **GRUPO** | Desplegable | Agrupación comercial del artículo para clasificación interna. |
| **GARANTIA** | Número | Meses de garantía del artículo. |
| **CLASE** | Desplegable | Solo visible en empresas de producción. Clasifica el artículo según su proceso productivo. |
| *Atributos dinámicos* | Desplegable | Aparecen según el TIPO seleccionado. Pueden ser: Color, Tamaño, Capacidad de almacenamiento, etc. Definen la variante. |

> 💡 El botón **Ver Variantes** (junto a PRODUCTO) abre una ventana con todas las variantes asociadas al mismo producto. El botón **BuscarModelo** abre un buscador de modelos existentes filtrado por la marca seleccionada.

---

### Impuestos

| Campo | Tipo | Descripción |
|---|---|---|
| **CONDICION** | Desplegable | Condición frente al IVA: Gravado, No Gravado o Exento. Afecta cómo se calcula el IVA en la factura. |
| **IVA** | Desplegable | Tasa de IVA aplicable (21%, 10.5%, 0%, etc.). Si la condición es No Gravado o Exento, se fuerza a 0. |
| **IMPUESTO INTERNO** | Número | Porcentaje de impuesto interno aplicable al artículo (solo para productos específicos). |
| **MONEDA** | Desplegable | Moneda en que está expresado el precio del artículo. En sistemas multimoneda este campo se oculta y se toma del parámetro global. |

---

### Stock

| Campo | Tipo | Descripción |
|---|---|---|
| **UNIDAD** | Desplegable | Unidad de medida del artículo (Unidad, Par, Caja, etc.). |
| **STOCK REPOSICION** | Número + AUTO/FIJO | Cantidad mínima para reponer. En modo **AUTO** se calcula a partir del promedio mensual de ventas. En modo **FIJO** respeta el valor ingresado. |
| **STOCK SEGURIDAD** | Número | Cantidad reservada que **no se sincroniza** con las tiendas virtuales (MercadoLibre, TiendaNube, etc.). Garantiza stock disponible para venta presencial. |
| **UBICACION** | Texto (20 car.) | Referencia física de la ubicación en el depósito (estante, pasillo, etc.). |

---

### Medidas

| Campo | Unidad | Descripción |
|---|---|---|
| **TAMAÑO** | Texto | Descripción libre del tamaño (ej: "L", "XL", "14\""). |
| **LARGO** | cm | Largo del artículo o su empaque para cálculo logístico. |
| **ANCHO** | cm | Ancho del artículo o su empaque. |
| **ALTO** | cm | Alto del artículo o su empaque. |
| **PESO** | kg | Peso del artículo para cálculo de flete y envíos. |
| **BULTOS** | Número | Cantidad de bultos que contiene el artículo. |

---

### Importe Asegurado / Consignación

| Campo | Descripción |
|---|---|
| **IMPORTE** | Valor declarado del artículo para seguro o para consignación a terceros. |

---

### Comercial

| Campo | Descripción |
|---|---|
| **PUNTOS** | Puntos que acumula el cliente al comprar este artículo (sistema de fidelización). |

---

### Importar artículos masivamente

Permite cargar un archivo Excel con múltiples artículos de una sola vez. La sección IMPORTAR ARTÍCULOS MASIVAMENTE incluye los siguientes elementos:

| Elemento | Descripción |
|---|---|
| **Ícono carpeta** | Abre el explorador de archivos para seleccionar el Excel a importar. |
| **Botón Importar** | Procesa el archivo seleccionado y realiza la importación. |
| **Botón Formato** | Descarga un archivo Excel de ejemplo con las columnas exactas que espera el sistema, con datos reales tomados del catálogo actual. Usarlo como plantilla garantiza el formato correcto. |

> ⚠️ Siempre descargá el **Formato** antes de armar tu Excel de importación. El sistema valida las columnas estrictamente y rechaza filas con datos inválidos.

---

### Web

| Campo | Descripción |
|---|---|
| **TITULO** | Título del artículo para las tiendas virtuales (MercadoLibre, TiendaNube, etc.). Máximo 60 caracteres. |
| **DESCRIPCION** | Descripción detallada del artículo para el canal web. Se muestra en la publicación online. |

---

### Fotos del artículo

En la parte inferior del formulario se muestran las fotos cargadas para el artículo. Cada foto tiene un botón para eliminarla (clic sobre la imagen). Para agregar una foto nueva, clic en el ícono **+**.

- **Tamaño máximo:** 1 MB por foto.
- **Formatos aceptados:** JPG, JPEG, PNG.

---

## Botones y acciones

| Botón / Acción | Descripción |
|---|---|
| **Guardar** | Graba los cambios del artículo. Si el artículo es nuevo, lo crea. Si ya existe, lo modifica. Pide confirmación antes de guardar. |
| **Cancelar** | Descarta los cambios y limpia el formulario. |
| **Eliminar** | Elimina el artículo seleccionado. Pide confirmación. No se puede eliminar si el artículo tiene movimientos de stock o ventas registradas, ni si es un artículo base del sistema. |
| **Buscar** (lupa) | Abre una ventana emergente con los artículos que coinciden con el texto ingresado en el campo Buscar. Al seleccionar uno, carga sus datos en el formulario. |
| **Detalle** (grilla) | Exporta el resultado de la búsqueda a Excel. |
| **Importar** | Carga masivamente artículos desde un archivo Excel. Pide confirmación del formato antes de proceder. |
| **Ver Variantes** | Abre una ventana con todas las variantes del producto seleccionado. |
| **BuscarModelo** | Abre un buscador de modelos existentes filtrado por la marca seleccionada. |

---

## Conceptos clave

### Producto vs. Variante (Artículo)

En Caddis, la estructura del catálogo tiene dos niveles:

- **Producto:** Agrupa todos los artículos que son variantes del mismo modelo. Por ejemplo, "iPhone 16 Pro" es un producto.
- **Variante (Artículo):** Es cada combinación específica: "iPhone 16 Pro - Negro - 256GB" es una variante. Cada variante tiene su propio SKU, stock, precio y foto.

> 💡 Cuando creás un artículo con **Tipo + Marca + Modelo**, el sistema busca automáticamente si ya existe ese producto. Si existe, el artículo nuevo se asocia como una variante. Si no existe, crea el producto nuevo.

---

### Estados del artículo

| Estado | Significado |
|---|---|
| **ACTIVO** | El artículo está disponible para la venta y para sincronizar con tiendas virtuales. |
| **INACTIVO** | El artículo no aparece en la búsqueda de ventas ni se sincroniza. |
| **DISCONTINUO** | Artículo descontinuado por el proveedor. Se conserva en el historial pero no se repone. |
| **SIN REPOSICION** | El artículo existe pero no se repone (se vende hasta agotar stock). |

---

### Condición de IVA y su efecto

| Condición | IVA | Efecto en factura |
|---|---|---|
| **Gravado** | Según tasa seleccionada (21%, 10.5%, etc.) | El IVA se calcula y discrimina en la factura |
| **No Gravado** | Se fuerza a 0% | El artículo no suma IVA al total |
| **Exento** | Se fuerza a 0% | Igual que No Gravado, sin IVA |

> ⚠️ Al cambiar la condición a **No Gravado** o **Exento**, el sistema fuerza el campo IVA a 0 automáticamente y pide confirmación antes de guardar.

---

### Stock de Seguridad

El **Stock de Seguridad** es la cantidad que Caddis reserva internamente y **no informa a las tiendas virtuales** (MercadoLibre, TiendaNube, etc.). Esto previene vender online un artículo que solo queda disponible para venta presencial.

**Ejemplo:** Si tenés 5 unidades de un artículo y el stock de seguridad es 2, las tiendas online verán solo 3 unidades disponibles.

---

### Servicio (sin control de stock)

Si el artículo es un **Servicio** (instalación, mantenimiento, garantía extendida, etc.), marcarlo como `SERVICIO = SI` hace que el sistema no descuente stock al facturarlo. Este tipo de artículo puede venderse ilimitadamente.

> 💡 Al activar SERVICIO, aparece la leyenda **"→ NO CONTROLA STOCK"** en el formulario como recordatorio visual.

---

## Paso a paso: Alta de un artículo nuevo

1. Ingresá a **Módulo 1 → Artículos → ABM Artículos**.
2. El formulario aparece en blanco. Completá los campos obligatorios:
   - **NOMBRE:** descripción completa del artículo.
   - **TIPO:** categoría del artículo.
   - **MARCA:** marca del fabricante.
3. Completá los campos opcionales según corresponda: ESTADO, SERVICIO, PRECIO LIBRE, MODELO, GRUPO, etc.
4. En la sección **IMPUESTOS**, seleccioná la CONDICION y la tasa de IVA correcta.
5. En la sección **STOCK**, definí la UNIDAD y, si aplica, el stock de seguridad.
6. Completá MEDIDAS y PESO si el artículo se despacha por correo o logística.
7. Si el artículo se vende online, completá **WEB → TITULO** y **DESCRIPCION**.
8. Hacé clic en **Guardar** y confirmá el diálogo.

> ✅ Si ya completaste TIPO + MARCA + MODELO, el sistema vinculará automáticamente el artículo a su producto (o creará el producto si es nuevo).

---

## Paso a paso: Buscar y modificar un artículo existente

1. En el campo **Buscar...** (parte superior del formulario), ingresá el nombre, código SKU o marca del artículo.
2. Hacé clic en el **ícono lupa**. Se abre una ventana emergente con los artículos que coinciden.
3. Hacé clic sobre el artículo deseado en la ventana emergente. Sus datos se cargan en el formulario.
4. Modificá los campos que necesitás cambiar.
5. Hacé clic en **Guardar** y confirmá.

> ⚠️ Algunos artículos base del sistema solo permiten modificar la descripción y el precio libre.

---

## Paso a paso: Eliminar un artículo

1. Usá el campo **Buscar...** + lupa para encontrar el artículo y seleccionarlo desde la ventana emergente.
2. Hacé clic en el botón **Eliminar** (o el equivalente en la barra de acciones).
3. El sistema pide confirmación: "¿Eliminar el Artículo?"
4. Confirmá la eliminación.

> ❌ **No se pueden eliminar** artículos que tengan movimientos de stock o ventas registradas. En ese caso el sistema informa que no es posible eliminarlo. La alternativa es pasarlo al estado **INACTIVO** para que no aparezca en ventas.
>
> ❌ Tampoco se pueden eliminar artículos base del sistema. Si intentás hacerlo, aparece el mensaje: *"No se puede eliminar este artículo"*.

---

## Paso a paso: Importar artículos masivamente desde Excel

### Paso 1 — Obtener el formato de importación

En la sección **IMPORTAR ARTÍCULOS MASIVAMENTE**, hacé clic en el botón **Formato**. El sistema descarga automáticamente un archivo Excel con las columnas exactas requeridas, pre-poblado con datos reales del catálogo como ejemplo. Usalo como plantilla: reemplazá los datos de ejemplo con los artículos a importar.

El archivo contiene las siguientes **25 columnas** (en ese orden):

| # | Columna en el Excel | Descripción | Valores válidos |
|---|---|---|---|
| 1 | **Codigo** | Código SKU del artículo. No puede contener `'` (apóstrofe), `"` (comilla simple) ni `;` (punto y coma). | Texto, máx. 20 car. |
| 2 | **EAN** | Código de barras EAN-13 o similar. | Texto, máx. 15 car. |
| 3 | **Activo** | Estado del artículo en el catálogo. | `SI`, `NO`, `DIS` (discontinuo), `SRP` (sin reposición) |
| 4 | **Servicio** | Indica si el artículo es un servicio (no controla stock). | `SI` / `NO` |
| 5 | **Descripcion** | Nombre/descripción completa del artículo. | Texto |
| 6 | **Tipo** | Tipo de artículo. Debe coincidir exactamente con un tipo existente en el sistema. | Texto (ej: `CELULAR`, `ACCESORIO`) |
| 7 | **Grupo** | Agrupación comercial. Debe coincidir con un grupo existente. | Texto |
| 8 | **Marca** | Marca del artículo. Debe coincidir con una marca existente. | Texto (ej: `SAMSUNG`, `APPLE`) |
| 9 | **Modelo** | Nombre del modelo. | Texto, máx. 50 car. |
| 10 | **Condicion** | Condición frente al IVA. | `Gravado` / `No Gravado` / `Exento` |
| 11 | **IVA** | Tasa de IVA en formato decimal. | Número **menor a 1** (ej: `0.21` para 21%, `0.105` para 10.5%) |
| 12 | **Stk Seguridad** | Stock de seguridad (no se informa a tiendas virtuales). | Número entero |
| 13 | **Stk Reposicion** | Cantidad mínima para reponer. | Número entero |
| 14 | **Auto Reposicion** | Modo de cálculo del stock de reposición. | `FIJO` / `NO` / `AUTO` |
| 15 | **Proveedor** | Nombre del depósito/proveedor. Debe coincidir con un depósito existente. | Texto |
| 16 | **Unidad Medida** | Unidad de medida del artículo. | Texto (ej: `Unidad`, `Par`, `Caja`) |
| 17 | **Tamano** | Descripción del tamaño (sin tilde en la ñ). | Texto (ej: `L`, `XL`, `14"`) |
| 18 | **Largo** | Largo del artículo en cm. | Número decimal |
| 19 | **Ancho** | Ancho del artículo en cm. | Número decimal |
| 20 | **Alto** | Alto del artículo en cm. | Número decimal |
| 21 | **Peso** | Peso del artículo en kg. | Número decimal |
| 22 | **Bultos** | Cantidad de bultos. | Número entero |
| 23 | **Ubicacion** | Ubicación física en el depósito. | Texto, máx. 20 car. |
| 24 | **Meses Garantia** | Meses de garantía del artículo. | Número entero |
| 25 | **Usa NSE** | Indica si el artículo usa número de serie individual (teléfonos, electrodomésticos u otros productos con identificación única). | `SI` / `NO` |

---

### Paso 2 — Completar el archivo Excel

Completá el archivo respetando el formato de cada columna:

> ⚠️ **Errores comunes que provocan que el sistema descarte filas:**
> - **Activo** con un valor distinto de `SI`, `NO`, `DIS` o `SRP` → la fila se elimina sin importar.
> - **IVA** con valor `21` en vez de `0.21` → el sistema lo rechaza (debe ser menor a 1).
> - **Codigo** con apóstrofe, comilla simple o punto y coma → la fila se descarta.
> - **Tipo**, **Marca** o **Grupo** que no existe en el sistema → el artículo se inserta sin esa referencia.

---

### Paso 3 — Importar el archivo

1. En la sección **IMPORTAR ARTÍCULOS MASIVAMENTE**, hacé clic en el **ícono de carpeta** y seleccioná el archivo Excel preparado.
2. Hacé clic en el botón **Importar**.
3. El sistema muestra un mensaje de confirmación advirtiendo que el formato tiene columnas específicas (incluido el campo Tamaño). Confirmá para continuar.
4. Al finalizar, aparece el mensaje: *"Proceso terminado"*.

---

### Qué hace el sistema al importar

El proceso de importación tiene dos comportamientos según si el artículo ya existe en el catálogo:

**Artículos nuevos** (Codigo no existe):
- Se crea el artículo con todos los campos del Excel.
- Se crea automáticamente el **producto** asociado (si no existe el par Tipo+Marca+Modelo).
- El artículo se agrega a las **listas de precios** configuradas.
- Se crea el registro de **costos** para el artículo.
- Se vincula al **proveedor/depósito** indicado en la columna Proveedor.

**Artículos existentes** (Codigo ya existe):
- Se actualizan únicamente los campos: **Activo**, **Descripcion**, **Modelo**, **Ubicacion** y **Usa NSE**.
- Los demás campos (Tipo, Marca, IVA, etc.) **no se modifican** para artículos existentes.
- Para artículos base del sistema, solo se actualiza la **Descripcion**.

> 💡 La importación nunca duplica artículos con el mismo Código+EAN: si el sistema detecta que el Codigo ya existe con el mismo EAN, omite esa fila.

---

## Paso a paso: Cargar fotos de un artículo

1. Buscá y seleccioná el artículo.
2. En la parte inferior del formulario, aparece el área de fotos.
3. Hacé clic en el ícono **+** (insertar) para seleccionar una imagen desde tu computadora.
4. La foto se sube automáticamente y aparece en la galería.
5. Para eliminar una foto, hacé clic sobre ella. El sistema pide confirmación.

> ⚠️ Cada foto debe pesar menos de **1 MB** y ser formato **JPG, JPEG o PNG**. Imágenes más grandes o en otro formato serán rechazadas.

---

## Paso a paso: Crear un artículo Gift Card

Las **Gift Cards** son artículos de tipo servicio que representan saldos prepagos. Deben configurarse en el sistema antes de poder emitirlas desde Facturación. Se crea un artículo por cada denominación de Gift Card que se quiera ofrecer (ej: $500, $1000, $2000).

### Paso 1 — Crear el artículo en ABM Artículos

| Campo | Valor requerido | Motivo |
|---|---|---|
| **SERVICIO** | **SI** | No controla stock — es obligatorio |
| **TIPO** | **GIFT-CARD** | Tipo específico para este artículo |
| **DESCRIPCION** | La denominación (ej: `$500`, `$1000`) | Identifica el valor en el comprobante |
| **IVA** | **0,00** | Sin IVA — funciona como una seña/crédito prepago |
| **ESTADO** | ACTIVO | |
| **CODIGO** | Código único por denominación (ej: `GFT10001`) | |

Repetí este proceso por cada denominación disponible: una Gift Card de $500, otra de $1000, etc.

> Si el tipo **GIFT-CARD** no existe en el sistema, el administrador debe crearlo primero desde **Stock → Tipos de Artículos**.

### Paso 2 — Asignar el precio en Listas de Precios

Una vez creados los artículos, asignales el precio desde **Stock → Listas de Precios**:

1. Seleccioná la **LISTA** a usar (ej: MINORISTA)
2. Filtrá por **TIPO = GIFT-CARD** para ver solo las Gift Cards
3. En la columna **Precio**, ingresá el valor de cada denominación (ej: 500 para la Gift Card de $500)
4. Guardá los cambios

> El precio debe coincidir con la denominación del artículo. Una vez configurado, las Gift Cards pueden emitirse y usarse como forma de pago desde **Facturación**. Consultá [**Facturación**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf) para el procedimiento completo.

---

## Errores frecuentes y soluciones

| Error / Mensaje | Causa | Solución |
|---|---|---|
| *"Controle el Tipo de Artículo"* | El campo TIPO está en blanco o en el valor por defecto. | Seleccioná un tipo válido en el desplegable TIPO. |
| *"Controle la Marca"* | El campo MARCA está en blanco. | Seleccioná una marca del desplegable. |
| *"Controle la Descripción"* | El campo NOMBRE está vacío. | Completá el nombre del artículo. |
| *"¿Es un Artículo sin IVA?"* | IVA = 0% con condición "Gravado". | Si el artículo no tiene IVA, confirmá. Si fue un error, cambiá el campo IVA. |
| *"No se puede eliminar este artículo"* | El artículo es un artículo base del sistema, o tiene movimientos de stock o ventas registradas. | No es posible eliminarlo. Pasalo al estado **INACTIVO** para que no aparezca en ventas. |
| *"Solo permite modificar Descripción y precio libre"* | El artículo es un artículo base del sistema. | Solo podés cambiar esos dos campos en este artículo. |
| *"El tamaño de la imagen debe ser menor a 1Mb"* | La foto pesa más de 1 MB. | Comprimí la imagen antes de subirla. |
| *"El tipo de archivo debe ser JPG, JPEG o PNG"* | Formato de foto no soportado. | Convertí la imagen a JPG o PNG. |

---

## Preguntas frecuentes (FAQ)

**¿Puedo tener el mismo artículo con dos precios distintos?**
Sí, usando **variantes**. Creá dos artículos con el mismo Tipo + Marca + Modelo pero con atributos distintos (ej: 128GB y 256GB). Cada uno tiene su propio precio.

**¿Qué pasa si desactivo un artículo que tiene stock?**
El stock se conserva en el sistema, pero el artículo no aparece en ventas ni se sincroniza con tiendas virtuales. Podés reactivarlo cuando quieras.

**¿El SKU/CODIGO es obligatorio?**
Sí, es obligatorio. Puede ingresarlo el usuario manualmente, o el sistema puede asignarlo automáticamente según la configuración del Tipo de artículo. Cada tipo puede tener un prefijo o esquema de numeración que genera el código en forma automática al guardar.

**¿Puedo cambiar el TIPO de un artículo después de crearlo?**
Sí, pero hay que tener cuidado: cambiar el tipo puede afectar los atributos dinámicos y la vinculación con el producto. Si el artículo tiene ventas registradas, no es recomendable cambiar el tipo.

**¿La foto aparece automáticamente en MercadoLibre o TiendaNube?**
No automáticamente. La foto se guarda en Caddis y luego puede usarse al publicar en las tiendas virtuales. Ver instructivos de los módulos 6 y 7.

**¿Qué es el campo EAN y para qué sirve?**
El EAN (European Article Number) es el código de barras estándar internacional. Sirve para identificar el artículo con lectoras de código de barras en el punto de venta y para publicar en marketplaces que lo requieren (como MercadoLibre).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Febrero 2026*
