# 15.09 GERENTES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Gerentes

---
<img src="imagenes/pantalla_gerentes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Gerentes** permite gestionar el listado de gerentes de la empresa. Son el nivel jerárquico más alto dentro del área comercial. Desde aquí podés:

- Dar de alta nuevos gerentes
- Modificar los datos de un gerente existente
- Activar o desactivar gerentes
- Asociar el gerente a un usuario del sistema

---

## ¿Cómo acceder?

**Menú → Administración → Gerentes**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno (asignado automáticamente, solo lectura). |
| **Estado** | **ACTIVO / INACTIVO**. Un gerente inactivo no aparece en los selectores. |
| **NOMBRE** | Nombre completo del gerente. |
| **DNI** | Número de DNI. |
| **LEGAJO** | Número de legajo interno. |
| **CATEGORIA** | Categoría laboral. |
| **INGRESO** | Fecha de ingreso a la empresa. |
| **EGRESO** | Fecha de egreso (si aplica). |
| **BASICO.FIJO** | Ingreso fijo mensual. |
| **ABSORBIBLE** | Monto absorbible por variables/comisiones. |
| **E-MAIL** | Correo electrónico. |
| **EMPRESA** | Empresa a la que pertenece (en entornos multi-empresa). |
| **USUARIO.ASOC** | Usuario del sistema vinculado a este gerente. |

---

## Grilla de gerentes

Muestra todos los gerentes registrados con: código, nombre, DNI/legajo, fecha de ingreso, ingreso fijo, ingreso variable, categoría y estado activo/inactivo.

---

## Flujo típico — Alta de gerente

1. Acceder a **Administración → Gerentes**
2. Completar **NOMBRE**, **DNI**, **LEGAJO**, **CATEGORIA**
3. Ingresar **BASICO.FIJO** y datos de contacto
4. Asociar el **USUARIO.ASOC** del sistema
5. Hacer clic en **Agregar**

---

## Notas importantes

- La jerarquía del sistema es: Gerente → Jefe de Ventas → Supervisor → Vendedor.
- El gerente aparece como filtro en varias pantallas del sistema (Acceso a Depósitos, Supervisores, etc.).
- Ver también: [**Jefes de Ventas**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_SubGerentes.pdf) (15.08) y [**Supervisores**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Supervisores.pdf) (15.07).
