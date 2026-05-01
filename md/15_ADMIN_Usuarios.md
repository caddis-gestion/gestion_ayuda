# 15.01 USUARIOS DEL SISTEMA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Usuarios del Sistema

---
<img src="imagenes/pantalla_usuarios.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## ¿Para qué sirve esta pantalla?

La pantalla de **Usuarios del Sistema** permite gestionar las cuentas de acceso al sistema. Desde aquí podés:

- Dar de alta nuevos usuarios
- Modificar datos de un usuario existente (nombre, mail, nivel de acceso)
- Activar o desactivar cuentas de usuario
- Resetear la contraseña de un usuario
- Asociar usuarios a vendedores, supervisores u otros roles del sistema

---

## ¿Cómo acceder?

**Menú → Administración → Usuarios del Sistema**

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **USUARIO** | Nombre de usuario (login). Identificador único para ingresar al sistema. |
| **NOMBRE** | Nombre completo del usuario. |
| **ACTIVO** | Estado de la cuenta: **SI** = activo, **NO** = inactivo (no puede ingresar). |
| **MAIL** | Correo electrónico del usuario (puede usarse para notificaciones). |
| **WHATSAPP** | Número de WhatsApp del usuario. |
| **NIVEL** | Nivel de acceso asignado. Define a qué pantallas e informes puede acceder. |
| **RESET PASSWORD** | Botón para forzar el reseteo de la contraseña del usuario seleccionado. |

---

## Grilla de usuarios

Muestra todos los usuarios registrados en el sistema con:

| Columna | Descripción |
|---|---|
| Usuario | Nombre de login. |
| Nombre | Nombre completo. |
| Activo | SI / NO. |
| Nivel | Nivel de acceso asignado. |
| Menú | Tipo de menú configurado para el usuario (Horizontal / Vertical). |
| Mail | Correo electrónico. |

---

## Flujo típico — Alta de usuario

1. Acceder a **Administración → Usuarios del Sistema**
2. Completar **USUARIO**, **NOMBRE**, **MAIL** y **NIVEL**
3. Dejar **ACTIVO = SI**
4. Hacer clic en **Agregar**
5. Comunicar las credenciales al usuario (puede cambiar su contraseña desde [**Perfil del Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Perfil_Usuario.pdf) — 15.16)

---

## Notas importantes

- El **NIVEL** de acceso controla qué pantallas e informes puede ver el usuario. Los niveles se configuran en [**Niveles de Acceso por Pantalla**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Pantallas.pdf) (15.02) y [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) (15.03).
- Un usuario **INACTIVO** no puede ingresar al sistema aunque conozca su contraseña.
- El botón **RESET PASSWORD** genera una nueva contraseña temporal para el usuario y se la envía por mail.
