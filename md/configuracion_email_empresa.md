# Correo para envio de Mails de la Empresa
### Configuracion — Integraciones

> **Version:** 1.0 — Abril 2026
> **Audiencia:** Administrador de sistemas o responsable del dominio de correo de la empresa

---

## Para que sirve esta configuracion?

Caddis puede enviar correos electronicos en nombre de la empresa: remitos, facturas, notificaciones, etc. Para que estos correos lleguen correctamente al destinatario y **no sean rechazados ni vayan a SPAM**, el dominio de la empresa debe autorizar a los servidores de Caddis a enviar mails desde su cuenta.

Esta autorizacion se realiza a traves de un registro **SPF** en el DNS del dominio.

> **Que es SPF?** SPF (Sender Policy Framework) es un mecanismo de seguridad del correo electronico que indica, a traves del DNS, cuales servidores estan autorizados a enviar mails en nombre de un dominio. Cuando un servidor de destino recibe un mail, verifica el SPF del dominio remitente para decidir si acepta el mensaje o lo marca como SPAM.

---

## Quien debe realizar esta configuracion?

El **encargado de sistemas o IT** de la empresa, que tenga acceso al panel de administracion del DNS donde esta alojado el dominio (por ejemplo: GoDaddy, NIC Argentina, Donweb, Cloudflare, etc.).

---

## Paso a paso

### Paso 1 — Ingresar al panel DNS del dominio

Ingresar al panel de administracion del proveedor donde esta registrado el dominio de la empresa (por ejemplo: `empresa.com.ar`).

Buscar la seccion de gestion de registros DNS y localizar el registro de tipo **TXT** que comienza con `v=spf1`.

### Paso 2 — Identificar el registro SPF actual

El registro SPF existente tiene una forma similar a esta (el contenido varia segun el proveedor de correo de la empresa):

**Ejemplo con Office 365:**
```
v=spf1 include:spf.protection.outlook.com -all
```

**Ejemplo con Google Workspace:**
```
v=spf1 include:_spf.google.com -all
```

> Si el dominio no tiene ningun registro SPF, se debe crear uno nuevo de tipo TXT.

### Paso 3 — Agregar la autorizacion de Caddis

Dentro del registro SPF existente, agregar el siguiente include **antes del `-all` final**:

```
include:email-smtp.us-east-1.amazonaws.com
```

**Ejemplo: como queda el registro modificado (con Office 365):**
```
v=spf1 include:spf.protection.outlook.com include:email-smtp.us-east-1.amazonaws.com -all
```

**Ejemplo: si el dominio no tenia SPF previo:**
```
v=spf1 include:email-smtp.us-east-1.amazonaws.com -all
```

> No eliminar los includes existentes. Solo agregar el de Caddis al final, antes del `-all`.

### Paso 4 — Guardar los cambios en el DNS

Guardar el registro TXT modificado. Los cambios en el DNS pueden demorar hasta **24-48 horas** en propagarse globalmente, aunque en la mayoria de los casos surten efecto en pocos minutos.

### Paso 5 — Notificar a soporte de Caddis

Una vez configurado el SPF, enviar un mail a **soporte@caddis.com.ar** indicando la **direccion de correo** que se utilizara para el envio (por ejemplo: `ventas@empresa.com.ar` o `info@empresa.com.ar`).

El equipo de Caddis enviara a esa direccion un **mail de validacion** que debera ser aprobado antes de que el envio de correos quede activo.

---

## Resumen del proceso

| Paso | Responsable | Accion |
|---|---|---|
| 1 | IT / Sistemas | Ingresar al panel DNS del dominio |
| 2 | IT / Sistemas | Localizar el registro TXT con `v=spf1` |
| 3 | IT / Sistemas | Agregar `include:email-smtp.us-east-1.amazonaws.com` antes del `-all` |
| 4 | IT / Sistemas | Guardar los cambios y esperar propagacion |
| 5 | IT / Sistemas | Enviar la direccion de correo a soporte@caddis.com.ar |
| 6 | Caddis | Enviar mail de validacion a la direccion indicada |
| 7 | IT / Sistemas | Aprobar el mail de validacion recibido |

---

## Notas importantes

- Esta configuracion debe realizarse **una sola vez por dominio**. Si la empresa tiene varias cuentas de correo del mismo dominio (`ventas@empresa.com.ar`, `info@empresa.com.ar`), el registro SPF se modifica una sola vez y aplica a todas.
- Si la empresa tiene **multiples dominios** (por ejemplo, opera con `empresa.com.ar` y `empresa-sa.com.ar`), el proceso debe repetirse para cada dominio.
- No modificar ni eliminar los `include:` existentes en el SPF: cada uno corresponde a un servicio autorizado (Office 365, Google, etc.) y eliminarlos puede hacer que esos correos tambien vayan a SPAM.
- Si hay dudas sobre como acceder al DNS o como identificar el registro SPF, contactar al proveedor de hosting o al equipo de soporte de Caddis.
