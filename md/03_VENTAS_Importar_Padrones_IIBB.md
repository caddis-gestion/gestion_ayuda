# 3.58 IMPORTAR PADRONES IIBB
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Importar Padrones IIBB

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Importar Padrones IIBB** permite cargar los padrones de Ingresos Brutos (percepciones y retenciones) publicados por las provincias. Una vez importados, el sistema aplica automáticamente las tasas correctas a cada cliente al facturar. Desde aquí podés:

- Seleccionar la provincia cuyo padrón querés importar
- Subir el archivo ZIP con el padrón descargado del organismo provincial
- Ejecutar la importación

---

<img src="imagenes/pantalla_importar_padrones_iibb.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Importar Padrones IIBB**

---

## Descripción general de la pantalla

La pantalla tiene un selector de provincia y un campo de selección de archivo.

---

## Formulario

| Campo / Botón | Descripción |
|---|---|
| **PROVINCIA** | Provincia cuyo padrón se va a importar |
| **Archivo ZIP** | Selector de archivo: elegí el ZIP con el padrón descargado del organismo recaudador provincial |
| **Importar Tasas de Percepciones de IIBB** | Botón que sube el archivo y ejecuta la importación |

---

## Paso a paso — Importar un padrón de IIBB

1. Descargá el padrón actualizado de la página web del organismo recaudador de la provincia correspondiente (ARBA, AGIP, API, etc.)
2. Seleccioná la **PROVINCIA** correcta en el selector
3. Hacé clic en el selector de **Archivo ZIP** y elegí el archivo descargado
4. Hacé clic en **Importar Tasas de Percepciones de IIBB**
5. El sistema procesa el archivo e informa el resultado

---

## Notas importantes

- Los padrones se publican periódicamente (generalmente cada mes o trimestre). Es importante mantenerlos actualizados para aplicar las tasas correctas.
- El formato del archivo ZIP varía según la provincia. Cada provincia publica su padrón en el formato estándar que el sistema reconoce.
- Los CUITs que tengan configurada una excepción en **Exceptuar IIBB** (3.53) mantienen su configuración particular incluso después de importar el padrón.
- Para verificar las tasas aplicadas a un cliente específico, usá **Consultar Límites de Créditos** o la ficha del cliente.
