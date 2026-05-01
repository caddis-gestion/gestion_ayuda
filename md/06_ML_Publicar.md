# 6.03 ML PUBLICAR ARTÍCULO
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Publicar Articulo

---

## ¿Para qué sirve esta pantalla?

**ML Publicar Artículo** permite crear una nueva publicación en MercadoLibre desde Caddis, sin necesidad de ingresar al portal de ML. Desde aquí podés:

- Seleccionar un artículo del catálogo de Caddis para publicar
- Configurar todos los parámetros de la publicación: título, categoría, descripción, tipo, condición, precio, stock, logística y garantía
- Cargar y gestionar las imágenes de la publicación
- Completar los atributos específicos que solicita ML según la categoría elegida

---

<img src="imagenes/pantalla_ml_publicar_articulo.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Publicar Articulo**

---

## Descripción general de la pantalla

La pantalla muestra un formulario de publicación organizado en secciones: datos del artículo, parámetros de la publicación, atributos dinámicos (según categoría) e imágenes.

---

## Sección: Artículo

| Campo | Descripción |
|---|---|
| **ARTICULO** | Buscador del artículo en el catálogo de Caddis. Completá el código o nombre y seleccioná el artículo a publicar. |

---

## Sección: Parámetros de la publicación

| Campo | Descripción |
|---|---|
| **ID** | ID de la publicación en ML (solo lectura — se completa automáticamente si ya existe una publicación vinculada). |
| **TITULO** | Título de la publicación. Máximo 60 caracteres. Aparece en los resultados de búsqueda de ML. |
| **CATEGORIA** | Categoría de ML en la que se va a publicar el artículo. Usá el buscador de categorías para encontrar la más adecuada. |
| **DESCRIPCION** | Texto de descripción detallada del producto que verán los compradores. |
| **TIPO** | Tipo de publicación: `gold_special` (Premium), `gold_pro` (Premium Pro), `classic` (Clásica), `free` (Gratuita). |
| **CONDICION** | `new` (Nuevo), `used` (Usado), `not_specified` (No especificado). |
| **CANTIDAD** | Stock disponible para esta publicación. |
| **PRECIO** | Precio de venta al público en ML. |
| **MONEDA** | Moneda de la publicación (generalmente `ARS` para Argentina). |
| **ENVIO** | Modo de envío: `me2` (Mercado Envíos), `not_specified` (a acordar). |
| **LOGISTICA** | Tipo de logística: `cross_docking` (Colecta), `self_service` (Flex), `fulfillment` (FULL). |

---

## Sección: Garantía

| Campo | Descripción |
|---|---|
| **GARANTIA TIPO** | Tipo de garantía: `guaranteed` (Garantía del vendedor), `no_warranty` (Sin garantía). |
| **GARANTIA TIEMPO** | Número de unidades de tiempo de garantía (ej: `12`). |
| **GARANTIA UNIDAD** | Unidad: `days` (días), `months` (meses), `years` (años). |

---

## Sección: Atributos

Los atributos son campos específicos que solicita MercadoLibre según la categoría elegida (ej: marca, modelo, capacidad, color). Se generan dinámicamente al seleccionar la categoría.

Completá todos los atributos requeridos (marcados con asterisco o color diferente) para poder publicar el artículo sin errores en ML.

---

## Sección: Imágenes

| Elemento | Descripción |
|---|---|
| **Subir imagen** | Selector de archivo para cargar una imagen desde el equipo (JPG/PNG). |
| **Imágenes existentes** | Vista previa de las imágenes ya cargadas para la publicación. Podés eliminar las que no quieras. |

> ℹ️ ML requiere imágenes de buena calidad (mínimo 500×500 px). Las imágenes con fondo blanco y el producto centrado tienen mejor desempeño en los resultados de búsqueda.

---

## Cómo crear una publicación paso a paso

1. Seleccioná el **ARTICULO** del catálogo de Caddis.
2. Completá el **TITULO** (descriptivo y con palabras clave).
3. Buscá y seleccioná la **CATEGORIA** más adecuada.
4. Escribí la **DESCRIPCION** del producto.
5. Elegí el **TIPO** de publicación y la **CONDICION**.
6. Ingresá el **PRECIO** y la **CANTIDAD** disponible.
7. Configurá el **ENVIO** y la **LOGISTICA**.
8. Completá los datos de **GARANTIA**.
9. Completá los **ATRIBUTOS** que aparecen para la categoría seleccionada.
10. Cargá al menos una **IMAGEN** del producto.
11. Hacé click en **Guardar** o **Publicar** para crear la publicación en ML.

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| Error al publicar por categoría | La categoría no acepta ese tipo de producto | Probá con una categoría más específica o diferente |
| Atributo requerido faltante | No completaste un atributo obligatorio de la categoría | Revisá los atributos marcados como requeridos |
| Imagen rechazada | Tamaño o formato no cumple con los requisitos de ML | Usá JPG o PNG con al menos 500×500 px |
| Precio inválido | El precio ingresado está por debajo del mínimo de ML | Verificá el precio mínimo permitido para esa categoría |

---

> 📖 Para gestionar publicaciones ya existentes (precios, stock, estado) consultá [**ML Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicaciones.pdf).
> 📖 Para editar los NSE/series de artículos en una venta consultá [**Editar Ítems de Venta**](https://ayuda.caddis.com.ar/instructivos/06_ML_Editar_Items.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
