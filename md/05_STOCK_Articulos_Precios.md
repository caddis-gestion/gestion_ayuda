# 5.47 ARTÍCULOS — PRECIOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.2 — Abril 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Artículos Precios

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Precios** permite consultar y actualizar los precios de venta de los artículos para una lista de precios específica. También permite modificar precios masivamente y cargar listas desde archivos. Desde aquí puedes:

- Seleccionar una lista de precios y ver los precios con costos y márgenes
- Editar el precio de venta directamente en la grilla
- Aplicar un porcentaje de variación masiva a todos los artículos filtrados
- Importar precios desde un archivo

---

<img src="imagenes/pantalla_articulos_precios.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal selecciona:
**Stock → Artículos Precios**
---

## Formulario

| Campo | Descripción |
|---|---|
| **LISTA** | Lista de precios a consultar/modificar. Botón **Agregar** para crear un artículo nuevo en la lista |
| **ARTICULO** | Código o descripción del artículo |
| **NEGOCIO** | Línea de negocio a la que pertenece el artículo |
| **TIPO** | Tipo de artículo |
| **GRUPO** | Grupo del artículo |
| **MARCA** | Marca del artículo |
| **PROVEEDOR** | Proveedor del artículo |

---

## Crear una nueva lista de precios

Para crear una lista nueva haz clic en el ícono **Alta de Listas** (ícono de edición junto al selector LISTA):

<img src="imagenes/articulos_precios_listas.png" style="width:auto; height:auto; max-width:100%; max-height:320px; display:block; margin:0 auto;">

Se abre el popup **Alta de Listas**:

| Paso | Campo / Acción | Descripción |
|---|---|---|
| 1 | Ícono de alta | Abre el popup Alta de Listas |
| 2 | **LISTA** | Escribe el nombre de la nueva lista (ej: `MAYORISTA`, `LOCALES`, `WEB`) |
| 3 | **Moneda** | Selecciona la moneda: `PESO ARGENTINO`, `DOLAR USA` o `EURO` |
| 4 | **Guardar** | Confirma la creación de la lista |
| 5 | Refrescar | Actualiza el selector LISTA para ver la nueva lista creada |

> Una vez creada la lista, carga los precios usando cualquiera de los tres métodos descriptos más adelante: importación desde Excel, edición directa en la grilla o variación masiva por porcentaje.

---

### Sección MODIFICAR MASIVAMENTE

| Campo | Descripción |
|---|---|
| **NUEVO PRECIO** | Nuevo precio a aplicar a todos los artículos filtrados (botón **Modificar**) — solo en empresas habilitadas |
| **VARIAR %** | Porcentaje de variación a aplicar (positivo o negativo) a todos los artículos filtrados (botón **Modificar**) |

### Sección IMPORTAR PRECIOS

Permite cargar masivamente precios de una lista desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Selecciona el archivo Excel (.xlsx) a importar |
| **Importar** | Procesa el archivo y actualiza los precios de la lista activa |
| **Formato** | Descarga un ejemplo del formato requerido con datos reales del sistema |

#### Formato del archivo de importación

El archivo debe tener **2 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | SKU del artículo en Caddis | Debe existir en la lista activa |
| **Precio Final** | Precio de venta **con IVA incluido** | Decimal, punto como separador. Ej: `4599.50`. Acepta el símbolo `$`. |

#### Validaciones del sistema

- El separador decimal **debe ser punto** (no coma). Ej: `4599.50`, no `4599,50`.
- Se acepta el símbolo `$` antes del número: el sistema lo elimina automáticamente.
- El artículo debe estar incluido en la lista activa; los que no se encuentran se omiten.

#### Qué hace el sistema al importar

- El precio ingresado es el **precio final con IVA**. El sistema divide por `(1 + tasa IVA)` para obtener el precio neto interno.
- Si el sistema tiene configurada una dirección de mail de alertas de precios, envía automáticamente un informe con los precios anteriores y los nuevos.

---

## Botón LISTAS — Comparar todas las listas

El botón **LISTAS** (en la parte superior de la pantalla) abre un popup de comparación que muestra **todos los artículos con sus precios en todas las listas simultáneamente**, en un formato de columnas:

<img src="imagenes/articulos_precios_popup_listas.png" style="width:100%; height:auto; display:block;">

Cada columna representa una lista de precios distinta. Puedes buscar artículos por descripción (por ejemplo: "batería") y ver de un vistazo el precio en cada lista. La celda resaltada en amarillo indica el precio actualmente activo o en edición.

> Esta vista es de solo lectura — para modificar precios usa la pantalla principal con la lista seleccionada.

---

## Panel derecho — Grilla de precios

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Precio Venta | Precio de venta con impuestos (editable directamente, resaltado en amarillo) |
| Costo con Impuestos | Costo total incluyendo IVA e Impuesto Interno |
| Costo sin Impuestos | Costo neto sin impuestos |
| MarkUp % | Porcentaje de markup sobre el costo |
| Margen % | Porcentaje de margen sobre el precio de venta |
| Iva % | Alícuota de IVA del artículo |
| Impuesto Interno % | Alícuota de impuesto interno |
| Moneda | Moneda de la lista de precios |
| Articulo | Descripción del artículo |
| Tipo | Tipo del artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Proveedores | Proveedores del artículo |

---

## Conceptos — Tipos de listas de precios

El sistema permite diseñar el control de precios de venta desde distintas configuraciones según las necesidades del negocio:

| Configuración | Cuándo se usa |
|---|---|
| **Lista única con moneda única** | Ventas en un solo local donde la lista es la misma para todos los clientes |
| **Lista única bimonetaria** | Comercios con productos importados cuyos precios dependen de la cotización del dólar. El sistema multiplica el precio de lista por la cotización oficial del BCRA, que se muestra en la barra del menú en tiempo real. Solo aplica para las monedas PESO-DÓLAR. |
| **Lista única con descuentos por cliente** | Venta mayorista: todos parten de la misma lista MINORISTA pero cada cliente tiene su propio porcentaje de descuento configurado |
| **Múltiples listas, moneda única** | Diferentes listas asignadas a distintos puntos de venta o clientes para diferenciar precios |
| **Múltiples listas con monedas distintas** | Similar al anterior, pero cada lista puede tener una moneda diferente |

---

## Conceptos — Tipos de descuentos

El sistema soporta cuatro mecanismos de descuento que se aplican en orden secuencial:

| Tipo | Descripción |
|---|---|
| **Promociones** | Descuentos por artículo o tipo de artículo. Pueden ser un importe fijo o un porcentaje sobre la lista MINORISTA. Se aplican al ingresar el artículo en la factura. |
| **Descuentos por cantidad** | Descuentos asociados a la cantidad vendida de un artículo. No se aplican si el artículo ya forma parte de una promoción. |
| **Vouchers** | Descuento general sobre el total de la factura (importe fijo o porcentaje). Se aplica después de las promociones y descuentos por cantidad. |
| **Descuentos o recargos por forma de pago** | Porcentaje de descuento o recargo según el medio de pago elegido. Se aplica sobre el total ya neteado de promos y vouchers. |

---

## Lógica de selección de lista al facturar

Al emitir una factura, el sistema determina qué lista de precios aplicar siguiendo este orden de prioridad:

1. **¿El cliente tiene una lista asignada?** → Toma la lista del cliente
2. **¿El PDV tiene una lista asignada?** → Toma la lista del PDV
3. **¿El cliente tiene descuentos configurados?** → Toma la lista MINORISTA y aplica el descuento definido para ese cliente
4. **Ninguna de las anteriores** → Toma la lista MINORISTA por defecto

---

## Orden de aplicación de descuentos al facturar

Los descuentos se aplican en el siguiente orden:

1. **Descuento por promoción o por cantidad** — se aplica sobre el precio de la lista
2. **Descuento por voucher** — se aplica sobre el total de la factura ya con los descuentos anteriores
3. **Descuento o recargo por forma de pago** — se aplica sobre el total ya neteado de promos y vouchers

**Fórmula del total de la factura:**

```
Total = Precio de Lista × (1 − Desc. Promo o Cantidad) × (1 − Desc. Voucher) × (1 − Desc./Recargo Pago)
```

**Ejemplo:**

| Concepto | Valor |
|---|---|
| Precio de lista | $10.000 |
| Descuento promoción (10%) | −$1.000 → subtotal $9.000 |
| Descuento voucher (5%) | −$450 → subtotal $8.550 |
| Descuento efectivo (3%) | −$256,50 → **Total $8.293,50** |

---

## Notas importantes

- La columna **Precio Venta** es editable directamente en la grilla.
- Solo se muestran artículos activos que tengan precio en la lista seleccionada.
- Los costos se toman del mayor entre Costo Reposición y Costo Compra según la configuración.
- El MarkUp% y Margen% se calculan automáticamente a partir del precio y el costo.
- En la modalidad **bimonetaria**, el precio de lista en dólares se convierte a pesos usando la cotización oficial del BCRA visible en la barra del menú.
