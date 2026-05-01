# 6.10 ML COBROS DE VENTAS
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Cobros

---

## ¿Para qué sirve esta pantalla?

**ML Cobros** permite consultar y gestionar todos los cobros registrados en MercadoLibre para una cuenta de vendedor. Desde aquí podés:

- Ver el detalle de cada cobro con su estado, subestado, importe y medio de pago
- Filtrar por estado, subestado, tipo de operación (suscripción, transferencia, pago regular) y rango de fechas
- Buscar cobros por comprador o referencia
- Actualizar el listado de cobros sincronizando con la API de ML
- Ver a qué venta, suscripción o punto de venta corresponde cada cobro
- Consultar si se emitió factura por cada cobro

---

<img src="imagenes/pantalla_ml_ventas_cobros.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Cobros**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda y botón de actualización.
- **Panel derecho (grilla):** Listado de cobros con sus datos principales.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio para ver resultados. |
| **DESDE** | Fecha de inicio del rango a consultar. |
| **HASTA** | Fecha de fin del rango. |
| **ESTADO** | Estado del cobro en ML (ej: `approved`, `rejected`, `pending`). |
| **SUBESTADO** | Subestado del cobro con mayor detalle. |
| **OPERACION** | Tipo de operación: `SUSCRIPCION`, `TRANSFERENCIA` o `PAGO REGULAR`. |
| **BUSCAR** | Campo de texto libre para buscar por cliente, referencia u otros datos. |

---

## Botón: Actualizar Cobros

Descarga desde la API de MercadoLibre los cobros del período seleccionado y los sincroniza en Caddis.

**Cuándo usarlo:** cuando hay cobros recientes que no aparecen en la grilla o cuando el estado de un cobro cambió.

1. Seleccioná el **USUARIO** ML.
2. Completá **DESDE** y **HASTA**.
3. Hacé click en **Actualizar Cobros**.
4. Confirmá el aviso.

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Cobro** | ID único del cobro en MercadoLibre |
| **Fecha** | Fecha en que se realizó el cobro |
| **Importe** | Monto del cobro |
| **Tipo Pago** | Medio de pago utilizado (tarjeta, débito, mercadopago, etc.) |
| **Estado** | Estado del cobro en ML |
| **SubEstado** | Subestado con más detalle |
| **Doc Tipo** | Tipo de documento del pagador |
| **Doc Nro** | Número de documento del pagador |
| **Cliente** | Nombre del pagador |
| **Descripcion** | Descripción del cobro |
| **Referencia** | Referencia interna del cobro |
| **Venta** | ID de la venta ML asociada a este cobro (si corresponde) |
| **Suscripcion** | ID de la suscripción asociada (si es cobro de suscripción) |
| **Store** | Identificador de la tienda |
| **POS** | Punto de venta ML desde donde se procesó el pago |
| **Factura** | Tipo y número de comprobante emitido por este cobro |

---

## Acciones desde la grilla

| Acción | Descripción |
|---|---|
| **Detalle** | Abre el detalle completo del cobro seleccionado |

---

## Conceptos clave

**¿Qué diferencia hay entre una venta y un cobro?**
- Una **venta** es el pedido del comprador. Puede tener un estado pendiente de pago o cancelado.
- Un **cobro** es el movimiento de dinero efectivo. Una venta puede tener uno o más cobros asociados (ej: cuotas de suscripción, devoluciones parciales).

**Tipos de operación:**
- `PAGO REGULAR`: pago de una compra normal en ML.
- `SUSCRIPCION`: pago de una cuota de suscripción (plan de pago periódico).
- `TRANSFERENCIA`: transferencia de fondos entre cuentas ML.

---

> 📖 Para ver las ventas de ML consultá [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).
> 📖 Para gestionar suscripciones y sus cobros consultá [**Suscripciones ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Suscripciones.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
