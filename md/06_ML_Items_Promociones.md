# ML Items Promociones

Pantalla para gestionar los items de publicaciones de MercadoLibre dentro de promociones. Permite visualizar, filtrar, activar e inactivar items en promociones, y sincronizar el estado con la API de ML.

## Como acceder

**Menu:** E-COMMERCES → ML Items Promociones

---

## Panel izquierdo — Filtros y configuracion

### Seccion superior: Seleccion de promocion

| Campo | Descripcion |
|---|---|
| **USUARIO** | Cuenta de ML (tienda) sobre la que se opera |
| **TIPO** | Tipo de promocion (DEAL, LIGHTNING, PRE_NEGOTIATED, etc.) |
| **PROMO** | Promocion especifica. Se filtra automaticamente segun el TIPO seleccionado |
| **ITEMS** | Estado del item dentro de la promocion (CANDIDATE, STARTED, PENDING, DELETED) |

> Al cambiar TIPO o PROMO la grilla se actualiza automaticamente.

### Seccion DETALLE PROMOCION

Aparece unicamente cuando se selecciona una promocion especifica. Muestra datos de solo lectura:

| Campo | Descripcion |
|---|---|
| **ESTADO** | Estado actual de la promocion en ML |
| **INICIA** | Fecha de inicio |
| **FINALIZA** | Fecha de fin |

### Seccion FILTRO PUBLICACIONES

Permite acotar los resultados de la grilla. Los filtros de esta seccion solo aplican cuando no se usa ITEM ni SKU.

| Campo | Descripcion |
|---|---|
| **TIPO** | Tipo de articulo (Todos / Articulos / Equipos / Filtro por lista) |
| **GRUPO** | Grupo de articulo |
| **MARCA** | Marca del articulo |
| **PROVEEDOR** | Proveedor del articulo |
| **ITEM** | ID de publicacion de ML (filtra ignorando el resto de los filtros) |
| **SKU** | Codigo de articulo (filtra ignorando el resto de los filtros) |

> **Prioridad de filtros:** si se ingresa ITEM o SKU, los demas filtros se ignoran.

### Seccion PROCESOS

Botones que operan sobre todos los items tildados en la grilla:

| Boton | Accion |
|---|---|
| **Actualizar Promociones** | Sincroniza promociones e items desde la API de ML hacia la base de datos local |
| **Inactivar Promociones** | Inactiva la promocion para los items tildados |
| **Activar Promociones** | Solicita un porcentaje de descuento y activa la promocion para los items tildados |

---

## Panel derecho — Grilla de items

Muestra los items participantes en promociones con la siguiente informacion:

| Columna | Descripcion |
|---|---|
| Checkbox | Seleccion para operaciones en lote |
| Item | ID de publicacion en ML |
| SKU | Codigo de articulo en Caddis |
| Titulo | Nombre de la publicacion |
| Precio Lista | Precio original antes del descuento |
| Precio Descuento | Precio con descuento activo en la promo |
| Precio Destacado | Precio especial para clientes con nivel de fidelidad |
| Promocion | Nombre de la promocion |
| Promo Tipo | Tipo de promocion |
| Estado Promocion | Estado del item dentro de la promo (con color de fondo) |
| Precio Sugerido | Precio sugerido por ML |
| Precio Minimo | Precio minimo permitido por ML |
| Precio Maximo | Precio maximo permitido por ML |
| Porcentaje Meli | Porcentaje de descuento absorbido por ML |
| Porcentaje Vendedor | Porcentaje de descuento absorbido por el vendedor |
| Stock ML | Stock disponible en ML |
| Stock FULL | Stock en deposito FULL de ML |
| Stock Minimo | Stock minimo requerido por la promo |
| Stock Maximo | Stock maximo permitido por la promo |
| Estado Publicacion | Estado de la publicacion (ACTIVE, PAUSED, etc.) |
| Tipo | Tipo de articulo |
| Grupo | Grupo del articulo |
| Marca | Marca del articulo |
| Proveedor | Proveedor del articulo |
| Semaforo | Estado visual del item en la promo: verde=STARTED, amarillo=PENDING, rojo=CANDIDATE/otro |

### Acciones por fila

| Accion | Descripcion |
|---|---|
| **Detalle** (lupa) | Abre ventana con el detalle completo de la publicacion |
| **Activar** (verde) | Abre popup para ingresar precios y activar el item en la promocion |
| **Inactivar** (rojo) | Inactiva el item de la promocion directamente, sin popup |

---

## Popup: Activar item en promocion

Se abre al hacer click en el boton **Activar** de la fila. Permite configurar los precios antes de activar el item.

| Campo | Descripcion |
|---|---|
| **Precio Original** | Precio de lista del articulo (se completa automaticamente desde la grilla, solo lectura) |
| **Precio Variacion** | Porcentaje de descuento a aplicar. Al modificarlo recalcula Precio Descuento automaticamente |
| **Precio Descuento** | Precio final con descuento. Al modificarlo recalcula Precio Variacion automaticamente. Se completa automaticamente desde la grilla |
| **Precio Destacado** | Precio especial para clientes con nivel de fidelidad alto (Mercado Puntos 3 a 6). Dejar vacio si no aplica ⚠ |
| **Desde** | Fecha de inicio del descuento |
| **Hasta** | Fecha de fin. Se completa automaticamente con la fecha FINALIZA de la promocion seleccionada |

> **Relacion Precio Variacion / Precio Descuento:**
> - Precio Descuento = Precio Original × (1 − Variacion / 100)
> - Precio Variacion = (1 − Precio Descuento / Precio Original) × 100

Segun el tipo de promocion pueden aparecer campos adicionales:

| Tipo | Campo extra |
|---|---|
| LIGHTNING | **Stock**: cantidad de unidades a incluir en la oferta relampago |
| PRE_NEGOTIATED | **Oferta**: identificador de la oferta pre-negociada con ML |

Al confirmar con **Activar Promocion** el sistema:
1. Verifica que el articulo cumpla los requisitos de ML (estado ACTIVE, condicion NEW, publicacion no gratuita, fechas dentro del maximo de 14 dias, validez del precio destacado)
2. Envia la solicitud a la API de ML
3. Actualiza el semaforo en la grilla al color correspondiente

---

## Proceso: Actualizar Promociones

Sincroniza el estado de la API de ML hacia la base de datos local. Se ejecuta en tres etapas:

**1. `actualizarPromociones()`**
Consulta todas las promociones disponibles en ML y las guarda/actualiza en la tabla `mercadolibre_promociones` (con paginacion de 50 en 50).

**2. `actualizarPromocionesItems()`**
Por cada promocion, consulta los items participantes en ML y los guarda/actualiza en `mercadolibre_promociones_items` (con paginacion por `searchAfter`).

**3. `limpiarPromocionesItems()`**
Recorre los items en la tabla local y elimina los registros que ya no existen en ML. Ademas:
- Elimina promociones vencidas (`finaliza < CURDATE()`)
- Elimina items huerfanos (sin promocion padre en la tabla)

> El proceso puede filtrarse por Item especifico, por SKU, por Promocion, por Tipo o ejecutarse para todas las promociones.

---

## Proceso: Activar Promociones (en lote)

Opera sobre los items **tildados** en la grilla. Solicita un porcentaje de descuento mediante un `prompt` y ejecuta `activarPromocionItems()`:

1. Para cada item seleccionado obtiene el articulo asociado y su lista de precios
2. Calcula el precio con descuento: `precio_venta × (1 − descuento/100)`
3. Llama a la API de ML para activar el descuento
4. Usa como fecha de inicio el dia de hoy y como fecha de fin el valor de FINALIZA de la promocion

---

## Proceso: Inactivar Promociones (en lote)

Opera sobre los items **tildados** en la grilla. Llama a `inactivarPromocionItems()` que por cada item ejecuta `inactivarItemDescuento()` contra la API de ML.

---

## Tablas de base de datos

| Tabla | Uso |
|---|---|
| `mercadolibre_promociones` | Cabecera de cada promocion de ML |
| `mercadolibre_promociones_items` | Items participantes en cada promocion con precios y estados |
| `mercadolibre_items` | Publicaciones de ML (fuente de SKU, stock, estado) |
| `age_union.mercadolibre_item_status` | Descripcion legible del estado de la publicacion |
| `age_union.mercadolibre_item_promo_status` | Descripcion legible del estado del item en la promo |
| `age_union.mercadolibre_item_promo_tipo` | Descripcion legible del tipo de promocion |
| `vista_articulos` | Vista de articulos (para filtros por tipo, grupo, marca, proveedor) |
