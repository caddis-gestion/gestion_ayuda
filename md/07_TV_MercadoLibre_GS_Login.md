# 7.02 TV MERCADO LIBRE GS LOGIN
### Módulo 7 — Tiendas Virtuales

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Tiendas Virtuales → TV Mercado Libre GS Login

---

## ¿Para qué sirve esta pantalla?

**TV Mercado Libre GS Login** permite conectar y gestionar la integración de cuentas de **MercadoLibre Global Selling** con Caddis. Desde aquí podés:

- Ver las cuentas ML Global Selling habilitadas para integración
- Integrar (conectar) una cuenta iniciando sesión en MercadoLibre
- Ver las cuentas ya integradas y desvincularlas si es necesario

> 💡 MercadoLibre Global Selling permite vender en múltiples países desde una sola cuenta. Esta pantalla gestiona específicamente esas cuentas internacionales, separadas de las cuentas locales (Módulo 6 — ML Login).

---

<img src="imagenes/pantalla_ml_login.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Tiendas Virtuales → TV Mercado Libre GS Login**

---

## Sección: Cuentas habilitadas para integración

Muestra la lista de cuentas de ML Global Selling cargadas en Caddis que aún no están conectadas (o cuyo token venció).

| Elemento | Descripción |
|---|---|
| **Campo de texto** (solo lectura) | Nombre de usuario de la cuenta ML. |
| **Botón Integrar** | Inicia el proceso de autorización abriendo una ventana de login de MercadoLibre. Al completar el login, el token queda guardado. |

---

## Sección: Cuentas integradas

Muestra las cuentas que ya tienen un token vigente (activo).

| Elemento | Descripción |
|---|---|
| **Campo de texto** (solo lectura) | Nombre de usuario de la cuenta ML integrada. |
| **Botón Desvincular** | Revoca la integración de la cuenta. La cuenta queda desconectada de Caddis. |
| **Campo ID** (solo lectura) | ID interno de la cuenta en MercadoLibre. |
| **Botón Refrescar pantalla** | Recarga la pantalla para ver el estado actualizado de las integraciones. |

---

## Cómo integrar una cuenta

1. En la sección **Cuentas habilitadas para integración**, localizá la cuenta.
2. Hacé clic en **Integrar**.
3. Se abre una ventana popup con el login de MercadoLibre.
4. Ingresá las credenciales de la cuenta ML.
5. Al autorizar, el popup se cierra y la cuenta pasa a la sección **Cuentas integradas**.
6. Hacé clic en **Refrescar pantalla** si la cuenta no aparece inmediatamente.

---

## Cómo desvincular una cuenta

1. En la sección **Cuentas integradas**, localizá la cuenta a desvincular.
2. Hacé clic en **Desvincular**.
3. El sistema pide confirmación: *"¿Desea desvincular esta cuenta?"*
4. Confirmá.
5. La cuenta deja de estar integrada y vuelve a aparecer en la sección de habilitadas.

> ⚠️ Desvincular una cuenta detiene la sincronización de stock, precios y ventas para esa cuenta hasta que se vuelva a integrar.

---

> 📖 Para gestionar cuentas de ML Argentina consultá [**Conexión / Login de Cuenta ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Login.pdf).
> 📖 Para publicaciones en ML Global Selling consultá la pantalla **TV Publicaciones** (7.06).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
