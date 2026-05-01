# 3.20 TERMINAL MERCADOPAGO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios de caja y facturación
> **Pantalla en el sistema:** Desde Facturación → botón MercadoPago (popup)

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Terminal MercadoPago** es una ventana emergente que permite buscar y vincular cobros realizados con el terminal de MercadoPago (QR o dispositivo Point) a una factura en proceso. Desde aquí podés:

- Ver los cobros aprobados de MercadoPago de los últimos 7 días para el PDV activo
- Seleccionar el cobro correspondiente a la venta que estás facturando
- Vincular ese cobro automáticamente como forma de pago de la factura

> ℹ️ Esta pantalla **no se accede desde el menú principal**. Se abre automáticamente al hacer clic en el botón **MercadoPago** en la pantalla de **Facturación** (3.01), cuando el PDV tiene un terminal MercadoPago configurado.

---

<img src="imagenes/pantalla_terminal_mercadopago.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

1. Accedé a la pantalla de **Facturación** (3.01) o **Facturación Rápida** (3.02)
2. Ingresá los artículos de la venta
3. Hacé clic en el botón **MercadoPago** (visible solo si el PDV tiene terminal MP configurado)
4. Se abrirá esta ventana emergente automáticamente

---

## Descripción general de la pantalla

La pantalla muestra una grilla con todos los cobros **aprobados** por MercadoPago en los últimos 7 días para el PDV de la factura actual. El sistema actualiza automáticamente la lista de cobros al abrirse, consultando la API de MercadoPago.

---

## Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Id** | Identificador único del cobro en MercadoPago |
| **Fecha Aprobado** | Fecha y hora en que MercadoPago confirmó el pago |
| **Importe** | Monto del cobro aprobado |
| **Pago Tipo** | Tipo de pago (tarjeta de débito, crédito, billetera, QR, etc.) |
| **Cliente Documento** | Número de documento del comprador (si MercadoPago lo reporta) |
| **Cliente** | Nombre del comprador (si MercadoPago lo reporta) |
| **MP Store** | Identificador del local/tienda en MercadoPago |
| **MP POS** | Identificador del terminal de cobro en MercadoPago |

> ℹ️ Solo aparecen cobros que **no han sido vinculados previamente** a otra factura del sistema. Los cobros ya aplicados no se muestran.

---

## Paso a paso: Vincular un cobro de MercadoPago

**Flujo completo en la pantalla de Facturación:**

**1.** Ingresá los artículos en la factura normalmente.

**2.** El cliente paga con el terminal MercadoPago (QR, dispositivo Point, etc.) y el pago queda aprobado.

**3.** En la pantalla de Facturación, hacé clic en el botón **MercadoPago**.

**4.** Se abre esta ventana. El sistema consulta los cobros recientes de MP automáticamente.

**5.** En la grilla, identificá el cobro del cliente (verificá el importe y la hora).

**6.** Hacé **doble clic** en la fila del cobro correspondiente.

**7.** La ventana se cierra y el cobro queda registrado como forma de pago en la factura.

**8.** Hacé clic en **Facturar** para emitir el comprobante.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| La grilla aparece vacía | No hay cobros aprobados en los últimos 7 días para este PDV | Verificar que el pago fue aprobado en MercadoPago y que el PDV es el correcto |
| "No hay Items ingresados en el comprobante" | Se abrió MP sin artículos en la factura | Ingresá los artículos primero y luego hacé clic en MercadoPago |
| "No hay importes ingresados en el comprobante" | El importe de la factura es cero | Verificá que los artículos tienen precio asignado |
| El cobro del cliente no aparece | El cobro aún no fue procesado por MercadoPago | Esperá unos minutos y volvé a abrir la ventana |

---

## Preguntas frecuentes

**¿Qué hago si el cobro del cliente no aparece en la lista?**
- Verificá que el pago esté aprobado en la app o dashboard de MercadoPago
- Asegurate de que el PDV de la factura coincide con el terminal MP del cobro
- Si el cobro es de más de 7 días atrás, no aparecerá en la lista (límite del sistema)

**¿Puedo usar MercadoPago y otro medio de pago juntos?**
Sí, podés registrar el cobro de MercadoPago y luego agregar otros medios de pago desde la ventana de **Pagos** para completar el total.

**¿Qué diferencia hay entre el botón MercadoPago en Facturación y esta pantalla?**
Son la misma funcionalidad. El botón **MercadoPago** en facturación es el que abre esta ventana emergente. No son dos pantallas separadas.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
