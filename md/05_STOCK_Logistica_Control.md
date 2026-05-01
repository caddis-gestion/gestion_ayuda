# 5.23 LOGÍSTICA — CONTROL
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Logística Control

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Logística Control** permite consultar y gestionar los envíos registrados en el sistema de logística. Desde aquí podés:

- Buscar envíos por PDV, cliente, factura o rango de fechas
- Asignar transportes a los envíos
- Imprimir remitos y etiquetas
- Consultar el detalle del comprobante asociado a cada envío

---

<img src="imagenes/pantalla_logistica_control.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Logística Control**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a consultar |
| **CLIENTE** | Filtra por cliente específico |
| **FACTURA** | Tipo y número de factura (con botón **Buscar**) |
| **DESDE** | Fecha de inicio del período |
| **HASTA** | Fecha de fin del período |

### Sección TRANSPORTES (si hay transportes integrados configurados)

| Campo/Acción | Descripción |
|---|---|
| **ENVIO ELEGIDO** | Número del envío actualmente seleccionado |
| Botones de transporte | Asigna el envío al transporte seleccionado (Envíopack, Rapiboy, etc.) |
| **Emitir Excel con detalle** | Genera un Excel con el detalle de los envíos |
| **Imprimir remitos y etiquetas** | Imprime los remitos y etiquetas del envío |

---

## Panel derecho — Grilla de envíos

| Columna | Descripción |
|---|---|
| Envio | Número de envío |
| Fecha | Fecha del envío |
| Factura Tipo | Tipo del comprobante de venta |
| Factura Nro | Número del comprobante |
| Factura Fecha | Fecha del comprobante |
| Remito Tipo | Tipo del remito asociado |
| Remito Nro | Número del remito |
| Valor Declarado | Valor declarado del envío |
| Transporte | Empresa de transporte asignada |
| Guia | Número de guía del transporte |
| Cliente | Nombre del cliente |
| Venta Virtual | Indica si es una venta de tienda online |
| Observaciones | Observaciones del comprobante |

**Acciones:**
- **Modificar:** Solicitar alta de entrega en la empresa de logística
- **Detalle:** Consultar el comprobante asociado
- **Etiqueta:** Imprimir la etiqueta de envío

---

## Notas importantes

- Los botones de transporte aparecen solo si la empresa tiene transportes integrados configurados (Envíopack, Rapiboy, etc.).
- Podés buscar un envío específico usando el campo **FACTURA** para localizarlo directamente.
