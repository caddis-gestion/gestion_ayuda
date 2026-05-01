# 5.26 REMITOS — FACTURAS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Remitos Facturas

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Remitos Facturas** permite generar un remito de entrega a partir de una factura de venta existente, y gestionar los remitos ya emitidos. Desde aquí podés:

- Buscar una factura de venta para generar su remito de entrega
- Configurar los datos del remito (PDV, fecha, cliente)
- Ver los remitos ya entregados asociados a una factura
- Imprimir remitos y etiquetas de envío

---

<img src="imagenes/pantalla_remitos_facturas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Remitos Facturas**

---

## Formulario — Búsqueda de factura

| Campo | Descripción |
|---|---|
| **FACTURA** | Tipo y número de la factura de venta a buscar |
| Botón **Buscar** | Localiza la factura en el sistema |
| Botón **Detalle** | Abre el detalle completo de la factura |

---

## Formulario — Datos del remito

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta desde el que se emite el remito |
| **FECHA** | Fecha del remito |
| **CLIENTE** | Cliente al que se entrega la mercadería |
| **REMITO** | Tipo (R o IR) y número del remito (generado automáticamente) |
| **OBSERVACIONES** | Notas adicionales para el remito |

---

## Panel izquierdo inferior — Remitos entregados

Muestra los remitos ya emitidos y entregados para la factura seleccionada:

| Columna | Descripción |
|---|---|
| Fecha | Fecha del remito |
| Remito | Tipo y número del remito |

**Acciones:**
- **Imprimir:** Imprime el remito
- **Etiqueta:** Imprime la etiqueta de envío del remito

---

## Panel derecho — Detalle de la factura

Muestra el contenido de la factura seleccionada: artículos, cantidades, precios y datos del comprobante.

---

## Notas importantes

- Esta pantalla se usa para generar la documentación de entrega cuando la factura ya fue emitida.
- Los tipos de factura admitidos incluyen FA, FB, FC, NC, OV, entre otros.
- El número de remito se asigna automáticamente por el sistema.
