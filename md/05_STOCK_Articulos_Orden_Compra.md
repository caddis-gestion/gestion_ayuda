# 5.XX ARTÍCULOS ORDEN DE COMPRA
### Módulo 5 — Stock y Logística

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Artículos Orden de Compra

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Orden de Compra** permite generar órdenes de compra a proveedores para los artículos que tienen pedidos o presupuestos pendientes sin orden de compra asignada. Desde aquí podés:

- Seleccionar el proveedor con artículos pendientes de orden de compra
- Ver el detalle de artículos y cantidades a pedir
- Definir la fecha y agregar observaciones
- Generar la orden de compra con los artículos pendientes

---

<img src="imagenes/pantalla_articulos_orden_compra.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Artículos Orden de Compra**

---

## Circuito completo de órdenes de compra

El sistema ofrece una herramienta para el ingreso y control de órdenes de compra a proveedores. El siguiente diagrama resume el circuito completo:

<img src="imagenes/diagrama_orden_compra_proveedor.png" style="width:auto; height:auto; max-width:100%; display:block;">

Los pedidos de mercadería pueden originarse de dos formas:

| Origen | Comprobante | Descripción |
|---|---|---|
| **Requerimientos internos** | PM — Pedido de Mercadería | El depósito o compras emite un pedido detallando artículos y cantidades necesarias para reponer stock |
| **Pedidos de clientes** | PP — Presupuesto | Un cliente solicita artículos que no están en stock; se les emite un presupuesto |

Ambos comprobantes (PM y PP) deben ser **aprobados por un responsable de compras** antes de poder generar la Orden de Compra al proveedor. Una vez aprobados, se acumulan por proveedor para confeccionar la OC.

---

## Paso a paso — Generar una Orden de Compra

### Etapa 1 — Emitir el pedido o presupuesto

- **Requerimiento interno:** desde **Stock → Pedidos de Mercadería**, emitir un PM indicando artículos y cantidades a reponer. Usar el botón **Stock Reposición** para ver artículos por debajo del stock mínimo.
- **Pedido de cliente:** desde **Ventas y Facturación → Presupuestos**, emitir un PP con los artículos demandados.

### Etapa 2 — Aprobar los pedidos pendientes

Desde **Stock → Pedidos Estado** se consultan todos los PM y PP pendientes de aprobación. El responsable de compras filtra por DESDE/HASTA y ESTADO = Pendiente, y aprueba los que corresponde. Solo los aprobados quedan disponibles para generar OC.

### Etapa 3 — Generar la Orden de Compra

1. Seleccioná el **PROVEEDOR** (solo aparecen los que tienen PM/PP aprobados sin OC)
2. Ingresá la **FECHA**
3. Seleccioná la **ACCION** (COMPRA LOCAL o CREAR EN LLC)
4. Agregá **OBSERVACIONES** si es necesario
5. Hacé clic en **Pedidos y Presupuestos** para ver los artículos pendientes del proveedor
6. Confirmá la generación de la OC

La OC queda registrada y pasa a estado **En Tránsito** hasta que se reciba la mercadería.

### Etapa 4 — Controlar OC en tránsito

Desde **Stock → Compras en Tránsito** se pueden ver todas las OC generadas y pendientes de recepción, con sus cantidades compradas, recibidas y pendientes, filtradas por proveedor y período.

### Etapa 5 — Recibir la mercadería

Cuando llega la mercadería del proveedor, se ingresa desde [**Artículos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Ingresos.pdf) asociando el remito a la **Orden de Compra** correspondiente. El sistema descuenta automáticamente las cantidades de la OC y la elimina del tránsito al completarse la recepción.

---

## Formulario

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de la orden de compra |
| **PROVEEDOR** | Proveedor al que se emite la orden. Solo muestra proveedores que tienen artículos con pedidos o presupuestos aprobados sin orden de compra asignada |
| **ACCION** | Tipo de acción: **COMPRA LOCAL** o **CREAR EN LLC** (disponible solo en empresas configuradas como importadoras USA) |
| **OBSERVACIONES** | Texto libre con observaciones para la orden de compra |

**Botón Pedidos y Presupuestos:** Abre el popup con los artículos pendientes del proveedor seleccionado y genera la orden de compra.

---

## Panel derecho — Detalle de la orden

Muestra el detalle de los artículos que se incluirán en la orden de compra para el proveedor seleccionado:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Articulo | Descripción del artículo |
| Stock Total | Stock actual en todos los almacenes |
| OC en Tránsito | Cantidad ya en tránsito en otras OC |
| Pedidos sin OC | Cantidad pedida aún sin orden de compra asignada |
| PP Sin Facturar | Cantidad de presupuestos sin facturar |
| Stk Min | Stock mínimo configurado para el artículo |
| Stock Repo | Cantidad sugerida a reponer |
| Comprar | Cantidad que se incluirá en esta OC (editable) |

---

## Pantallas relacionadas en el circuito

| Pantalla | Función |
|---|---|
| **Stock → Pedidos de Mercadería** | Emitir pedidos internos de reposición (PM) |
| **Ventas → Presupuestos** | Emitir presupuestos a clientes por artículos sin stock (PP) |
| **Stock → Pedidos Estado** | Aprobar o rechazar PM y PP pendientes antes de generar OC |
| **Stock → Compras en Tránsito** | Consultar OC generadas pendientes de recepción |
| [**Stock → Artículos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Ingresos.pdf) | Recibir la mercadería asociándola a la OC correspondiente |

---

## Notas importantes

- Solo aparecen en el selector de **PROVEEDOR** aquellos que tienen artículos con PM o PP aprobados y sin OC generada.
- Los PM y PP **deben estar aprobados** desde Pedidos Estado para poder incluirse en una OC.
- La OC permanece en estado **En Tránsito** hasta que se reciba la mercadería desde Artículos Ingresos.
- La opción **CREAR EN LLC** solo está disponible en empresas habilitadas como importadoras desde USA.
