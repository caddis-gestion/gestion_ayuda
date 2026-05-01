# 5.35 EQUIPOS — ARREGLOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Arreglos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Arreglos** permite consultar el estado del stock de equipos que se encuentran en proceso de arreglo o reparación. Desde aquí podés:

- Filtrar equipos por proveedor, almacén, estado, tipo de equipo y otros datos
- Buscar equipos por número de pedido, remito o número de despacho
- Ingresar rangos múltiples de NSE para consultas masivas

---

<img src="imagenes/pantalla_equipos_arreglos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Arreglos**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PROVEEDOR** | Proveedor al que se envió el equipo para arreglo |
| **ALMACEN** | Almacén donde se encuentra el equipo |
| **F.INGRESO** | Fecha de ingreso del equipo |
| **F.VENCE** | Fecha de vencimiento del arreglo o garantía |
| **PEDIDO** | Número de pedido asociado |
| **REMITO** | Número de remito del arreglo |
| **DESPACHO** | Número de despacho |
| **DOC ASOC** | Documento asociado (según operadora) |
| **EQUIPO** | Modelo/código del equipo |
| **EQ.TIPO** | Tipo de equipo |
| **ESTADO** | Estado del equipo (solo estados con código menor a 90) |

**Acciones:**
- **Multiple:** Ingresa múltiples NSE para filtrar
- **Rango:** Busca por rango de NSE

---

## Panel derecho — Grilla de resultados

| Columna | Descripción |
|---|---|
| NSE | Número de serie del equipo |
| Tipo Compra | Tipo de contrato/compra del equipo |
| [campos del equipo] | Marca, modelo y datos adicionales según configuración |
| Ingreso | Fecha de ingreso al almacén |
| Vence | Fecha de vencimiento |
| Almacen | Nombre del almacén |
| Pedido | Número de pedido |
| Remito | Número de remito |
| Despacho | Número de despacho |
| Facturado | Indica si el equipo fue facturado |

---

## Notas importantes

- Esta pantalla trabaja con equipos identificados por NSE (número de serie en hexadecimal).
- Solo se muestran estados con código menor a 90 (estados operativos, excluye estados de tránsito/especiales).
- El campo DOC ASOC es específico para integraciones con operadoras (Movistar, etc.).
