# 15.08 JEFES DE VENTAS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Jefes de Ventas

---
<img src="imagenes/pantalla_subgerentes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Jefes de Ventas** (Sub-Gerentes) permite gestionar el listado de jefes de ventas de la empresa. Son el nivel jerárquico entre los supervisores y los gerentes. Desde aquí podés:

- Dar de alta nuevos jefes de ventas
- Modificar los datos de un jefe de ventas existente
- Activar o desactivar jefes de ventas
- Asignar el gerente al que reporta cada jefe de ventas

---

## ¿Cómo acceder?

**Menú → Administración → Jefes de Ventas**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno (asignado automáticamente, solo lectura). |
| **Estado** | **ACTIVO / INACTIVO**. Un jefe de ventas inactivo no aparece en los selectores. |
| **NOMBRE** | Nombre completo. |
| **DNI** | Número de DNI. |
| **LEGAJO** | Número de legajo interno. |
| **CATEGORIA** | Categoría laboral. |
| **GERENTE** | Gerente al que reporta este jefe de ventas. |
| **INGRESO** | Fecha de ingreso a la empresa. |
| **EGRESO** | Fecha de egreso (si aplica). |
| **BASICO.FIJO** | Ingreso fijo mensual. |
| **ABSORBIBLE** | Monto absorbible por variables/comisiones. |
| **E-MAIL** | Correo electrónico. |
| **EMPRESA** | Empresa a la que pertenece (en entornos multi-empresa). |
| **USUARIO.ASOC** | Usuario del sistema vinculado a este jefe de ventas. |

---

## Grilla de jefes de ventas

Muestra todos los jefes de ventas registrados con: código, nombre, DNI/legajo, fecha de ingreso, ingreso fijo, ingreso variable, categoría y estado activo/inactivo.

---

## Flujo típico — Alta de jefe de ventas

1. Acceder a **Administración → Jefes de Ventas**
2. Completar **NOMBRE**, **DNI**, **LEGAJO**, **CATEGORIA**
3. Seleccionar el **GERENTE** al que reporta
4. Ingresar **BASICO.FIJO** y datos de contacto
5. Asociar el **USUARIO.ASOC** del sistema
6. Hacer clic en **Agregar**

---

## Notas importantes

- La jerarquía del sistema es: Gerente → Jefe de Ventas → Supervisor → Vendedor.
- El jefe de ventas aparece como **JEFE.VENTAS** en la pantalla de Supervisores, donde cada supervisor queda asignado a uno.
- Ver también: [**Supervisores**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Supervisores.pdf) (15.07) y [**Gerentes**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Gerentes.pdf) (15.09).
