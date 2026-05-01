# 15.03 NIVELES DE ACCESO POR INFORME
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Niveles de Acceso por Informe

---
<img src="imagenes/pantalla_niveles_informes.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Niveles de Acceso por Informe** permite definir qué reportes e informes puede ejecutar cada nivel de usuario. Desde aquí podés:

- Seleccionar un nivel de acceso y ver qué informes tiene habilitados
- Habilitar o deshabilitar el acceso a informes específicos para ese nivel

---

## ¿Cómo acceder?

**Menú → Administración → Niveles de Acceso por Informe**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **NIVEL** | Selector del nivel de acceso a configurar. Al cambiar el nivel, la grilla se actualiza mostrando los informes habilitados para ese nivel. |

---

## Grilla de informes

Muestra todos los informes disponibles en el sistema con un checkbox por informe:

| Columna | Descripción |
|---|---|
| Checkbox | Tildado = el nivel puede ejecutar ese informe. Destildado = sin acceso. |
| Módulo | Módulo al que pertenece el informe. |
| Informe | Nombre del informe/reporte. |

Para habilitar o deshabilitar el acceso, simplemente marcar o desmarcar el checkbox correspondiente. Los cambios se guardan al hacer clic en **Guardar**.

---

## Flujo típico — Configurar acceso a informes

1. Seleccionar el **NIVEL** a configurar
2. Tildar o destildar los checkboxes de los informes deseados
3. Guardar los cambios

---

## Notas importantes

- Los niveles de acceso se asignan a usuarios desde [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf) (15.01).
- Los cambios en los niveles afectan inmediatamente a todos los usuarios con ese nivel.
- Para configurar acceso a pantallas funcionales, usar [**Niveles de Acceso por Pantalla**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Pantallas.pdf) (15.02).
