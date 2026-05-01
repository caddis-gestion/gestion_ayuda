# 3.21 REASIGNAR FACTURACIÓN
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Supervisores y administradores del sistema
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Reasignar Facturación

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Reasignar Facturación** permite modificar la asignación de responsables en facturas ya emitidas. Desde aquí podés:

- Cambiar el Punto de Venta, vendedor, supervisor, jefe de ventas o gerente asignado a una factura
- Corregir asignaciones incorrectas en comprobantes emitidos (ej.: una factura que quedó asignada al vendedor equivocado)
- Aplicar los cambios a múltiples facturas simultáneamente
- Afectar los cálculos de comisiones y objetivos de ventas

> ⚠️ Esta pantalla modifica datos de facturas ya emitidas. Los cambios afectan directamente los informes de ventas, comisiones y objetivos. Usar con cuidado y solo cuando sea necesario.

---

<img src="imagenes/pantalla_reasignar_facturacion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Reasignar Facturación**

---

## Descripción general de la pantalla

La pantalla está dividida en dos secciones:

- **Selector de tipo:** permite elegir el tipo de comprobante a reasignar
- **Sección "Definir nuevas asignaciones":** permite seleccionar el nuevo PDV, vendedor, supervisor, jefe de ventas y gerente
- **Panel derecho:** grilla con las facturas del período actual que serán afectadas por la reasignación

---

## Campos del formulario

### Tipo de comprobante

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de comprobante sobre el que se aplica la reasignación (TK, EB, EA, A, B, NC, etc.). Por defecto: TK. |

---

### Definir nuevas asignaciones

Para cada nivel de la jerarquía de ventas, podés elegir el nuevo responsable y si aplicar el cambio (checkbox):

| Campo | Descripción |
|---|---|
| **PDV** | Nuevo Punto de Venta a asignar. Muestra la categoría actual del PDV (solo lectura). |
| **VEND** | Nuevo vendedor a asignar. Muestra la categoría actual del vendedor. |
| **SUP** | Nuevo supervisor a asignar. Muestra la categoría actual del supervisor. |
| **J.VTAS** | Nuevo jefe de ventas (subgerente) a asignar. |
| **GTE** | Nuevo gerente a asignar. |
| **Checkbox** | En cada fila: indica si se aplica ese nivel de cambio (PDV, vendedor, supervisor, etc.). |

---

## Grilla del panel derecho

La grilla muestra las facturas del usuario actual que serán afectadas, con sus asignaciones actuales:

| Columna | Descripción |
|---|---|
| **Tipo** | Tipo de comprobante |
| **Factura** | Número de factura |
| **Fecha** | Fecha de emisión |
| **PDV** | PDV actual de la factura |
| **Vendedor** | Vendedor actual y su categoría |
| **Supervisor** | Supervisor actual y su categoría |
| **Subgerente** | Jefe de ventas actual y su categoría |
| **Gerente** | Gerente actual y su categoría |

---

## Paso a paso: Reasignar facturas a un vendedor diferente

**Caso típico:** Un vendedor emitió facturas que en realidad corresponden a otro vendedor.

**1.** En el campo **TIPO**, seleccioná el tipo de comprobante a reasignar (ej.: TK).

**2.** En la sección "Definir nuevas asignaciones":
   - En **VEND**, seleccioná el nuevo vendedor correcto.
   - Asegurate de que el checkbox de VEND esté tildado.
   - Si también necesitás cambiar el PDV u otros niveles, seleccioná los nuevos valores y tildá sus checkboxes.

**3.** Revisá la grilla del panel derecho para confirmar qué facturas serán afectadas.

**4.** Hacé clic en el botón de aplicar/guardar.

**5.** El sistema actualizará las facturas seleccionadas con las nuevas asignaciones.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| La grilla aparece vacía | No hay facturas del tipo seleccionado para el período actual | Cambiá el tipo de comprobante o verificá el período |
| Los cambios no afectan los informes | Los informes tienen caché | Actualizá la pantalla de Ventas Totales para ver los cambios |

---

## Preguntas frecuentes

**¿Los cambios afectan las comisiones ya calculadas?**
Sí, al cambiar el vendedor asignado, los cálculos de comisiones del período afectado pueden verse modificados. Verificá con el administrador antes de hacer cambios masivos.

**¿Puedo reasignar facturas de cualquier período?**
Depende de la configuración del sistema. Generalmente se pueden reasignar facturas del mes en curso o períodos recientes.

**¿Se puede ver quién hizo una reasignación?**
El sistema registra los cambios, pero la visibilidad del historial de modificaciones depende de la configuración de auditoría del sistema.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
