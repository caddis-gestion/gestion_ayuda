# 3.63 MODIFICAR PRESUPUESTO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Modificar Presupuesto

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Modificar Presupuesto** permite actualizar los precios de los artículos de un presupuesto ya emitido. Es útil cuando los precios cambiaron entre la fecha de emisión y la fecha de facturación. Desde aquí podés:

- Buscar un presupuesto por número
- Ver los artículos y sus precios actuales
- Modificar el precio de venta de cada artículo directamente en la grilla

---

<img src="imagenes/pantalla_modificar_presupuesto.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Modificar Presupuesto**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con la búsqueda y datos del presupuesto, y un panel derecho con el detalle de artículos editable.

---

## Panel izquierdo — Búsqueda y datos

| Campo / Botón | Descripción |
|---|---|
| **PRESUPUESTO** | Número del presupuesto a modificar |
| **Buscar** | Busca el presupuesto e indica sus datos |
| **FECHA** | Fecha de emisión del presupuesto (sólo lectura) |
| **CLIENTE** | Cliente del presupuesto (sólo lectura) |
| **MONEDA** | Moneda del presupuesto (sólo lectura) |

---

## Panel derecho — Grilla de artículos

Muestra los artículos del presupuesto. La columna **Precio Vta** es editable (resaltada en amarillo):

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| **Precio Vta** | Precio de venta con IVA (editable — campo resaltado en amarillo) |
| Iva % | Porcentaje de IVA del artículo |
| Moneda | Moneda del precio |
| Articulo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Proveedores | Proveedores del artículo |
| Variante | Variante del artículo |

---

## Paso a paso — Modificar precios de un presupuesto

1. Ingresá el número del **PRESUPUESTO** y hacé clic en **Buscar**
2. El sistema carga los datos del presupuesto y sus artículos en la grilla
3. En la columna **Precio Vta** (amarilla), hacé clic en el precio que querés cambiar
4. Ingresá el nuevo precio con IVA incluido
5. Guardá el cambio

---

## Notas importantes

- Solo se puede modificar el **Precio de Venta**. No permite cambiar artículos, cantidades ni datos del cliente.
- Los cambios afectan el presupuesto: cuando se facture desde **Facturar Presupuestos** (3.56), se usarán los precios actualizados.
- El precio se ingresa con IVA incluido; el sistema calcula el IVA automáticamente según la tasa del artículo.
