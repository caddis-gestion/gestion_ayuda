# 3.29 COMPENSACIONES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Caja → Compensaciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Compensaciones** permite registrar adelantos de caja que se le entregan a un vendedor y que luego se descuentan automáticamente de su próxima rendición. Desde aquí podés:

- Registrar una compensación (adelanto) para un vendedor
- Consultar el historial de compensaciones de un vendedor
- Importar compensaciones en forma masiva desde un archivo
- Borrar una compensación si fue cargada por error

> ℹ️ Cuando un vendedor tiene saldo de compensaciones pendientes y rinde en la pantalla **Cobros** (3.23), el tipo de pago "Compensaciones" le permite descontar ese saldo de la rendición.

---

<img src="imagenes/pantalla_compensaciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Caja → Compensaciones**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de carga y el panel derecho con el historial del vendedor seleccionado.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **VENDEDOR** | Vendedor al que se le asigna la compensación. Al seleccionarlo, la grilla se actualiza con su historial. |
| **FECHA** | Fecha de la compensación |
| **IMPORTE** | Monto de la compensación a registrar |
| **OBSERV.** | Descripción del motivo (ej. "Adelanto de sueldo", "Fondo cambio") |

### Sección IMPORTAR

Permite cargar masivamente compensaciones para múltiples vendedores desde un archivo Excel o CSV.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) o CSV (separado por `;`) a importar. |
| **Importar** | Procesa el archivo y registra las compensaciones con la fecha actual. |

> Esta sección no tiene botón **Formato**. Preparar el archivo manualmente siguiendo la estructura indicada a continuación.

#### Formato del archivo de importación

El archivo debe tener **3 columnas**, con el encabezado en la primera fila:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **DNI** | DNI del vendedor | Debe coincidir con el DNI registrado en el sistema |
| **Compensacion** | Importe a registrar | Número positivo (mayor a 0) |
| **Observaciones** | Texto descriptivo del motivo | Texto libre |

**Formato de archivo:**
- Excel: `.xlsx`
- CSV: separado por punto y coma (`;`), con comillas dobles (`"`) como delimitador de texto.

#### Validaciones del sistema

- Los registros con **Compensacion ≤ 0** se descartan automáticamente.
- El **DNI** debe coincidir exactamente con el de un vendedor activo en el sistema; los que no se encuentran se omiten silenciosamente.

#### Qué hace el sistema al importar

Por cada fila válida, el sistema registra una compensación para ese vendedor con la **fecha actual del día**. El saldo queda disponible para descontarlo en la rendición de cobros a través del tipo de pago "Compensaciones".

---

## Panel derecho — Historial de compensaciones

Muestra todas las compensaciones activas del vendedor seleccionado:

| Columna | Descripción |
|---|---|
| Legajo | Número de legajo del vendedor |
| Vendedor | Nombre del vendedor |
| Fecha | Fecha de la compensación |
| Importe | Monto de la compensación |
| Lote | Lote de rendición en el que fue descontada (si ya se aplicó) |
| Observaciones | Notas registradas |

**Acciones disponibles:**
- **Borrar:** Elimina la compensación (sólo si aún no fue aplicada en una rendición)

---

## Paso a paso — Registrar una compensación

1. Seleccioná el **VENDEDOR**
2. Ingresá la **FECHA**
3. Completá el **IMPORTE** del adelanto
4. Agregá una **OBSERVACIÓN** (ej. "Adelanto de gastos de traslado")
5. Guardá el registro

> La compensación queda disponible para ese vendedor. La próxima vez que rinda en **Cobros** (3.23), el sistema mostrará el saldo disponible en el tipo de pago "Compensaciones".

---

## Cómo se aplica la compensación en la rendición

En la pantalla **Cobros** (3.23), cuando el cajero elige **T PAGO = Compensaciones**:
- Aparece un selector de vendedor
- El sistema muestra el saldo disponible de compensaciones de ese vendedor
- El cajero puede incluir ese monto en la rendición, descontándolo del total

---

## Notas importantes

- El importe de la compensación queda pendiente hasta que el vendedor lo rinde en **Cobros**.
- Una compensación registrada **reduce el efectivo en caja** al momento de la rendición.
- Si se registró por error, se puede borrar siempre que no haya sido incluida en un lote de rendición.
