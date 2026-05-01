# 3.38 CAI PARAMETROS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → CAI Parametros

---

## ¿Para qué sirve esta pantalla?

La pantalla de **CAI Parametros** permite configurar y gestionar los datos del CAI (Código de Autorización de Impresión) para los talonarios de comprobantes de papel (remitos y comprobantes no electrónicos). Desde aquí podés:

- Registrar un nuevo CAI con su rango de numeración y fecha de vencimiento
- Consultar el estado de los CAI vigentes (Ok, Vencido, En error)
- Modificar o eliminar registros de CAI existentes

> ℹ️ El CAI es el código que AFIP otorga para autorizar la impresión de talonarios de papel (remitos, comprobantes internos, etc.). No aplica a comprobantes electrónicos.

---

<img src="imagenes/pantalla_cai_parametros.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → CAI Parametros**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de carga y un panel derecho con la grilla de CAI registrados.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **ZONA** | Zona operativa (si aplica). Al seleccionar una zona, el filtro PDV se oculta. |
| **PDV** | Punto de venta al que corresponde el CAI (cuando no se usa Zona) |
| **TIPO** | Tipo de comprobante: **RM** (Remito) o **R** (Remito interno) |
| **CAI** | Número de CAI otorgado por AFIP (hasta 14 caracteres) |
| **VENCE** | Fecha de vencimiento del CAI |
| **DESDE** | Número inicial del rango de comprobantes autorizado |
| **HASTA** | Número final del rango de comprobantes autorizado |

---

## Panel derecho — Grilla de CAI

Muestra todos los CAI registrados para el PDV o Zona seleccionada:

| Columna | Descripción |
|---|---|
| POS / Zona | Punto de venta o zona a la que pertenece el CAI |
| CAI Nro | Número de CAI |
| CAI Vto | Fecha de vencimiento |
| Factura Tipo | Tipo de comprobante (RM, R) |
| Factura Desde | Número inicial del rango |
| Factura Hasta | Número final del rango |
| Proxima | Próximo número a utilizar |
| **Estado** | Estado del CAI: **Ok** (vigente y dentro del rango), **Vencido** (fecha superada), **En error** (próximo número fuera del rango). Resaltado en amarillo. |

**Acciones disponibles:**
- **Modificar:** Edita los datos del CAI seleccionado
- **Borrar:** Elimina el registro de CAI

---

## Paso a paso — Registrar un nuevo CAI

1. Seleccioná el **PDV** (o la **ZONA** si corresponde)
2. Elegí el **TIPO** de comprobante (RM o R)
3. Ingresá el número de **CAI** tal como figura en la autorización de AFIP
4. Ingresá la fecha de **VENCIMIENTO**
5. Completá los campos **DESDE** y **HASTA** con el rango de numeración autorizado
6. Guardá el registro

---

## Notas importantes

- El sistema marca en **amarillo** los CAI con estado distinto de "Ok" para facilitar la identificación de talonarios vencidos o con errores.
- Cuando el próximo número a emitir supera el **HASTA** del rango, el estado pasa a "En error" y es necesario registrar un nuevo CAI.
- Si el CAI está **Vencido**, tampoco se pueden emitir comprobantes con ese talonario, aunque queden números disponibles.
