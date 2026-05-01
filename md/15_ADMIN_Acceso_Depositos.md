# 15.04 ACCESO A DEPÓSITOS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Acceso a Depósitos

---
<img src="imagenes/pantalla_acceso_depositos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Acceso a Depósitos** permite definir a qué puntos de venta y depósitos puede acceder cada usuario. Desde aquí podés:

- Seleccionar un usuario y ver qué depósitos/PDV tiene habilitados
- Habilitar o deshabilitar el acceso a depósitos específicos para ese usuario
- Filtrar la lista de depósitos por tipo, zona, gerente, jefe de ventas o supervisor

---

## ¿Cómo acceder?

**Menú → Administración → Acceso a Depósitos**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **USUARIO** | Usuario al que se le configuran los accesos. Al seleccionarlo, la grilla muestra los depósitos/PDV con sus accesos actuales. |
| **TIPO** | Filtro por tipo de depósito (Punto de Venta, Depósito central, etc.). |
| **ZONA** | Filtro por zona geográfica. |
| **GERENTE** | Filtro por gerente responsable del PDV. |
| **JEFE VENTAS** | Filtro por jefe de ventas asignado. |
| **SUPERVISOR** | Filtro por supervisor asignado al PDV. |

---

## Grilla de depósitos

Muestra todos los depósitos/puntos de venta del sistema con:

| Columna | Descripción |
|---|---|
| Checkbox | Tildado = el usuario tiene acceso a ese depósito/PDV. |
| Código | Código interno del depósito. |
| Nombre | Nombre del depósito o punto de venta. |
| Tipo | Tipo de depósito. |
| Zona | Zona asignada. |

Para habilitar o deshabilitar el acceso, marcar o desmarcar el checkbox correspondiente y guardar.

---

## Flujo típico — Asignar accesos a un usuario

1. Seleccionar el **USUARIO**
2. Usar los filtros si hay muchos depósitos para acotar la vista
3. Tildar los depósitos/PDV a los que debe tener acceso
4. Guardar los cambios

---

## Notas importantes

- Un usuario solo puede operar en los depósitos/PDV que tenga habilitados en esta pantalla.
- Si un usuario no tiene acceso a ningún depósito, no podrá realizar operaciones de stock ni ventas.
- El acceso a cajas se configura por separado en [**Acceso a Cajas**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Cajas.pdf) (15.05).
