# 3.39 CAMBIOS DE MERCADERÍA
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Facturación → Cambios de Mercadería

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Cambios de Mercadería** permite procesar el cambio de un artículo vendido: el cliente devuelve un producto y recibe otro a cambio. El sistema genera automáticamente la nota de crédito por el artículo devuelto y la nueva factura por el artículo entregado. Desde aquí podés:

- Buscar la factura original del artículo a cambiar
- Registrar el o los artículos devueltos por el cliente
- Registrar el o los artículos entregados en reemplazo
- Gestionar la diferencia de precio (a favor o en contra del cliente)

---

<img src="imagenes/pantalla_cambios_mercaderia.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Facturación → Cambios de Mercadería**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario del cambio y dos paneles derechos:
- **Panel derecho superior:** Artículos devueltos por el cliente (NC)
- **Panel derecho inferior:** Artículos entregados en reemplazo (nueva factura)

---

## Panel izquierdo — Formulario

### Sección Datos de la Factura

| Campo / Botón | Descripción |
|---|---|
| **FACTURA** | Tipo y número de la factura original a cambiar. Tipos disponibles: EA, A, IA, PA, TK, B, EB, PB, EC, C, IC, PC, M, EM, X, P, NDEA, NDEB, IV |
| **Buscar** | Busca la factura indicada y carga los datos del cliente |
| **Detalle** | Abre el detalle completo de la factura buscada |
| **PDV** | Punto de venta donde se procesa el cambio |
| **VENDEDOR** | Vendedor asignado al cambio |
| **FECHA** | Fecha del cambio |
| **CLIENTE** | Cliente que realiza el cambio (se carga automáticamente al buscar la factura) |

### Sección Datos de la NC

| Campo | Descripción |
|---|---|
| **NC** | Tipo de nota de crédito (se asigna automáticamente según el tipo de factura original) y número de la NC |
| **NUEVA FC** | Para facturas tipo A, B o C: tipo y número de la nueva factura a emitir |
| **LISTA** | Lista de precios para los artículos de reemplazo |
| **ARTICULO** | Código del artículo a entregar en reemplazo. Botón **Buscar** para buscar en el catálogo; botón **#Series** para ingreso masivo de NSE. |
| **IMPORTE** | Importe del artículo de reemplazo |
| **CANTIDAD** | Cantidad del artículo de reemplazo |

**Botón PAGOS:** Abre el popup de medios de pago para registrar diferencias de precio (si el artículo de reemplazo es más caro o más barato).

**OBSERVACIONES:** Notas del cambio.

---

## Panel derecho superior — Artículos devueltos

Muestra los artículos que el cliente devuelve (originados en la factura buscada):

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo devuelto |
| Articulo | Descripción + NSE (si aplica) |
| Cantidad | Cantidad devuelta |
| Total | Importe original del artículo |
| Q_FC | Cantidad ya utilizada en cambios anteriores |

Los artículos se cargan automáticamente desde la factura original. Podés ajustar la cantidad en la columna **Cantidad** si el cambio es parcial. Botón **Borrar** para quitar un ítem.

---

## Panel derecho inferior — Artículos entregados

Muestra los artículos que se entregan al cliente como reemplazo (la nueva factura):

Funciona igual que la grilla de artículos de facturación: muestra los ítems ingresados con su código, descripción, cantidad e importe.

---

## Paso a paso — Procesar un cambio de mercadería

1. Ingresá el tipo y número de la **FACTURA** original y hacé clic en **Buscar**
2. El sistema carga los datos del cliente y los artículos devueltos en el panel superior
3. Ajustá la cantidad a devolver si el cambio es parcial
4. Seleccioná el **PDV**, **VENDEDOR** y verificá la **FECHA**
5. En el campo **ARTICULO**, ingresá o buscá el artículo de reemplazo
6. Completá **IMPORTE** y **CANTIDAD**, y hacé clic en **Ingresar artículo**
7. Si hay diferencia de precio, hacé clic en **Pagos** y registrá el medio de pago
8. Agregá **OBSERVACIONES** si es necesario
9. Guardá el cambio — el sistema emite la NC y la nueva factura automáticamente

---

## Notas importantes

- El sistema determina automáticamente el tipo de nota de crédito según el tipo de factura original (ej: factura B → NCIB o NCB; factura A → NCIA, NCEA o NCA).
- Para facturas tipo A, B o C, el campo **NUEVA FC** permite ingresar el número de la factura de reemplazo.
- Si el artículo de reemplazo tiene un precio mayor al original, la diferencia se cobra al cliente mediante el botón **Pagos**.
- Si el artículo de reemplazo tiene un precio menor, la diferencia queda como saldo a favor del cliente.
