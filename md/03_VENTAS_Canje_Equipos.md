# 3.40 CANJE EQUIPOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Canje Equipos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Canje Equipos** permite registrar operaciones de canje, compra o devolución de equipos usados. Desde aquí podés:

- Registrar un **Plan Canje**: el cliente entrega un equipo viejo y recibe uno nuevo
- Registrar una **Compra de Equipo**: la empresa compra un equipo usado a un cliente
- Registrar una **Devolución de Equipo**: el equipo vuelve al stock sin transacción de compra

---

<img src="imagenes/pantalla_canje_equipos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Canje Equipos**

---

## Descripción general de la pantalla

La pantalla tiene un único panel izquierdo con el formulario. Los campos disponibles varían según la **OPERACION** seleccionada.

---

## Campo principal

| Campo | Descripción |
|---|---|
| **OPERACION** | Tipo de operación: vacío, PLAN CANJE, COMPRA DE EQUIPO o DEVOLUCIÓN EQUIPO |

---

## Campos según tipo de operación

### PLAN CANJE

El cliente entrega un equipo viejo como parte de pago de uno nuevo. No requiere PDV ni vendedor (se asocia a la venta ya existente).

| Campo | Descripción |
|---|---|
| **EQUIPO** | Modelo del equipo entregado por el cliente |
| **IMEI** | Número IMEI del equipo (hasta 15 dígitos numéricos) |
| **ID** | Identificador de la operación de canje |

### COMPRA DE EQUIPO

La empresa compra un equipo usado directamente al cliente.

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta donde se realiza la compra |
| **VENDEDOR** | Vendedor que registra la operación |
| **CLIENTE** | Cliente que vende el equipo |
| **EQUIPO** | Modelo del equipo comprado |
| **IMEI** | Número IMEI del equipo |
| **IMPORTE** | Precio pagado al cliente por el equipo |
| **CONTRATO** | Número de contrato o referencia de la operación |

### DEVOLUCIÓN EQUIPO

El equipo vuelve al stock sin pago al cliente.

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta |
| **VENDEDOR** | Vendedor que registra la devolución |
| **CLIENTE** | Cliente que devuelve el equipo |
| **EQUIPO** | Modelo del equipo devuelto |
| **IMEI** | Número IMEI del equipo |
| **CONTRATO** | Número de contrato o referencia |

> En la **Devolución**, no se ingresa IMPORTE ya que no hay pago al cliente.

---

## Notas importantes

- El campo **EQUIPO** permite buscar el modelo desde el catálogo de equipos del sistema.
- El **IMEI** debe ingresarse con solo dígitos numéricos (sin guiones ni espacios).
- Las operaciones de **COMPRA DE EQUIPO** pueden generar movimientos de stock y registros contables según la configuración del sistema.
