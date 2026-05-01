# 5.12 ARTÍCULOS PRODUCCIÓN
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Produccion

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Producción** permite registrar el ingreso de artículos producidos internamente (fabricación o ensamble propio), relacionando el producto final con el depósito de destino. Desde aquí podés:

- Crear un remito de producción indicando el producto final obtenido
- Registrar la cantidad producida y la unidad de medida
- Consultar el historial de producciones realizadas para cada depósito

---

<img src="imagenes/pantalla_articulos_produccion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Produccion**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de producción y un panel derecho con el historial de producciones del depósito seleccionado.

---

## Panel izquierdo

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha de la producción |
| **REMITO** | Número de remito de producción (se asigna automáticamente) |
| **DEPOSITO** | Depósito de destino donde se acredita el producto producido |
| **OBSERVACIONES** | Notas sobre la producción |

### Sección Producto final

| Campo | Descripción |
|---|---|
| **PROD. FINAL** | Artículo resultante de la producción |
| **DESCRIPCION** | Descripción del artículo (solo lectura, se completa automáticamente) |
| **CANTIDAD** | Cantidad producida |
| **Unidad** | Unidad de medida (ej. unidades, kg, litros) |

---

## Panel derecho — Historial de producciones

Muestra las producciones anteriores hacia el depósito seleccionado:

| Columna | Descripción |
|---|---|
| Codigo | Código del producto |
| Descripcion | Tipo y descripción del artículo producido |
| Cantidad | Cantidad producida con unidad |
| Fecha | Fecha del movimiento |
| Remito | Número de remito |
| Usuario | Usuario que registró la producción |
| Observaciones | Notas del movimiento |

---

## Notas importantes

- El movimiento de producción proviene siempre de un depósito de producción interno definido en el sistema.
- La unidad de medida disponible depende del artículo seleccionado como producto final.
