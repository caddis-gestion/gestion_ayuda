# 3.61 LÍMITES DE CRÉDITOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Limites de Creditos

---

## ¿Para qué sirve esta pantalla?

Para los clientes habilitados para comprar en cuenta corriente, el sistema permite establecer un límite de crédito máximo con el fin de controlar y evitar que se excedan al momento de facturar. Ese límite se va liberando a medida que el cliente va cancelando su deuda.

Desde esta pantalla podés:

- Asignar un límite de crédito a un cliente
- Definir el plazo máximo de cobro (en días)
- Configurar si la mercadería se libera contra pago o automáticamente
- Agregar observaciones sobre el crédito del cliente
- Consultar el estado de crédito de todos los clientes (límite, deuda actual, saldo disponible)
- Editar límites y plazos directamente en la grilla

---

<img src="imagenes/pantalla_limites_creditos.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Limites de Creditos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario y un panel derecho con la grilla de todos los límites configurados. Los límites se pueden ingresar completando el formulario de la izquierda **o** editando directamente en la celda correspondiente de la grilla.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **CLIENTE** | Cliente mayorista al que se asigna el límite. Al seleccionarlo, se cargan los datos actuales. |
| **CREDITO** | Monto máximo de crédito en pesos que se le otorga al cliente. Si se establece en **0**, el cliente no tiene límite asociado y puede comprar ilimitadamente más allá de su deuda. |
| **PLAZO MAXIMO** | Cantidad máxima de días de plazo para el pago. Al facturar y elegir la forma de pago "Cta Cte", el sistema solo muestra las opciones de plazo autorizadas según este valor. |
| **MERCADERIA** | **CONTRA PAGO**: la mercadería no se entrega hasta que se paga. **LIBERADA**: se entrega la mercadería al cliente aunque no haya pagado aún. |
| **OBSERVACIONES** | Notas sobre el crédito del cliente (ej. historial, condiciones especiales) |

> ⚠️ La opción **CONTRA PAGO** anula el control de límite de crédito: no se podrá entregar la mercadería hasta que el cliente cancele la factura emitida. Se utiliza cuando el depósito está separado de la administración (circuito de **Entrega en Depósito**).

---

## Panel derecho — Grilla de límites

Muestra todos los clientes con límite de crédito configurado, con su estado actual:

| Columna | Descripción |
|---|---|
| CUIT | CUIT del cliente |
| Limite | Límite de crédito asignado en pesos (editable directamente en la grilla) |
| Deuda | Deuda actual del cliente (facturas pendientes menos cobros aprobados) |
| Saldo | Saldo disponible (Límite − Deuda). Puede ser negativo si superó el límite. |
| Plazo Máximo | Plazo en días configurado (editable directamente en la grilla) |
| Liberar Mercadería | SI o NO según la configuración de MERCADERIA |
| Cliente | Nombre del cliente |

> Las columnas **Limite** y **Plazo Máximo** son editables directamente en la grilla sin necesidad de usar el formulario izquierdo.

---

## Pantalla relacionada — CTA CTE Condiciones

Los plazos y condiciones generales de pago en cuenta corriente se definen desde la pantalla **CTA CTE Condiciones**. Desde allí se crean todas las condiciones de pago disponibles, definiendo para cada una el **plazo de vencimiento** y la **tasa de interés** aplicable. Esa tasa es usada por el sistema al momento de facturar para recalcular el monto de la factura según el plazo elegido.

---

## Paso a paso — Asignar un límite de crédito

1. Seleccioná el **CLIENTE**
2. Ingresá el monto de **CREDITO** (en 0 = sin límite)
3. Definí el **PLAZO MAXIMO** en días
4. Elegí el comportamiento de **MERCADERIA** (CONTRA PAGO o LIBERADA)
5. Agregá **OBSERVACIONES** si es necesario
6. Hacé clic en **Guardar**

---

## Notas importantes

- Si el **CREDITO** se establece en **0**, el cliente no tiene límite asociado y puede comprar en cuenta corriente ilimitadamente, independientemente de su deuda acumulada.
- El **PLAZO MAXIMO** controla qué opciones de plazo se muestran al facturar con "Cta Cte": el sistema solo muestra las condiciones de pago autorizadas para ese cliente.
- La **Deuda** se calcula en tiempo real sumando todas las facturas en cuenta corriente pendientes de cobro y restando los cobros aprobados.
- Si el **Saldo** es negativo, el cliente superó su límite de crédito.
- Para **consultar** el estado de crédito sin modificar, usá la pantalla **Consultar Límites de Créditos** (3.44).
