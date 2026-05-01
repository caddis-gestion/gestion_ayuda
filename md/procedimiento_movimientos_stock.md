# Procedimiento: Movimientos de Stock

> **Versión:** 1.0 — Abril 2026
> **Audiencia:** Operadores de depósito, encargados de compras y logística

---

## ¿De qué trata este procedimiento?

Este documento describe el circuito completo de movimientos de stock en Caddis: desde la generación de una orden de compra al proveedor hasta la recepción de mercadería y los traslados internos entre depósitos.

Caddis distingue dos tipos de artículos que siguen circuitos similares pero con pantallas separadas:

| Tipo | Descripción | Identificación |
|---|---|---|
| **Artículos** | Accesorios, repuestos, insumos y cualquier mercadería sin número de serie | Se controla por cantidad |
| **Equipos (con NSE)** | Celulares, tablets y equipos que tienen Número de Serie (IMEI/NSE) | Cada unidad se identifica individualmente |

---

## Circuito completo

```
[1. PEDIDO]        Pedido de Mercadería (PM) o Presupuesto de cliente (PP)
        │
        ▼
[2. APROBACIÓN]    Responsable aprueba el pedido en Pedidos Estado
        │
        ▼
[3. ORDEN COMPRA]  Se genera la OC al proveedor
        │
        ▼
[4. INGRESO]       Llega la mercadería → se registra el ingreso vinculado a la OC
        │
        ▼
[5. TRASLADO]      (opcional) Se transfiere stock entre depósitos o sucursales
```

---

## Diferencia entre Artículos y Equipos con NSE

| Aspecto | Artículos | Equipos con NSE |
|---|---|---|
| Control de stock | Por cantidad total | Por número de serie individual |
| Ingreso | [**Artículos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Ingresos.pdf) | [**Equipos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Equipos_Ingresos.pdf) |
| Traslados | [**Artículos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Movimientos.pdf) | [**Equipos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Equipos_Movimientos.pdf) |
| Carga masiva | Importar desde Excel | Ingreso múltiple o por rango de NSE |
| Comprobante de ingreso | Remito de ingreso | Remito de ingreso con OC asociada |

---

## Paso 1: Generar el pedido

Antes de comprar al proveedor, el sistema requiere que exista un pedido aprobado. Hay dos orígenes posibles:

### 1.1 Pedido de reposición interno (PM)

Se usa cuando el depósito necesita reponer stock propio, sin que medie un pedido de cliente.

**Pantalla:** [**Pedidos de Mercadería**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Pedidos_Mercaderia.pdf)
**Menú:** Stock → Pedidos Mercadería

| Paso | Acción |
|---|---|
| 1 | Ingresar la **FECHA** del pedido |
| 2 | Usar **Stock Reposición** para ver los artículos por debajo del stock mínimo, o ingresar los artículos manualmente |
| 3 | Completar **CÓDIGO** y **CANTIDAD** por cada artículo |
| 4 | Guardar el pedido |

> El pedido queda en estado **Pendiente** hasta que un responsable lo apruebe.

---

### 1.2 Pedido de cliente (PP)

Cuando un cliente solicita artículos que no están en stock, se emite un presupuesto (PP) desde Ventas. Una vez aprobado, entra en el circuito de compras del mismo modo que un PM.

---

## Paso 2: Aprobar el pedido

**Pantalla:** [**Pedidos Mercadería Estado**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Pedidos_Mercaderia_Estado.pdf)
**Menú:** Stock → Pedidos Mercadería Estado

| Paso | Acción |
|---|---|
| 1 | Filtrar por **ESTADO = Pendiente** y rango de fechas |
| 2 | Seleccionar el pedido en la grilla |
| 3 | Hacer clic en **Aprobar** |

Solo los pedidos en estado **Aprobado** quedan disponibles para generar una Orden de Compra.

> También desde esta pantalla se puede **rechazar** un pedido (queda descartado), **borrar** uno aprobado o ver el **detalle** del estado de cada artículo.

---

## Paso 3: Generar la Orden de Compra al proveedor

**Pantalla:** [**Artículos Orden de Compra**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Orden_Compra.pdf)
**Menú:** Stock → Artículos Orden de Compra

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **PROVEEDOR** (solo aparecen los que tienen pedidos aprobados sin OC) |
| 2 | Ingresar la **FECHA** |
| 3 | Agregar **OBSERVACIONES** si corresponde |
| 4 | Hacer clic en **Pedidos y Presupuestos** para ver y confirmar los artículos a pedir |

La OC queda registrada en estado **En Tránsito** hasta que se reciba la mercadería.

> Para controlar las OC pendientes de recepción, consultar [**Compras en Tránsito**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Orden_Compra_Transito.pdf).

---

## Paso 4: Registrar el ingreso de mercadería

Cuando llega la mercadería del proveedor, se registra el ingreso. Aquí se separan los dos circuitos según el tipo de artículo.

### 4A — Ingreso de Artículos (sin NSE)

**Pantalla:** [**Artículos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Ingresos.pdf)
**Menú:** Stock → Artículos Ingresos

| Paso | Acción |
|---|---|
| 1 | Verificar o ajustar la **FECHA** |
| 2 | Seleccionar el **ORIGEN** (proveedor) |
| 3 | Seleccionar el **DESTINO** (depósito donde ingresa el stock) |
| 4 | Usar **Ordenes Compra** para vincular a la OC pendiente (recomendado) o ingresar artículos manualmente con **ARTÍCULO / COSTO NETO / CANTIDAD** |
| 5 | Alternativa: importar desde Excel con el botón **Importar** (columnas: Codigo, Cantidad, Costo, Despacho) |
| 6 | Confirmar el ingreso |

---

### 4B — Ingreso de Equipos (con NSE)

**Pantalla:** [**Equipos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Equipos_Ingresos.pdf)
**Menú:** Stock → Equipos Ingresos

| Paso | Acción |
|---|---|
| 1 | Verificar la **FECHA** (el número interno se asigna automáticamente) |
| 2 | Completar **PEDIDO**, **REMITO** y **FC.NUMERO / FC.FECHA** del proveedor |
| 3 | Seleccionar **ALMACEN**, **ORIGEN** y **DESTINO** |
| 4 | Seleccionar la **O. DE COMPRA** a la que aplica el ingreso |
| 5 | Ingresar los equipos: individualmente por **NSE**, con **Multiple** (varios NSE a la vez) o con **Rango** (secuencia continua) |
| 6 | Confirmar el ingreso |

> Cada NSE ingresado queda registrado individualmente. El sistema descuenta automáticamente las cantidades pendientes de la OC seleccionada.

---

## Paso 5: Trasladar stock entre depósitos (opcional)

Una vez que la mercadería está en stock, puede transferirse entre depósitos o sucursales.

### 5A — Movimiento de Artículos (sin NSE)

**Pantalla:** [**Artículos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Movimientos.pdf)
**Menú:** Stock → Artículos Movimientos

| Paso | Acción |
|---|---|
| 1 | Seleccionar **ORIGEN** (depósito que envía el stock) |
| 2 | Seleccionar **DESTINO** (depósito que recibe) |
| 3 | Ingresar artículos con **ARTÍCULO / CANTIDAD** o importar desde Excel |
| 4 | Confirmar el movimiento |

> El botón **Reponer** calcula automáticamente los artículos que el destino necesita según sus mínimos.

---

### 5B — Movimiento de Equipos (con NSE)

**Pantalla:** [**Equipos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Equipos_Movimientos.pdf)
**Menú:** Stock → Equipos Movimientos

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **TIPO** (Traslado de Mercadería o Movimiento Interno) |
| 2 | Seleccionar **ORIGEN** y **DESTINO** |
| 3 | Seleccionar el **VENDEDOR** asignado (si aplica) |
| 4 | Ingresar equipos por NSE: individualmente, con **Multiple** o con **Rango** |
| 5 | Confirmar el movimiento |

> Si el depósito destino tiene una **Asignación** activa, seleccionarla con el botón **Buscar** para asociar el movimiento.

---

## Presupuestos pendientes de facturación

Cuando se generan PP (presupuestos de cliente) con artículos que estaban sin stock y se recibieron luego de una OC, el sistema permite consultar cuáles ya tienen mercadería disponible para facturar.

**Pantalla:** [**Presupuestos Pendientes Facturación**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Presupuestos_Pendientes_Facturacion.pdf)
**Menú:** Stock → Presupuestos Pendientes Facturación

Desde aquí se pueden aprobar los PP para que queden disponibles para facturación desde Ventas.

---

## Resumen de pantallas del circuito

| Pantalla | Cuándo usarla |
|---|---|
| [**Pedidos de Mercadería**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Pedidos_Mercaderia.pdf) | Generar un pedido de reposición interno |
| [**Pedidos Mercadería Estado**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Pedidos_Mercaderia_Estado.pdf) | Aprobar / rechazar pedidos pendientes |
| [**Artículos Orden de Compra**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Orden_Compra.pdf) | Generar la OC al proveedor |
| [**Compras en Tránsito**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Orden_Compra_Transito.pdf) | Consultar OC pendientes de recepción |
| [**Artículos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Ingresos.pdf) | Recibir mercadería sin NSE del proveedor |
| [**Equipos Ingresos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Equipos_Ingresos.pdf) | Recibir equipos con NSE del proveedor |
| [**Artículos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Movimientos.pdf) | Transferir artículos sin NSE entre depósitos |
| [**Equipos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Equipos_Movimientos.pdf) | Transferir equipos con NSE entre depósitos |
| [**Presupuestos Pendientes Facturación**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Presupuestos_Pendientes_Facturacion.pdf) | Habilitar PP para facturar una vez recibida la mercadería |
