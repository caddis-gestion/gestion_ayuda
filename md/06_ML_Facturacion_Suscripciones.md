# 6.19 ML FACTURACIÓN DE SUSCRIPCIONES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Facturacion Suscripciones

---

## ¿Para qué sirve esta pantalla?

**ML Facturación de Suscripciones** permite emitir comprobantes fiscales para los cobros de suscripciones (planes de pago recurrente) de MercadoLibre. Desde aquí podés:

- Consultar los cobros de suscripciones de un período
- Filtrar por estado de cobro, subestado, tipo de operación y rango de fechas
- Emitir facturas para los cobros seleccionados en lote
- Imprimir los comprobantes emitidos
- Ver el total de importes a facturar de la selección

---

<img src="imagenes/pantalla_ml_facturacion_suscripciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Facturacion Suscripciones**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de cobros y parámetros de facturación.
- **Panel derecho (grilla):** Listado de cobros de suscripciones con todos sus datos.

---

## Panel izquierdo: Filtros

### Cobros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio. |
| **DESDE** | Fecha de inicio del rango de cobros. |
| **HASTA** | Fecha de fin del rango. |
| **ESTADO** | Estado del cobro (ej: `approved`, `rejected`, `pending`). |
| **SUBESTADO** | Subestado del cobro con mayor detalle. |
| **OPERACION** | Tipo de operación: `SUSCRIPCION`, `TRANSFERENCIA`, `PAGO REGULAR`. |
| **FACTURACION** | Filtra por estado de facturación: `EMITIDAS` o `PENDIENTES`. |
| **BUSCAR** | Campo de texto libre para buscar por cliente, referencia u otros datos. |

### Facturar

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta desde donde se emite la factura. |
| **VENDEDOR** | Vendedor asignado a los comprobantes. |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Cobro** | ID del cobro en ML |
| **Fecha** | Fecha del cobro |
| **Importe** | Monto del cobro |
| **Tipo Pago** | Medio de pago utilizado |
| **Cobro Estado** | Estado del cobro |
| **Cobro Subestado** | Subestado del cobro |
| **Suscripcion Estado** | Estado de la suscripción asociada |
| **Doc Tipo** | Tipo de documento del cliente |
| **Doc Nro** | Número de documento del cliente |
| **Cliente** | Nombre del cliente |
| **Descripcion** | Descripción del cobro |
| **Referencia** | Referencia de la suscripción |
| **Factura Tipo** | Tipo de comprobante emitido |
| **Factura Nro** | Número del comprobante |
| **Suscripcion** | ID de la suscripción en ML |
| **Totales** | Acumula el importe de las filas seleccionadas |
| **Detalle** | Abre el detalle del cobro |
| **Imprimir** | Imprime el comprobante del cobro |
| **Checkbox** | Selección para facturación en lote |

---

## Cómo facturar cobros de suscripciones

1. Seleccioná el **USUARIO** ML.
2. Completá el rango **DESDE** / **HASTA**.
3. Filtrá por **ESTADO** = `approved` y **FACTURACION** = `PENDIENTES` para ver los cobros aprobados sin factura.
4. Seleccioná el **PDV** y **VENDEDOR** para los comprobantes.
5. Marcá con el **checkbox** los cobros a facturar (o seleccioná todos).
6. Hacé click en **Facturar** y confirmá el aviso.
7. Los comprobantes se generan automáticamente y la columna **Factura Tipo/Nro** se completa.

---

## Preguntas frecuentes

**¿Qué diferencia hay entre ML Cobros y ML Facturación de Suscripciones?**
- **ML Cobros** (6.10): muestra todos los cobros de ML (ventas regulares + suscripciones + transferencias) para consulta.
- **ML Facturación de Suscripciones**: está orientada exclusivamente a emitir facturas para los cobros de suscripciones.

**¿Puedo facturar cobros rechazados?**
No. Solo se deben facturar cobros en estado `approved`. Los cobros rechazados no generan ingreso real.

---

> 📖 Para ver el listado general de suscripciones consultá [**Suscripciones ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Suscripciones.pdf).
> 📖 Para ver todos los cobros de ML consultá [**Cobros de Ventas ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas_Cobros.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
