# 6.20 ML SUCURSALES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Sucursales

---

## ¿Para qué sirve esta pantalla?

**ML Sucursales** permite gestionar las sucursales del vendedor registradas en MercadoLibre. Las sucursales son los puntos físicos que aparecen en ML como lugares de retiro o entrega para los compradores. Desde aquí podés:

- Consultar las sucursales ya sincronizadas con ML
- Vincular un PDV de Caddis con su sucursal correspondiente en ML
- Actualizar los datos de dirección, horarios, teléfono y ubicación geográfica de cada sucursal
- Activar o desactivar sucursales

---

<img src="imagenes/pantalla_ml_sucursales.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Sucursales**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Selector de PDV y formulario de datos de la sucursal.
- **Panel derecho (grilla):** Listado de sucursales vinculadas a ML.

---

## Panel izquierdo: Datos de la sucursal

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta de Caddis. El dropdown solo muestra los PDV que tienen configurado un código de MercadoLibre (`Deposito_MercadoLibre IS NOT NULL`). |
| **Nombre** | Nombre de la sucursal como aparece en ML |
| **Domicilio** | Dirección física de la sucursal |
| **Horarios** | Horarios de atención |
| **Estado** | Estado de la sucursal en ML (`active`, `inactive`) |
| **Latitud** | Coordenada geográfica — latitud |
| **Longitud** | Coordenada geográfica — longitud |
| **Cod. Área** | Código de área del teléfono |
| **Telefono** | Número de teléfono de la sucursal |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Id Mercadolibre** | ID de la sucursal en ML |
| **PDV_Caddis** | Punto de venta de Caddis vinculado |
| **Pdv_MLibre** | ID interno del PDV en ML |
| **Domicilio** | Dirección de la sucursal |
| **Horarios** | Horarios de atención |
| **Estado** | Estado en ML |
| **Latitud** | Coordenada geográfica |
| **Longitud** | Coordenada geográfica |
| **Codigo de area** | Código de área del teléfono |
| **Telefono** | Número de teléfono |

---

## Acciones desde la grilla

| Acción | Descripción |
|---|---|
| **Modificar** | Carga los datos de la sucursal seleccionada en el formulario izquierdo para editarlos |
| **Borrar** | Elimina la vinculación de la sucursal seleccionada |

---

## Notas

- Esta pantalla es de uso administrativo. Generalmente la configura el administrador del sistema al dar de alta una nueva sucursal o cuando cambia la dirección de un local.
- Las coordenadas de latitud y longitud son necesarias para que ML muestre correctamente la ubicación de la sucursal en el mapa de locales de retiro.
- Para que un PDV aparezca en el dropdown de esta pantalla, debe tener configurado el campo `Deposito_MercadoLibre` en los parámetros del PDV.

---

> 📖 Para configurar los parámetros de un PDV consultá el instructivo **PDV Parámetros** (3.56).
> 📖 Para vincular la cuenta ML con Caddis consultá [**Conexión / Login de Cuenta ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Login.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
