# Procedimiento: Usuarios y Accesos al Sistema

> **Versión:** 1.0 — Abril 2026
> **Audiencia:** Administradores del sistema responsables de gestionar cuentas de usuario y permisos de acceso

---

## ¿De qué trata este procedimiento?

Este documento describe el circuito completo para dar acceso a un nuevo usuario al sistema Caddis: desde la creación del perfil de seguridad hasta el primer ingreso. También cubre cómo ajustar accesos individuales a pantallas, informes y puntos de venta.

El sistema maneja dos niveles de control de acceso:

| Nivel | Descripción |
|---|---|
| **Por Nivel** | Un "nivel" es un perfil de seguridad (ej: "Vendedor", "Supervisor"). Se configuran una sola vez y se reutilizan para todos los usuarios del mismo rol. |
| **Individual** | Excepciones específicas para un usuario particular, sin afectar al resto del nivel. |

---

## Circuito completo

```
[1. NIVEL DE ACCESO]    Crear nivel → Asignar pantallas → Asignar informes
         │
         ▼
[2. USUARIO]            Dar de alta el usuario → Asignar nivel → Comunicar credenciales
         │
         ▼
[3. ACCESO A PDV]       Habilitar puntos de venta para el usuario
         │
         ▼
[4. ACCESOS INDIVIDUALES]   (opcional) Excepciones de pantallas o informes por usuario
         │
         ▼
[5. PRIMER INGRESO]     Usuario ingresa al sistema → Cambia su contraseña
```

---

## Paso 1: Crear el nivel de acceso (una sola vez por rol)

Un nivel de acceso define qué pantallas e informes puede ver un grupo de usuarios. Si el nivel ya existe (ej: "Vendedor"), saltear este paso.

### 1.1 Crear el nivel

**Pantalla:** [**Niveles de Usuarios**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Usuarios.pdf)
**Menú:** Administración → Accesos → Niveles Usuarios

| Paso | Acción |
|---|---|
| 1 | Ingresar el nombre del nivel (ej: "Vendedor", "Supervisor", "Gerencia") |
| 2 | Hacer clic en **Agregar** |

> El código del nivel se asigna automáticamente.

---

### 1.2 Asignar pantallas al nivel

**Pantalla:** [**Niveles de Acceso por Pantalla**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Pantallas.pdf)
**Menú:** Administración → Niveles de Acceso por Pantalla

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **NIVEL** a configurar |
| 2 | Filtrar por **VENTANA** (módulo) para acotar la vista |
| 3 | Tildar las pantallas a las que el nivel debe tener acceso |
| 4 | Guardar los cambios |

> Los cambios afectan a **todos los usuarios** que tengan ese nivel asignado.

---

### 1.3 Asignar informes al nivel

**Pantalla:** [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf)
**Menú:** Administración → Niveles de Acceso por Informe

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **NIVEL** a configurar |
| 2 | Tildar los informes y reportes a los que el nivel debe tener acceso |
| 3 | Guardar los cambios |

---

## Paso 2: Dar de alta el usuario

**Pantalla:** [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf)
**Menú:** Administración → Usuarios del Sistema

| Paso | Acción |
|---|---|
| 1 | Completar **USUARIO** (nombre de login, ej: `jgarcia`) |
| 2 | Completar **NOMBRE** (nombre completo del empleado) |
| 3 | Completar **MAIL** (dirección de correo para notificaciones y recuperación de contraseña) |
| 4 | Seleccionar el **NIVEL** de acceso correspondiente al rol del usuario |
| 5 | Dejar **ACTIVO = SI** |
| 6 | Hacer clic en **Agregar** |
| 7 | Comunicar al usuario su **nombre de usuario** y **grupo**, para que pueda generar su contraseña desde la pantalla de login |

> Sin correo electrónico, el usuario no podrá generar su contraseña ni recuperarla en caso de olvido.

---

## Paso 3: Habilitar acceso a puntos de venta

**Pantalla:** [**Acceso a Depósitos**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Depositos.pdf)
**Menú:** Administración → Acceso a Depósitos

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** |
| 2 | Usar los filtros (**TIPO**, **ZONA**, **GERENTE**, etc.) si hay muchos depósitos |
| 3 | Tildar los puntos de venta y depósitos desde donde el usuario operará |
| 4 | Guardar los cambios |

> Un usuario sin depósitos habilitados no puede realizar ventas ni movimientos de stock.

---

## Paso 4: Configurar excepciones individuales (opcional)

Si el usuario necesita acceso a una pantalla o informe que su nivel no tiene habilitado — o debe ser bloqueado en algo que el nivel sí tiene — se configura individualmente sin afectar al resto del nivel.

### 4.1 Excepciones de pantallas

**Pantalla:** [**Acceso al Menú por Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Menu.pdf)
**Menú:** Administración → Accesos al Menú

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** |
| 2 | Seleccionar el **MÓDULO** (VENTANA) que contiene la pantalla a modificar |
| 3 | Si aplica, seleccionar la **SUB-VENTANA** |
| 4 | Tildar o destildar el checkbox de la pantalla |
| 5 | Guardar los cambios |

---

### 4.2 Excepciones de informes

**Pantalla:** [**Acceso a Informes por Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Informes.pdf)
**Menú:** Administración → Accesos → Accesos a Informes

| Paso | Acción |
|---|---|
| 1 | Seleccionar el **USUARIO** |
| 2 | Tildar o destildar el checkbox del informe |
| 3 | Guardar los cambios |

---

## Paso 5: Primer ingreso al sistema

**Pantalla:** [**Login**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Login.pdf)

El usuario no recibe una contraseña inicial. Debe generarla él mismo desde la pantalla de login:

| Paso | Acción |
|---|---|
| 1 | Ingresar el **Usuario** y el **Grupo** en la pantalla de login |
| 2 | Hacer clic en **¿Generar una nueva contraseña?** |
| 3 | El sistema envía la contraseña al correo registrado en su cuenta |
| 4 | Con esa contraseña, ingresar completando los tres campos: **Usuario**, **Contraseña** y **Grupo** |

> Para que el envío funcione, el usuario debe tener un correo electrónico cargado en [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf). Si no lo tiene, el Administrador debe cargarlo antes de este paso.

Una vez adentro, el usuario puede cambiar su contraseña desde [**Perfil del Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Perfil_Usuario.pdf).

---

## Resumen de pantallas involucradas

| Pantalla | Cuándo usarla |
|---|---|
| [**Niveles de Usuarios**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Usuarios.pdf) | Crear un nuevo rol/perfil de seguridad |
| [**Niveles de Acceso por Pantalla**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Pantallas.pdf) | Definir qué pantallas tiene un nivel |
| [**Niveles de Acceso por Informe**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Niveles_Informes.pdf) | Definir qué informes tiene un nivel |
| [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf) | Dar de alta / modificar / desactivar usuarios |
| [**Acceso a Depósitos**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Depositos.pdf) | Habilitar PDV/depósitos por usuario |
| [**Acceso al Menú por Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Menu.pdf) | Excepciones de pantallas por usuario |
| [**Acceso a Informes por Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Acceso_Informes.pdf) | Excepciones de informes por usuario |
| [**Perfil del Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Perfil_Usuario.pdf) | Cambio de contraseña y apariencia del sistema |

---

## Operaciones frecuentes

### Dar de baja a un usuario

1. Ir a [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf)
2. Seleccionar el usuario
3. Cambiar **ACTIVO = NO**
4. Guardar

> El usuario queda inactivo pero sus datos se conservan. No puede ingresar al sistema.

---

### Resetear la contraseña de un usuario

1. Ir a [**Usuarios del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Usuarios.pdf)
2. Seleccionar el usuario
3. Hacer clic en **RESET PASSWORD**
4. El sistema envía la nueva contraseña al correo del usuario

> Si el usuario no tiene mail cargado, el reset no puede enviarse. Cargarlo antes.

---

### El usuario olvidó su contraseña

1. El propio usuario hace clic en **¿Generar una nueva contraseña?** en la pantalla de Login
2. El sistema envía una nueva contraseña al correo registrado
3. El usuario ingresa y cambia la contraseña desde [**Perfil del Usuario**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Perfil_Usuario.pdf)
