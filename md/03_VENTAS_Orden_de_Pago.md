# 3.33 ORDEN DE PAGO
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Cta Cte Clientes → Orden de Pago

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Orden de Pago** permite registrar pagos realizados a clientes mayoristas (por ejemplo, devoluciones de dinero, reintegros o pagos por notas de crédito). Desde aquí podés:

- Crear una orden de pago a favor de un cliente
- Registrar el medio de pago utilizado (efectivo, cheque, transferencia, etc.)
- Consultar las órdenes de pago ya registradas para el cliente

---

<img src="imagenes/pantalla_orden_de_pago.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Cta Cte Clientes → Orden de Pago**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de la orden y una sección de pagos, y un panel derecho con la grilla de valores ingresados.

---

## Panel izquierdo — Datos de la orden

| Campo | Descripción |
|---|---|
| **ORDEN NRO** | Número de la orden de pago, asignado automáticamente (formato: 0001-XXXXXXXX). Campo de sólo lectura. |
| **PDV** | Punto de venta desde el que se emite la orden |
| **FECHA** | Fecha de la orden (por defecto: hoy) |
| **CLIENTE** | Cliente mayorista al que se le realiza el pago |
| **OBSERVACIONES** | Notas opcionales sobre la orden |

---

## Sección PAGOS — Ingresar medio de pago

Permite registrar el dinero que se entrega al cliente, eligiendo el tipo de pago:

| Campo | Descripción |
|---|---|
| **TIPO** | Medio de pago: Efectivo, Tarjeta Débito, Tarjeta Crédito, Cheque, Transferencia Bancaria, Débito Bancario, Compensaciones, Marketplace, Certificados |
| **IMPORTE** | Monto del pago |
| **COTIZACIÓN** | Tipo de cambio (sólo en entornos multimoneda) |
| **Ingresar Pago** | Confirma el medio de pago y lo agrega a la grilla derecha |

### Campos adicionales según tipo de pago

Según el **TIPO** seleccionado, aparecen campos extra:

| Tipo | Campos adicionales |
|---|---|
| **Tarjeta Débito / Crédito** | TARJETA (entidad), Plataforma, Nro de cupón, Fecha, Cuotas, Cupón |
| **Cheque / Transferencia / Débito Bancario** | BANCO, Nro de cheque/transferencia, Fecha |
| **Marketplace** | Plataforma, Referencia, Fecha |
| **Certificados** | Certificado; Provincia (sólo en ciertos casos) |

---

## Panel derecho — Grilla de pagos ingresados

Muestra los medios de pago ya cargados para la orden en curso:

| Columna | Descripción |
|---|---|
| Tipo Pago | Medio de pago seleccionado |
| Importe | Monto en pesos |
| Entidad | Banco, tarjeta o plataforma según el tipo |

**Acciones disponibles:**
- **Borrar:** Elimina el ítem de pago de la grilla
- **Detalle:** Muestra el detalle completo del ítem

---

## Paso a paso — Registrar una orden de pago

1. Seleccioná el **PDV** y el **CLIENTE**
2. Verificá la **FECHA**
3. En la sección **PAGOS**, elegí el **TIPO** de pago
4. Completá los campos correspondientes al tipo elegido
5. Ingresá el **IMPORTE**
6. Hacé clic en **Ingresar Pago** — aparece en la grilla derecha
7. Agregá una **OBSERVACIÓN** si es necesario
8. Guardá la orden

---

## Notas importantes

- La orden de pago queda registrada en la cuenta corriente del cliente como un egreso a favor del mismo.
- Se puede ingresar más de un medio de pago por orden (por ejemplo, parte en efectivo y parte en cheque).
- El número de orden se asigna automáticamente y no puede modificarse.
