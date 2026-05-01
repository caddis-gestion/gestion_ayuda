# 6.23 ML LISTAS DE PRECIOS
### Módulo 6 — Mercado Libre

> **Versión:** 1.1 — Abril 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Listas Precios

---

## ¿Para qué sirve esta pantalla?

**ML Listas de Precios** permite configurar qué lista de precios de Caddis se usa para calcular los precios de cada tipo de publicación de MercadoLibre. Desde aquí podés:

- Ver y modificar la relación entre el tipo de publicación ML y la lista de precios de Caddis
- Configurar listas de precios separadas para MarketPlace y para M-Shop (Mercado Shop)
- Diferenciar listas de precios según la **campaña de cuotas** activa en cada publicación
- Actualizar la configuración al seleccionar el usuario ML

---

<img src="imagenes/pantalla_ml_listas_precios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Listas Precios**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros y campos de configuración.
- **Panel derecho (grilla):** Listado de combinaciones tipo + campaña con sus listas de precios asignadas.

---

## Panel izquierdo: Campos

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Al seleccionar, carga automáticamente la configuración de listas de precios de esa cuenta y las campañas disponibles. |
| **TIPO** | Tipo de publicación de ML (MLItemTipo: Premium, Clásica, Gratuita, etc.). Actúa como filtro de la grilla. |
| **CAMPAÑA** | Campaña de cuotas sin interés activa en las publicaciones (ej: `6x_campaign`, `12x_campaign`). Seleccionar **SIN CAMPAÑA** para configurar el precio base sin campaña. Las opciones se cargan dinámicamente desde las publicaciones de la cuenta seleccionada. |
| **LISTA MARKET** | Lista de precios de Caddis a asignar para MarketPlace. |
| **LISTA MSHOP** | Lista de precios de Caddis a asignar para Mercado Shop. Solo visible si la cuenta usa MShop. |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Publicacion Tipo** | Tipo de publicación ML (ej: `gold_special`, `gold_pro`, `classic`, `free`) |
| **Campaña** | Campaña de cuotas sin interés asociada a la fila. Vacío o `SIN CAMPAÑA` = precio base. |
| **Lista Precios MarketPlace** | Lista de precios de Caddis usada para calcular el precio de MarketPlace — fondo amarillo |
| **Lista Precios M-Shop** | Lista de precios de Caddis usada para calcular el precio de M-Shop (si aplica) |
| **Usuario Tienda** | Cuenta ML dueña de esta configuración |

---

## Cómo funciona la relación entre listas, tipos y campañas

Cada fila de la grilla representa una combinación única de **tipo de publicación + campaña**. Esto permite asignar listas de precios distintas según si la publicación tiene o no una campaña de cuotas activa.

**Ejemplo:**

| Tipo | Campaña | Lista asignada |
|---|---|---|
| gold_special | *(sin campaña)* | Lista Minorista |
| gold_special | 12x_campaign | Lista Cuotas 12 |
| gold_pro | 6x_campaign | Lista Cuotas 6 |

Cuando se ejecuta **Actualizar Precios Masivamente** en [**ML Precios**](https://ayuda.caddis.com.ar/instructivos/06_ML_Precios.pdf) (6.06), el sistema:

1. Toma cada publicación de la cuenta ML.
2. Identifica el **Tipo de publicación** y la **Campaña de cuotas** activa (campo `installments_campaign`).
3. Busca en esta pantalla la fila que coincide con ese par tipo + campaña.
4. Calcula el precio usando la lista asignada a esa fila.
5. Envía el precio calculado a ML.

> Si una publicación no tiene campaña activa, el sistema usa la fila con **SIN CAMPAÑA** del mismo tipo. Si no existe esa fila, la publicación no recibe actualización de precio.
>
> **Excepción — `gold_pro`:** las publicaciones de tipo `gold_pro` sin campaña asignada se tratan automáticamente como `6x_campaign`. Esto significa que en la grilla siempre aparecen como `6x_campaign`, nunca como SIN CAMPAÑA. La lista a asignar para `gold_pro` debe configurarse en la fila `gold_pro + 6x_campaign`.

---

## Cómo modificar la lista asignada a un tipo + campaña

1. Seleccioná el **USUARIO** ML.
2. Opcionalmente filtrá por **TIPO** para acotar la grilla.
3. En la grilla, seleccioná la fila a modificar (combinación de tipo + campaña).
4. Hacé clic en **Modificar**.
5. Cambiá la **LISTA MARKET** y/o **LISTA MSHOP**.
6. Guardá los cambios.

---

## Cómo agregar una nueva combinación tipo + campaña

Si aparece una nueva campaña en las publicaciones ML (ej: una nueva campaña del banco), la fila correspondiente puede no existir aún:

1. Seleccioná el **USUARIO** ML.
2. Seleccioná el **TIPO** de publicación.
3. En el selector **CAMPAÑA**, elegí la nueva campaña (aparece automáticamente si ya hay publicaciones con esa campaña).
4. Asigná la **LISTA MARKET** (y **LISTA MSHOP** si aplica).
5. Guardá — se crea la nueva fila en la grilla.

---

> Para actualizar los precios de las publicaciones usando estas listas consultá [**Precios de Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Precios.pdf).
> Para ver las publicaciones activas y sus precios actuales consultá [**ML Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Publicaciones.pdf).
