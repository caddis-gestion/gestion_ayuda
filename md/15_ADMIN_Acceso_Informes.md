# 15.21 ACCESO A INFORMES POR USUARIO
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Accesos → Accesos a Informes

---
<img src="imagenes/pantalla_acceso_informes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Accesos a Informes** permite configurar el acceso a reportes e informes del sistema de forma **individual por usuario**, independientemente del nivel de acceso asignado. Desde aquí podés:

- Seleccionar un usuario y ver qué informes tiene habilitados en su acceso personal
- Habilitar o deshabilitar el acceso a informes específicos para ese usuario

---

## ¿Cómo acceder?

**Menú → Administración → Accesos → Accesos a Informes**

---

## Diferencia con Niveles de Acceso por Informe

| Pantalla | Descripción |
|---|---|
| [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) (15.03) | Configura qué informes puede ver un **nivel de acceso** completo. Afecta a todos los usuarios de ese nivel. |
| **Accesos a Informes** (15.21) | Configura qué informes puede ejecutar un **usuario específico**, con independencia de su nivel. Permite dar permisos individuales. |

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **USUARIO** | Usuario al que se le configura el acceso individual a informes. Al seleccionarlo, la grilla muestra los informes habilitados para ese usuario. |
| **NIVEL** | Nivel de acceso del usuario seleccionado (referencial). |

---

## Grilla de informes

Muestra todos los informes disponibles del sistema con:

| Columna | Descripción |
|---|---|
| Checkbox | Tildado = el usuario tiene acceso a ese informe. Destildado = sin acceso. |
| Informe | Nombre del informe o reporte. |

Para habilitar o deshabilitar el acceso, marcar o desmarcar el checkbox y guardar.

---

## Notas importantes

- Esta pantalla permite dar a un usuario acceso a un informe que su nivel no tiene habilitado, sin modificar el nivel de todos los demás.
- Para configurar acceso a pantallas funcionales por usuario, ver [**Acceso al Menú por Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Menu.pdf) (15.20).
- Para configurar acceso a informes por nivel (configuración masiva), ver [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) (15.03).
