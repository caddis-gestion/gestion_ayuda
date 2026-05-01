# 15.32 CATEGORÍAS COMISIONALES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Comisiones → Categorías Comisionales

---

## ¿Para qué sirve esta pantalla?

Permite crear y administrar las categorías comisionales del sistema. Cada categoría define un grupo de clasificación que se asigna a los **puntos de venta, vendedores, supervisores, jefes de ventas y gerentes**, y se utiliza en el cálculo de comisiones.

Cuando un vendedor emite un comprobante en Facturación, el sistema registra automáticamente en cada venta los datos del punto de venta, vendedor, supervisor, jefe de ventas y gerente junto con su categoría comisional vigente en ese momento. Esa información queda asociada permanentemente a la venta y es la base para los reportes e informes de comisiones.

---

<img src="imagenes/pantalla_admin_categorias_comisionales.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Comisiones → Categorías Comisionales**

---

## Panel izquierdo — Datos de la categoría

| Campo | Descripción |
|---|---|
| CATEGORIA | Código de la categoría (máximo 15 caracteres). Se ingresa manualmente. |
| DESCRIPCION | Nombre o descripción de la categoría (máximo 25 caracteres). |
| ACTIVA | Indica si la categoría está habilitada. Opciones: **SI** / **NO**. |

### Botones de acción

| Botón | Descripción |
|---|---|
| Agregar | Crea una nueva categoría con los datos ingresados en el panel izquierdo. |
| Modificar | Guarda los cambios realizados sobre la categoría seleccionada. |
| Borrar | Elimina la categoría seleccionada del sistema. |

---

## Grilla derecha — Lista de categorías

Muestra todas las categorías comisionales registradas en el sistema:

| Columna | Descripción |
|---|---|
| Categoría | Código de la categoría comisional. |
| Descripción | Nombre descriptivo de la categoría. |
| (botones) | Acciones disponibles: **Modificar** / **Borrar** |

> **Nota:** Las categorías con código `SINCAT` o `SC` están reservadas por el sistema y no aparecen en la grilla.

> **Tip:** Para modificar o borrar una categoría, hacé clic en el botón correspondiente en la fila de la grilla. Los datos se cargarán automáticamente en el panel izquierdo para su edición.

---

## Asociación a la estructura comercial

Una vez creadas las categorías, deben asignarse a cada integrante de la estructura comercial desde sus respectivas pantallas de alta o modificación:

| Pantalla | Campo | Descripción |
|---|---|---|
| [**Puntos de Venta**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Puntos_de_Venta.pdf) | CATEGORIA | Categoría comisional del PDV |
| [**Vendedores**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Vendedores.pdf) | CATEGORIA | Categoría comisional del vendedor |
| [**Supervisores**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Supervisores.pdf) | CATEGORIA | Categoría comisional del supervisor |
| [**Jefes de Ventas**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_SubGerentes.pdf) | CATEGORIA | Categoría comisional del jefe de ventas |
| [**Gerentes**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Gerentes.pdf) | CATEGORIA | Categoría comisional del gerente |

Cada vez que se registra una venta en Facturación, el sistema toma automáticamente la categoría asignada en ese momento al PDV, vendedor, supervisor, jefe de ventas y gerente, y la guarda junto con la operación.

> **Importante:** El cambio de categoría **no es retroactivo**. Las ventas ya registradas conservan la categoría que estaba asignada al momento de la facturación. Solo las operaciones nuevas, a partir del cambio, tomarán la nueva categoría.

---

## Corrección de ventas anteriores — Reasignar Ventas

Si fuera necesario corregir la asignación de categoría (u otros datos comerciales) en operaciones ya registradas, se puede utilizar la pantalla **Reasignar Ventas**. Desde allí es posible modificar el PDV, vendedor, supervisor, jefe de ventas y/o gerente asociados a comprobantes ya emitidos.

Acceso: [**Reasignar Ventas**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Reasignar_Ventas.pdf) — Menú → Ventas → Reasignar Ventas

---
