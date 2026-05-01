# 5.XX REPOSICIÓN LOCALES
### Módulo 5 — Stock y Logística

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Artículos Reposición Locales

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Reposición Locales** permite calcular automáticamente las cantidades a reponer en cada punto de venta, basándose en el historial de ventas y los parámetros de reposición configurados. Desde aquí podés:

- Calcular qué artículos necesitan reposición y en qué cantidad según las ventas del período
- Consultar el stock actual en el PDV y en el depósito central
- Ajustar manualmente las cantidades a reponer
- Guardar el pedido de reposición o recuperar uno guardado anteriormente
- Exportar el pedido a PDF

---

<img src="imagenes/pantalla_reposicion_locales.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Artículos Reposición Locales**

---

## Métodos de cálculo de reposición

El sistema puede calcular la reposición usando dos métodos:

### 1 — Índice de reposición

Se define un índice que el sistema multiplica por las ventas del período seleccionado para determinar el stock objetivo en el PDV.

**Ejemplo:** Si se desea mantener en el punto de venta el doble de lo vendido en el período, el índice es **2**. Si en ese período se vendieron 3 unidades, el sistema calculará que se deben reponer 6 − stock actual.

> El índice general se configura en los parámetros del sistema y se muestra como **INDICE DE REPOSICION** (solo lectura) en el formulario.

### 2 — Stock mínimo de reposición

Se define por artículo y por punto de venta desde [**Mínimos Reposición PDV**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Minimos_Reposicion.pdf). El valor puede ser distinto para el mismo artículo en distintos puntos de venta.

> **Regla de prioridad:** Si el stock mínimo de reposición de un artículo es **0**, el sistema utiliza el índice de reposición general para ese artículo.

---

## Formulario

| Campo | Descripción |
|---|---|
| **PEDIDO** | Número del pedido guardado (solo lectura) |
| **PDV** | Punto de venta para el que se calcula la reposición |
| **FECHA** | Fecha del pedido de reposición |
| **PROVEEDOR** | Filtra los artículos por proveedor. Al cambiar aplica el filtro automáticamente. |
| **PERIODO DE VENTAS** | Cantidad de días de ventas a considerar para el cálculo (por defecto: 7 días) |
| **INDICE DE REPOSICION** | Índice de reposición configurado en los parámetros del sistema (solo lectura) |

**Botones de acción:**

| Botón | Descripción |
|---|---|
| **Nuevo** | Limpia el formulario para comenzar un nuevo cálculo |
| **Guardar** | Guarda el pedido de reposición y genera un número interno de pedido |
| **Eliminar** | Elimina el pedido guardado y libera el stock reservado |
| **Reponer** | Calcula las cantidades a reponer según las ventas del período e índice/mínimos definidos |
| **PDF** | Exporta el pedido actual a PDF |
| **Buscar Pedido** | Recupera un pedido de reposición guardado anteriormente por su número |

---

## Panel derecho — Grilla de reposición

Muestra los artículos con sus datos de stock y las cantidades calculadas:

| Columna | Descripción |
|---|---|
| Pedido | Número del pedido al que pertenece la fila |
| Fecha | Fecha del pedido |
| Codigo | Código del artículo |
| Ventas | Unidades vendidas en el período seleccionado |
| Stock Repo | Stock mínimo de reposición configurado para el artículo en el PDV |
| Stock PDV | Stock actual en el punto de venta |
| Stock Central | Stock disponible en el depósito central |
| Tomado | Cantidad ya tomada del stock central para este pedido |
| Reponer | Cantidad a reponer calculada por el sistema (editable, en amarillo) |
| Entregado | Cantidad ya entregada de pedidos anteriores |
| Articulo | Descripción del artículo |
| Tipo | Tipo del artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |

La columna **Reponer** es editable directamente en la grilla para ajustar la cantidad antes de confirmar el pedido.

---

## Paso a paso — Generar un pedido de reposición

1. Seleccioná el **PDV** a reponer
2. Ingresá el **PERIODO DE VENTAS** (días a considerar)
3. Opcionalmente filtrá por **PROVEEDOR**
4. Hacé clic en **Reponer** — el sistema calcula las cantidades necesarias para cada artículo cruzando ventas, stock actual y parámetros de reposición
5. Revisá la grilla y ajustá manualmente la columna **Reponer** donde sea necesario (ej. artículos de temporada, nuevos ingresos, etc.)
6. Hacé clic en **Guardar** — el sistema genera un número interno de pedido

> El pedido puede modificarse o eliminarse hasta que se realice el movimiento de mercadería al PDV.

---

## Envío de la mercadería al local

Una vez guardado el pedido, el envío físico de la mercadería se gestiona desde [**Artículos Movimientos**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Articulos_Movimientos.pdf):

1. Abrí **Artículos Movimientos**
2. Hacé clic en el botón **Reponer**
3. Seleccioná el número de pedido generado en esta pantalla
4. El sistema arma el remito automáticamente con las cantidades definidas
5. A medida que los pedidos se van entregando, desaparecen de la lista de pedidos pendientes

---

## Notas importantes

- El sistema calcula la reposición cruzando las ventas del período, el stock disponible en el PDV y en el depósito central.
- Si el **stock mínimo de reposición** de un artículo es **0**, se aplica el **índice general**.
- La columna **Reponer** puede ajustarse manualmente para corregir desvíos por períodos atípicos (ej. Navidad, artículos nuevos).
- Al **Eliminar** el pedido se libera el stock que estaba reservado.
- Para configurar los mínimos de reposición por artículo y PDV usá [**Mínimos Reposición PDV**](https://ayuda.caddis.com.ar/instructivos/05_STOCK_Minimos_Reposicion.pdf).
