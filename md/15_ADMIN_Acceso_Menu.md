# 15.20 ACCESO AL MENÚ POR USUARIO
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Accesos al Menú

---
<img src="imagenes/pantalla_acceso_menu.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Accesos al Menú** permite configurar el acceso a pantallas del sistema de forma **individual por usuario**, independientemente del nivel de acceso asignado. Desde aquí podés:

- Seleccionar un usuario y ver qué pantallas tiene habilitadas en su acceso personal
- Habilitar o deshabilitar el acceso a pantallas específicas para ese usuario
- Filtrar por módulo (ventana) y sub-sección para encontrar rápidamente la pantalla a configurar

---

## ¿Cómo acceder?

**Menú → Administración → Accesos al Menú**

---

## Diferencia con Niveles de Acceso por Pantalla

| Pantalla | Descripción |
|---|---|
| [**Niveles de Acceso por Pantalla**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Pantallas.pdf) (15.02) | Configura qué pantallas puede ver un **nivel de acceso** completo. Afecta a todos los usuarios de ese nivel. |
| **Accesos al Menú** (15.20) | Configura qué pantallas puede ver un **usuario específico**, con independencia de su nivel. Permite dar permisos individuales. |

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **USUARIO** | Usuario al que se le configura el acceso individual. Al seleccionarlo, la grilla se actualiza con sus pantallas habilitadas. |
| **NIVEL** | Nivel de acceso del usuario seleccionado (referencial, solo lectura). |
| **VENTANA** | Filtro por módulo del sistema. Al seleccionar un módulo, la grilla muestra solo las pantallas de ese módulo. |
| **SUB-VENTANA** | Filtro por sub-sección dentro del módulo seleccionado. |

---

## Grilla de pantallas

Muestra las pantallas disponibles para el módulo/sub-ventana seleccionado con:

| Columna | Descripción |
|---|---|
| Checkbox | Tildado = el usuario tiene acceso a esa pantalla. Destildado = sin acceso. |
| Pantalla | Nombre de la pantalla/funcionalidad. |

Para habilitar o deshabilitar el acceso, marcar o desmarcar el checkbox y guardar.

---

## Flujo típico — Dar acceso a una pantalla puntual a un usuario

1. Seleccionar el **USUARIO**
2. Seleccionar el **MÓDULO** (VENTANA) donde está la pantalla
3. Si aplica, seleccionar la **SUB-VENTANA**
4. Tildar el checkbox de la pantalla a habilitar
5. Guardar los cambios

---

## Notas importantes

- Esta pantalla permite **excepciones individuales**: si un usuario necesita acceso a una pantalla que su nivel no tiene habilitada, puede configurarse aquí sin cambiar el nivel de todos los demás usuarios.
- Los cambios son inmediatos para el usuario afectado.
- Para configurar acceso a informes por usuario, consultar al administrador (los informes se gestionan por nivel en [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) — 15.03).
