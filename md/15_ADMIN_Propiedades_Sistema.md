# 15.15 PROPIEDADES DEL SISTEMA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Propiedades del Sistema

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Propiedades del Sistema** centraliza la configuración global del comportamiento del sistema. Desde aquí podés ajustar parámetros que afectan a todos los módulos: facturación, cobranza, caja, descuentos, compras, stock y correos de notificación.

---

## ¿Cómo acceder?

**Menú → Administración → Propiedades del Sistema**

---

## Sección: Facturación

| Parámetro | Descripción |
|---|---|
| **MONTO MÁXIMO FC SIN DNI** | Importe máximo de una factura sin requerir el DNI del cliente. Por encima de este monto, el sistema solicita el DNI obligatoriamente. |
| **LIBERAR PRECIO ARTÍCULOS** | Permite que el vendedor modifique el precio unitario de un artículo al facturar. |
| **LIBERAR LISTAS DE PRECIO** | Permite que el vendedor cambie la lista de precios aplicada en una factura. |
| **LIBERAR CLIENTE CTA CTE** | Permite facturar a clientes en cuenta corriente aunque tengan el límite de crédito superado. |
| **MONTO MÍNIMO T. CRÉDITO** | Importe mínimo para habilitar el pago con tarjeta de crédito en facturación. |
| **PANTALLA REDUCIDA DE PAGOS** | Activa una vista simplificada del panel de cobros (útil para puntos de venta con pantallas pequeñas). |

---

## Sección: Cobranza

| Parámetro | Descripción |
|---|---|
| **CONTROL LÍMITES DE CRÉDITO** | Activa el control del límite de crédito en la cobranza de cuenta corriente. |
| **APROBAR COBRANZA EN CTA. CTE.** | Requiere aprobación de gerencia para aplicar cobranzas en cuenta corriente por encima del límite. |

---

## Sección: Caja

| Parámetro | Descripción |
|---|---|
| **HABILITAR USO DE CAJEROS** | Activa el módulo de cajeros (permite que múltiples operadores trabajen sobre la misma caja). |

---

## Sección: Descuento por Forma de Pago

Permite configurar un porcentaje de descuento automático según el medio de pago seleccionado al cobrar:

| Medio de Pago | Descripción |
|---|---|
| **EFECTIVO** | Descuento al cobrar en efectivo. |
| **BILLETERA** | Descuento al cobrar con billetera virtual (MercadoPago, etc.). |
| **DÉBITO** | Descuento al cobrar con tarjeta de débito. |
| **TRANSFERENCIA** | Descuento al cobrar con transferencia bancaria. |
| **DEPÓSITO** | Descuento al cobrar con depósito bancario. |
| **DÓLAR** | Descuento al cobrar en dólares. |

---

## Sección: Compras

| Parámetro | Descripción |
|---|---|
| **LISTA DE PRECIOS** | Define la lista de precios que se actualiza automáticamente al registrar una factura de compra. |
| **COSTO EN MONEDA** | Define si el costo de los artículos se guarda en moneda local o en la moneda de la factura de compra. |

---

## Sección: Stock

| Parámetro | Descripción |
|---|---|
| **SIN CONTROL DE STOCK** | Desactiva el control de stock negativo (permite vender sin stock disponible). |
| **DEVOLUCIONES A DEPÓSITO CENTRAL** | Las devoluciones de clientes se acreditan siempre al depósito central, no al PDV. |
| **MOVER ENTRE DEPÓSITOS/PDV** | Habilita la transferencia de stock entre depósitos y puntos de venta. |
| **DEPÓSITO RESERVA PP** | Depósito utilizado para reservar artículos de presupuestos/pedidos. |
| **CONTROL LÍMITE DE CRÉDITO** | Activa el control de crédito también en el módulo de stock. |
| **EQUIPOS EN TRÁNSITO** | Habilita el seguimiento de equipos con NSE en tránsito entre depósitos. |
| **ARTÍCULOS EN TRÁNSITO** | Habilita el seguimiento de artículos en tránsito entre depósitos. |
| **ÍNDICES REPOSICIÓN** | Activa los índices de reposición automática para alertas de stock mínimo. |

---

## Sección: Correos de Envío

Permite configurar las direcciones de correo electrónico que reciben notificaciones automáticas del sistema:

| Parámetro | Descripción |
|---|---|
| **ENVÍO DE FACTURAS** | Correo al que se envían copias de facturas emitidas. |
| **ALERTA TIENDAS STOCK 0** | Correo que recibe alertas cuando un artículo llega a stock cero en tiendas virtuales (TiendaNube, etc.). |
| **ALERTAS DE STOCK** | Correo que recibe alertas de stock mínimo. |
| **ALERTA DE PRECIOS** | Correo que recibe notificaciones de cambios de precios. |
| **ALERTA DE NC** | Correo que recibe alertas de notas de crédito emitidas. |
| **ALERTA DE PP APROBADO** | Correo que recibe notificación cuando un presupuesto/pedido es aprobado. |
| **FACTURAS DE ABONOS** | Correo al que se envían las facturas de abonos generadas automáticamente. |

---

## Notas importantes

- Los cambios en las propiedades del sistema afectan inmediatamente a todos los usuarios y módulos.
- Algunos parámetros requieren reinicio de sesión para tomar efecto.
- Esta pantalla es de uso exclusivo del administrador del sistema. Modificar parámetros incorrectamente puede afectar el funcionamiento del negocio.
