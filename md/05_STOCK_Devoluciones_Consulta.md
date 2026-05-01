# 5.33 DEVOLUCIONES — CONSULTA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Devoluciones Consulta

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Devoluciones Consulta** permite consultar el historial de devoluciones registradas, con múltiples filtros de búsqueda. Desde aquí podés:

- Buscar devoluciones por lote, período, motivo, estado o usuario
- Ver el detalle de cada devolución con la factura y nota de crédito asociada

---

<img src="imagenes/pantalla_devoluciones_consulta.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Devoluciones Consulta**

---

## Formulario

| Campo | Descripción |
|---|---|
| **LOTE** | Número del lote de devolución a consultar |
| **DESDE** | Fecha de inicio del período (por defecto: últimos 7 días) |
| **HASTA** | Fecha de fin del período |
| **MOTIVO** | Motivo de la devolución |
| **ESTADO** | Estado de la devolución |
| **USUARIO** | Usuario que registró la devolución |

Los filtros se aplican automáticamente al cambiar cualquier campo.

---

## Panel derecho — Grilla de devoluciones

| Columna | Descripción |
|---|---|
| Devolucion | Código identificador de la devolución |
| Fecha | Fecha y hora de creación |
| Estado | Estado actual de la devolución |
| Motivo | Motivo de la devolución |
| Factura | Número de factura de origen |
| NC | Nota de crédito asociada (si fue emitida) |
| Articulo Codigo | Código del artículo devuelto |
| Articulo Nombre | Descripción del artículo |
| Articulo Serie | Número de serie del artículo |
| Observaciones | Observaciones registradas |

Las primeras 4 columnas están fijas para facilitar la navegación horizontal.

**Acciones:**
- **Detalle:** Abre el detalle de la devolución seleccionada

---

## Notas importantes

- Los resultados se ordenan por número de lote descendente (los más recientes primero).
- Para registrar nuevas devoluciones usá la pantalla **Devoluciones**.
- Para gestionar envíos a garantía usá **Devoluciones Garantía**.
