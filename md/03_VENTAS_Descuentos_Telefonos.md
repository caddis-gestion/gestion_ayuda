# 3.50 DESCUENTOS TELÉFONOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Descuentos Telefonos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Descuentos Teléfonos** permite asignar descuentos especiales a clientes mayoristas para modelos de teléfono específicos. El descuento se aplica automáticamente al facturar ese modelo al cliente. Desde aquí podés:

- Asignar un descuento a un cliente para un modelo de teléfono específico
- Consultar los descuentos por modelo ya asignados al cliente seleccionado
- Eliminar descuentos existentes

---

<img src="imagenes/pantalla_descuentos_telefonos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Descuentos Telefonos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de carga y un panel derecho con la grilla de descuentos del cliente seleccionado.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **CLIENTE** | Cliente mayorista al que se le asigna el descuento. Al seleccionarlo, la grilla muestra sus descuentos configurados. |
| **TELEFONOS** | Modelo de teléfono al que aplica el descuento (buscador de artículos/equipos) |
| **DESCUENTO** | Porcentaje de descuento a aplicar (ej. 3 para 3%) |

---

## Panel derecho — Grilla de descuentos

Muestra los descuentos por modelo asignados al cliente seleccionado, ordenados por marca y código:

| Columna | Descripción |
|---|---|
| Cliente | Nombre del cliente |
| Marca | Marca del teléfono |
| Modelo | Descripción del modelo |
| Descuento | Porcentaje de descuento asignado |

**Acciones disponibles:**
- **Borrar:** Elimina el descuento del cliente para ese modelo

---

## Paso a paso — Asignar un descuento por modelo

1. Seleccioná el **CLIENTE** mayorista
2. Buscá el modelo en el campo **TELEFONOS**
3. Ingresá el porcentaje de **DESCUENTO**
4. Guardá el registro

---

## Notas importantes

- Este tipo de descuento es más específico que el de **Descuentos Artículos** (3.49): aplica sólo a un modelo exacto, no a toda la categoría.
- Si el cliente tiene descuento por tipo de artículo y también por modelo específico, el sistema aplica el que corresponda según la configuración.
- Se pueden asignar múltiples descuentos por modelo para un mismo cliente (uno por cada modelo).
