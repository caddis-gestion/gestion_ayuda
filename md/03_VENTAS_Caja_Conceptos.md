# 3.35 CAJA CONCEPTOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Caja → Caja Conceptos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Caja Conceptos** permite administrar los conceptos disponibles para los movimientos manuales de caja. Estos conceptos aparecen como opciones en el campo **CONCEPTO** de la pantalla **Caja Movimientos** (3.28). Desde aquí podés:

- Agregar nuevos conceptos de caja (ej. "Gastos de envío", "Adelanto de sueldo", "Fondo de caja")
- Modificar el nombre de un concepto existente
- Eliminar conceptos que ya no se usan

---

<img src="imagenes/pantalla_caja_conceptos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Caja → Caja Conceptos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de carga y un panel derecho con la grilla de conceptos existentes.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código numérico del concepto. Se asigna automáticamente al guardar; campo de sólo lectura. |
| **CONCEPTO** | Nombre descriptivo del concepto (ej. "Viáticos", "Gastos varios", "Fondo cambio") |

---

## Panel derecho — Grilla de conceptos

Muestra todos los conceptos de caja configurados en el sistema:

| Columna | Descripción |
|---|---|
| Codigo | Código numérico del concepto |
| Concepto | Nombre del concepto |

**Acciones disponibles:**
- **Modificar:** Carga el concepto en el formulario para editar su nombre
- **Borrar:** Elimina el concepto de la lista

---

## Paso a paso — Agregar un nuevo concepto

1. En el campo **CONCEPTO**, escribí el nombre del nuevo concepto
2. Guardá el registro
3. El sistema asigna automáticamente un **CODIGO** y el concepto aparece en la grilla

---

## Notas importantes

- Los conceptos configurados aquí son los que aparecen en el selector **CONCEPTO** de **Caja Movimientos** (3.28).
- No se pueden eliminar conceptos que ya estén siendo utilizados en movimientos de caja registrados.
- Es recomendable usar nombres claros y descriptivos para facilitar la identificación al momento de registrar los movimientos.
