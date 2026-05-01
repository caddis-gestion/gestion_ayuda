# 5.03 ARTÍCULOS INVENTARIO
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos Inventario

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Inventario** permite realizar el conteo físico de stock de un depósito y compararlo contra el stock registrado en el sistema. Desde aquí podés:

- Seleccionar un punto de venta/depósito a auditar
- Ingresar las cantidades físicas contadas de cada artículo
- Ver la diferencia entre lo contado y lo registrado en Caddis
- (Solo administradores) Usar lectura por RFID para el conteo

---

<img src="imagenes/pantalla_articulos_inventario.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Articulos Inventario**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con los filtros de búsqueda y un panel derecho con la grilla comparativa de stock.

---

## Panel izquierdo

| Campo / Botón | Descripción |
|---|---|
| **PDV** | Punto de venta / depósito a inventariar. Al seleccionarlo se carga la grilla. |
| **ARTICULO** | Código o descripción del artículo a ingresar la cantidad contada |
| **CANTIDAD** | Cantidad física contada del artículo |
| **Ingresar** | Registra la cantidad contada |
| **Multiple** | Permite ingresar múltiples artículos de una vez |

### Control de Stock por RFID (solo administradores)

| Botón | Descripción |
|---|---|
| **Habilitar lectura por RFID** | Activa el lector RFID para el conteo automático |
| **Descargar lectura solicitada** | Importa los datos leídos por el dispositivo RFID |

---

## Panel derecho — Grilla comparativa

Muestra todos los artículos con stock en el depósito seleccionado y los compara con la auditoría:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad Auditada | Cantidad física contada (editable, resaltada en amarillo) |
| Stock Caddis | Stock registrado en el sistema |
| Diferencia | Diferencia entre lo contado y lo registrado (resaltada en amarillo) |
| Articulo | Descripción del artículo |
| Tipo / Grupo / Marca / Variante | Clasificación del artículo |

---

## Notas importantes

- La columna **Cantidad Auditada** es editable directamente en la grilla.
- La **Diferencia** en negativo indica que hay menos stock físico que el registrado; en positivo, hay más.
- La pantalla solo muestra artículos que tienen stock o que fueron contados (no muestra artículos con stock 0 sin contar).
- La lectura por RFID solo está disponible para usuarios con perfil ADMINISTRADOR.
