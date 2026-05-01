# 5.09 ARTÍCULOS COMPUESTOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Compuestos

---

## ¿Para qué sirve esta pantalla?

Los **artículos compuestos** son artículos que para su venta utilizan más de un insumo o componente. Por ejemplo: un "Café con Leche" que consume café, leche, azúcar, cuchara y vaso.

Caddis creó esta herramienta para que al facturar el artículo compuesto, el sistema descuente automáticamente del stock todos sus insumos en las cantidades configuradas, mientras el cliente ve en la factura únicamente el artículo que pidió.

Desde esta pantalla podés:

- Definir qué insumos componen un artículo compuesto y en qué cantidad
- Agregar o quitar componentes de un artículo
- Indicar si cada componente descuenta stock o no al facturar

---

<img src="imagenes/pantalla_articulos_compuestos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Compuestos**

---

## Requisito previo — Crear los artículos en el sistema

Antes de configurar un artículo compuesto, todos los artículos involucrados deben existir en el catálogo (**Stock → Artículos**):

| Tipo de artículo | Configuración en ABM Artículos | Ejemplo |
|---|---|---|
| **Insumos / componentes** | `SERVICIO = NO` — llevan control de stock | Café, Leche, Azúcar, Vaso, Cuchara |
| **Artículo compuesto** (el que se vende) | `SERVICIO = SI` — no lleva stock propio; se factura normalmente | Café Chico Cortado, Café con Leche |

> El artículo compuesto que se factura al cliente debe tener `SERVICIO = SI` porque el stock se gestiona a través de sus insumos, no del artículo en sí.

---

## Formulario

| Campo | Descripción |
|---|---|
| **ARTICULO** | El artículo compuesto que se va a vender (el "producto terminado"). Ej.: CAFÉ CHICO CORTADO |
| **COMPUESTO** | El insumo o componente que forma parte del artículo. Se ingresa uno a la vez. Ej.: CAFÉ |
| **CANTIDAD** | Cantidad del insumo que consume una unidad del artículo compuesto. Ej.: 10 (gramos de café por taza) |
| **USA STOCK** | Indica si este componente descuenta stock al vender el artículo compuesto (SI / NO) |

**Botones:**
- **Nuevo:** Limpia el formulario para agregar un nuevo artículo compuesto.
- **Guardar:** Guarda el componente ingresado y lo agrega a la grilla del panel derecho.

---

## Panel derecho — Grilla de componentes

Muestra todos los insumos configurados para el artículo seleccionado. Cada fila representa un componente:

| Columna | Descripción |
|---|---|
| *(ícono cesto)* | Elimina el componente del artículo compuesto |
| **Cantidad** | Cantidad del insumo por unidad de artículo compuesto |
| **Compuesto** | Nombre del insumo/componente |
| **Artículo** | Nombre del artículo compuesto al que pertenece |

---

## Paso a paso — Configurar un artículo compuesto

**Ejemplo:** configurar "CAFÉ CHICO CORTADO" con sus insumos (Café × 10, Leche × 10, Azúcar × 3, Vaso Chico × 1, Cuchara × 1).

**1. Seleccionar el artículo compuesto**
- En el campo **ARTICULO**, buscá y seleccioná el artículo terminado (ej.: CAF10002 - CAFÉ CHICO CORTADO).
- El campo CANTIDAD se inicializa en 1.

**2. Agregar el primer insumo**
- En el campo **COMPUESTO**, buscá y seleccioná el primer insumo (ej.: CAFÉ).
- En **CANTIDAD**, ingresá cuántas unidades de ese insumo consume el artículo (ej.: 10).
- Hacé clic en **Guardar**.
- El insumo aparece en la grilla del panel derecho con su cantidad y el nombre del artículo.

**3. Agregar los insumos restantes**
- Sin cambiar el **ARTICULO**, seleccioná el siguiente insumo en **COMPUESTO**, completá la **CANTIDAD** y guardá.
- Repetí este paso para cada componente hasta completar la composición.

**4. Verificar la composición**
- La grilla debe mostrar todos los insumos con sus cantidades correctas.
- Si necesitás eliminar un componente, usá el ícono del cesto en su fila.

---

## Comportamiento al facturar

Una vez configurado el artículo compuesto, se factura como cualquier artículo común desde la pantalla de Facturación. El cliente ve únicamente el artículo compuesto en el comprobante.

Internamente, al facturar una unidad del artículo compuesto, el sistema **descuenta automáticamente del stock** cada insumo en la cantidad configurada:

| Insumo | Cantidad configurada | Efecto al facturar 1 unidad |
|---|---|---|
| CAFÉ | 10 | −10 unidades de stock |
| LECHE | 10 | −10 unidades de stock |
| AZÚCAR | 3 | −3 unidades de stock |
| VASO CHICO | 1 | −1 unidad de stock |
| CUCHARA | 1 | −1 unidad de stock |

> Si se facturan 2 unidades del artículo compuesto, el descuento de stock se multiplica proporcionalmente.

---

## Notas importantes

- Si **USA STOCK = NO**, el componente figura en la composición pero **no genera movimiento de stock** al facturar. Útil para insumos que se contabilizan de otra forma o que no requieren control.
- Si el artículo seleccionado no tiene componentes aún, el panel derecho aparece vacío.
- Un artículo compuesto puede tener tantos componentes como sea necesario.
- Los insumos deben existir previamente en el catálogo de artículos antes de poder seleccionarlos como componentes.
- El precio del artículo compuesto se define en la lista de precios como cualquier otro artículo — es independiente de los costos de los insumos.
