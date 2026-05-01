# 4.10 PROVEEDORES
### Módulo 4 — Compras

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Compras → Proveedores

---
<img src="imagenes/pantalla_abm_proveedores.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Proveedores** permite gestionar el listado de proveedores del sistema. Desde aquí podés:

- Dar de alta nuevos proveedores
- Modificar los datos de un proveedor existente (razón social, CUIT, domicilio, condición impositiva, etc.)
- Desactivar proveedores que ya no se usan
- Buscar proveedores por nombre
- Consultar la constancia de inscripción en AFIP directamente desde la pantalla

---

## ¿Cómo acceder?

**Menú → Compras → Proveedores**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **CODIGO** | Número de código interno del proveedor (asignado automáticamente por el sistema, solo lectura). |
| **Estado** | Combo **ACTIVO / INACTIVO**. Un proveedor inactivo no aparece en los selectores del resto del sistema. |
| **PROVEEDOR** | Razón social del proveedor. |
| **FANTASIA** | Nombre de fantasía o comercial. |
| **CUIT / TAX ID** | CUIT (Argentina) o Tax ID (empresas extranjeras). |
| **E-MAIL** | Correo electrónico de contacto. |
| **DOMICILIO** | Dirección del proveedor. |
| **C.POSTAL** | Código postal. |
| **LOCALIDAD** | Ciudad o localidad. |
| **PAIS** | País de origen del proveedor. Al cambiar el país, se actualiza el combo de provincia. |
| **PROVINCIA** | Provincia o estado. |
| **TELEFONO** | Teléfono de contacto. |
| **TRANSPORTE** | Transportista habitual que usa el proveedor para enviar mercadería. |

### Sección: Datos Impositivos (solo para proveedores argentinos)

| Campo | Descripción |
|---|---|
| **IVA** | Condición frente al IVA del proveedor (Responsable Inscripto, Monotributista, Exento, etc.). Define qué tipo de factura emite. |
| **IIBB** | Condición de Ingresos Brutos del proveedor. |
| **IIBB Nº** | Número de inscripción en IIBB. |

### Sección: Filtro

Campo de búsqueda por nombre para filtrar el listado de proveedores en la grilla derecha.

---

## Botón: Ver en AFIP

Disponible solo para proveedores argentinos. Al hacer clic, abre la consulta de la constancia de inscripción del proveedor en el padrón de AFIP, usando el CUIT ingresado.

---

## Grilla de resultados

La grilla derecha muestra todos los proveedores del sistema con los siguientes datos:

| Columna | Descripción |
|---|---|
| Código | Código interno del proveedor. |
| Activo | Indica si el proveedor está activo o inactivo. |
| CUIT | CUIT o Tax ID. |
| Condición IVA | Tipo de IVA del proveedor. |
| Condición IIBB | Tipo de IIBB. |
| IIBB Nro | Número de IIBB. |
| Proveedor | Razón social. |
| Nombre Fantasía | Nombre comercial. |
| Domicilio | Dirección. |
| Localidad | Ciudad. |
| CP | Código postal. |
| Provincia | Provincia. |
| País | País. |
| Teléfono | Contacto telefónico. |
| Email | Correo electrónico. |
| Transporte | Transportista asignado. |

Desde la grilla se puede **modificar** o **borrar** cada proveedor.

---

## Flujo típico — Alta de proveedor

1. Acceder a **Compras → Proveedores**
2. Completar los campos: **PROVEEDOR**, **CUIT**, **IVA**, **IIBB**, domicilio y datos de contacto
3. Hacer clic en **Agregar** (botón de la barra de acciones)
4. El proveedor queda disponible en todo el sistema

---

## Notas importantes

- Los proveedores tienen códigos negativos (≤ −100) en la base de datos, lo que los diferencia de los depósitos y puntos de venta.
- La condición de **IVA** del proveedor define qué tipos de factura de compra se pueden registrar (Fact. A, B, C, NC, etc.).
- Para proveedores extranjeros (País ≠ AR), los campos impositivos se reemplazan por **TAX ID** y la moneda se toma de los parámetros de la empresa.
