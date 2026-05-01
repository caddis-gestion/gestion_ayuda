# 3.52 EMPRESAS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Empresas

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Empresas** permite administrar las empresas emisoras de comprobantes configuradas en el sistema. En entornos multi-empresa, cada empresa tiene sus propios datos fiscales y puede emitir facturas de forma independiente. Desde aquí podés:

- Ver y editar los datos de la empresa activa
- Agregar nuevas empresas (en entornos multi-empresa)
- Configurar los datos fiscales, domicilio y parámetros de facturación de crédito

> ⚠️ Esta pantalla es de uso administrativo. Modificar los datos incorrectamente puede afectar la facturación electrónica.

---

<img src="imagenes/pantalla_empresas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Empresas**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario completo de la empresa y un panel derecho con la grilla de empresas existentes.

---

## Panel izquierdo — Formulario

### Sección Datos Empresa

| Campo | Descripción |
|---|---|
| **NOMBRE** | Razón social de la empresa |
| **NOMBRE FANTASIA** | Nombre comercial (puede diferir de la razón social) |
| **CUIT** | CUIT de la empresa |
| **INSC.IIBB** | Número de inscripción en Ingresos Brutos |
| **IVA** | Condición frente al IVA (Responsable Inscripto, Monotributista, etc.) |
| **INICIO ACTIV.** | Fecha de inicio de actividades |
| **ALIAS** | Alias interno de la empresa en el sistema (sólo editable por soporte técnico) |
| **LOGO** | Ruta o nombre del archivo de logo de la empresa |

### Sección Datos Domicilio

| Campo | Descripción |
|---|---|
| **PAIS** | País de la empresa |
| **PROVINCIA** | Provincia |
| **LOCALIDAD** | Localidad |
| **C.POSTAL** | Código postal |
| **DOMICILIO** | Dirección fiscal |
| **E-MAIL** | Correo electrónico de la empresa |
| **TELEFONO** | Teléfono de la empresa |

### Sección Datos Envío

| Campo | Descripción |
|---|---|
| **DOMICILIO ENVIO** | Domicilio de envío (para remitos y documentación) |

### Sección Facturas de Crédito

| Campo | Descripción |
|---|---|
| **PYME CBU** | CBU de la cuenta bancaria para Facturas de Crédito Electrónicas MiPyME |
| **PYME TRANSMISION** | Modalidad de transmisión: **SCA** (Sistema de Circulación Abierta) o **ADC** (Agente de Depósito Colectivo) |

---

## Panel derecho — Grilla de empresas

Muestra todas las empresas configuradas en el sistema:

| Columna | Descripción |
|---|---|
| Id | Identificador de la empresa |
| CUIT | CUIT de la empresa |
| IIBB | Número de inscripción IIBB |
| IVA | Condición IVA |
| Nombre | Razón social |
| Activo Facturar | Indica si la empresa puede facturar (SI/NO) |
| País, Provincia, Localidad, CPostal, Domicilio | Datos de domicilio |
| Email, Telefono | Contacto |
| Inicio Act. | Fecha de inicio de actividades |
| Alias, Logo | Configuración interna |
| Pyme CBU, Pyme Trans. | Datos de facturas de crédito |

**Acciones disponibles:**
- **Modificar:** Edita los datos de la empresa
- **Borrar:** Elimina la empresa

---

## Notas importantes

- El campo **ALIAS** solo puede ser modificado por el soporte técnico de Caddis.
- Los datos de **FACTURAS DE CRÉDITO** son necesarios solo si la empresa emite Facturas de Crédito Electrónicas MiPyME.
- Modificar el CUIT o los datos fiscales requiere coordinación con AFIP para actualizar los certificados digitales.
