# 15.31 TRANSPORTES
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Administración → Logística → Transportes

---

## ¿Para qué sirve esta pantalla?

Permite administrar las empresas de transporte utilizadas para envíos y logística. Desde aquí se registran los datos completos de cada transportista (razón social, CUIT, domicilio, contacto) y se puede activar o desactivar cada uno según su estado operativo. La información registrada aquí es utilizada por el sistema al gestionar envíos y documentos logísticos.

---

<img src="imagenes/pantalla_transportes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Logística → Transportes**

---

## Panel izquierdo — Datos del transporte

| Campo | Descripción |
|---|---|
| CODIGO | Código asignado automáticamente por el sistema (solo lectura) |
| ESTADO | Estado del transporte: **ACTIVO** o **INACTIVO** |
| CUIT / DNI | Identificación fiscal de la empresa de transporte |
| NOMBRE | Razón social del transporte (máximo 50 caracteres) |
| DOMICILIO | Dirección de la empresa (máximo 50 caracteres) |
| LOCALIDAD | Localidad donde opera (máximo 30 caracteres) |
| C.POSTAL | Código postal |
| PAIS | País de la empresa (selector) |
| PROVINCIA | Provincia (selector, se filtra según el país seleccionado) |
| TELEFONO | Número de teléfono de contacto (máximo 50 caracteres) |
| E-MAIL | Correo electrónico de contacto (máximo 50 caracteres) |

### Botones de acción

| Botón | Descripción |
|---|---|
| Agregar | Crea un nuevo transporte con los datos ingresados |
| Modificar | Guarda los cambios sobre el transporte seleccionado |
| Borrar | Elimina el transporte seleccionado del sistema |

---

## Grilla derecha — Lista de transportes

Muestra todos los transportes registrados en el sistema:

| Columna | Descripción |
|---|---|
| Código | Código único del transporte |
| Activo | Indica si el transporte está activo: **SI** o **NO** |
| Transporte | Nombre (razón social) del transporte |
| Teléfono | Número de contacto |
| Email | Correo electrónico de contacto |
| (botones) | Acciones disponibles: **Modificar** / **Borrar** |

> **Tip:** Los transportes con estado **INACTIVO** no aparecen disponibles para selección en las pantallas operativas del sistema. Usá el campo **ESTADO** para habilitar o deshabilitar transportistas sin necesidad de eliminarlos.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
