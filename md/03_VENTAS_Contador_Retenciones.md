# 3.45 CONTADOR RETENCIONES
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Contador Retenciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Contador Retenciones** permite configurar el próximo número a utilizar para los comprobantes de retención de Ingresos Brutos (IIBB) por provincia. Desde aquí podés:

- Ver el número de retención actual para cada provincia de Argentina
- Modificar el contador si fue necesario reiniciarlo o corregirlo

> ℹ️ Esta pantalla es de uso administrativo. Normalmente se configura una sola vez y no requiere mantenimiento frecuente, salvo que haya un error en la numeración.

---

<img src="imagenes/pantalla_contador_retenciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Contador Retenciones**

---

## Descripción general de la pantalla

La pantalla muestra una lista con todas las provincias de Argentina que tienen retención de IIBB habilitada, junto con el próximo número de retención a emitir para cada una.

---

## Listado de provincias

Cada fila corresponde a una provincia y muestra:

| Campo | Descripción |
|---|---|
| **Nombre de la provincia** | Provincia de Argentina (sólo las que tienen retención de IIBB configurada) |
| **Número** | Próximo número de retención a utilizar para esa provincia. Es un campo editable. |

---

## Cómo modificar un contador

1. Localizá la provincia cuyo contador necesitás corregir
2. Modificá el número en el campo correspondiente
3. Guardá los cambios

---

## Notas importantes

- El contador se incrementa automáticamente cada vez que se emite un comprobante de retención para esa provincia.
- Solo modificar este valor si hubo un error en la numeración o si se reinicia el talonario.
- Las provincias mostradas son sólo las que tienen alias configurado (provincias habilitadas para retención en el sistema).
