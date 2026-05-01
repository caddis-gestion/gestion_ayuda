# 6.18 ML SUSCRIPCIONES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnices)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Suscripciones

---

## ¿Para qué sirve esta pantalla?

**ML Suscripciones** permite gestionar los planes de pago recurrente (suscripciones) configurados en MercadoLibre. Estos son acuerdos de débito automático periódico que los compradores aceptan para pagar en cuotas. Desde aquí podés:

- Ver todas las suscripciones activas, pausadas o canceladas de una cuenta ML
- Filtrar por estado y cuota (pendiente/cobrada)
- Ver los totales de suscripciones por estado
- Modificar el importe de las cuotas en lote
- Actualizar el listado de suscripciones desde la API de ML
- Acceder al detalle de cada suscripción para ver su historial de cobros

---

<img src="imagenes/pantalla_ml_suscripciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Suscripciones**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros, totales y opciones de modificación masiva.
- **Panel derecho (grilla):** Listado de suscripciones con sus datos.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Al seleccionar, actualiza automáticamente el listado. |
| **ESTADO** | Estado de la suscripción (excluye `pending` que está en proceso de creación). |
| **CUOTA** | `Todo` — muestra todas las cuotas. `Pendiente` — cuotas aún no cobradas. `Cobrado` — cuotas ya acreditadas. |
| **E-MAIL** | Filtra por e-mail del cliente. |

### Cantidades (solo lectura)

| Campo | Descripción |
|---|---|
| **AUTORIZADAS** | Número de suscripciones en estado autorizado |
| **CANCELADAS** | Número de suscripciones canceladas |
| **PAUSADAS** | Número de suscripciones pausadas |
| **TOTAL** | Total de suscripciones cargadas |

---

## Botón: Actualizar Suscripciones

Descarga desde la API de MercadoLibre las suscripciones del usuario seleccionado y actualiza el estado de las existentes en Caddis.

---

## Sección: Modificar importes

Permite cambiar el importe de las cuotas futuras para las suscripciones seleccionadas en la grilla.

| Campo | Descripción |
|---|---|
| **NUEVO IMPORTE** | Nuevo valor de la cuota a aplicar |
| **Modificar Importes** | Botón para aplicar el nuevo importe a las suscripciones seleccionadas |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Cliente** | Nombre del cliente con la suscripción |
| **Estado Cuota** | Estado del cobro de la cuota actual — fondo amarillo |
| **Importe** | Importe de la cuota |
| **Cuotas Cobradas** | Cantidad de cuotas ya cobradas |
| **Pago Actual** | Fecha del cobro actual |
| **Proximo Pago** | Fecha del próximo débito automático |
| **Fecha Creacion** | Fecha en que se creó la suscripción |
| **Referencia** | Código de referencia de la suscripción |
| **Detalle** | Botón para abrir el detalle completo de la suscripción |
| **Codigo Cliente** | Código del cliente en Caddis |
| **Suscripcion** | ID de la suscripción en ML |
| **Estado** | Estado de la suscripción (`authorized`, `paused`, `cancelled`) |
| **Usuario** | Cuenta ML dueña de la suscripción |
| **Checkbox** | Para seleccionar suscripciones en lote |

---

## Semáforo de estado

El semáforo indica el estado del cobro de la cuota:

| Color | Significado |
|---|---|
| Verde | Cuota cobrada correctamente |
| Amarillo | Cuota pendiente de cobro |
| Rojo | Cobro fallido o rechazado |

---

## Preguntas frecuentes

**¿Qué es una suscripción en ML?**
Es un acuerdo por el cual el comprador autoriza que se le debite automáticamente un importe periódico (mensual, semanal, etc.). Se usa principalmente para planes de pago en cuotas de artículos o servicios recurrentes.

**¿Puedo cancelar una suscripción desde Caddis?**
No directamente desde la grilla. Para cambiar el estado de una suscripción, accedé al **Detalle** y modificá el estado desde allí.

**¿Cómo sé qué cuotas están pendientes de cobro?**
Usá el filtro **CUOTA = Pendiente** para ver solo las cuotas que todavía no fueron debitadas.

---

> 📖 Para ver el detalle de una suscripción y su historial de cobros consultá [**Detalle de Suscripción ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Suscripciones_Consulta.pdf).
> 📖 Para facturar los cobros de suscripciones consultá [**Facturación de Suscripciones ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion_Suscripciones.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
