# 7.03 TV TIENDANUBE LOGIN
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Tiendanube Login

---

## ¿Para qué sirve esta pantalla?

**TV Tiendanube Login** permite conectar y gestionar la integración de cuentas de **TiendaNube** con Caddis. Desde aquí podés:

- Ver las cuentas TiendaNube habilitadas para integración
- Integrar (conectar) una cuenta iniciando sesión en TiendaNube
- Ver las cuentas ya integradas y desvincularlas si es necesario

---

<img src="imagenes/pantalla_tv_tiendanube_login.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Tiendanube Login**

---

## Sección: Cuentas habilitadas para integración

Muestra la lista de cuentas de TiendaNube cargadas en Caddis.

| Elemento | Descripción |
|---|---|
| **Campo de texto** (solo lectura) | URL o nombre de usuario de la tienda TiendaNube. |
| **Botón Integrar** | Inicia el proceso de autorización abriendo una ventana popup de TiendaNube. |

Si no hay cuentas configuradas, aparece el mensaje: *"No existen accesos habilitados en Caddis para Tiendanube"*.

---

## Sección: Cuentas integradas

Muestra las cuentas con token vigente (activo).

| Elemento | Descripción |
|---|---|
| **Campo de texto** (solo lectura) | Nombre de la cuenta TiendaNube integrada. |
| **Botón Desvincular** | Revoca la integración. |
| **Campo ID** (solo lectura) | ID interno de la tienda en TiendaNube. |

Si ninguna cuenta está integrada, aparece: *"No hay cuentas integradas actualmente"*.

---

## Cómo integrar una cuenta

1. En la sección **Cuentas habilitadas para integración**, localizá la cuenta.
2. Hacé clic en **Integrar**.
3. Se abre una ventana popup con el login de TiendaNube.
4. Ingresá las credenciales de administrador de la tienda.
5. Al autorizar, el popup se cierra y la cuenta pasa a la sección **Cuentas integradas**.

> ⚠️ La integración con TiendaNube requiere que el sistema esté configurado en un entorno de producción con la URL de callback correcta. Si el popup no completa el proceso, consultá con el administrador del sistema.

---

## Cómo desvincular una cuenta

1. En la sección **Cuentas integradas**, hacé clic en **Desvincular**.
2. Confirmá el diálogo: *"¿Desea desvincular esta cuenta?"*
3. La cuenta deja de sincronizarse con Caddis.

---

> 📖 Para publicar artículos en TiendaNube consultá [**Publicar Artículo (Individual)**](https://ayuda.caddis.com.ar/instructivos/07_TV_Publicar_Articulo.pdf).
> 📖 Para gestionar ventas de TiendaNube consultá [**Ventas de Tienda Virtual**](https://ayuda.caddis.com.ar/instructivos/07_TV_Ventas.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
