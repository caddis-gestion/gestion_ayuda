# 5.43 RECEPCIÓN DE EQUIPOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Recepción Equipos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Recepción de Equipos** permite registrar la recepción de equipos que ingresan al local provenientes de clientes (por reparación, cambio u otro motivo). La pantalla tiene tres pestañas: Recepción, Historia y Movimientos. Desde aquí podés:

- Registrar la recepción de un equipo con datos del cliente y descripción
- Consultar el historial de movimientos del equipo recepcionado
- Registrar movimientos internos del equipo (traslado entre depósitos)

---

<img src="imagenes/pantalla_recepcion_equipos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Recepción Equipos**

---

## Pestaña RECEPCIÓN — Datos del equipo recepcionado

| Campo | Descripción |
|---|---|
| **NRO RECEPCION** | Número asignado automáticamente a la recepción (solo lectura) |
| **FECHA** | Fecha de recepción del equipo |
| **PDV** | Punto de venta que recibe el equipo |
| **VENDEDOR** | Vendedor que atiende la recepción |
| **CLIENTE** | Cliente que entrega el equipo |
| **NRO SERIE** | Número de serie del equipo recibido (asignado automáticamente) |
| **DESCRIPCION** | Descripción del equipo (modelo, problema, etc.) |
| **OBSERVACIONES** | Notas adicionales sobre la recepción |

---

## Pestaña HISTORIA — Movimientos del equipo

Muestra los movimientos registrados para el equipo recepcionado:

| Columna | Descripción |
|---|---|
| Fecha | Fecha del movimiento |
| Mov. | Número de movimiento |
| Origen | Depósito de origen |
| Destino | Depósito de destino |
| Usuario | Usuario que realizó el movimiento |
| Observ. mov. | Observaciones del movimiento |

---

## Pestaña MOVIMIENTOS — Registrar traslado

Permite registrar el traslado del equipo a otro depósito:

| Campo | Descripción |
|---|---|
| **DESTINO** | Depósito de destino del equipo |
| **OBSERVACIONES** | Notas del movimiento |
| Botón **Multiple** | Ingresa múltiples equipos a la vez |

La grilla lateral muestra los equipos cargados para el movimiento:

| Columna | Descripción |
|---|---|
| Eq. Serie | Número de serie del equipo |
| Error | Marca si el equipo tiene error al cargarse |
| Recepc. | Número de recepción |
| Desc. equipo | Descripción del equipo |
| Deposito actual | Depósito donde se encuentra actualmente |
| Mensaje error | Detalle del error si corresponde |

---

## Notas importantes

- Esta pantalla es específica para empresas con integración de operadoras (Movistar).
- Cada recepción queda numerada y permite rastrear el ciclo del equipo en el local.
- Los movimientos de la pestaña **Historia** se ordenan del más reciente al más antiguo.
