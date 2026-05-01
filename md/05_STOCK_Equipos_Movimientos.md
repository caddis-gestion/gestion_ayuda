# 5.41 EQUIPOS — MOVIMIENTOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Movimientos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Movimientos** permite registrar traslados de equipos (con NSE/IMEI) entre puntos de venta. A diferencia de los artículos sin serie, cada equipo se identifica individualmente. Desde aquí podés:

- Registrar un remito de movimiento de equipos entre PDVs
- Ingresar equipos de forma individual, múltiple o por rango de NSE
- Asociar una asignación previa al movimiento
- Consultar la historia del NSE en tiempo real

---

<img src="imagenes/pantalla_equipos_movimientos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Movimientos**

---

## Formulario

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha del movimiento |
| **TIPO** | TRASLADO DE MERCADERÍA o MOVIMIENTO INTERNO (según configuración) |
| **REMITO** | Número de remito externo y número interno (solo lectura, asignado automáticamente) |
| **ASIGNACION** | Asignación previa asociada al movimiento (botón **Buscar** para localizarla) |
| **ORIGEN** | PDV de origen de los equipos |
| **DESTINO** | PDV de destino |
| **VENDEDOR** | Vendedor asignado al movimiento |
| **OBSERVACIONES** | Notas adicionales |
| **SALDO DISPONIBLE** | Saldo de la asignación disponible (solo lectura) |

**Acciones:**
- **Multiple:** Ingresa múltiples NSE de una vez
- **Rango:** Ingresa un rango continuo de NSE
- **Preentrega:** Genera un remito de preentrega
- **Historia:** Consulta la historia de un NSE
- **Rto Agencia:** Genera el remito oficial de agencia

---

## Panel derecho — Grilla de equipos en el movimiento

| Columna | Descripción |
|---|---|
| Equipo | Marca y modelo del equipo |
| Cantidad | Unidades incluidas en el movimiento |
| Importe | Importe total del movimiento para ese equipo |
| Errores | Cantidad de equipos con error |

**Acciones:**
- **Detalle:** Muestra el detalle de NSE del equipo en el movimiento

---

## Notas importantes

- El campo **ORIGEN** puede estar bloqueado según la configuración de movimientos entre sucursales.
- El **SALDO DISPONIBLE** refleja el crédito disponible del PDV para recibir equipos cuando hay asignaciones.
- Los equipos con error (NSE no reconocido o ya movido) se contabilizan separadamente en la columna **Errores**.
