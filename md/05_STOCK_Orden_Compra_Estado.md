# 5.22 ORDEN DE COMPRA — ESTADO
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Orden de Compra Estado

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Orden de Compra Estado** permite consultar el estado global de las Órdenes de Compra en un período determinado. Podés filtrar por estado y visualizar los resultados agrupados por OC, artículo o proveedor. Desde aquí podés:

- Filtrar OC por rango de fechas y estado
- Ver el estado de recepción de mercadería (pendiente, recibido, descartado)
- Enviar órdenes de compra al proveedor e imprimirlas
- Acceder al detalle de cada OC

---

<img src="imagenes/pantalla_orden_compra_estado.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Orden de Compra Estado**

---

## Formulario

| Campo | Descripción |
|---|---|
| **DESDE** | Fecha de inicio del período a consultar |
| **HASTA** | Fecha de fin del período |
| **ESTADO** | Estado de las OC: PENDIENTE, ENVIADO o COMPLETO |
| **MOSTRAR POR** | Agrupa los resultados: ORDEN DE COMPRA, ARTICULO o PROVEEDOR |

---

## Panel derecho — Grilla de resultados

### Vista por ORDEN DE COMPRA

| Columna | Descripción |
|---|---|
| Fecha | Fecha de la OC |
| Tipo | Tipo de comprobante (OC) |
| Numero | Número de la OC |
| Cantidad | Cantidad total pedida |
| Recibido | Cantidad recibida |
| Descartado | Cantidad descartada |
| Pendiente | Cantidad pendiente de recibir (en amarillo) |
| Proveedor | Nombre del proveedor |
| Estado | Estado actual de la OC |

**Acciones:**
- **Borrar:** Elimina la Orden de Compra
- **Enviar:** Envía la OC al proveedor por correo
- **Imprimir:** Imprime el comprobante
- **Detalle:** Ver el estado detallado de la OC (abre la pantalla Orden de Compra Control)

### Vista por ARTÍCULO

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Articulo | Descripción del artículo |
| Cantidad | Cantidad total pedida |
| Recibido | Cantidad recibida |
| Descartado | Cantidad descartada |
| Pendiente | Cantidad pendiente (en amarillo) |

### Vista por PROVEEDOR

| Columna | Descripción |
|---|---|
| Proveedor | Nombre del proveedor |
| Cantidad | Cantidad total pedida |
| Recibido | Cantidad recibida |
| Descartado | Cantidad descartada |
| Pendiente | Cantidad pendiente (en amarillo) |

---

## Notas importantes

- El estado por defecto al abrir la pantalla es **PENDIENTE**.
- Usá la vista por **ARTÍCULO** para detectar faltantes de stock en tránsito.
- Usá la vista por **PROVEEDOR** para tener un resumen consolidado de lo que adeuda cada proveedor.
