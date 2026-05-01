# 15.26 CONSULTAR ORDEN DE PAGO A PROVEEDOR
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Administración → Proveedores → Orden Pago Modificar

---

## ¿Para qué sirve esta pantalla?

Permite buscar y consultar órdenes de pago a proveedores ya registradas en el sistema. Ingresando el número de orden de pago se accede a todos los datos de la misma: proveedor, fecha, medios de pago utilizados y observaciones. También permite imprimir el detalle de la orden. Si la orden fue cancelada o tiene una nota de crédito asociada, el sistema lo indica visualmente con alertas de color.

---

<img src="imagenes/pantalla_orden_pago_modificar.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Administración → Proveedores → Orden Pago Modificar**

---

## Buscar una orden de pago

En la parte superior de la pantalla se encuentra el campo de búsqueda:

| Campo / Botón | Descripción |
|---|---|
| ORDEN DE PAGO | Número de la orden de pago a consultar |
| Buscar | Carga los datos de la orden ingresada |
| Detalle | Genera e imprime el comprobante de la orden de pago |

---

## Indicadores de estado

Una vez cargada la orden, el sistema puede mostrar los siguientes indicadores:

| Indicador | Color | Significado |
|---|---|---|
| CANCELADA | Rojo | La orden de pago fue cancelada |
| Número de NC | Amarillo | La orden tiene una nota de crédito asociada; se muestra el número de la NC |

---

## Datos de la orden (solo lectura)

Los siguientes campos se muestran con la información registrada al momento de crear la orden. No pueden modificarse desde esta pantalla:

| Campo | Descripción |
|---|---|
| PROVEEDOR | Razón social del proveedor |
| CUIT / DNI | Identificación fiscal del proveedor |
| FECHA | Fecha de emisión de la orden de pago |
| OBSERVACIONES | Notas o comentarios registrados en la orden |

---

## Grilla de medios de pago

Muestra el detalle de cada medio de pago utilizado en la orden:

| Columna | Descripción |
|---|---|
| Tipo Pago | Tipo de medio de pago utilizado (cheque, transferencia, efectivo, etc.) |
| Importe | Monto pagado con ese medio |
| Entidad | Banco o entidad financiera asociada |
| Referencia | Número de cheque, transferencia u otro identificador |
| Fecha | Fecha del medio de pago |
| Provincia | Provincia de la entidad bancaria (cuando aplica) |
| Certificado | Número de certificado (cuando aplica) |

---

## Información de auditoría

Al pie de la pantalla se muestra el usuario que realizó la última modificación sobre la orden y la fecha en que se efectuó.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
