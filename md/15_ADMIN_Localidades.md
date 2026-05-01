# 15.11 LOCALIDADES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Localidades

---
<img src="imagenes/pantalla_localidades.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Localidades** permite gestionar el listado de localidades disponibles en el sistema, organizadas por provincia. Las localidades se usan en los datos de domicilio de clientes, proveedores y puntos de venta. Desde aquí podés:

- Agregar nuevas localidades para una provincia
- Modificar el nombre, sublocalidad o código postal de una localidad existente
- Eliminar localidades que ya no se utilicen

---

## ¿Cómo acceder?

**Menú → Administración → Localidades**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PROVINCIA** | Selector de provincia. Al cambiar la provincia, la grilla se actualiza mostrando solo las localidades de esa provincia. |
| **LOCALIDAD** | Nombre de la localidad (hasta 50 caracteres). |
| **SUBLOCALIDAD** | Nombre de la sublocalidad o barrio (hasta 50 caracteres). Campo opcional. |
| **C.POSTAL** | Código postal de la localidad (hasta 4 caracteres). |

---

## Grilla de localidades

Muestra las localidades de la provincia seleccionada con:

| Columna | Descripción |
|---|---|
| Provincia | Nombre de la provincia. |
| Localidad | Nombre de la localidad. |
| Sublocalidad | Nombre de la sublocalidad (si aplica). |
| CPostal | Código postal. |

---

## Flujo típico — Alta de localidad

1. Seleccionar la **PROVINCIA** correspondiente
2. Ingresar el **NOMBRE** de la localidad y el **C.POSTAL**
3. Completar **SUBLOCALIDAD** si corresponde
4. Hacer clic en **Agregar**

---

## Notas importantes

- Las localidades están vinculadas a una provincia; al seleccionar la provincia, la grilla muestra solo las localidades de esa provincia.
- El sistema incluye una base de localidades preexistente. Solo agregar localidades nuevas si no están en el listado.
