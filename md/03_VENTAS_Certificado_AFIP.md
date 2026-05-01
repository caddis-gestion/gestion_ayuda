# 3.41 CERTIFICADO AFIP
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Abril 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Certificado AFIP

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Certificado AFIP** permite gestionar el certificado digital necesario para la facturación electrónica. El certificado es la "llave" que autoriza a Caddis a comunicarse con el Web Service de AFIP para emitir facturas electrónicas (A, B, C).

Desde aquí podés:

- Generar el archivo de solicitud (`.ped`) para enviar a AFIP
- Importar el certificado digital (`.crt`) otorgado por AFIP
- Verificar que el certificado esté activo y funcionando correctamente

> ⚠️ Esta pantalla es de uso técnico-administrativo. Normalmente sólo se usa cuando el certificado digital está por vencer o al configurar una nueva empresa para facturación electrónica.

---

<img src="imagenes/pantalla_certificado_afip.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Certificado AFIP**

---

## Descripción general de la pantalla

La pantalla muestra los tres pasos del proceso de renovación del certificado digital, más un área de texto con el resultado de las operaciones.

---

## Selector de empresa

| Campo | Descripción |
|---|---|
| **EMPRESA** | Seleccioná la empresa para la que se gestionará el certificado (en entornos multi-empresa) |

---

## Proceso completo — Renovar el certificado AFIP

El proceso tiene dos partes: una acción en Caddis, luego pasos en el portal de AFIP, y finalmente volver a Caddis.

### Parte 1 — En Caddis: descargar el archivo request

<img src="imagenes/cert_afip_caddis_paso1.png" style="width:auto; height:auto; max-width:100%; max-height:450px; display:block;">

Hacé clic en **"Crear archivo request"** (PASO #1). El sistema genera y descarga un archivo comprimido `.zip` que contiene el archivo `.ped`.

1. Descomprimí el `.zip` descargado
2. Guardá el archivo `.ped` en un lugar accesible (por ejemplo, el escritorio)

---

### Parte 2 — En el portal AFIP: crear el certificado digital

Ingresá a [www.afip.gob.ar](https://www.afip.gob.ar) con el CUIT y Clave Fiscal del titular de la empresa.

**Paso 2.1 — Ir a Administración de Certificados Digitales**

<img src="imagenes/cert_afip_afip_mis_servicios.png" style="width:100%; height:auto; display:block;">

En "Mis servicios", buscá y hacé clic en **Administración de Certificados Digitales**.

---

**Paso 2.2 — Seleccionar el alias existente**

<img src="imagenes/cert_afip_afip_alias.png" style="width:100%; height:auto; display:block;">

Verás la lista de alias configurados. Hacé clic en **Ver** junto al alias de Caddis (generalmente llamado `FcElectronicaXX` o similar).

> Si no existe ningún alias, hacé clic en **Agregar alias** y creá uno nuevo con el nombre que prefieras.

---

**Paso 2.3 — Ver el detalle del alias**

<img src="imagenes/cert_afip_afip_alias_detalle.png" style="width:100%; height:auto; display:block;">

En el detalle del alias podés ver los certificados vigentes y su fecha de vencimiento. Para agregar el nuevo certificado hacé clic en **Agregar Certificado**.

---

**Paso 2.4 — Subir el archivo .ped**

<img src="imagenes/cert_afip_afip_subir_ped.png" style="width:100%; height:auto; display:block;">

Seleccioná el archivo `.ped` generado en el Paso 1 y confirmá la operación. AFIP procesará el archivo y generará el nuevo certificado `.crt`. Descargá el `.crt` a tu computadora.

---

### Parte 3 — En Caddis: importar y verificar el certificado

**Paso 3.1 — Importar el certificado (.crt)**

<img src="imagenes/cert_afip_caddis_paso2.png" style="width:auto; height:auto; max-width:100%; max-height:450px; display:block;">

1. Hacé clic en **"Seleccionar archivo"** y elegí el `.crt` descargado de AFIP
2. Hacé clic en **"Importar certificado"** (PASO #2)

El sistema mostrará un mensaje confirmando que el certificado fue importado correctamente.

---

**Paso 3.2 — Verificar el estado del servicio**

<img src="imagenes/cert_afip_caddis_paso3_ok.png" style="width:auto; height:auto; max-width:100%; max-height:500px; display:block;">

Hacé clic en **"Verificar estado del servicio"** (PASO #3). En el área de texto aparecerá el resultado:

- **Certificado: OK** — el certificado está activo y vigente
- **Ticket de acceso: OK** — la comunicación con AFIP funciona correctamente
- Se listan los PDV habilitados con su estado (`Bloqueado: N` = funcionando)

---

## Configuración inicial — Pasos previos en AFIP

> Estos pasos sólo son necesarios la **primera vez** que se configura la facturación electrónica para una empresa, o si se cambia el alias/representante en AFIP. En renovaciones posteriores del certificado no es necesario repetirlos.

### A — Adherir al servicio de Facturación Electrónica

Este paso autoriza a tu usuario de AFIP a usar el Web Service de facturación electrónica en nombre de la empresa.

**A.1 — Ir a Administrador de Relaciones de Clave Fiscal**

<img src="imagenes/cert_afip_afip_mis_servicios_pve.png" style="width:100%; height:auto; display:block;">

En "Mis servicios", hacé clic en **Administrador de Relaciones de Clave Fiscal**.

---

**A.2 — Nueva relación → WebServices**

<img src="imagenes/cert_afip_afip_admin_relaciones.png" style="width:100%; height:auto; display:block;">

Hacé clic en **Nueva Relación**. En la sección "Servicios Habilitados", seleccioná **WebServices**.

---

**A.3 — Buscar el servicio de Facturación Electrónica**

<img src="imagenes/cert_afip_afip_lista_fe.png" style="width:auto; height:auto; max-width:100%; max-height:400px; display:block;">

En la lista de WebServices, buscá y seleccioná **Facturación Electrónica** (wsfev1).

---

**A.4 — Confirmar la incorporación**

<img src="imagenes/cert_afip_afip_incorporar_relacion.png" style="width:100%; height:auto; display:block;">

Verificá que los campos Autorizante y Representado correspondan a la empresa correcta, y confirmá la operación haciendo clic en **Confirmar**.

---

### B — Adherir al servicio de Administración de Certificados Digitales

Repetí los mismos pasos A.1 a A.4, pero en A.3 buscá y seleccioná el servicio **Administración de Certificados Digitales** en lugar de Facturación Electrónica.

<img src="imagenes/cert_afip_afip_lista_cert_admin.png" style="width:auto; height:auto; max-width:100%; max-height:400px; display:block;">

---

### C — Administración de Puntos de Venta en AFIP

Los puntos de venta deben estar dados de alta en AFIP para poder emitir comprobantes electrónicos.

**C.1 — Ir a Administración de Puntos de Venta y Domicilios**

En "Mis servicios", hacé clic en **Administración de Puntos de Venta y Domicilios**.

<img src="imagenes/cert_afip_afip_pve_empresa.png" style="width:100%; height:auto; display:block;">

Seleccioná la empresa a representar.

---

**C.2 — Alta y gestión de puntos de venta**

<img src="imagenes/cert_afip_afip_pve_menu.png" style="width:100%; height:auto; display:block;">

Desde el menú principal del PVE podés:

- **A/B/M de puntos de venta**: dar de alta, modificar o baja puntos de venta
- **Domicilio - Punto Venta - Vincular**: asociar un domicilio fiscal a cada punto de venta

> Cada PDV configurado en Caddis debe tener su correspondiente punto de venta dado de alta en AFIP con el mismo número.

---

## Área de resultado

El cuadro de texto de sólo lectura muestra el resultado de las operaciones realizadas (mensajes de éxito, errores, estado del servicio, etc.).

---

## Notas importantes

- Los certificados digitales de AFIP tienen una vigencia de **2 años**. Es recomendable renovarlos con anticipación antes del vencimiento.
- Si el certificado vence, el sistema no puede emitir comprobantes electrónicos hasta que se renueve.
- El proceso requiere acceso al portal de AFIP con **clave fiscal nivel 3** del titular de la empresa.
- Cada empresa en un entorno multi-empresa tiene su propio certificado. El selector EMPRESA en la pantalla permite gestionar cada uno por separado.
- En caso de dudas durante la renovación, contactá al soporte técnico de Caddis.
