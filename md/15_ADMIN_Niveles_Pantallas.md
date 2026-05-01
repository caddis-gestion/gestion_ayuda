# 15.02 NIVELES DE ACCESO POR PANTALLA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Niveles de Acceso por Pantalla

---
<img src="imagenes/pantalla_niveles_pantallas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Niveles de Acceso por Pantalla** permite definir qué pantallas del sistema puede ver cada nivel de usuario. Desde aquí podés:

- Seleccionar un nivel de acceso y ver qué pantallas tiene habilitadas
- Habilitar o deshabilitar el acceso a pantallas específicas para ese nivel
- Filtrar por ventana/módulo para encontrar rápido la pantalla a configurar

---

## ¿Cómo acceder?

**Menú → Administración → Niveles de Acceso por Pantalla**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **NIVEL** | Selector del nivel de acceso a configurar. Al cambiar el nivel, la grilla se actualiza mostrando las pantallas habilitadas para ese nivel. |
| **VENTANA** | Filtro opcional por módulo o ventana para acotar la grilla. |

---

## Grilla de pantallas

Muestra todas las pantallas del sistema con un checkbox por pantalla:

| Columna | Descripción |
|---|---|
| Checkbox | Tildado = el nivel tiene acceso a esa pantalla. Destildado = sin acceso. |
| Módulo | Módulo al que pertenece la pantalla. |
| Pantalla | Nombre de la pantalla/funcionalidad. |

Para habilitar o deshabilitar el acceso, simplemente marcar o desmarcar el checkbox correspondiente. Los cambios se guardan al hacer clic en **Guardar**.

---

## Flujo típico — Configurar acceso a pantallas

1. Seleccionar el **NIVEL** a configurar
2. Opcionalmente filtrar por **VENTANA** para encontrar la sección deseada
3. Tildar o destildar los checkboxes de las pantallas
4. Guardar los cambios

---

## Notas importantes

- Los niveles de acceso se asignan a usuarios desde [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf) (15.01).
- Los cambios en los niveles afectan inmediatamente a todos los usuarios con ese nivel.
- Para configurar acceso a informes (reportes), usar [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) (15.03).
