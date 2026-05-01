# 15.17 CONCEPTOS DE CAJA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Conceptos de Caja

---
<img src="imagenes/pantalla_conceptos_caja.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Conceptos de Caja** permite gestionar los conceptos utilizados para registrar movimientos de caja que no son cobros ni pagos directos (ej: gastos varios, retiros, depósitos en banco). Desde aquí podés:

- Dar de alta nuevos conceptos de caja
- Modificar el nombre, grupo y signo de un concepto existente
- Eliminar conceptos que ya no se usen

---

## ¿Cómo acceder?

**Menú → Administración → Conceptos de Caja**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno del concepto (hasta 5 caracteres). |
| **NOMBRE** | Nombre descriptivo del concepto (hasta 50 caracteres). Ej: "Gasto limpieza", "Retiro de efectivo". |
| **GRUPO** | Grupo al que pertenece el concepto (para agrupar en informes). Los grupos son categorías predefinidas en el sistema. |
| **SIGNO** | Define si el concepto **PAGA** (egreso de caja, suma al gasto) o **DESCUENTA** (ingreso a caja, reduce el saldo). |

---

## Grilla de conceptos

Muestra todos los conceptos de caja registrados con:

| Columna | Descripción |
|---|---|
| Código | Código del concepto. |
| Concepto | Nombre del concepto. |
| Grupo | Grupo al que pertenece. |

---

## Flujo típico — Alta de concepto

1. Acceder a **Administración → Conceptos de Caja**
2. Ingresar el **CODIGO** y el **NOMBRE**
3. Seleccionar el **GRUPO** correspondiente
4. Elegir el **SIGNO**: PAGA (egreso) o DESCUENTA (ingreso)
5. Hacer clic en **Agregar**

---

## Notas importantes

- Los conceptos de caja se usan en los movimientos manuales de caja (egresos e ingresos varios).
- El **SIGNO** determina cómo impacta el movimiento en el saldo de la caja: **PAGA** reduce el saldo (es un egreso), **DESCUENTA** lo aumenta (es un ingreso).
- Los grupos permiten clasificar los conceptos para los informes de caja.
