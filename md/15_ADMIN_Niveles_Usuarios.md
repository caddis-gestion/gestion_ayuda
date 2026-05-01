# 15.22 NIVELES DE USUARIOS
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Accesos → Niveles Usuarios

---
<img src="imagenes/pantalla_niveles_usuarios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Niveles de Usuarios** es el ABM (alta, baja y modificación) de los niveles de acceso disponibles en el sistema. Los niveles son los perfiles de seguridad que se asignan a los usuarios. Desde aquí podés:

- Crear nuevos niveles de acceso con un nombre descriptivo
- Modificar el nombre de un nivel existente
- Eliminar niveles que ya no se utilicen

---

## ¿Cómo acceder?

**Menú → Administración → Accesos → Niveles Usuarios**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **NIVEL** | Nombre descriptivo del nivel de acceso (ej: "Vendedor", "Supervisor", "Gerencia", "Admin"). |

El código del nivel se asigna automáticamente y es de solo lectura.

---

## Grilla de niveles

Muestra todos los niveles de acceso existentes con:

| Columna | Descripción |
|---|---|
| Código | Identificador numérico del nivel. |
| Nivel | Nombre del nivel. |

Desde la grilla se puede **modificar** el nombre de un nivel o **borrar** niveles que no tengan usuarios asignados.

---

## Flujo típico — Crear un nuevo nivel

1. Acceder a **Administración → Accesos → Niveles Usuarios**
2. Ingresar el **NOMBRE** del nuevo nivel
3. Hacer clic en **Agregar**
4. Luego configurar las pantallas permitidas en [**Niveles de Acceso por Pantalla**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Pantallas.pdf) (15.02)
5. Y los informes permitidos en [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) (15.03)

---

## Notas importantes

- Los niveles aquí creados son los que aparecen en el selector de **NIVEL** al dar de alta o modificar un usuario en [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf) (15.01).
- Crear el nivel es solo el primer paso; sin configurar las pantallas e informes permitidos, el usuario con ese nivel no podrá acceder a ninguna funcionalidad.
