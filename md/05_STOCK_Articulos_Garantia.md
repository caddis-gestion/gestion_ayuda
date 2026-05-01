# 5.46 ARTÍCULOS — GARANTÍA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Artículos Garantía

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos Garantía** permite configurar los artículos de garantía extendida que se ofrecen junto con la venta de productos. Permite definir la compañía aseguradora, el plazo, la tasa o importe fijo, y si se cotiza automáticamente. Desde aquí podés:

- Crear y configurar artículos de garantía extendida
- Asociarlos a una compañía aseguradora
- Definir si la cotización se aplica automáticamente al vender
- Ver, modificar y eliminar las garantías configuradas

---

<img src="imagenes/pantalla_articulos_garantia.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Artículos Garantía**

---

## Formulario

| Campo | Descripción |
|---|---|
| **COMPAÑIA** | Compañía aseguradora que provee la garantía extendida |
| **CODIGO** | Código del artículo de garantía (máx. 8 caracteres) |
| **GARANTIA** | Descripción de la garantía (hasta 255 caracteres, se guarda en mayúsculas) |
| **PLAZO** | Duración de la garantía en meses (máx. 2 dígitos) |
| **TASA** | Porcentaje del importe del artículo asegurado (%) |
| **IMPORTE** | Importe fijo de la garantía (alternativa a la tasa) |
| **AUTOMATICO** | SI/NO — Si la garantía se cotiza automáticamente en la venta |

---

## Panel derecho — Grilla de garantías

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo de garantía |
| Tasa | Tasa porcentual configurada |
| Importe | Importe fijo configurado |
| Plazo | Plazo de la garantía en meses |
| Cotizacion Automatica | SI/NO — cotización automática activada |
| Garantía | Descripción de la garantía |
| Aseguradora | Nombre de la compañía aseguradora |

**Acciones:**
- **Modificar:** Edita la garantía seleccionada
- **Borrar:** Elimina la garantía

---

## Notas importantes

- Solo se muestran artículos de tipo 21 (garantías extendidas).
- Se puede usar tasa O importe fijo, no ambos simultáneamente.
- Las compañías aseguradoras se configuran en tablas globales del sistema.
