# 6.01 ML LOGIN
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Login

---

## ¿Para qué sirve esta pantalla?

**ML Login** permite vincular las cuentas de MercadoLibre con el sistema Caddis. Desde aquí podés:

- Ver todas las cuentas de vendedor configuradas por el administrador
- Conectar una cuenta de ML con Caddis a través de la autorización oficial de la API
- Ver qué cuentas están activamente integradas y con qué estado tiene el token de acceso
- Desvincular una cuenta si ya no se usa o si es necesario reconectarla

> ℹ️ Esta pantalla generalmente la configura el administrador del sistema. Los vendedores operativos raramente necesitan acceder a ella.

---

<img src="imagenes/pantalla_ml_login.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Login**

---

## Descripción general de la pantalla

La pantalla se organiza en dos secciones:

- **Cuentas configuradas**: listado de todas las cuentas de ML cargadas en el sistema, con el botón para iniciar el proceso de vinculación.
- **Cuentas integradas**: listado de las cuentas que ya completaron el proceso de autorización y tienen un token activo.

---

## Sección: Cuentas configuradas

Muestra el logo de MercadoLibre y una tabla con todas las cuentas de vendedor cargadas en el sistema. Cada fila tiene:

| Elemento | Descripción |
|---|---|
| **Nombre de cuenta** | Identificador de la cuenta ML configurada en Caddis |
| **Botón Integrar cuenta** | Inicia el proceso de autorización OAuth con la API de ML para esa cuenta |

### Cómo integrar una cuenta

1. Hacé click en el botón **Integrar cuenta** junto a la cuenta deseada.
2. El sistema abrirá la página de autorización de MercadoLibre en el navegador.
3. Iniciá sesión con las credenciales del vendedor en ML (si no estás logueado).
4. Autorizá a la aplicación Caddis haciendo click en **Autorizar**.
5. ML redirige de vuelta a Caddis con el token de acceso generado.
6. La cuenta aparecerá ahora en la sección **Cuentas integradas**.

> ⚠️ El token de MercadoLibre tiene una vigencia limitada. Si vence, la sincronización de ventas, publicaciones y envíos deja de funcionar. En ese caso, repetí el proceso de integración para renovarlo.

---

## Sección: Cuentas integradas

Muestra las cuentas que ya tienen un token de acceso válido registrado en el sistema.

| Columna | Descripción |
|---|---|
| **Cuenta** | Nombre de la cuenta de ML integrada |
| **Token vigente** | Indica si el token de acceso está activo y válido |
| **Botón Desvincular** | Elimina el token y desvincula la cuenta del sistema |

### Desvincular una cuenta

1. Ubicá la cuenta en la sección **Cuentas integradas**.
2. Hacé click en **Desvincular**.
3. Confirmá la acción.
4. La cuenta vuelve a aparecer solo en la sección de cuentas configuradas, sin token activo.

> ⚠️ Al desvincular una cuenta, todas las operaciones automáticas de esa cuenta (sincronización de ventas, actualización de precios, etc.) dejarán de funcionar hasta que se vuelva a integrar.

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| No se puede integrar la cuenta | El vendedor rechazó la autorización en ML | Repetir el proceso y confirmar la autorización |
| Token vencido | Los tokens de ML expiran periódicamente | Desvincular y volver a integrar la cuenta |
| Cuenta no aparece en el listado | No está cargada en la configuración del sistema | Contactar al administrador para agregar la cuenta |

---

## Preguntas frecuentes

**¿Con qué frecuencia hay que re-integrar la cuenta?**
Depende de la configuración de la API. Generalmente los tokens duran varios meses, pero pueden vencer antes si no hay actividad. El sistema avisa cuando una operación falla por token vencido.

**¿Puedo tener varias cuentas de ML integradas?**
Sí. El sistema permite integrar múltiples cuentas de vendedor. Cada una aparece como una opción en los filtros de las pantallas de ventas, publicaciones y envíos.

---

