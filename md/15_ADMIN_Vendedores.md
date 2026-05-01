# 15.06 VENDEDORES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Vendedores

---
<img src="imagenes/pantalla_vendedores.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Vendedores** permite gestionar el listado de vendedores de la empresa. Desde aquí podés:

- Dar de alta nuevos vendedores
- Modificar los datos de un vendedor existente
- Activar o desactivar vendedores
- Asociar el vendedor a un usuario del sistema y a un punto de venta

---

## ¿Cómo acceder?

**Menú → Administración → Vendedores**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno del vendedor (asignado automáticamente, solo lectura). |
| **Estado** | **ACTIVO / INACTIVO**. Un vendedor inactivo no aparece en los selectores del sistema. |
| **NOMBRE** | Nombre completo del vendedor. |
| **DNI** | Número de DNI. |
| **NACIMIENTO** | Fecha de nacimiento. |
| **CUIT** | CUIT del vendedor. |
| **LEGAJO** | Número de legajo interno. |
| **LIBRE** | Indica si el vendedor puede operar en más de un punto de venta. Si está activo, el vendedor aparece en el listado de vendedores de la pantalla Facturación independientemente del PDV seleccionado por el usuario. |
| **CATEGORIA** | Categoría laboral del vendedor. |
| **PDV** | Punto de venta donde trabaja habitualmente el vendedor. |
| **IVA** | Condición frente al IVA del vendedor (para liquidaciones). |
| **FECHA INGRESO** | Fecha de ingreso a la empresa. |
| **FECHA EGRESO** | Fecha de egreso (si aplica). |
| **BASICO FIJO** | Sueldo básico fijo mensual. |
| **ABSORBIBLE** | Monto absorbible por comisiones. |
| **DOMICILIO** | Dirección del vendedor. |
| **TELEFONO** | Teléfono de contacto. |
| **E-MAIL** | Correo electrónico. |
| **USUARIO ASOCIADO** | Usuario del sistema vinculado a este vendedor. |

---

## Grilla de vendedores

Muestra todos los vendedores registrados con sus datos principales: código, nombre, legajo, PDV asignado, categoría, ingreso fijo, ingreso variable y estado activo/inactivo.

---

## Flujo típico — Alta de vendedor

1. Acceder a **Administración → Vendedores**
2. Completar los campos obligatorios: **NOMBRE**, **DNI**, **CATEGORIA**, **PDV**
3. Ingresar **BASICO FIJO** y **ABSORBIBLE** si corresponde
4. Asociar el **USUARIO** del sistema
5. Hacer clic en **Agregar**

---

## Notas importantes

- El vendedor debe estar asociado a un **USUARIO** del sistema para poder iniciar sesión y operar.
- El campo **ABSORBIBLE** define el monto de sueldo fijo que se absorbe cuando el vendedor alcanza cierto nivel de comisiones.
- Para configurar supervisores, ver [**Supervisores**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Supervisores.pdf) (15.07).
