# 7.06 TV PUBLICACIONES
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Publicaciones

---

## ¿Para qué sirve esta pantalla?

**TV Publicaciones** es el panel de control de todas las publicaciones activas en una tienda virtual. Desde aquí podés:

- Consultar y filtrar el catálogo de artículos publicados
- Ver stock disponible, precio en la tienda y precio en Caddis
- Actualizar publicaciones, stock y precios masivamente
- Identificar artículos con diferencias de precio entre la tienda y Caddis

---

<img src="imagenes/pantalla_tv_publicaciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Publicaciones**

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **TIENDA** | Selector de tienda virtual (banner superior). |
| **USUARIO** | Cuenta de la tienda virtual. Al cambiar, actualiza la grilla. |
| **RESULTADOS** | Cantidad máxima de publicaciones a mostrar: 10, 100, 1000, 10000, TODO. |
| **VARIANTE** | ID de variante en la tienda virtual. Enter para buscar. |
| **PRODUCTO** | ID de producto en la tienda virtual. Enter para buscar. |
| **SKU** | Código SKU de Caddis. Enter para buscar. |
| **ESTADO** | Estado de la publicación (activa, pausada, etc. — opciones según la tienda). |
| **MARCA** | Filtro por marca del artículo. |

### Sección LISTA DE PRECIOS

Muestra (solo lectura) el nombre de la lista de precios asignada a la cuenta seleccionada.

### Sección OPERACIONES MASIVAS

| Botón | Descripción |
|---|---|
| **Actualizar Publicaciones** | Sincroniza los datos de publicaciones desde la tienda (baja datos actualizados). |
| **Actualizar Stock Masivamente** | Envía el stock de Caddis a la tienda para todas las publicaciones visibles en la grilla. |
| **Actualizar Precios Masivamente** | Envía los precios de la lista asignada a la tienda para todas las publicaciones visibles en la grilla. Si hay un proceso en curso, muestra el botón "Detalle de importación en proceso..." |

> 💡 El botón **Actualizar Precios** actúa sobre las publicaciones visibles en ese momento (según los filtros aplicados). Usá RESULTADOS: TODO para actualizar todo el catálogo, o filtrá por SKU/Marca para actualizar solo un subconjunto.

---

## Panel derecho: Grilla de publicaciones

> ℹ️ Se requiere seleccionar al menos un filtro Y un usuario de tienda para visualizar publicaciones.

| Columna | Descripción |
|---|---|
| **Producto** | ID del producto en la tienda virtual |
| **Variante** | ID de la variante (si difiere del producto) |
| **SKU** | Código del artículo en Caddis |
| **Titulo** | Nombre de la publicación en la tienda |
| **Estado** | Estado de la publicación |
| **Stock Tienda** | Stock informado a la tienda virtual |
| **Stock Disponible** | Stock real disponible en Caddis (depósitos del usuario) |
| **Stock Seguridad** | Stock de seguridad reservado (no publicado) |
| **Stock Pendiente** | Stock comprometido en ventas pendientes |
| **Unidades x bulto** | Unidades por bulto del artículo |
| **Precio Tienda** | Precio actual en la tienda virtual |
| **Precio Caddis** | Precio de la lista asignada en Caddis *(fondo amarillo)* |
| **Es Promo** | SI si tiene promoción activa |
| **Es Compuesto** | SI si es un artículo compuesto |
| **Stock Editable** | SI si el stock puede modificarse directamente en la tienda |
| **Stock Exceptuado** | SI si el artículo está en la lista de excepciones de stock |
| **Peso (kg)** | Peso del artículo |
| **Largo / Ancho / Alto (cm)** | Dimensiones del artículo |
| **Fecha Creacion** | Fecha en que se publicó el artículo |
| **Usuario Tienda** | Cuenta de la tienda que tiene la publicación |
| **Observaciones** | Notas generales de la publicación |
| **Observaciones Stock** | Mensajes del último proceso de sincronización de stock |
| **Observaciones Precio** | Mensajes del último proceso de sincronización de precios |

> 💡 La columna **Precio Caddis** (fondo amarillo) permite comparar rápidamente si el precio en la tienda coincide con el precio de la lista. Si difieren, puede ser necesario actualizar precios.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
