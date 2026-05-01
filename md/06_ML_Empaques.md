# 6.15 ML EMPAQUES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Empaques

---

## ¿Para qué sirve esta pantalla?

**ML Empaques** permite gestionar los paquetes (empaques) de envío de MercadoLibre, especialmente para ventas que se agrupan en un mismo despacho por zona geográfica. Desde aquí podés:

- Consultar ventas filtradas por usuario ML, zona (código postal) y rango de fechas
- Ver el estado logístico de cada envío con sus datos de tracking y cliente
- Gestionar la agrupación de paquetes por código postal

---

<img src="imagenes/pantalla_ml_empaques.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Empaques**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros de búsqueda.
- **Panel derecho (grilla):** Listado de envíos con datos de tracking, cliente y estado. Las primeras 2 columnas son fijas.

---

## Panel izquierdo: Filtros

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio para ver resultados. |
| **ZONA** | Código postal de destino. Filtra ventas con envío a esa zona. Se selecciona de un dropdown. |
| **DESDE** | Fecha de inicio del rango de ventas. |
| **HASTA** | Fecha de fin del rango. |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta en ML |
| **Fecha** | Fecha de la venta |
| **Estado** | Estado de la orden |
| **Shipping Tipo** | Tipo de logística del envío |
| **Shipping Estado** | Estado del envío en ML |
| **Shipping Subestado** | Subestado del envío con mayor detalle |
| **Shipping Tracking** | ID de seguimiento del envío |
| **Pack** | ID de paquete agrupado (si aplica) |
| **Cliente** | Nombre del comprador |
| **Domicilio** | Dirección de entrega |
| **Cpostal** | Código postal de entrega |
| **Localidad** | Localidad de entrega |
| **Telefono** | Teléfono del comprador |
| **Fc_Tipo** | Tipo de comprobante fiscal emitido |
| **Fc_Nro** | Número del comprobante fiscal |
| **Checkbox** | Selección para agrupar o procesar múltiples envíos |

---

## Uso típico

La pantalla de empaques se usa para:

1. **Agrupar envíos por zona**: filtrá por **ZONA** (código postal) para ver todos los paquetes con destino a la misma área y organizarlos para el despacho conjunto.
2. **Controlar el estado del despacho**: verificá qué ventas de un período tienen el envío en qué estado antes de la colecta.
3. **Preparar la documentación**: revisá los datos de cliente y domicilio antes de imprimir las etiquetas.

---

> 📖 Para imprimir etiquetas de envío consultá [**Etiquetas de Envío ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Etiquetas.pdf).
> 📖 Para armar los paquetes físicos consultá [**Armar Envíos ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Armar_Envios.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
