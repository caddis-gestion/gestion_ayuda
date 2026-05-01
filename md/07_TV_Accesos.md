# 7.01 TV ACCESOS
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Accesos

---

## ¿Para qué sirve esta pantalla?

**TV Accesos** es el panel central de configuración de todas las cuentas de tiendas virtuales conectadas a Caddis. Desde aquí podés:

- Ver todas las cuentas (accesos) de cada tienda virtual (MercadoLibre, TiendaNube, Shopify, WooCommerce, etc.)
- Crear nuevos accesos o eliminar los existentes
- Configurar los parámetros de sincronización de cada cuenta (stock automático, porcentajes, etc.)
- Guardar cambios de parámetros para múltiples cuentas al mismo tiempo

---

<img src="imagenes/pantalla_tv_accesos.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Accesos**

---

## Descripción general de la pantalla

La pantalla muestra una **grilla horizontal** con una fila por cada cuenta (acceso) configurada, donde se pueden editar los parámetros directamente en la celda. El encabezado está fijo al hacer scroll horizontal.

### Botones superiores

| Botón | Descripción |
|---|---|
| **Crear acceso** | Abre una ventana emergente para dar de alta una nueva cuenta de tienda virtual. |
| **Guardar parámetros** | Graba todos los cambios de parámetros realizados en la grilla de una sola vez. |

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| *(Ícono borrar)* | Elimina el acceso seleccionado. Pide confirmación. |
| *(Ícono editar)* | Abre el popup para editar los datos del acceso. |
| **TIENDA** | Logo de la tienda virtual (MercadoLibre, TiendaNube, Shopify, etc.). |
| **CUENTA** | Nombre de usuario de la cuenta en la tienda. |
| *Columnas de parámetros* | Una columna por cada parámetro configurable. Pueden ser checkbox (SI/NO) o porcentaje (%). Los parámetros varían según la tienda. |

---

## Parámetros configurables

Cada columna de parámetro corresponde a una configuración de la cuenta. Los tipos posibles son:

| Tipo de parámetro | Cómo se edita |
|---|---|
| **Booleano (SI/NO)** | Checkbox. Marcar = SI, desmarcar = NO. |
| **Porcentaje (%)** | Campo numérico. Ingresar el valor sin el símbolo %. |
| **Texto/número** | Campo de texto editable. |

> 💡 Los parámetros disponibles dependen de qué tiendas están configuradas. Ejemplos típicos: sincronización automática de stock, porcentaje de recargo de precio, etc.

---

## Cómo crear un nuevo acceso

1. Hacé clic en el botón **Crear acceso**.
2. Se abre un popup con el formulario de alta.
3. Completá los datos requeridos (tienda, usuario, credenciales).
4. Guardá desde el popup.
5. El nuevo acceso aparece en la grilla.

> **Si la cuenta creada es de MercadoLibre:** una vez guardado el acceso es necesario autenticar la cuenta contra la plataforma de ML. Para eso ingresá a [**ML Login**](https://ayuda.caddis.com.ar/instructivos/06_ML_Login.pdf), seleccioná la cuenta y hacé clic en **Integrar cuenta**. Esto abre el proceso de autorización en MercadoLibre y vincula el token de acceso necesario para la sincronización.

---

## Cómo modificar parámetros de una cuenta

1. En la fila de la cuenta, modificá el valor del parámetro deseado (checkbox o número).
2. Repetí para todas las cuentas/parámetros que necesitás cambiar.
3. Hacé clic en **Guardar parámetros** para aplicar todos los cambios de una sola vez.

> ⚠️ Los cambios de parámetros **no se guardan automáticamente**. Siempre hacé clic en **Guardar parámetros** al terminar.

---

## Cómo eliminar un acceso

1. En la fila del acceso a eliminar, hacé clic en el **ícono de borrar** (primera columna).
2. El sistema pide confirmación: *"¿Eliminar acceso [usuario] de tienda [tienda]?"*
3. Confirmá para eliminar.

> ⚠️ Eliminar un acceso desvincula la cuenta de Caddis. Las publicaciones y ventas históricas se conservan pero ya no se sincronizarán.

---

