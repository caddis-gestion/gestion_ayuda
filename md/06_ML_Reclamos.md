# 6.17 ML RECLAMOS
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Reclamos

---

## ¿Para qué sirve esta pantalla?

**ML Reclamos** permite consultar y gestionar todos los reclamos activos y resueltos de MercadoLibre para una cuenta de vendedor. Desde aquí podés:

- Ver todos los reclamos con su estado, tipo, etapa y acciones pendientes
- Filtrar por múltiples criterios: recurso, estado, tipo de reclamo, etapa, acción requerida, reputación
- Controlar el estado de las devoluciones asociadas
- Ver cuándo vence el plazo para tomar acción en cada reclamo
- Identificar reclamos que afectan la reputación del vendedor

---

<img src="imagenes/pantalla_ml_reclamos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Reclamos**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda organizados en cuatro grupos.
- **Panel derecho (grilla):** Listado de reclamos con todos sus datos.

---

## Panel izquierdo: Filtros

### Filtros principales

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio para ver resultados. |
| **DESDE** | Fecha de inicio del rango de reclamos a consultar. |
| **HASTA** | Fecha de fin del rango. |
| **VER POR** | Criterio de fecha: por creación del reclamo o por última actualización. |

### Filtros de reclamos

| Campo | Descripción |
|---|---|
| **RECURSO** | Tipo de recurso del reclamo (`order` = venta, `shipment` = envío). |
| **ESTADO** | Estado del reclamo (`opened`, `closed`, `resolved`). |
| **TIPO** | Tipo de reclamo (ej: `not_delivered`, `item_not_as_described`, etc.). |
| **ETAPA** | Etapa del proceso de reclamo (ej: `dispute`, `claim`, `mediation`). |
| **ACCION** | Tipo de acción que ML requiere del vendedor. |
| **REPUTACION** | Filtra reclamos según si afectan o no la reputación del vendedor. |

### Filtros de resolución

| Campo | Descripción |
|---|---|
| **RAZON** | Razón de resolución del reclamo (ej: `seller_refund`, `ml_refund`, etc.). |

### Filtros de envíos

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de logística del envío asociado al reclamo. |

### Filtros de devoluciones

| Campo | Descripción |
|---|---|
| **ESTADO** | Estado de la devolución asociada al reclamo. |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Id Reclamo** | ID único del reclamo en ML |
| **Recurso** | Tipo de recurso: `order` (venta) o `shipment` (envío) |
| **Id Recurso** | ID de la venta o envío asociado al reclamo |
| **Estado** | Estado actual del reclamo |
| **Afecta Rep.** | `SI`/`NO` — indica si el reclamo afecta la reputación del vendedor |
| **Tipo Reclamo** | Motivo del reclamo |
| **Etapa** | Etapa del proceso de reclamo |
| **Descripcion** | Descripción del reclamo ingresada por el comprador |
| **Cliente** | Nombre del comprador que realizó el reclamo |
| **Tipo envio** | Tipo de logística del envío |
| **Actualizado** | Fecha de última actualización del reclamo |
| **Creado** | Fecha de creación del reclamo |
| **Devoluc. Estado** | Estado de la devolución (si hay una asociada) |
| **Accion Oblig.** | Acción que ML requiere que tome el vendedor |
| **Acc. Fecha Lím.** | Fecha límite para tomar la acción requerida |
| **Resolucion** | Razón de resolución del reclamo |
| **Fecha Resoluc.** | Fecha en que se resolvió el reclamo |
| **Beneficiario** | A quién favoreció la resolución (vendedor o comprador) |
| **Resolvente** | Quién resolvió el reclamo (ML, vendedor o comprador) |

---

## Conceptos clave

### Etapas de un reclamo

| Etapa | Descripción |
|---|---|
| `claim` | Reclamo inicial — el comprador abrió el reclamo |
| `dispute` | El comprador solicitó intervención de ML |
| `mediation` | ML está mediando en el conflicto |

### Acciones más comunes requeridas por ML

| Acción | Descripción |
|---|---|
| `respond` | El vendedor debe responder al reclamo |
| `refund` | ML requiere que el vendedor realice el reembolso |
| `return` | El comprador debe devolver el artículo |

---

## Preguntas frecuentes

**¿Cómo sé si un reclamo afecta mi reputación?**
La columna **Afecta Rep.** muestra `SI` para los reclamos que impactan en la reputación del vendedor. Estos son los más urgentes de resolver.

**¿Qué pasa si vence la Acc. Fecha Lím.?**
Si no tomás la acción requerida antes del vencimiento, ML puede resolver el reclamo automáticamente en favor del comprador.

**¿Puedo responder reclamos desde Caddis?**
No. Caddis solo muestra la información de los reclamos. Para responder, accedé directamente al portal de MercadoLibre.

---

> 📖 Para ver el detalle de una venta con reclamo consultá [**Detalle de Venta ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas_Consulta.pdf).
> 📖 Para comunicarte con el comprador consultá [**Mensajes ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Mensajes.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
