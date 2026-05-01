# 5.25 LOGÍSTICA EXTERNA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Logística Externa

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Logística Externa** permite gestionar los envíos a domicilio a través de transportes externos o integrados (Envíopack, Rapiboy, MercadoLibre, etc.). Desde aquí podés:

- Consultar envíos pendientes, a programar, entregados o con cobro pendiente
- Filtrar por PDV, tipo de venta, cliente, factura, período y turno de entrega
- Marcar envíos como entregados
- Asignar transportes integrados o externos
- Imprimir remitos, etiquetas y exportar a Excel

---

<img src="imagenes/pantalla_logistica_externa.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Logística Externa**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a consultar |
| **ESTADO** | TODOS / A ENTREGAR / A PROGRAMAR / ENTREGADO / COBRO PENDIENTE |
| **VENTA** | Filtra por tipo de venta: TODOS, MAYORISTA, MINORISTA, tiendas virtuales (TiendaNube, WooCommerce, etc.) o lógistica de MercadoLibre |
| **CLIENTE** | Filtra por cliente específico |
| **FACTURA** | Tipo y número de comprobante (con botón **Buscar**) |
| **DESDE** | Fecha de inicio del período |
| **HASTA** | Fecha de fin del período |
| **ID ENVIO** | Número de envío (solo lectura, se completa al seleccionar registros) |
| **CON TURNO** | Filtra por si tiene turno de entrega asignado: TODOS / NO / SI |

### Sección TRANSPORTES (cuando hay un envío seleccionado)

**Transportes integrados:** botones de los transportes configurados (Envíopack, Rapiboy, etc.) para enviar al sistema del transporte.

**Detalle en Excel / Remitos y Etiquetas:** generación de documentación del envío.

**Transportes externos:**
| Campo/Acción | Descripción |
|---|---|
| Campo transporte | Selector de transporte externo |
| **Asociar transporte** | Vincula el transporte externo al envío seleccionado |
| **Etiquetas** | Imprime las etiquetas generadas por el sistema |

---

## Panel derecho — Grilla de envíos

Las columnas disponibles varían según el estado seleccionado. Las más comunes son:

| Columna | Descripción |
|---|---|
| Fecha, Factura, Cliente | Datos del comprobante de venta |
| Remito | Remito de entrega asociado |
| Transporte / Guía | Empresa y número de guía |
| Fecha entrega | Fecha en que se realizó o programó la entrega |
| Turno | Turno de entrega asignado |

**Acciones según estado:**
- **A ENTREGAR:** Aprobar (marcar como entregado), Detalle
- **A PROGRAMAR:** Modificar (definir fecha de entrega), Detalle
- **ENTREGADO:** Borrar (quitar del envío), Modificar (elegir envío), Etiqueta, Estado del envío, Detalle, Pagos
- **TODOS:** Detalle

---

## Notas importantes

- La columna de selección (checkbox) aparece únicamente en estado **A ENTREGAR** para agrupar varios envíos.
- Los transportes integrados aparecen solo si están configurados para la empresa.
- Podés combinar un transporte externo con los envíos cuando el transportista no está integrado al sistema.
