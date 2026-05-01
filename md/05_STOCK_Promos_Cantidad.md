# 5.XX PROMOS POR CANTIDAD
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Promos Cantidad

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Promos por Cantidad** permite definir descuentos automáticos que se aplican cuando se vende una cantidad superior a un umbral establecido para un artículo. Desde aquí podés:

- Seleccionar el artículo al que aplica la promo
- Definir la cantidad mínima, el descuento porcentual y la fecha de vencimiento
- Ver y eliminar las promociones ya configuradas para el artículo

---

<img src="imagenes/pantalla_promos_cantidad.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Promos Cantidad**

---

## Formulario

| Campo | Descripción |
|---|---|
| **ARTICULO** | Código del artículo al que se aplica la promoción |
| **CANTIDAD** | Cantidad mínima a partir de la cual se activa el descuento |
| **DESCUENTO** | Porcentaje de descuento a aplicar cuando se supera la cantidad |
| **VENCE** | Fecha de vencimiento de la promoción |

---

## Panel de descuentos configurados

Debajo del formulario, al seleccionar un artículo válido, se muestran todos los descuentos por cantidad ya configurados:

| Columna | Descripción |
|---|---|
| CANTIDAD | Umbral de cantidad (el descuento se aplica cuando la venta supera este valor) |
| DESCUENTO | Porcentaje de descuento |
| VENCIMIENTO | Fecha hasta la que está vigente la promoción |

**Acciones:**
- **Borrar:** Elimina la promoción de cantidad

---

## Notas importantes

- El descuento se aplica automáticamente en la venta cuando la cantidad del artículo supera el umbral definido.
- Se pueden configurar múltiples rangos de cantidad con distintos descuentos para el mismo artículo.
- Si el artículo ingresado no existe en el sistema, se muestra el mensaje **NO EXISTE EL ARTICULO**.
