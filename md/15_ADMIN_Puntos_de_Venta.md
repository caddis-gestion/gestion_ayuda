# 15.34 PUNTOS DE VENTA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Estructura Comercial → Puntos de Venta

---

## ¿Para qué sirve esta pantalla?

Permite administrar los puntos de venta (PDV) de la empresa. Cada punto de venta representa una sucursal o local desde donde se opera el sistema. Aquí se definen sus datos generales, la jerarquía comercial asignada (gerente, jefe de ventas, supervisor), el almacén de stock vinculado y otros parámetros operativos.

---

<img src="imagenes/pantalla_admin_puntos_venta.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Estructura Comercial → Puntos de Venta**

---

## Panel izquierdo — Datos del punto de venta

### Datos generales

| Campo | Descripción |
|---|---|
| CODIGO | Código numérico asignado automáticamente por el sistema (solo lectura). |
| Estado | Estado del PDV: **ACTIVO** / **INACTIVO**. Se muestra junto al código. |
| NOMBRE | Nombre del punto de venta (máximo 50 caracteres). |
| EMPRESA | Empresa a la que pertenece el PDV (visible solo en entornos multi-empresa). |
| TIPO | Tipo de punto de venta. Se selecciona de la lista de tipos de PDV configurados. |

### Jerarquía comercial

| Campo | Descripción |
|---|---|
| GERENTE | Gerente asignado al PDV. |
| JEFE DE VENTAS | Jefe de ventas asignado (filtrado según el gerente elegido). |
| SUPERVISOR | Supervisor asignado (filtrado según gerente y jefe de ventas). |

### Datos operativos

| Campo | Descripción |
|---|---|
| INICIO DE ACTIVIDAD | Fecha en que el PDV comenzó a operar. |
| ZONA | Zona geográfica o comercial a la que pertenece el PDV. |
| ALMACEN | Almacén de stock vinculado al PDV. |
| CATEGORIA | Categoría comisional del PDV. |
| AUTOCOMISIONA | Indica si el PDV genera sus propias comisiones. Opciones: **SI** / **NO**. |

### Datos de contacto y domicilio

| Campo | Descripción |
|---|---|
| DOMICILIO | Dirección del punto de venta (máximo 100 caracteres). |
| C. POSTAL | Código postal (máximo 10 caracteres). |
| LOCALIDAD | Localidad del PDV (máximo 100 caracteres). |
| PROVINCIA | Provincia donde se ubica el PDV. |
| TELEFONO | Teléfono de contacto (máximo 50 caracteres). |
| E-MAIL | Correo electrónico del PDV (máximo 50 caracteres). |
| TRANSPORTISTA | Nombre del transportista habitual del PDV (máximo 100 caracteres). |

### Otros parámetros

| Campo | Descripción |
|---|---|
| FACTURADOR | Indica si el PDV tiene el módulo de facturación activado. Opciones: **ACTIVADO** / **INACTIVO**. Solo visible en instalaciones que no son de gestión pura. |
| REPARACIONES | Indica si el PDV opera el módulo de reparaciones. Opciones: **SI** / **NO**. Solo visible en instalaciones Argentina. |

### Botones de acción

| Botón | Descripción |
|---|---|
| Agregar | Crea un nuevo punto de venta con los datos ingresados. |
| Modificar | Guarda los cambios sobre el PDV seleccionado. |
| Borrar | Elimina el PDV seleccionado. |

---

## Grilla derecha — Lista de puntos de venta

Muestra todos los puntos de venta registrados en el sistema con sus datos principales.

> **Tip:** Para modificar un PDV, hacé clic en el botón Modificar de la fila correspondiente. Los datos se cargarán en el panel izquierdo para su edición.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
