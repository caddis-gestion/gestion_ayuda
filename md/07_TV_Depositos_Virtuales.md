# 7.19 TV DEPÓSITOS VIRTUALES
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Depósitos Virtuales

---

## ¿Para qué sirve esta pantalla?

**TV Depósitos Virtuales** permite vincular los depósitos físicos de Caddis con las cuentas de tiendas virtuales. Cada depósito virtual define cómo se comporta ese punto de venta en relación al stock y a la logística de envíos. Desde aquí podés:

- Agregar depósitos virtuales a una cuenta de tienda
- Configurar las opciones de stock, armado de remitos y logística de cada depósito
- Ordenar los depósitos para determinar la prioridad de uso de stock

---

<img src="imagenes/pantalla_tv_depositos_virtuales.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Depósitos Virtuales**

---

## Panel izquierdo: Agregar depósito

| Campo / Botón | Descripción |
|---|---|
| **TIENDA** | Selector de tienda virtual. |
| **USUARIO** | Cuenta de la tienda donde se agregará el depósito. |
| **PDV** | Punto de venta (depósito físico) a vincular. Desplegable con los PDV configurados en Caddis. |
| **Agregar** | Vincula el PDV seleccionado como depósito virtual de la cuenta. |

---

## Panel derecho: Grilla de depósitos virtuales

Lista los depósitos ya configurados para la cuenta seleccionada.

| Columna | Descripción |
|---|---|
| **Orden** | Número de orden de prioridad (editable, fondo amarillo). El sistema usa primero el depósito con menor número de orden para tomar stock. |
| **Depósito** | Nombre del depósito físico vinculado. |
| **Cód Externo** | Código del depósito en la tienda virtual (asignado por la plataforma). |
| **Tipo** | Clasificación del depósito. |
| **Remito Automático** | SI: el sistema genera el remito de manera automática al confirmar la venta. |
| **Altera Stock** | SI: las ventas de esta tienda descuentan stock en este depósito. |
| **Entrega en Mostrador** | SI: permite registrar retiros del comprador en el local. |
| **Envía a Domicilio** | SI: habilita el despacho a domicilio desde este depósito. |
| **Envía Logística Interna** | SI: habilita el uso de logística interna de la tienda virtual. |
| **Recibe Logística Interna** | SI: el depósito puede recibir devoluciones vía logística interna. |
| **Borrar** | Elimina el depósito virtual de la cuenta. |

---

## Configuración del orden de depósitos

El campo **Orden** define la prioridad: cuando una venta necesita descontar stock, el sistema usa primero el depósito con el número más bajo. Podés editar el valor directamente en la celda amarilla y guardar con el botón correspondiente.

---

## Uso típico

1. Seleccioná la **TIENDA** y el **USUARIO**.
2. Elegí el **PDV** a vincular y hacé clic en **Agregar**.
3. En la grilla, configurá las opciones de cada depósito (Remito Automático, Altera Stock, etc.).
4. Ajustá el **Orden** para definir la prioridad de uso de stock entre depósitos.

> ⚠️ Si un depósito tiene **Altera Stock = NO**, las ventas de esa tienda no descontarán inventario en Caddis. Verificá esta configuración antes de comenzar a operar.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
