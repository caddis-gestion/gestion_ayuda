# PROMOCIONES DE ARTÍCULOS
### Módulo 1 — Artículos

> **Versión:** 1.0 — Febrero 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Artículos → Promociones Articulos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Promociones de Artículos** permite crear y gestionar combos de venta con condiciones de precio especiales. Una promoción agrupa uno o más artículos o equipos bajo un código de promo, y al aplicarla en la pantalla de facturación el sistema los carga automáticamente con los precios o descuentos configurados.

Desde aquí podés:

- Crear nuevas promociones con código, descripción y fecha de vencimiento
- Agregar múltiples ítems a una misma promoción (artículos, tipos de artículo, equipos)
- Configurar el precio, descuento o cantidad de cada ítem de la promo
- Restringir la promoción a una forma de pago específica (ej.: solo con tarjeta de crédito Visa)
- Modificar fecha de vencimiento, precios o cantidades de promos existentes
- Eliminar ítems individuales de una promo o eliminar la promo completa

> 📖 Para aprender a aplicar una promoción en una venta, consultá [**Facturación (A / B / C / M)**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf).

---

## Cómo acceder

Desde el menú principal seleccioná:
**Artículos → Promociones Articulos**

---

## Descripción general de la pantalla

![Pantalla Promociones Artículos](imagenes/pantalla_promos_articulos.png)

La pantalla muestra:

- **Panel izquierdo:** Formulario para crear o agregar ítems a una promoción, con secciones "Formas de pago" y "Datos de producto". Botones **Nuevo** (limpiar formulario) y exportación a Excel.
- **Panel derecho:** Cuando se carga una promo existente, aparece el detalle completo con todos sus ítems y las opciones de edición rápida (precio, descuento, cantidad) por ítem.

---

## Conceptos clave

### ¿Qué es una Promoción de Artículos?

Una **promo** es un conjunto de condiciones de venta identificadas con un código único. Cuando el operador aplica ese código en la facturación, el sistema carga automáticamente los artículos correspondientes con el precio o descuento configurado.

Cada promo tiene:
- Un **código** (PROMO): identificador único, máximo 20 caracteres
- Una **descripción** (DESCRIPCION): nombre legible de la promo
- Una **fecha de vencimiento** (VENCE): después de esa fecha la promo no aplica
- Una **forma de pago** opcional: si se configura, la factura solo puede emitirse con ese medio de pago
- Uno o más **ítems**: cada ítem define el artículo/equipo y su precio o descuento

### Tipos de producto en una promo

| Tipo de producto | Qué incluye |
|---|---|
| **ARTICULO** | Un artículo específico del catálogo, identificado por código |
| **TIPO DE ARTICULO** | Todos los artículos que pertenecen a un tipo dado (ej.: "ACCESORIOS") |
| **EQUIPO** | Un equipo específico identificado por su número de serie (NSE/IMEI) |
| **MARCA DE EQUIPO** | Todos los equipos de una marca y/o tipo de equipo determinado |
| **CUALQUIER EQUIPO** | Cualquier equipo con número de serie, sin restricción de marca o modelo |

> 💡 Los tipos EQUIPO, MARCA DE EQUIPO y CUALQUIER EQUIPO solo están disponibles si la empresa tiene habilitado el uso de NSE (número de serie de equipos).

### Precio en una promo: tres opciones excluyentes

Para cada ítem de la promo hay **tres maneras** de fijar el beneficio, y solo se puede usar una por ítem:

| Campo | Descripción | Cuándo usarlo |
|---|---|---|
| **DTO %** | Porcentaje de descuento sobre el precio de lista del artículo | Cuando querés aplicar un % de rebaja |
| **IMPORTE UNIT** | Precio unitario fijo de venta (solo para ARTICULO y TIPO DE ARTICULO) | Cuando el artículo tiene un precio especial fijo por unidad |
| **IMPORTE TOTAL** | Precio total fijo del ítem para la cantidad configurada | Cuando el combo tiene un precio cerrado (ej.: kit por $50.000) |

> ⚠️ Solo uno de los tres campos puede tener valor mayor a cero. Si se completan dos o más, el sistema mostrará un error.

---

## Campos del formulario (panel izquierdo)

### Sección: Datos de la promo

| Campo | Descripción |
|---|---|
| **PROMO** | Código único que identifica la promoción (máx. 20 caracteres). Se ingresa directamente o se busca con el botón **Buscar** para cargar una promo existente. No puede coincidir con el código (SKU) de un artículo. |
| **DESCRIPCION** | Nombre descriptivo de la promo (máx. 255 caracteres). Se muestra en el buscador de promos al facturar. |
| **VENCE** | Fecha hasta la cual la promo es válida. Después de esa fecha no podrá aplicarse. Incluye un botón **Modificar** para actualizar la fecha sin necesidad de re-ingresar los ítems. |

---

### Sección: Formas de pago

| Campo | Descripción |
|---|---|
| **FORMA** | Forma de pago que el cliente debe usar para acceder a esta promoción. Opciones: `TODAS` (sin restricción), o un tipo de pago específico (Efectivo, Débito, Crédito, etc.). Si se elige una forma específica, el sistema validará al facturar que el pago coincida. |
| **TARJETA** | Solo aparece si FORMA es Débito o Crédito. Permite restringir la promo a una tarjeta específica (ej.: Visa, Mastercard) o elegir `TODAS` para cualquier tarjeta del tipo seleccionado. |

---

### Sección: Datos de producto

| Campo | Descripción |
|---|---|
| **PRODUCTO** | Tipo de artículo al que aplica este ítem de la promo. Determina qué campos adicionales aparecen (ver tabla de tipos más arriba). |
| **ARTICULO** | (Solo si PRODUCTO = ARTICULO) Buscador del artículo específico a incluir en la promo. |
| **EQUIPO** | (Solo si PRODUCTO = EQUIPO) Buscador del equipo/NSE a incluir. |
| **MARCA** | (Solo si PRODUCTO = MARCA DE EQUIPO) Selección de la marca de equipo. |
| **TIPO** | (Solo si PRODUCTO = TIPO DE ARTICULO) Selección del tipo de artículo de la tabla de tipos configurados. |
| **CANTIDAD** | Cantidad del artículo/equipo que incluye la promo (ej.: `2` = dos unidades de ese artículo). |
| **DTO %** | Porcentaje de descuento sobre el precio de lista (ej.: `20.00` = 20% de rebaja). Solo uno de los tres campos de precio puede completarse. |
| **IMPORTE UNIT** | Precio unitario fijo a facturar (ej.: `15000.00` = $15.000 por unidad). Solo para ARTICULO y TIPO DE ARTICULO. Solo uno de los tres. |
| **IMPORTE TOTAL** | Precio total fijo para la cantidad configurada (ej.: `25000.00` = $25.000 por el combo). Solo uno de los tres. |

---

## Panel derecho: Detalle de la promo

Cuando se carga una promo existente (por código o búsqueda), el panel derecho muestra:

- **Encabezado** (fondo rosa): Nombre de la promo, código, fecha de vencimiento, tipo de pago requerido y tarjeta (si aplica)
- **Ítems:** Cada ítem de la promo aparece en un bloque con:
  - Nombre del artículo (o descripción del tipo/marca)
  - Campo **Precio** editable (presioná Enter para guardar el cambio)
  - Campo **Descuento** editable (presioná Enter para guardar)
  - Campo **Cantidad** editable (presioná Enter para guardar)
  - Botón **Borrar** para eliminar ese ítem de la promo

> 💡 Las ediciones de precio, descuento y cantidad se guardan **ítem por ítem** presionando Enter en el campo modificado. No hace falta un botón "Guardar" global para estos cambios.

---

## Paso a paso: Crear una promoción nueva

**Caso típico:** Promo "KIT NAVIDAD" — comprando un artículo A y un artículo B juntos, el cliente paga un precio especial total de $80.000, pagando con cualquier medio.

### Paso 1: Ingresar los datos de la promo

**1.** En el campo **PROMO**, escribí el código de la nueva promo (ej.: `KITNAVIDAD`).

**2.** En el campo **DESCRIPCION**, escribí el nombre visible (ej.: `KIT NAVIDAD 2026 - COMBO A+B`).

**3.** En el campo **VENCE**, elegí la fecha de vencimiento (ej.: `31/12/2026`).

**4.** En el campo **FORMA**, dejá `TODAS` si no hay restricción de pago, o elegí la forma requerida.

**5.** Si elegiste Débito o Crédito, seleccioná la tarjeta en el campo **TARJETA** (o dejá `TODAS`).

---

### Paso 2: Agregar el primer ítem

**6.** En el campo **PRODUCTO**, seleccioná el tipo: `ARTICULO`.

**7.** En el campo **ARTICULO**, buscá y seleccioná el artículo A.

**8.** En **CANTIDAD**, ingresá `1`.

**9.** En **IMPORTE TOTAL**, ingresá `40000.00` (precio especial por ese artículo en la promo). Dejá DTO % e IMPORTE UNIT en `0.00`.

**10.** Hacé clic en el botón **Ingresar** (o presioná Enter en el campo IMPORTE TOTAL).

**11.** El sistema pedirá confirmación "¿Ingresá el Registro?". Hacé clic en **Aceptar**.

**12.** El ítem aparecerá en el panel derecho.

---

### Paso 3: Agregar el segundo ítem

**13.** Repetí los pasos 6 a 11 para el artículo B, con su precio correspondiente.

**14.** La promo queda configurada con ambos ítems en el panel derecho.

> 💡 Podés seguir agregando ítems a la misma promo repitiendo el proceso. Los ítems se acumulan sin borrar los anteriores.

---

## Paso a paso: Agregar ítems de distintos tipos

### Ítem tipo: TIPO DE ARTICULO con descuento porcentual

1. En **PRODUCTO**, seleccioná `TIPO DE ARTICULO`
2. En **TIPO**, seleccioná el tipo de artículo (ej.: "ACCESORIOS")
3. En **CANTIDAD**, ingresá la cantidad mínima requerida (ej.: `1`)
4. En **DTO %**, ingresá el porcentaje de descuento (ej.: `15.00` para 15% off). Dejá IMPORTE UNIT e IMPORTE TOTAL en `0.00`
5. Hacé clic en **Ingresar** y confirmá

### Ítem tipo: EQUIPO (NSE específico)

1. En **PRODUCTO**, seleccioná `EQUIPO`
2. En **EQUIPO**, buscá y seleccioná el equipo por número de serie o código
3. Definí DTO % o IMPORTE TOTAL (no se usa IMPORTE UNIT para equipos)
4. Hacé clic en **Ingresar** y confirmá

### Ítem tipo: MARCA DE EQUIPO

1. En **PRODUCTO**, seleccioná `MARCA DE EQUIPO`
2. En **MARCA**, seleccioná la marca (ej.: SAMSUNG)
3. Opcionalmente, seleccioná también el TIPO de equipo para restringir aún más (ej.: solo SAMSUNG Galaxy)
4. Definí DTO % o IMPORTE TOTAL y hacé clic en **Ingresar**

### Ítem tipo: CUALQUIER EQUIPO

1. En **PRODUCTO**, seleccioná `CUALQUIER EQUIPO`
2. No se requieren datos adicionales de artículo
3. Definí DTO % o IMPORTE TOTAL y hacé clic en **Ingresar**
4. El descuento aplicará a cualquier equipo con NSE que se incluya en la factura con esta promo

---

## Paso a paso: Modificar una promo existente

### Cambiar la fecha de vencimiento

**1.** En el campo **PROMO**, ingresá el código o usá el botón **Buscar** para cargar la promo.

**2.** En el campo **VENCE**, modificá la fecha.

**3.** Hacé clic en el botón **Modificar** que aparece al lado del campo VENCE.

> 💡 El botón **Modificar** junto a VENCE actualiza la fecha (y el nombre) sin necesidad de tocar los ítems.

### Cambiar precio, descuento o cantidad de un ítem

**1.** Cargá la promo en el panel izquierdo para que aparezcan sus ítems en el panel derecho.

**2.** En el panel derecho, localizá el ítem que querés modificar.

**3.** Editá el campo **Precio**, **Descuento** o **Cantidad** directamente en el panel derecho.

**4.** Presioná **Enter** en el campo modificado para guardar el cambio.

> ⚠️ Al modificar el Precio de un ítem, el sistema pone automáticamente el Descuento en 0 (y viceversa). No pueden coexistir los dos.

---

## Paso a paso: Eliminar un ítem de una promo

**1.** Cargá la promo para ver sus ítems en el panel derecho.

**2.** En el ítem que querés quitar, hacé clic en el botón **Borrar** (ícono de papelera).

**3.** El sistema pedirá confirmación. Confirmá para eliminar ese ítem de la promo.

> ℹ️ Eliminar un ítem de la promo no elimina la promo completa. Los demás ítems permanecen.

---

## Paso a paso: Eliminar una promo completa

Para eliminar la promo entera, debés borrar uno a uno todos sus ítems desde el panel derecho.

> ⚠️ **No se puede eliminar** una promo que ya fue aplicada en una **factura emitida**. El sistema mostrará el mensaje "Existen Ventas asociadas a esta Promoción". En ese caso, la alternativa es cambiar la fecha de vencimiento a una fecha pasada para que deje de estar disponible.

---

## Restricciones de forma de pago: cómo funcionan en facturación

Cuando una promo tiene una **FORMA** de pago configurada (distinta de "TODAS"), el sistema realiza una validación especial al momento de emitir la factura:

- Calcula el subtotal correspondiente a los artículos de esa promo
- Verifica que exista un pago del tipo requerido que cubra al menos ese subtotal
- Si el pago no cumple la condición, bloquea la facturación y muestra el mensaje:

> `"Debe existir al menos un pago del tipo [FORMA] por un valor mínimo de $[MONTO]"`

**Ejemplo:** Promo "VISA 3 CUOTAS" configurada con FORMA = Crédito y TARJETA = Visa. Al facturar, el sistema verificará que haya un pago con Visa crédito que cubra el subtotal de los artículos incluidos en esa promo. Si el operador cobra todo en efectivo, la factura no puede emitirse.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Debe ingresar un Código de Promo" | El campo PROMO está vacío | Completá el campo con un código único |
| "Debe ingresar una descripcion de la promo" | El campo DESCRIPCION está vacío | Completá el nombre de la promo |
| "No se puede usar un SKU de producto como código de Promo" | El código ingresado ya existe como artículo | Elegí un código diferente que no coincida con ningún artículo |
| "Controle el Vencimiento" | El campo VENCE está vacío | Ingresá una fecha de vencimiento válida |
| "Debe ingresar un Producto" | No se seleccionó un tipo de producto | Seleccioná el tipo en el campo PRODUCTO |
| "Debe ingresar un Importe o un Descuento" | Todos los campos de precio están en 0 | Completá DTO %, IMPORTE UNIT o IMPORTE TOTAL con un valor mayor a 0 |
| "Se debe ingresar solo uno: Importe Total, Importe Unitario o Descuento" | Más de un campo de precio tiene valor | Dejá solo uno con valor, los demás en 0.00 |
| "No se pueden combinar las promociones para equipos" | Se intentó agregar un ítem de artículo en una promo que ya tiene equipos (o viceversa) | Usá promos separadas para artículos y para equipos |
| "No se puede ingresar el mismo artículo en diferentes registros" | El artículo ya existe como ítem en esa promo | Modificá el ítem existente en lugar de agregar uno nuevo |
| "Existen Ventas asociadas a esta Promoción" (al eliminar) | La promo ya fue usada en facturas | No se puede eliminar; cambiá la fecha de vencimiento a una fecha pasada |
| "Debe existir al menos un pago del tipo X..." (al facturar) | La factura tiene artículos de una promo pero el pago no coincide con la forma requerida | Registrá el pago con la forma de pago que exige la promo |

---

## Preguntas frecuentes

**¿Cuántos ítems puede tener una promo?**
No hay límite. Podés agregar tantos ítems como sean necesarios.

**¿Puedo mezclar artículos y equipos en la misma promo?**
No. Una promo no puede tener simultáneamente ítems de tipo ARTICULO/TIPO_ARTICULO e ítems de tipo EQUIPO/MARCA_EQUIPO/CUALQUIER_EQUIPO. Usá promos separadas para cada caso.

**¿Puedo poner el mismo artículo dos veces en una promo?**
No. Si intentás agregar un artículo que ya está en la promo, el sistema lo rechazará. Podés modificar la cantidad del ítem existente desde el panel derecho.

**¿Una promo puede tener ítems con descuento y otros con precio fijo?**
Sí. Cada ítem tiene su propio precio independiente. Un ítem puede tener DTO % y otro IMPORTE TOTAL.

**¿Qué pasa si la promo vence?**
Después de la fecha de VENCE, la promo no aparecerá en el buscador de promos de la pantalla de facturación.

**¿Cómo busco una promo existente para editarla?**
Ingresá el código en el campo PROMO y el sistema lo cargará automáticamente al salir del campo (evento onBlur). También podés usar el botón **Buscar** para abrir el buscador de promos y seleccionarla por nombre o código.

**¿La promo aplica a todos los PDVs?**
Sí. Las promos están disponibles en todos los puntos de venta de la empresa.

---

## Referencia rápida de campos

| Campo | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| PROMO | Texto (máx. 20) | Sí | Código único de la promo |
| DESCRIPCION | Texto (máx. 255) | Sí | Nombre de la promo |
| VENCE | Fecha | Sí | Fecha de vencimiento |
| FORMA | Lista | No | Forma de pago requerida (TODAS = sin restricción) |
| TARJETA | Lista | No | Tarjeta requerida (solo si FORMA = Débito o Crédito) |
| PRODUCTO | Lista | Sí | Tipo de artículo del ítem |
| ARTICULO / EQUIPO / TIPO / MARCA | Buscador/Lista | Condicional | Identificador del artículo según tipo |
| CANTIDAD | Número | Sí (para Artículo/Tipo) | Unidades del ítem en la promo |
| DTO % | Número decimal | Uno de los tres | Porcentaje de descuento |
| IMPORTE UNIT | Número decimal | Uno de los tres | Precio unitario fijo (solo Artículo/Tipo) |
| IMPORTE TOTAL | Número decimal | Uno de los tres | Precio total fijo del ítem |

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Febrero 2026*
