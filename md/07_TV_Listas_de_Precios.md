# 7.05 TV LISTAS DE PRECIOS
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Listas de precios

---

## ¿Para qué sirve esta pantalla?

**TV Listas de Precios** permite asignar a cada cuenta de tienda virtual la **lista de precios** de Caddis que se usará para sincronizar precios, y la **moneda** en que se publicarán. Desde aquí podés:

- Ver todas las cuentas de tiendas virtuales (TiendaNube, Shopify, WooCommerce, etc.) y su lista asignada
- Cambiar la lista de precios de una cuenta
- Cambiar la moneda de sincronización de una cuenta

> ℹ️ Las cuentas de MercadoLibre (local y Global Selling) y MercadoPago no aparecen en esta pantalla — su lista de precios se gestiona desde las pantallas ML correspondientes.

---

<img src="imagenes/pantalla_tv_listas_precios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Listas de precios**

---

## Descripción de la pantalla

La pantalla muestra una sección por cada **tipo de tienda** que tiene cuentas configuradas. Dentro de cada sección, hay una fila por cuenta.

| Elemento | Descripción |
|---|---|
| **Título de sección** | Nombre de la tienda virtual (ej: TIENDANUBE, SHOPIFY, WOOCOMMERCE). |
| **Etiqueta de cuenta** | Nombre de usuario o URL de la cuenta (columna izquierda). |
| **Desplegable Lista** | Lista de precios de Caddis a usar para esta cuenta. |
| **Desplegable Moneda** | Moneda en que se sincronizarán los precios (ej: Pesos, Dólares). |
| **Ícono guardar** | Guarda la configuración de lista y moneda para esa cuenta. |

---

## Cómo asignar o cambiar la lista de precios

1. Localizá la cuenta de la tienda virtual.
2. En el desplegable **Lista**, seleccioná la lista de precios deseada.
3. En el desplegable **Moneda**, seleccioná la moneda correcta.
4. Hacé clic en el **ícono de guardar** (ícono de diskette/guardar) de esa fila.
5. El sistema pide confirmación: *"¿Asignar lista [nombre lista] en [moneda] a cuenta [usuario]?"*
6. Confirmá para guardar.

> ⚠️ Cada cuenta tiene su propio botón de guardar. Los cambios se aplican **individualmente por fila**.

---

## Relación con la sincronización de precios

Cuando se ejecuta la sincronización de precios (desde **TV Publicaciones** → botón "Actualizar Precios Masivamente"), el sistema toma el precio de la lista asignada en esta pantalla y lo convierte a la moneda configurada antes de publicarlo en la tienda.

> 💡 Si los precios en la tienda virtual no se actualizan correctamente, verificar que la lista y moneda asignadas en esta pantalla sean las correctas.

---

> 📖 Para actualizar precios masivamente en la tienda consultá [**Publicaciones en Tienda Virtual**](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicaciones.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
