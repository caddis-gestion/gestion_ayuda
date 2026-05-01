# Procedimiento: Integracion Caddis — Telegram

> **Version:** 1.0 — Abril 2026
> **Audiencia:** Administradores y responsables que configuran notificaciones del sistema

---

## De que trata este procedimiento?

Caddis puede enviar notificaciones automaticas a traves de **Telegram** directamente al celular de los usuarios configurados. Para recibir estas notificaciones, cada persona debe vincular su cuenta de Telegram a la empresa en Caddis a traves del bot oficial **CaddisERPBot**.

Una vez configurada la integracion, el usuario recibe mensajes automaticos del sistema segun las notificaciones que le hayan sido asignadas (por ejemplo: alertas de stock en 0, remitos no emitidos en ML, etc.).

---

## Circuito completo

```
[1. EN TELEGRAM]    Buscar CaddisERPBot → INICIAR → ingresar CUIT → confirmar
         |
         v
[2. EN CADDIS]      Mensajeria Contactos → asociar usuario de Caddis al contacto
         |
         v
[3. EN CADDIS]      Accesos a Notificaciones → activar las notificaciones del usuario
         |
         v
[RESULTADO]         El contacto de Telegram recibe las notificaciones configuradas
```

---

## Paso 1: Conectar el bot desde Telegram

El usuario debe realizar estos pasos en su celular, desde la app de Telegram.

**1.1 — Buscar el bot**

<img src="imagenes/telegram_proc_paso1.png" style="width:auto; height:auto; max-width:100%; max-height:494px; display:block; margin:0 auto;">

Abrir Telegram y tocar la **lupa de busqueda** (esquina superior derecha). Escribir exactamente: **CaddisERPBot** (respetando mayusculas y minusculas). En los resultados aparecera el contacto **CADDIS (bot)**. Tocarlo para abrir la conversacion.

**1.2 — Iniciar la comunicacion con el bot**

<img src="imagenes/telegram_proc_paso2.png" style="width:auto; height:auto; max-width:100%; max-height:624px; display:block; margin:0 auto;">

Al abrir el chat por primera vez, presionar el boton **INICIAR** o **START** que aparece en la parte inferior de la pantalla.

**1.3 — Registrar el CUIT de la empresa**

<img src="imagenes/telegram_proc_paso3.png" style="width:auto; height:auto; max-width:100%; max-height:780px; display:block; margin:0 auto;">

El bot iniciara automaticamente el flujo de registro:

1. El bot pide: *"Para registrar su contacto, enviar por favor el CUIT de la empresa, sin guiones ni espacios."*
2. El usuario escribe el CUIT de su empresa (ejemplo: `30123456780`) y lo envia
3. El bot responde: *"¿Confirmar registro de contacto [nombre] para empresa [X]? (Si/No)"*
4. El usuario responde **Si**
5. El bot confirma: *"Hola [nombre], tu contacto fue registrado en Caddis para la empresa [X]."*

> Si el CUIT ingresado no corresponde a ninguna empresa en Caddis, el bot indicara que no encontro la empresa. Verificar que el CUIT este cargado correctamente en el sistema.

---

## Paso 2: Asociar el contacto a un usuario en Caddis

Una vez que el contacto quedo registrado en Caddis, un administrador debe asociarlo a un **usuario del sistema** desde la pantalla **Mensajeria Contactos**.

<img src="imagenes/telegram_proc_paso4.png" style="width:auto; height:auto; max-width:100%; max-height:780px; display:block; margin:0 auto;">

1. Ir a **Administracion → Mensajeria Contactos**
2. El contacto recien registrado aparecera en la grilla con: **Plataforma** = TELEGRAM, **Nombre Completo**, **Numero** (ID de Telegram) y **Fecha inicio**
3. En la columna **Usuario** (recuadrado en rojo), seleccionar el usuario de Caddis que corresponde a esa persona

> Esta asociacion es obligatoria. Sin un usuario de Caddis asignado, el contacto no puede recibir ninguna notificacion.

---

## Paso 3: Configurar las notificaciones del usuario

Las notificaciones que recibira cada usuario se configuran desde **Administracion → Accesos a Notificaciones**:

1. Seleccionar el **USUARIO** en el desplegable
2. En la grilla aparecen todas las notificaciones disponibles del sistema
3. Tildar (activar) las notificaciones que debe recibir ese usuario

| Notificacion | Descripcion |
|---|---|
| ML Control de Stock en 0 | Avisa cuando un articulo sincronizado con ML llega a stock 0 |
| ML Control remitos no emitidos | Avisa cuando hay ventas de ML sin remito generado |

> Cada usuario tiene su propia configuracion de notificaciones independiente.

---

## Resumen del circuito

| Paso | Donde | Accion |
|---|---|---|
| 1.1 | Telegram (celular) | Buscar **CaddisERPBot** y abrir el chat |
| 1.2 | Telegram (celular) | Presionar **INICIAR / START** |
| 1.3 | Telegram (celular) | Enviar el CUIT de la empresa y confirmar con **Si** |
| 2 | Caddis — Mensajeria Contactos | Asociar el contacto al usuario de Caddis correspondiente |
| 3 | Caddis — Accesos a Notificaciones | Activar las notificaciones para ese usuario |

---

## Notas importantes

- El bot se llama **CaddisERPBot** (respetando exactamente las mayusculas). Si se escribe diferente, no aparece en la busqueda.
- El CUIT debe ingresarse **sin guiones ni espacios** (solo los 11 numeros).
- Si una persona tiene Telegram en varios dispositivos, el registro aplica a todos (la cuenta de Telegram es unica por numero de telefono).
- Para desregistrar un contacto: eliminarlo desde **Mensajeria Contactos** con el boton de papelera.
- La configuracion de notificaciones es **por usuario de Caddis**, no por contacto de Telegram. Si se cambia el usuario asociado a un contacto, cambian tambien las notificaciones que recibe.
