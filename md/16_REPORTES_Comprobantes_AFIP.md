# 16.06 CONTROL DE COMPROBANTES AFIP
### Módulo 16 — Reportes

> **Versión:** 1.1 — Abril 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reportes → Comprobantes AFIP Control

---

## ¿Para qué sirve esta pantalla?

Permite controlar y conciliar los comprobantes electrónicos emitidos en AFIP contra los registros de Caddis. Detecta diferencias entre los importes declarados en AFIP y los calculados en Caddis, ayudando a identificar inconsistencias antes de presentar declaraciones juradas.

---

<img src="imagenes/pantalla_control_comprobantes_afip.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Reportes → Comprobantes AFIP Control**

---

## Filtros del panel izquierdo

| Campo | Descripción |
|---|---|
| PDV | Punto de venta / prefijo de comprobante electrónico |
| DESDE | Fecha de inicio |
| HASTA | Fecha de fin |
| ESTADO | TODO: muestra todos; EN ERROR: solo comprobantes con discrepancia |

Botón **Actualizar comprobantes AFIP**: consulta los servidores de AFIP y actualiza el estado de todos los comprobantes del PDV seleccionado para el período indicado. El proceso puede demorar unos segundos.

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| AFIP Tipo | Tipo de comprobante según AFIP |
| AFIP Comprobante | Número de comprobante en AFIP (punto de venta - número) |
| AFIP Importe Total | Importe declarado en AFIP |
| AFIP Doc Nro | CUIT/DNI del receptor según AFIP |
| AFIP Cliente | Nombre del receptor según AFIP (o "CONSUMIDOR FINAL") |
| AFIP Proceso | Fecha y hora en que AFIP procesó el comprobante |
| Caddis Importe Total | Importe calculado por Caddis |
| Caddis Factura Nro | Número de factura en Caddis |
| CAE Nro | Código de Autorización Electrónico |
| CAE Vto | Vencimiento del CAE |
| Caddis Doc Nro | CUIT/DNI según Caddis |
| Caddis Cliente | Nombre del cliente en Caddis |
| Caddis Usuario | Usuario que emitió el comprobante |
| Caddis Fecha | Fecha de emisión en Caddis |
| Semáforo | Verde: importes coinciden; Rojo: hay discrepancia |

---

## Acciones por comprobante

Cada fila de la grilla puede tener los siguientes botones de acción:

| Botón | Descripción |
|---|---|
| **Detalle AFIP** | Abre una ventana emergente con el detalle completo del comprobante consultado en AFIP en tiempo real |
| **Guardar Comprobante** | Abre una ventana emergente para registrar el CAE de un comprobante que fue emitido pero no quedó guardado en Caddis (ver sección siguiente) |
| **Imprimir** | Genera e imprime el comprobante en formato PDF |

> ⚠️ Los comprobantes marcados en **rojo** tienen diferencia entre el importe declarado en AFIP y el registrado en Caddis. Revisá el comprobante antes de presentar declaraciones juradas.

---

## Guardar comprobante no registrado

Cuando un comprobante fue enviado a AFIP y tiene asignado un número de factura, pero el CAE **no quedó guardado** en Caddis (por ejemplo por un corte de conexión durante la emisión), el botón **Guardar Comprobante** abre una ventana emergente que permite recuperar y registrar ese CAE.

### Datos que muestra la ventana

La ventana presenta dos bloques de información en paralelo:

**Datos de Caddis**

| Campo | Descripción |
|---|---|
| PDV | Punto de venta desde el que se emitió |
| Fc Tipo | Tipo de comprobante (FA, FB, FC, etc.) |
| Fc Nro | Número de factura en Caddis |
| Fc Fecha | Fecha de la factura |
| Cliente | Nombre del cliente |
| CUIT | CUIT del cliente en Caddis |
| TOTAL | Importe total calculado por Caddis |

**Datos de AFIP** *(consultados en tiempo real al abrir la ventana)*

| Campo | Descripción |
|---|---|
| FC A EMITIR | Número de comprobante registrado en AFIP (punto de venta - número) |
| CUIT | CUIT del receptor según AFIP |
| TOTAL AFIP | Importe total declarado en AFIP |
| CAE NRO | Código de Autorización Electrónico otorgado por AFIP |
| CAE VTO | Fecha de vencimiento del CAE |

### Validaciones antes de guardar

Al presionar **Guardar Comprobante**, el sistema verifica:

1. **Que exista una factura a emitir** — si el campo FC A EMITIR está vacío, no hay comprobante pendiente y no es posible guardar
2. **Que los importes coincidan** — si el TOTAL de Caddis no coincide con el TOTAL AFIP, el sistema muestra un aviso y no permite guardar
3. **Que los CUIT coincidan** — si el CUIT del cliente en Caddis difiere del reportado por AFIP, el sistema muestra un aviso y no permite guardar
4. **Confirmación manual** — el sistema solicita confirmar antes de ejecutar el guardado

Una vez guardado exitosamente, el sistema registra el CAE en Caddis, genera el comprobante impreso y cierra la ventana actualizando la grilla principal.

---

## Editar CAE directamente en la grilla

Las columnas **CAE Nro** y **CAE Vto** son editables directamente en la grilla, lo que permite corregir manualmente un CAE mal registrado sin necesidad de anular el comprobante.

| Columna editable | Validación |
|---|---|
| **CAE Nro** | Debe tener exactamente 14 dígitos numéricos |
| **CAE Vto** | Debe ser una fecha válida |

> Esta funcionalidad está pensada para correcciones puntuales. Si hay diferencia en importe o CUIT entre Caddis y AFIP, primero investigá la causa antes de editar el CAE manualmente.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.1 — Abril 2026*
