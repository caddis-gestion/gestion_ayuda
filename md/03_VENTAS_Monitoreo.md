# 3.22 MONITOREO DE FACTURACIÓN
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Administradores del sistema y usuarios de soporte técnico
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Monitoreo de Facturación

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Monitoreo de Facturación** es una herramienta de administración técnica que permite gestionar comprobantes emitidos a nivel de base de datos. Desde aquí podés:

- Seleccionar la empresa (base de datos) a monitorear en entornos multi-empresa
- Eliminar comprobantes de venta emitidos (anulación técnica)
- Eliminar fichas de operación internas
- Realizar correcciones de emergencia cuando hay inconsistencias en los comprobantes

> ⚠️ **Esta pantalla es de uso exclusivo para administradores y técnicos del sistema.** Las operaciones que se realizan aquí son **irreversibles** y pueden afectar la contabilidad y los registros fiscales. No usar sin autorización.

---

<img src="imagenes/pantalla_monitoreo_facturacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Monitoreo de Facturación**

> ℹ️ Esta pantalla solo es visible para usuarios con permisos de administración del sistema.

---

## Descripción general de la pantalla

La pantalla está organizada en secciones:

1. **Selector de BASE:** Para entornos multi-empresa, permite elegir qué empresa/base de datos se está monitoreando
2. **Eliminar comprobantes emitidos:** Sección para anular técnicamente facturas, notas de crédito y otros comprobantes
3. **Eliminar ficha:** Sección para eliminar fichas internas de operación

---

## Sección: Selector de BASE

| Campo | Descripción |
|---|---|
| **BASE** | Selector de empresa. Muestra todas las bases de datos del sistema con acceso habilitado (bases con `Base_Menu = 20`). Al cambiar la base, todas las operaciones de monitoreo afectan a esa empresa. |

---

## Sección: Eliminar Comprobantes Emitidos

Esta sección permite la **eliminación técnica** de comprobantes del sistema.

| Campo/Botón | Descripción |
|---|---|
| **Tipo de comprobante** | Lista desplegable con todos los tipos de comprobante disponibles (ver tabla más abajo). |
| **N° de Factura** | Número del comprobante a eliminar. |
| **Eliminar** | Botón que ejecuta la eliminación del comprobante seleccionado. La acción es irreversible y pide confirmación. |

### Tipos de comprobante disponibles para eliminar

| Categoría | Tipos |
|---|---|
| **Facturas de venta** | IA, EA, A, IB, EB, B, IC, EC, C, IM, EM, M, X, TK, PA, PB, IV, OV, P, RC |
| **Notas de crédito** | NCIB, NCIA, NCB, NCA, NCX, NCEA, NCEB, NCMQ |
| **Notas de débito** | ND, NDA, NDB, NDX, NDEA, NDEB |
| **Remitos** | R, IR |
| **Comprobantes especiales** | RM, IRM (Movistar), RS (Resumen) |

> ⚠️ La eliminación de un comprobante **no revierte automáticamente los movimientos de stock, cuenta corriente ni AFIP**. Deben ajustarse manualmente si fuera necesario.

---

## Sección: Eliminar Ficha

| Campo/Botón | Descripción |
|---|---|
| **N° de Ficha** | Número de la ficha interna de operación a eliminar. |
| **Eliminar** | Botón que ejecuta la eliminación de la ficha. La acción es irreversible. |

> ℹ️ Una "ficha" es un registro interno del sistema que agrupa los datos de una operación en proceso. Se usa principalmente para diagnóstico técnico y limpieza de operaciones incompletas.

---

## Cuándo usar esta pantalla

| Situación | Acción a tomar |
|---|---|
| Una factura quedó con estado "emitida" pero AFIP no la recibió | Verificar en AFIP y eliminar para regenerar |
| Una operación quedó incompleta y dejó datos huérfanos | Eliminar la ficha correspondiente |
| Se emitió un comprobante duplicado por error técnico | Eliminar el duplicado y verificar stock y cuenta corriente |
| Inconsistencia entre el sistema y la contabilidad | Analizar y eliminar el comprobante con supervisión contable |

---

## Procedimiento recomendado antes de eliminar un comprobante

1. **Verificar el comprobante** en la pantalla de búsqueda correspondiente (ej.: buscar la factura en Ventas Totales o en la cuenta corriente del cliente).
2. **Revisar si está enviado a AFIP:** si ya fue autorizado por AFIP, la eliminación del sistema no lo revoca en AFIP. Puede ser necesario emitir una nota de crédito en su lugar.
3. **Consultar con el contador o responsable** antes de eliminar comprobantes con impacto contable.
4. **Registrar la operación:** dejar constancia de qué se eliminó, cuándo y por qué motivo.
5. **Ejecutar la eliminación** con el botón correspondiente.
6. **Verificar el resultado:** confirmar que el comprobante ya no aparece y que los registros relacionados (stock, cuenta corriente) quedaron correctos.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "No se encontró el comprobante" | El tipo/número no existe en la base seleccionada | Verificar tipo, número y base seleccionada |
| "No se puede eliminar" | El comprobante tiene registros relacionados que lo protegen | Analizar dependencias antes de eliminar |
| No aparecen opciones en el selector BASE | El usuario no tiene acceso a otras bases | Solo aparece la empresa propia; es normal |

---

## Preguntas frecuentes

**¿Se puede recuperar un comprobante eliminado?**
No. La eliminación es definitiva. Una vez eliminado, solo se puede recuperar si existe un backup de la base de datos.

**¿La eliminación de un comprobante avisa a AFIP?**
No. Eliminar un comprobante del sistema **no cancela la autorización en AFIP**. Si el comprobante fue autorizado electrónicamente, se debe emitir una Nota de Crédito para anularlo fiscalmente.

**¿Quién puede usar esta pantalla?**
Solo usuarios con perfil de administrador del sistema o técnicos autorizados por la empresa.

**¿Para qué sirve eliminar una ficha?**
Las fichas son registros temporales de operaciones en curso. Si una operación quedó incompleta (ej.: se cayó la conexión a mitad de una factura), puede dejar una ficha "colgada". Eliminarla limpia ese estado y permite reiniciar la operación.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
