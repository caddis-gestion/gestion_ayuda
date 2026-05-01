# 5.XX PEDIDOS DE MERCADERÍA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Pedidos Mercadería

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Pedidos de Mercadería** permite generar pedidos de reposición de artículos al depósito central o al proveedor. Desde aquí podés:

- Crear pedidos de mercadería ingresando artículos manualmente o importando desde un archivo
- Consultar el informe de stock a reponer según los mínimos configurados
- Agregar observaciones al pedido

---

<img src="imagenes/pantalla_pedidos_mercaderia.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Pedidos Mercadería**

---

## Formulario

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha del pedido |
| **OBSERVACIONES** | Texto libre con observaciones para el pedido |
| **CODIGO** | Código del artículo a agregar al pedido (máx. 15 caracteres). Tiene botón **Buscar** para localizar el artículo. Solo visible en modo gestión. |
| **CANTIDAD** | Cantidad a pedir del artículo seleccionado. Botón **Ingresar** para agregar a la lista. Solo visible en modo gestión. |

**Botón Stock Reposición:** Genera un informe de los artículos que necesitan reposición según los mínimos definidos.

### Sección IMPORTAR

Permite cargar masivamente los artículos del pedido desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y agrega los artículos al pedido activo. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **2 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Articulo_Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Cantidad a pedir** | Cantidad a incluir en el pedido | Entero positivo |

#### Validaciones del sistema

- El artículo debe existir en el catálogo de Caddis (de lo contrario se omite sin avisar).
- **El artículo debe tener un proveedor asociado** — si no lo tiene, el sistema devuelve error: *"Artículo: XXX sin proveedor asociado"* y cancela toda la importación.
- Se requiere un PDV activo con lista de precios de proveedor configurada en los parámetros del sistema (`sOCListaProveedor`).

#### Qué hace el sistema al importar

El sistema inserta los artículos en el movimiento de pedido activo, tomando automáticamente el precio de la lista de precios de proveedor configurada. Si el artículo ya estaba en el pedido, lo reemplaza.

---

## Panel derecho — Detalle del pedido

Muestra los artículos ya ingresados en el pedido actual con sus cantidades y datos de identificación.

---

## Notas importantes

- El informe de **Stock Reposición** es útil para identificar qué artículos están por debajo de su mínimo configurado antes de armar el pedido.
- Usá la importación para cargar pedidos con gran cantidad de artículos de forma eficiente.
