# 15.14 DATOS DE LA EMPRESA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Datos de la Empresa

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Datos de la Empresa** permite gestionar la información fiscal, domiciliaria y de facturación de la empresa (o empresas, en sistemas multi-empresa). Estos datos se usan en los comprobantes emitidos y en las integraciones con AFIP. Desde aquí podés:

- Configurar los datos fiscales de la empresa (CUIT, condición IVA, IIBB)
- Actualizar domicilio, contacto y logo
- Configurar datos para Facturas de Crédito Electrónica PyME
- Activar o desactivar empresas para facturación (en entornos multi-empresa)

---

## ¿Cómo acceder?

**Menú → Administración → Datos de la Empresa**

---

## Campos del formulario

### Datos Generales

| Campo | Descripción |
|---|---|
| **NOMBRE** | Razón social de la empresa. Aparece en los comprobantes. |
| **NOMBRE FANTASIA** | Nombre comercial o de fantasía. |
| **CUIT** | CUIT de la empresa para AFIP. |
| **INSC. IIBB** | Número de inscripción en Ingresos Brutos. |
| **IVA** | Condición frente al IVA (Responsable Inscripto, Monotributista, Exento, etc.). |
| **INICIO ACTIV.** | Fecha de inicio de actividades ante AFIP. |
| **ALIAS** | Alias interno de la empresa en el sistema. Solo puede editarlo el soporte técnico. |
| **LOGO** | Imagen del logo de la empresa que aparece en los comprobantes impresos. |

### Datos Domicilio

| Campo | Descripción |
|---|---|
| **PAIS** | País de la empresa. |
| **PROVINCIA** | Provincia (se actualiza según el país seleccionado). |
| **LOCALIDAD** | Ciudad o localidad. |
| **C.POSTAL** | Código postal. |
| **DOMICILIO** | Dirección completa. |
| **E-MAIL** | Correo electrónico de contacto. |
| **TELEFONO** | Teléfono de contacto. |

### Datos Envío

| Campo | Descripción |
|---|---|
| **DOMICILIO ENVIO** | Domicilio alternativo para envíos (puede diferir del domicilio fiscal). |

### Facturas de Crédito PyME

| Campo | Descripción |
|---|---|
| **PYME CBU** | CBU de la cuenta bancaria para Facturas de Crédito Electrónica MiPyME. |
| **PYME TRANSMISION** | Modo de transmisión de la factura de crédito: **SCA** (Sistema de Circulación Abierta) o **ADC** (Agente de Depósito Colectivo). |

---

## Grilla de empresas

En entornos multi-empresa, muestra todas las empresas configuradas con sus datos principales: ID, CUIT, IIBB, IVA, nombre, estado activo para facturar, país, provincia, localidad, domicilio, etc.

---

## Notas importantes

- Los datos de esta pantalla se imprimen en los comprobantes de venta y se envían a AFIP en la facturación electrónica. Mantenerlos correctos y actualizados es fundamental.
- El **ALIAS** de la empresa lo gestiona exclusivamente el soporte técnico de Caddis; no debe modificarse por el usuario final.
- Para sistemas con una sola empresa, esta pantalla muestra y edita los datos de esa empresa directamente.
