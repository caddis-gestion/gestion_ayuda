# 3.57 IMPORTAR CLIENTES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Importar Clientes

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Importar Clientes** permite cargar masivamente clientes al sistema desde un archivo comprimido (ZIP). Es útil cuando se migra desde otro sistema o cuando se necesita dar de alta una gran cantidad de clientes de una sola vez. Desde aquí podés:

- Seleccionar el archivo ZIP con los datos de clientes a importar
- Ejecutar la importación masiva

---

<img src="imagenes/pantalla_importar_clientes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Importar Clientes**

---

## Formulario

| Campo / Botón | Descripción |
|---|---|
| **Archivo ZIP** | Selector de archivo: elegí el archivo ZIP que contiene el Excel con los datos de clientes |
| **Importar Clientes** | Sube el archivo y ejecuta la importación |
| **Formato** | Abre un popup con un ejemplo del formato requerido usando datos reales del sistema |

### Formato del archivo de importación

El archivo debe ser un **Excel (.xlsx)** con las siguientes columnas:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Cuit** | CUIT del cliente (sin guiones ni puntos) | 7, 8 u 11 dígitos |
| **Cliente** | Nombre o razón social | Texto libre |
| **Domicilio** | Domicilio del cliente | Texto libre |
| **Localidad** | Localidad del cliente | Texto libre |
| **Codigo Postal** | Código postal | Texto/número |
| **Provincia** | Nombre de la provincia | Debe coincidir con la tabla de provincias del sistema |
| **Pais** | Nombre del país | Debe coincidir con la tabla de países del sistema |
| **Telefono** | Teléfono de contacto | Texto libre |
| **EMail** | Correo electrónico | Texto libre |
| **Iva** | Código de condición de IVA | Código válido en el sistema (ej: `CF`, `RI`, `EX`) |
| **Vendedor** | Nombre del vendedor asignado | Debe coincidir con un vendedor existente |

#### Validaciones del sistema

- Los registros con CUIT o DNI que no tengan **7, 8 u 11 dígitos** se descartan y se muestran en el informe de errores.
- Los guiones y puntos del CUIT o DNI se eliminan automáticamente antes del control.
- La **Provincia** y el **País** se resuelven por nombre exacto; si no coinciden, el campo queda vacío.
- El **Vendedor** se resuelve por nombre exacto; si no coincide, queda sin vendedor asignado.

#### Comportamiento: clientes nuevos vs. existentes

| Situación | Qué hace el sistema |
|---|---|
| **CUIT no existe** | Inserta el cliente como nuevo con todos los campos informados |
| **CUIT ya existe** | Actualiza todos los campos: nombre, domicilio, localidad, CP, provincia, país, teléfono, email, IVA y vendedor |

---

## Notas importantes

- Usá el botón **Formato** para descargar un ejemplo con datos reales antes de preparar el archivo.
- La importación puede demorar varios minutos si el archivo contiene muchos registros.
- Esta pantalla es de uso ocasional y generalmente la utiliza el equipo de implementación.
