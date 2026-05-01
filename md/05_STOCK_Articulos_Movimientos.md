# 5.04 ARTÍCULOS MOVIMIENTOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Movimientos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Movimientos** permite registrar transferencias de stock entre depósitos o sucursales. Se usa para mover mercadería de un local a otro, o para registrar salidas y entradas internas. Desde aquí podés:

- Crear un remito de movimiento de stock entre depósitos
- Definir el origen y destino del movimiento
- Ingresar artículos con precio de venta y cantidad
- Importar el detalle desde un archivo
- Reponer stock automáticamente

---

<img src="imagenes/pantalla_articulos_movimientos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Movimientos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario del movimiento y un panel derecho con el detalle de artículos cargados.

---

## Encabezado del movimiento

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha del movimiento |
| **REMITO** | Número de remito de movimiento (se asigna automáticamente) |
| **ORIGEN** | Depósito de origen del stock |
| **DESTINO** | Depósito de destino. Puede ser otro PDV, almacén central u otro depósito según la configuración del sistema |
| **OBSERVACIONES** | Notas sobre el movimiento |

---

## Sección de artículos

| Campo / Botón | Descripción |
|---|---|
| **ARTICULO** | Código o descripción del artículo a transferir |
| **P.VENTA** | Precio de venta del artículo (se autocompleta) |
| **CANTIDAD** | Cantidad a transferir |
| **Ingresar** | Agrega el artículo al movimiento |
| **Multiple** | Permite ingresar múltiples artículos a la vez |
| **Reponer** | Calcula y carga automáticamente los artículos que necesitan reposición |

---

## Sección IMPORTAR

Permite cargar masivamente el detalle de un movimiento de stock desde un archivo Excel.

| Campo / Botón | Descripción |
|---|---|
| **Selector de archivo** | Seleccioná el archivo Excel (.xlsx) a importar. |
| **Importar** | Procesa el archivo y agrega los artículos al movimiento activo. |
| **Formato** | Muestra un ejemplo del formato requerido con datos reales del sistema. |

#### Formato del archivo de importación

El archivo debe tener **3 columnas**:

| Columna | Descripción | Valores válidos |
|---|---|---|
| **Codigo** | SKU del artículo en Caddis | Debe existir en el catálogo |
| **Cantidad** | Cantidad de unidades a mover | Entero positivo |
| **Costo** | Costo unitario del artículo | Decimal. Acepta `$` y miles con punto. Ej: `3.500,00` o `3500.00` |

#### Validaciones del sistema

- El artículo debe existir en el catálogo de Caddis; los no encontrados se omiten.
- El símbolo `$` en el costo se elimina automáticamente.
- Se aceptan **ambos formatos** de número decimal: punto o coma como separador decimal (el sistema detecta y convierte automáticamente).

#### Qué hace el sistema al importar

El sistema inserta los artículos en el movimiento de stock activo. Si el artículo ya estaba en el movimiento, lo reemplaza con los nuevos datos de cantidad y costo.

---

## Panel derecho — Detalle del movimiento

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Unidades a transferir |
| Precio Unitario | Precio de venta (con IVA, editable) |
| Total | Precio total |
| Articulo | Descripción |
| Tipo / Grupo / Marca / Variante | Clasificación |

**Acciones:**
- **Borrar:** Elimina un artículo del movimiento

---

## Notas importantes

- El depósito **DESTINO** disponible depende de la configuración: si `sStkMovSucursales` está activo, se puede mover a cualquier sucursal; si no, solo al depósito local o central.
- El movimiento descuenta stock del ORIGEN y lo acredita en el DESTINO al confirmarse.
- El precio de venta (col 3) es editable en la grilla.
