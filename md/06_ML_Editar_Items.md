# 6.05 ML EDITAR ÍTEMS DE VENTA
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Ventana emergente accesible desde ML Ventas

---

## ¿Para qué sirve esta pantalla?

**ML Editar Ítems** es una ventana emergente que permite asignar o corregir los números de serie (NSE/IMEI) de los equipos incluidos en una venta de MercadoLibre. Desde aquí podés:

- Ver todos los ítems (artículos) de una orden de venta ML
- Ingresar o modificar el número de serie de cada equipo
- Guardar los cambios para vincular correctamente el NSE al movimiento de stock

> ℹ️ Esta pantalla se usa principalmente para celulares y equipos que se tracean por número de serie. Si la venta incluye artículos sin NSE (accesorios, consumibles), esas filas no requieren edición.

---

<img src="imagenes/pantalla_ml_editar_items.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Esta pantalla es una ventana emergente. Se accede desde:
**ML Ventas → seleccionar una venta → botón Modificar**

---

## Descripción de la pantalla

La ventana muestra una tabla con todos los ítems de la orden de venta seleccionada.

| Columna | Descripción |
|---|---|
| **Codigo** | Código del artículo en Caddis |
| **Serie** | Campo editable — ingresá o modificá el número de serie (NSE/IMEI) del equipo |
| **Nombre** | Nombre o descripción del artículo |

---

## Cómo editar los números de serie

1. Abrí la venta en **ML Ventas** y hacé click en **Modificar**.
2. Se abre la ventana con la lista de ítems de esa venta.
3. En la columna **Serie**, ingresá el NSE o IMEI correspondiente a cada equipo.
4. Si hay varios ítems, completá cada fila por separado.
5. Hacé click en **Guardar** para registrar los cambios.

---

## Notas importantes

- El número de serie ingresado debe existir en el inventario del depósito vinculado a la venta. Si el NSE no existe, el sistema mostrará un error al guardar.
- Cambiar el NSE en esta ventana actualiza el vínculo entre la venta ML y el equipo físico en el sistema de stock de Caddis.
- Si la venta ya fue remitada con un NSE correcto, no es necesario editar este campo.

---

> 📖 Para ver y gestionar las ventas de ML consultá [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
