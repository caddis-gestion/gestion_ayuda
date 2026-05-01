# 3.19 TERMINAL CLOVER
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Administradores del sistema
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Terminal Clover

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Terminal Clover** permite configurar y gestionar la integración entre Caddis y los terminales de pago **Clover**. Desde aquí podés:

- Ver las cuentas Clover habilitadas para tu empresa
- Conectar (integrar) una cuenta Clover con el sistema ingresando el código de autorización
- Asignar el Punto de Venta de Caddis correspondiente a cada cuenta Clover
- Desconectar (desvincular) una cuenta Clover cuando ya no se usa
- Verificar el estado de vigencia de cada integración

> ℹ️ El terminal **Clover** es un dispositivo de cobro con tarjeta. Al integrarlo con Caddis, los cobros realizados desde el terminal pueden vincularse automáticamente a las facturas del sistema.

---

<img src="imagenes/pantalla_terminal_clover.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Terminal Clover**

---

## Descripción general de la pantalla

La pantalla muestra el **logo de Clover** y debajo un listado de todas las cuentas habilitadas para integración con tu empresa. Las cuentas con integración activa y vigente se muestran en **verde**; las con integración vencida o sin conectar, en **rojo**.

---

## Información por cuenta Clover

Para cada cuenta listada, la pantalla muestra:

| Campo | Descripción |
|---|---|
| **Canal de Venta** | Nombre del canal o local asociado a esta cuenta Clover |
| **Usuario/Merchant** | Identificador de la cuenta en Clover (Merchant ID) |
| **PDV asociado** | Punto de Venta de Caddis al que está vinculado este terminal |
| **Código de autorización** | Campo donde se ingresa el token/código para conectar la cuenta |

---

## Botones disponibles por cuenta

| Botón | Qué hace |
|---|---|
| **Integrar cuenta** | Conecta la cuenta Clover con Caddis usando el código de autorización ingresado. Solo disponible para usuarios de soporte. |
| **Desvincular cuenta** | Desconecta la integración activa. Solo aparece si la cuenta tiene una integración vigente. |

---

## Paso a paso: Conectar un terminal Clover

**Requisitos previos:**
- Tener acceso al panel de administración de Clover
- Obtener el código de autorización (token) desde la cuenta Clover
- Ser usuario con permisos de soporte en Caddis

**1.** En la cuenta Clover correspondiente, ingresá el **código de autorización** en el campo de texto.

**2.** Seleccioná el **PDV** de Caddis al que querés asociar este terminal.

**3.** Hacé clic en **Integrar cuenta**.

**4.** El sistema intentará conectar con Clover usando ese código. Si es exitoso, el indicador de la cuenta pasará a **verde** (vigente).

---

## Paso a paso: Desconectar un terminal Clover

**1.** En la cuenta que querés desconectar (fondo verde), hacé clic en **Desvincular cuenta**.

**2.** Confirmá la acción.

**3.** El indicador pasará a **rojo** y el terminal ya no estará integrado con Caddis.

---

## Cómo usar el terminal Clover en facturación

Una vez integrado, el terminal Clover se usa desde la pantalla de **Facturación** (3.01):

1. Ingresá los artículos en la factura
2. Hacé clic en el botón **Clover** en el formulario de facturación
3. El sistema buscará automáticamente los cobros recientes del terminal Clover asociado al PDV
4. Seleccioná el cobro correspondiente para vincularlo a la factura
5. Hacé clic en **Facturar**

---

## Preguntas frecuentes

**¿Qué pasa si el token de integración vence?**
El indicador pasará a rojo y los cobros del terminal no podrán vincularse automáticamente a Caddis. Necesitarás obtener un nuevo código de autorización desde Clover y reconectar.

**¿Puedo tener múltiples terminales Clover por empresa?**
Sí, podés tener varias cuentas Clover, una por cada canal de venta o local. Cada una se asocia a su PDV correspondiente.

**¿Quién puede integrar/desvincular cuentas?**
Solo los usuarios con perfil de **soporte** en Caddis tienen acceso al campo de código de autorización. Los demás usuarios pueden ver el estado de las integraciones pero no modificarlas.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
