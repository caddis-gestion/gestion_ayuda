# 15.07 SUPERVISORES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Supervisores

---
<img src="imagenes/pantalla_supervisores.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Supervisores** permite gestionar el listado de supervisores de la empresa. Los supervisores son el nivel jerárquico intermedio entre los vendedores y los jefes de ventas. Desde aquí podés:

- Dar de alta nuevos supervisores
- Modificar los datos de un supervisor existente
- Activar o desactivar supervisores
- Asignar el gerente y jefe de ventas al que reporta el supervisor

---

## ¿Cómo acceder?

**Menú → Administración → Supervisores**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno del supervisor (asignado automáticamente, solo lectura). |
| **Estado** | **ACTIVO / INACTIVO**. Un supervisor inactivo no aparece en los selectores. |
| **NOMBRE** | Nombre completo del supervisor. |
| **DNI** | Número de DNI. |
| **LEGAJO** | Número de legajo interno. |
| **CUIT** | CUIT del supervisor. |
| **CATEGORIA** | Categoría laboral. |
| **GERENTE** | Gerente al que reporta este supervisor. |
| **JEFE.VENTAS** | Jefe de ventas (Sub-Gerente) al que reporta. Se filtra según el gerente seleccionado. |
| **INGRESO** | Fecha de ingreso a la empresa. |
| **EGRESO** | Fecha de egreso (si aplica). |
| **BASICO FIJO** | Ingreso fijo mensual. |
| **ABSORBIBLE** | Monto absorbible por comisiones/variables. |
| **DOMICILIO** | Dirección del supervisor. |
| **TELEFONO** | Teléfono de contacto. |
| **E-MAIL** | Correo electrónico. |
| **EMPRESA** | Empresa a la que pertenece (en entornos multi-empresa). |
| **USUARIO.ASOC** | Usuario del sistema vinculado a este supervisor. |

---

## Grilla de supervisores

Muestra todos los supervisores registrados con: código, nombre, legajo/DNI, fecha de ingreso, ingreso fijo, ingreso variable, categoría y estado activo/inactivo.

---

## Flujo típico — Alta de supervisor

1. Acceder a **Administración → Supervisores**
2. Completar **NOMBRE**, **DNI**, **LEGAJO**, **CATEGORIA**
3. Seleccionar el **GERENTE** y **JEFE.VENTAS** al que reporta
4. Ingresar **BASICO FIJO** y datos de contacto
5. Asociar el **USUARIO.ASOC** del sistema
6. Hacer clic en **Agregar**

---

## Notas importantes

- La jerarquía del sistema es: Gerente → Jefe de Ventas (Sub-Gerente) → Supervisor → Vendedor.
- Al seleccionar el **GERENTE**, el combo de **JEFE.VENTAS** se filtra automáticamente mostrando solo los jefes de ventas que dependen de ese gerente.
- Ver también: [**Jefes de Ventas**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_SubGerentes.pdf) (15.08) y [**Gerentes**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Gerentes.pdf) (15.09).
