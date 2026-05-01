# 3.46 CTA CTE CONDICIONES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Cta Cte Condiciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cta Cte Condiciones** permite administrar las condiciones de pago disponibles para las ventas en cuenta corriente. Cada condición define un plazo de días y una tasa de interés. Desde aquí podés:

- Agregar nuevas condiciones de pago (ej. "30 días sin interés", "60 días con 5%")
- Modificar condiciones existentes
- Eliminar condiciones que ya no se usan

---

<img src="imagenes/pantalla_cta_cte_condiciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Cta Cte Condiciones**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de carga y un panel derecho con la grilla de condiciones existentes.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **CONDICION** | Nombre descriptivo de la condición (ej. "30 días", "60 días 5%") |
| **PLAZO** | Cantidad de días del plazo de pago |
| **TASA** | Tasa de interés mensual (en %). Ingresá 0 si es sin interés. |

---

## Panel derecho — Grilla de condiciones

Muestra todas las condiciones de pago configuradas, ordenadas por plazo:

| Columna | Descripción |
|---|---|
| Condicion | Nombre de la condición |
| Plazo | Cantidad de días |
| Tasa | Tasa de interés mostrada con IVA incluido |

**Acciones disponibles:**
- **Modificar:** Carga la condición en el formulario para editarla
- **Borrar:** Elimina la condición

---

## Paso a paso — Agregar una condición de pago

1. Ingresá el nombre en **CONDICION** (ej. "30 días")
2. Completá el **PLAZO** en días (ej. 30)
3. Ingresá la **TASA** de interés mensual (ej. 0 para sin interés, o 5 para 5%)
4. Guardá el registro

---

## Notas importantes

- Las condiciones configuradas aquí aparecen como opciones en la pantalla **Definir Abonos** (3.47) y en otros contextos de venta en cuenta corriente.
- La tasa que se muestra en la grilla ya incluye el IVA correspondiente.
- El plazo define cuántos días tiene el cliente para pagar antes de que se aplique el interés.
