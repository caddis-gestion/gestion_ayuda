# 12.04 ENTREGA A CLIENTE
### Módulo 12 — Reparaciones

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reparaciones → Entrega a cliente

---

## ¿Para qué sirve esta pantalla?

**Entrega a Cliente** registra la devolución física del equipo reparado al cliente. Es el **último paso del circuito de reparaciones**, posterior a la facturación. Permite agregar observaciones específicas de la entrega y confirmar que el equipo fue retirado.

---

<img src="imagenes/pantalla_entrega_cliente.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Reparaciones → Entrega a cliente**

---

## Requisito previo

Para registrar la entrega, la orden debe:

1. Tener estado **REPARACION TERMINADA**
2. Haber sido **facturada** desde [**Facturación**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf) (el sistema la identifica como tipo **REPA** en el buscador de reparaciones)

> Si la orden no fue facturada, registrar la entrega no cierra el ciclo de cobro. Asegurate de facturar antes de usar esta pantalla.

---

## Ubicación en el circuito de reparaciones

| Paso | Pantalla | Acción |
|---|---|---|
| 1 | [**Nueva Reparación**](https://ayuda.caddis.com.ar/instructivos/12_REP_Nueva_Reparacion.pdf) | Ingreso del equipo, condiciones, observaciones y seña |
| 2 | [**Modificar Reparación**](https://ayuda.caddis.com.ar/instructivos/12_REP_Modificar_Reparacion.pdf) | Actualización del presupuesto y datos durante la reparación |
| 3 | [**Estados**](https://ayuda.caddis.com.ar/instructivos/12_REP_Estados.pdf) | Cambio de estado de la orden (ej. EN REPARACION → REPARACION TERMINADA) |
| 4 | [**Facturación**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf) | Cobro de la reparación (tipo REPA) |
| **5** | **Entrega a Cliente** | **Registro de la entrega física del equipo** |

---

## Descripción general de la pantalla

La pantalla muestra los datos de la orden en modo **solo lectura**. Solo el campo de observaciones de entrega es editable. Se busca la orden por número en el campo **Entregar**.

---

## Información mostrada

| Campo | Descripción |
|---|---|
| **ENTREGAR** | Campo de búsqueda: ingresar el número de orden para cargarla |
| **ORDEN NRO** | Número de la orden de reparación |
| **ORDEN ANT** | Orden anterior relacionada (si aplica) |
| **ESTADO** | Estado actual de la orden (debe ser REPARACION TERMINADA) |
| **PDV** | Punto de venta |
| **VENDEDOR** | Vendedor de la orden |
| **CLIENTE** | Nombre del cliente que retira el equipo |
| **ARTÍCULO** | Equipo entregado |
| **NSE / IMEI** | Número de serie o IMEI del equipo |
| **CONDICIONES** | Condiciones de recepción registradas al ingreso (solo lectura) |
| **OBSERVACIONES** | Observaciones originales de la reparación (solo lectura) |
| **OBSERVACIONES DE ENTREGA** | Texto libre para registrar detalles de la entrega (editable) |
| **SEÑA — IMPORTE** | Seña cobrada al inicio (solo lectura) |

### Grilla del presupuesto

Muestra los ítems del presupuesto sin opción de borrar.

| Columna | Descripción |
|---|---|
| Artículo | Nombre del repuesto o servicio |
| Cant. | Cantidad |
| Importe | Precio unitario con IVA |
| Total | Subtotal |

**Botón PDF:** Genera el comprobante de entrega en PDF.

---

## Paso a paso — Registrar la entrega del equipo

1. Asegurate de que la orden tenga estado **REPARACION TERMINADA** y esté facturada
2. Ingresá el número de orden en el campo **Entregar**
3. Verificá que el equipo y el cliente sean correctos
4. Ingresá las **OBSERVACIONES DE ENTREGA** (estado del equipo al ser devuelto, trabajo realizado, aclaraciones al cliente, etc.)
5. Guardá para registrar la entrega — el sistema actualiza el estado de la orden a **ENTREGADO A CLIENTE**
6. Opcionalmente, generá el PDF de entrega con el botón **PDF**

---

## Notas importantes

- Esta pantalla es **solo lectura** excepto por el campo OBSERVACIONES DE ENTREGA.
- La orden debe tener estado **REPARACION TERMINADA** para poder registrar la entrega.
- Los comprobantes emitidos (seña y reparación terminada) se rinden al final del día desde **Cierre de Caja Diario**.
- Para consultar el historial de traslados del equipo usá [**Traslados Historia**](https://ayuda.caddis.com.ar/instructivos/12_REP_Traslados_Historia.pdf) (12.05).
- Para ver el historial completo de todas las reparaciones (con filtros por estado y depósito) usá **Reportes → Informes → Reparaciones**.
