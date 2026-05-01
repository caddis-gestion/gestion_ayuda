# 15.18 PERCEPCIONES IIBB
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Percepciones IIBB

---
<img src="imagenes/pantalla_perciibb.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Percepciones IIBB** (Ingresos Brutos) permite gestionar el padrón de contribuyentes sujetos a percepción y retención de IIBB por provincia. Desde aquí podés:

- Consultar si un proveedor o cliente está sujeto a percepción/retención de IIBB en una provincia
- Ver las tasas de percepción y retención vigentes para cada CUIT según el padrón
- Marcar excepciones para que el sistema no aplique percepción o retención a determinados contribuyentes
- Definir la vigencia (desde/hasta) de cada excepción

---

## ¿Cómo acceder?

**Menú → Administración → Percepciones IIBB**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PROVINCIA** | Provincia del padrón de IIBB a consultar. |
| **CUIT** | CUIT del contribuyente a consultar o configurar. |
| **PERCEPCION %** | Tasa de percepción de IIBB aplicable (en porcentaje). |
| **RETENCION %** | Tasa de retención de IIBB aplicable (en porcentaje). |
| **EXCEPTUAR** | **SI / NO**. Si es SI, el sistema no aplica percepción/retención a ese CUIT aunque esté en el padrón. |
| **DESDE** | Fecha de inicio de la excepción (si aplica). |
| **HASTA** | Fecha de fin de la excepción (si aplica). |

---

## Grilla del padrón

Muestra los contribuyentes del padrón de la provincia seleccionada con:

| Columna | Descripción |
|---|---|
| CUIT | CUIT del contribuyente. |
| Nombre | Razón social. |
| Fecha | Fecha de actualización del padrón. |
| Tasa Percepción | Tasa de percepción según el padrón. |
| Tasa Retención | Tasa de retención según el padrón. |
| Excepción Percepción | Si tiene excepción de percepción configurada. |
| Excepción Retención | Si tiene excepción de retención configurada. |
| Exceptuar | SI/NO — indica si está excluido del cálculo automático. |
| Provincia | Provincia del padrón. |

---

## Notas importantes

- El padrón de IIBB se actualiza periódicamente con los datos publicados por cada provincia. El sistema calcula automáticamente la percepción/retención en las operaciones de compra y venta según este padrón.
- Si un contribuyente está en el padrón pero no corresponde aplicarle percepción/retención (por convenio o acuerdo), marcarlo como **EXCEPTUAR = SI** con el período de vigencia correspondiente.
- Las percepciones calculadas en facturas de compra se ven en la columna **PERC IIBB** de la pantalla de [**Facturas de Compra**](https://ayuda.caddis.com.ar/instructivos/04_COMPRAS_Facturas.pdf) (4.07).
