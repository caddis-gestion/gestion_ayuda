# 6.24 ML DETALLE DE SUSCRIPCIÓN
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Ventana emergente accesible desde ML Suscripciones

---

## ¿Para qué sirve esta pantalla?

**ML Detalle de Suscripción** es una ventana emergente que muestra el detalle completo de una suscripción de MercadoLibre y su historial de cobros. Desde aquí podés:

- Ver todos los datos de la suscripción: estado, cliente, importe, próximo pago y cuotas cobradas
- Cambiar el estado de la suscripción (pausar, reactivar)
- Modificar el importe, la referencia y la fecha de próximo pago
- Ver el historial detallado de todos los cobros de la suscripción

---

<img src="imagenes/pantalla_ml_suscripciones_consulta.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Esta pantalla es una ventana emergente. Se accede desde:
**ML Suscripciones → seleccionar una suscripción → botón Detalle**

---

## Sección: Datos de la suscripción

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta ML de la suscripción (solo lectura) |
| **SUSCRIPCION** | ID de la suscripción en ML + semáforo de estado (solo lectura) |
| **ESTADO** | Estado actual de la suscripción. Editable: al cambiar y guardar, se actualiza en ML. Opciones: `authorized`, `paused`, `cancelled`. |
| **CLIENTE** | Nombre del cliente (solo lectura) |
| **FECHA** | Fecha de creación de la suscripción (solo lectura) |
| **TITULO** | Descripción del plan de suscripción (editable — área de texto) |
| **REFERENCIA** | Referencia interna de la suscripción (editable) |
| **IMPORTE** | Importe de la cuota (editable) |
| **PROXIMO PAGO** | Fecha del próximo débito automático (solo lectura) + estado del cobro próximo |
| **CUOTAS PAGAS** | Cantidad de cuotas ya cobradas (solo lectura) |

---

## Sección: Datos de facturación

Muestra el historial de todos los cobros de la suscripción.

| Columna | Descripción |
|---|---|
| **Id de Cuota** | ID del cobro en ML |
| **Importe** | Monto de la cuota |
| **Estado** | Estado del cobro (ej: `approved`, `rejected`, `pending`) |
| **Subestado** | Subestado con mayor detalle |
| **Intentos** | Número de intentos de cobro realizados |
| **Fecha Debito** | Fecha en que se intentó o realizó el débito |
| **Metodo Pago** | Método de pago utilizado |
| **Tipo** | Tipo de pago |
| **Ultima Modificacion** | Fecha de la última actualización del cobro |
| **Id de Cobro** | ID del pago registrado en ML |

> ℹ️ La columna **Estado** del historial tiene fondo amarillo para facilitar la identificación de cobros pendientes o fallidos.

---

## Cómo pausar o reactivar una suscripción

1. En el campo **ESTADO**, seleccioná el nuevo estado:
   - `paused` para pausar la suscripción (no se realizarán débitos hasta que se reactive).
   - `authorized` para reactivar una suscripción pausada.
2. Hacé click en el botón **Guardar** (o el botón de submit del campo ESTADO).
3. El sistema actualiza el estado en ML.

---

> 📖 Para ver el listado general de suscripciones consultá [**Suscripciones ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Suscripciones.pdf).
> 📖 Para facturar los cobros de suscripciones consultá [**Facturación de Suscripciones ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Facturacion_Suscripciones.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
