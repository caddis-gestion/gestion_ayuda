# 3.47 DEFINIR ABONOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Definir Abonos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Definir Abonos** permite configurar los abonos recurrentes asociados a clientes. Un abono es un cargo periódico (mensual) que se factura automáticamente al cliente. Desde aquí podés:

- Crear un nuevo abono recurrente para un cliente
- Definir el período de vigencia, el PDV de facturación y la condición de pago
- Consultar los abonos activos e inactivos
- Modificar o eliminar abonos existentes

---

<img src="imagenes/pantalla_definir_abonos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Definir Abonos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de configuración del abono y un panel derecho con la grilla de abonos existentes.

---

## Panel izquierdo — Formulario

### Sección Abono

| Campo | Descripción |
|---|---|
| **ESTADO** | ACTIVO o INACTIVO. Los abonos inactivos no se facturan. |

### Sección Periodo

| Campo | Descripción |
|---|---|
| **FECHA INICIO** | Fecha de inicio del abono (día, mes y año en selectores separados) |
| **FECHA CADUCIDAD** | Fecha hasta la que el abono estará vigente. Por defecto: un año desde hoy. |

> La frecuencia es mensual (fija).

### Sección Facturación

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta desde el que se emitirá la factura del abono. Sólo muestra PDV con facturación electrónica habilitada. |
| **TIPO DE FC** | Tipo de comprobante a emitir (A, B, C, etc.), según los disponibles para el PDV y empresa seleccionada |
| **CLIENTE** | Cliente al que se le factura el abono |
| **CTA CTE** | Condición de pago (lista de condiciones configuradas en Cta Cte Condiciones) |

---

## Panel derecho — Grilla de abonos

Muestra todos los abonos configurados en el sistema:

| Columna | Descripción |
|---|---|
| Estado | ACTIVO o INACTIVO |
| Modo | MANUAL o AUTOMATICO |
| Cliente | Nombre del cliente |
| PDV | Punto de venta de facturación |
| Empresa | Empresa facturante |
| Factura Tipo | Tipo de comprobante |
| Condicion | Condición de pago asignada |
| Administracion | Vendedor o administrador asignado al cliente |
| Frecuencia | MENSUAL (actualmente la única frecuencia disponible) |
| Inicio | Fecha de inicio del abono |
| Caducidad | Fecha de vencimiento del abono |

**Acciones disponibles:**
- **Modificar:** Edita la configuración del abono
- **Detalle:** Ver el detalle del abono y su historial de facturación
- **Borrar:** Elimina el abono

---

## Notas importantes

- Los abonos se facturan desde la pantalla **Facturación Abonos** (3.48), que genera las facturas en forma masiva para todos los abonos activos del período.
- Un abono **INACTIVO** no genera factura aunque esté dentro del período de vigencia.
- La **FECHA CADUCIDAD** determina hasta cuándo se factura el abono. Una vez superada, el abono deja de procesarse automáticamente.
