# 15.37 ABM PROVEEDORES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Proveedores → ABM Proveedores

---

## ¿Para qué sirve esta pantalla?

Permite administrar el maestro de proveedores del sistema. Desde aquí se crean, modifican y desactivan los proveedores que abastecen a la empresa. Cada proveedor almacena sus datos de identificación, contacto, domicilio, condición impositiva y datos logísticos, y luego puede asociarse a compras, órdenes de pago y cuenta corriente.

> **Nota:** Esta pantalla gestiona el registro maestro de proveedores desde el módulo Administración. Para registrar facturas de compras o gestionar la cuenta corriente de un proveedor, véase el módulo Compras.

---

<img src="imagenes/pantalla_admin_proveedores.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Proveedores → ABM Proveedores**

---

## Panel izquierdo — Datos del proveedor

### Identificación

| Campo | Descripción |
|---|---|
| CODIGO | Código numérico asignado automáticamente por el sistema (solo lectura). |
| Estado | Estado del proveedor: **ACTIVO** / **INACTIVO**. Se muestra junto al código. |
| PROVEEDOR | Razón social del proveedor (máximo 100 caracteres). |
| FANTASIA | Nombre de fantasía o nombre comercial (máximo 100 caracteres). |
| CUIT / TAX ID | CUIT (Argentina) o identificador fiscal (otros países) del proveedor (máximo 11 caracteres). Incluye botón **Ver en AFIP** para consultar la constancia de inscripción (solo Argentina). |
| E-MAIL | Correo electrónico de contacto (máximo 50 caracteres). |

### Domicilio

| Campo | Descripción |
|---|---|
| DOMICILIO | Dirección del proveedor (máximo 100 caracteres). |
| C.POSTAL | Código postal (máximo 10 caracteres). |
| LOCALIDAD | Localidad (máximo 100 caracteres). |
| PAIS | País del proveedor. Al cambiar el país se actualiza la lista de provincias. |
| PROVINCIA | Provincia del proveedor (filtrada según el país seleccionado). |
| TELEFONO | Teléfono de contacto (máximo 50 caracteres). |
| TRANSPORTE | Nombre del transportista habitual del proveedor (máximo 100 caracteres). |

### Datos impositivos (solo Argentina)

Esta sección aparece cuando el país seleccionado es Argentina.

| Campo | Descripción |
|---|---|
| IVA | Condición frente al IVA del proveedor (ej: Responsable Inscripto, Monotributista, etc.). |
| IIBB | Condición de Ingresos Brutos del proveedor. |
| IIBB Nro | Número de inscripción en Ingresos Brutos (máximo 13 caracteres). |

### Relación con proveedor en USA (si aplica)

En instalaciones con el módulo de importación USA activo, aparece una sección adicional para asociar al proveedor local con su correspondiente en Estados Unidos.

### Filtro de búsqueda

El panel incluye un campo de texto para filtrar la grilla de proveedores por nombre, permitiendo localizar rápidamente un proveedor específico.

### Botones de acción

| Botón | Descripción |
|---|---|
| Agregar | Crea un nuevo proveedor con los datos ingresados. |
| Modificar | Guarda los cambios sobre el proveedor seleccionado. |
| Borrar | Elimina el proveedor seleccionado. |
| Ver en AFIP | Consulta la constancia de inscripción del proveedor en la web de AFIP (solo Argentina). |

---

## Grilla derecha — Lista de proveedores

Muestra todos los proveedores registrados con sus datos principales:

| Columna | Descripción |
|---|---|
| Código | Código único del proveedor. |
| Activo | Indica si el proveedor está activo (SI/NO). |
| CUIT | Número de CUIT o identificador fiscal. |
| Condición IVA | Condición frente al IVA. |
| Condición IIBB | Condición de Ingresos Brutos. |
| IIBB Nro | Número de IIBB. |
| Proveedor | Razón social. |
| Nombre Fantasía | Nombre comercial. |
| Domicilio | Dirección del proveedor. |
| Localidad | Localidad. |
| CP | Código postal. |
| Provincia | Provincia. |
| País | País. |
| Teléfono | Teléfono de contacto. |
| Email | Correo electrónico. |
| Transporte | Transportista habitual. |
| (botones) | Acciones disponibles: **Modificar** / **Borrar** |

> **Tip:** Usá el campo de filtro en el panel izquierdo para buscar proveedores por nombre. Para modificar un proveedor, hacé clic en el botón Modificar de la fila correspondiente.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
