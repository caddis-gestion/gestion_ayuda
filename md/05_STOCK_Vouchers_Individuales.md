# 5.XX VOUCHERS INDIVIDUALES
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Vouchers Individuales

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Vouchers Individuales** permite crear y administrar vouchers de descuento con código único para cada cliente o uso específico. A diferencia de las promos generales, cada voucher tiene un código irrepetible. Desde aquí podés:

- Crear vouchers individuales con descuento porcentual o importe fijo
- Definir fecha de vencimiento, uso múltiple y si el importe es editable
- Consultar y eliminar vouchers existentes

---

<img src="imagenes/pantalla_vouchers_individuales.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Vouchers Individuales**

---

## Formulario

| Campo | Descripción |
|---|---|
| **DESCRIPCION** | Nombre o descripción del voucher (máx. 30 caracteres) |
| **ALIAS** | Nombre corto o código de referencia del voucher (máx. 20 caracteres) |
| **VENCE** | Fecha de vencimiento del voucher |
| **DTO %** | Porcentaje de descuento que aplica el voucher |
| **IMPORTE** | Importe fijo de descuento (alternativo al porcentaje) |
| **MULTIUSO** | **SI**: el voucher puede usarse más de una vez. **NO**: se invalida al primer uso. |
| **EDITABLE** | **SI**: permite modificar el importe al momento de aplicar el voucher. **NO**: el importe es fijo. |

---

## Panel derecho — Grilla de vouchers

Muestra todos los vouchers individuales creados en el sistema:

| Columna | Descripción |
|---|---|
| Id | Identificador interno del voucher |
| Voucher | Código único del voucher |
| Vence | Fecha de vencimiento |
| Descuento | Porcentaje de descuento |
| Importe | Importe fijo de descuento |
| Descripcion | Nombre o descripción del voucher |
| Alias | Alias o código de referencia |
| Editable | Indica si el importe es editable al aplicar |
| Multiuso | Indica si el voucher es de uso múltiple |
| Usado | Cantidad de veces que fue utilizado |

**Acciones disponibles:**
- **Modificar:** Edita los datos del voucher
- **Borrar:** Elimina el voucher del sistema

---

## Notas importantes

- Cada voucher individual tiene un código único generado por el sistema que lo distingue de otros vouchers.
- Si configurás **DTO %** e **IMPORTE** simultáneamente, el sistema aplica ambos según la configuración de la venta.
- Los vouchers ya utilizados (columna **Usado** > 0) no deben eliminarse si se necesita mantener el historial de uso.
