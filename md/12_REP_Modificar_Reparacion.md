# 12.02 MODIFICAR REPARACIÓN
### Módulo 12 — Reparaciones

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reparaciones → Modificar Reparacion

---

## ¿Para qué sirve esta pantalla?

**Modificar Reparación** permite editar los datos de una orden de reparación ya existente: actualizar las observaciones, agregar ítems al presupuesto, modificar el NSE del equipo o cambiar el vendedor asignado.

---

<img src="imagenes/pantalla_modificar_reparacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Reparaciones → Modificar Reparacion**

---

## Campos del formulario

### Datos generales

| Campo | Descripción |
|---|---|
| **ORDEN NRO** | Número de la orden a modificar (solo lectura, asignado al crear). |
| **ORDEN ANT** | Número de orden anterior relacionada (solo lectura). |
| **ESTADO** | Estado actual de la orden (solo lectura en modificación). |
| **PDV** | Punto de venta (solo lectura). |
| **VENDEDOR** | Vendedor asignado. Editable. |
| **CLIENTE** | Cliente (solo lectura). |
| **ARTÍCULO** | Equipo en reparación (solo lectura). |
| **NSE** | Número de serie o IMEI. Editable. |

### Sección CONDICIONES

Casillas que indican el estado físico del equipo al momento de recepción. Editables.

### Sección OBSERVACIONES

Texto libre editable para actualizar detalles sobre la falla o el avance de la reparación.

### Sección SEÑA

| Campo | Descripción |
|---|---|
| **IMPORTE** | Monto de seña. Solo editable si no tiene recibo generado. |

### Sección PRESUPUESTO

Permite agregar o eliminar ítems del presupuesto.

| Campo / Botón | Descripción |
|---|---|
| **CÓDIGO** | SKU del repuesto o servicio. Buscá con el botón **Buscar**. |
| **IMPORTE** | Precio unitario. |
| **CANTIDAD** | Cantidad de unidades. |
| **Ingresar** | Agrega el ítem a la grilla. |

### Grilla del presupuesto

| Columna | Descripción |
|---|---|
| **Artículo** | Nombre del repuesto o servicio. |
| **Cant.** | Cantidad. |
| **Importe** | Precio con IVA. |
| **Total** | Subtotal. |
| **Borrar** | Elimina el ítem. |

---

> 📖 Para consultar una orden sin modificarla usá [**Consultar Reparación**](https://ayuda.caddis.com.ar/instructivos/12_REP_Consultar_Reparacion.pdf).
> 📖 Para registrar la entrega al cliente consultá [**Entrega a Cliente**](https://ayuda.caddis.com.ar/instructivos/12_REP_Entrega_Cliente.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
