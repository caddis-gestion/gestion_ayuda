# 5.32 DEVOLUCIONES
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Devoluciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Devoluciones** permite registrar la devolución de artículos vendidos, asociándola a la factura original. Cada devolución queda agrupada en un lote. Desde aquí podés:

- Buscar la factura de venta a la que corresponde la devolución
- Seleccionar qué artículos de esa factura se devuelven
- Indicar el motivo y el estado de cada devolución
- Registrar observaciones por ítem
- Consultar el historial de un lote de devoluciones

---

<img src="imagenes/pantalla_devoluciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Devoluciones**

---

## Formulario — Búsqueda

| Campo | Descripción |
|---|---|
| **POR FACTURA** | Tipo y número de la factura de venta (con botón **Buscar** y **Detalle**) |
| **POR LOTE** | Número del lote de devolución existente |

---

## Panel de devoluciones

Al cargar una factura, se muestra la lista de artículos facturados (uno por unidad). Para cada artículo:

| Campo | Descripción |
|---|---|
| Checkbox | Selección del ítem para incluirlo en la devolución |
| Código | Código del artículo (solo lectura) |
| Nº de Serie | Número de serie del artículo si corresponde (solo lectura) |
| **Motivo** | Motivo de la devolución (seleccionable de lista) |
| **Estado** | Estado de la devolución (visible para usuarios con permiso de modificación) |
| **Observaciones** | Texto libre con notas adicionales sobre este ítem |

Hay un checkbox **"Seleccionar todo"** para marcar todos los ítems de la factura de una vez.

---

## Historial de lote

Si ya existe un lote de devoluciones para la factura buscada, se muestra el historial con los cambios realizados al lote.

---

## Notas importantes

- Cada búsqueda de factura genera o recupera automáticamente el número de lote de devoluciones asociado.
- La devolución se registra por unidad de cada artículo facturado.
- Para consultar devoluciones registradas usá **Devoluciones Consulta**.
- Para gestionar las que deben enviarse al proveedor en garantía usá **Devoluciones Garantía**.
