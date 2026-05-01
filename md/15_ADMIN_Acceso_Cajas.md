# 15.05 ACCESO A CAJAS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Acceso a Cajas

---
<img src="imagenes/pantalla_acceso_cajas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Acceso a Cajas** (también llamada **Cajeros**) permite vincular cada usuario con su caja dentro de un punto de venta. Cada usuario es responsable de los saldos que figuren en su caja asignada. Desde aquí podés:

- Asignar o cambiar la caja de un usuario dentro de un punto de venta
- Consultar qué usuarios tienen cajas asignadas en cada PDV

---

## ¿Cómo acceder?

**Menú → Administración → Acceso a Cajas**

---

## Requisito previo — Configurar cantidad de cajas por PDV

Antes de asignar cajeros, es necesario definir cuántas cajas tendrá cada Punto de Venta. Esto se hace desde [**PDV Parámetros**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_PDV_Parametros.pdf), en el campo **CAJAS**.

> Si las cajas no están configuradas en PDV Parámetros, no habrá opciones disponibles para asignar en esta pantalla.

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta donde se realiza la asignación. |
| **USUARIO** | Usuario al que se le asigna la caja. |
| **CAJA** | Caja del PDV que se asigna al usuario seleccionado. |

---

## Grilla de asignaciones

Muestra las asignaciones usuario-caja existentes para el PDV seleccionado:

| Columna | Descripción |
|---|---|
| Usuario | Nombre del usuario. |
| PDV | Punto de venta. |
| Caja | Caja asignada. |

---

## Flujo típico — Asignar una caja a un usuario

1. Configurar la cantidad de cajas del PDV desde [**PDV Parámetros**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_PDV_Parametros.pdf) (si aún no se hizo)
2. Seleccionar el **PDV**
3. Seleccionar el **USUARIO**
4. Seleccionar la **CAJA** que se le asignará
5. Guardar los cambios

---

## Notas importantes

- Cada usuario puede tener **una única caja** en **un único punto de venta**.
- Una vez asignado, el usuario **solo puede ver y operar su propia caja**; no tiene acceso a las cajas de otros usuarios.
- Para transferir dinero entre cajas, ambos cajeros deben coordinarse: uno registra un egreso y el otro un ingreso desde [**Caja Movimientos**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Caja_Movimientos.pdf) (3.28). Si solo uno lo registra, el sistema lo interpreta como una extracción.
- Para habilitar el acceso del usuario al PDV completo, usar [**Acceso a Depósitos**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Depositos.pdf) (15.04).
