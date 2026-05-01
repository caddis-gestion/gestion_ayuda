# 6.06 ML PRECIOS DE PUBLICACIONES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Precios

---

## ¿Para qué sirve esta pantalla?

**ML Precios** permite visualizar y actualizar masivamente los precios de las publicaciones activas en MercadoLibre. Desde aquí podés:

- Consultar el precio actual de cada publicación y compararlo con el precio calculado por Caddis
- Actualizar los precios de todas las publicaciones en un solo paso
- Filtrar publicaciones por estado, logística, exceptuadas, catálogo, bultos, marca, ítem y SKU
- Ver el semáforo de diferencia de precio (verde = igual, amarillo = diferencia leve, rojo = diferencia importante)
- Controlar si una publicación es excluida de las actualizaciones automáticas de precio

---

<img src="imagenes/pantalla_ml_publicaciones_precios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Precios**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda y botón de actualización masiva de precios.
- **Panel derecho (grilla):** Listado de publicaciones con sus precios actuales, calculados y diferencia.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio para ver resultados. |
| **ESTADO** | Estado de la publicación en ML (`active`, `paused`, `closed`, etc.). |
| **LOGISTICA** | Tipo de logística de la publicación. |
| **EXCEPTUADOS** | `SI` muestra solo publicaciones excluidas de la actualización automática. `NO` muestra las no excluidas. |
| **CATALOGO** | Filtra publicaciones de catálogo (oferta única en ML). |
| **BULTOS** | Filtra por cantidad de unidades por bulto. |
| **MARCA** | Marca del artículo. |
| **ITEM** | ID de publicación ML específica. |
| **SKU** | Código del artículo en Caddis. |

---

## Botón: Actualizar Precios Masivamente

Envía a MercadoLibre los precios calculados por Caddis para todas las publicaciones del usuario seleccionado (o las filtradas, según corresponda).

**Cuándo usarlo:** cuando se actualizó la lista de precios en Caddis y se quiere reflejar el cambio en todas las publicaciones de ML.

**Cómo ejecutarlo:**
1. Seleccioná el **USUARIO** ML.
2. Aplicá filtros si querés actualizar solo un subconjunto de publicaciones.
3. Hacé click en **Actualizar Precios Masivamente**.
4. Confirmá el aviso.
5. El proceso corre en segundo plano.

> ⚠️ La actualización masiva solo afecta las publicaciones que NO estén marcadas como exceptuadas.

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Item** | ID de la publicación en ML |
| **SKU** | Código del artículo en Caddis |
| **Variante** | Variante del artículo (color, capacidad, etc.) |
| **ML Precio Regular** | Precio actual en ML sin descuento |
| **ML Descuento** | Porcentaje de descuento aplicado en ML |
| **ML Precio Marketplace** | Precio efectivo de venta en ML (con descuento) — fondo amarillo |
| **Caddis Precio Marketplace** | Precio calculado por Caddis para la publicación — fondo amarillo |
| **Caddis Lista Marketplace** | Lista de precios de Caddis usada para calcular el precio |
| **MShop** | Precio para Mercado Shop (si aplica) |
| **Cantidad por Bulto** | Unidades físicas por paquete de envío |
| **Tipo Publicacion** | Tipo de publicación (Premium, Clásica, etc.) |
| **Estado** | Estado actual de la publicación |
| **Logistica** | Tipo de logística |
| **Exceptuado** | `SI` si la publicación está excluida de actualizaciones automáticas |
| **Titulo** | Título de la publicación |
| **Color** | Color del artículo (si aplica) |
| **Categoria** | Categoría de ML |
| **Es Promo** | Indica si la publicación tiene una promoción activa |
| **Condicion** | Nuevo / Usado |
| **Usuario** | Cuenta ML dueña de la publicación |
| **Error** | Último error registrado al intentar actualizar el precio |

> ℹ️ Las columnas **ML Precio Marketplace** y **Caddis Precio Marketplace** tienen fondo amarillo para facilitar la comparación visual. El semáforo de la grilla indica si hay diferencia entre ambos precios.

---

## Semáforo de diferencia de precio

| Color | Significado |
|---|---|
| Verde | El precio de ML coincide con el calculado por Caddis |
| Amarillo | Hay una diferencia menor (dentro del rango tolerado) |
| Rojo | La diferencia es significativa — conviene actualizar |

---

## Acciones desde la grilla

Seleccioná una fila y usá los botones disponibles:

| Acción | Descripción |
|---|---|
| **Modificar** | Edita los parámetros de precio de esa publicación (precio, lista, exceptuado, etc.) |

---

## Preguntas frecuentes

**¿Qué es una publicación "exceptuada"?**
Es una publicación que se excluyó de la actualización automática de precios. Su precio en ML no cambia aunque se ejecute "Actualizar Precios Masivamente". Se usa para publicaciones con precio especial o acordado con un comprador.

**¿Por qué mi precio en ML es diferente al de Caddis?**
Puede haber un descuento aplicado directamente en ML, o puede que la lista de precios de Caddis se actualizó pero aún no se ejecutó la actualización masiva. Revisá las columnas **ML Precio Marketplace** y **Caddis Precio Marketplace**.

---

> 📖 Para gestionar listas de precios por tipo de publicación consultá [**Listas de Precios ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Listas_Precios.pdf).
> 📖 Para activar o inactivar promociones de precio consultá [**Promociones en ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Promociones.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
