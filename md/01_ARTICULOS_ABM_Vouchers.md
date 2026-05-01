# VOUCHERS INDIVIDUALES
### Módulo 1 — Artículos

> **Versión:** 1.0 — Febrero 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Artículos → Vouchers Individuales

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Vouchers Individuales** permite crear y gestionar códigos de descuento únicos que los operadores entregan a clientes para ser aplicados al momento de facturar. Desde aquí podés:

- Crear nuevos vouchers con descuento porcentual o de monto fijo
- Consultar todos los vouchers existentes y si ya fueron utilizados
- Modificar los datos de un voucher
- Eliminar vouchers que no hayan sido usados en facturas o presupuestos

> 📖 Para aprender a aplicar un voucher al momento de facturar, consultá [**Facturación (A / B / C / M)**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf).

---

## Cómo acceder

Desde el menú principal seleccioná:
**Artículos → Vouchers Individuales**

---

## Descripción general de la pantalla

![Pantalla Vouchers Individuales](imagenes/pantalla_vouchers_individuales.png)

La pantalla está dividida en dos paneles:

- **Panel izquierdo:** Formulario para crear o modificar un voucher (campos DESCRIPCION, ALIAS, VENCE, DTO %, IMPORTE, MULTIUSO, EDITABLE) con los botones **Nuevo** y **Guardar**
- **Panel derecho:** Grilla con todos los vouchers individuales cargados, incluyendo columnas para identificar cada voucher, su vencimiento, tipo de descuento y estado de uso

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **DESCRIPCION** | Nombre o descripción larga del voucher (máx. 30 caracteres). Se muestra en la grilla de la derecha como referencia interna. |
| **ALIAS** | Código corto que el operador ingresará en la pantalla de facturación para aplicar el descuento (máx. 20 caracteres). **Este es el "código" del voucher que se entrega al cliente.** |
| **VENCE** | Fecha de vencimiento del voucher. Después de esa fecha, el voucher no podrá aplicarse en ninguna factura. Campo obligatorio. |
| **DTO %** | Porcentaje de descuento a aplicar sobre el total de la factura (ej.: `10.00` = 10% de descuento). **Completar solo este campo o IMPORTE, nunca ambos.** |
| **IMPORTE** | Monto fijo de descuento en pesos (ej.: `5000.00` = $5.000 de descuento). **Completar solo este campo o DTO %, nunca ambos.** |
| **MULTIUSO** | **NO** → el voucher se puede usar una sola vez y queda marcado como "utilizado" después de la primera factura. **SI** → el voucher puede aplicarse en múltiples facturas sin límite. |
| **EDITABLE** | **NO** → el descuento del voucher no puede modificarse al aplicarlo en una factura. **SI** → el operador puede ajustar el monto al momento de usarlo. |

---

## Conceptos clave

### Descuento porcentual vs. descuento fijo

Un voucher solo puede tener **uno** de los dos tipos de descuento:

| Tipo | Campo a completar | Ejemplo |
|---|---|---|
| Porcentual | **DTO %** (dejar IMPORTE en 0) | `10.00` → descuenta el 10% del total |
| Monto fijo | **IMPORTE** (dejar DTO % en 0) | `5000.00` → descuenta $5.000 del total |

> ⚠️ Si se completan **ambos campos** o se dejan **ambos en cero**, el sistema mostrará un error al intentar guardar.

---

### Alias: el código del voucher

El **ALIAS** es el identificador que el operador de caja tipea en el campo Voucher de la pantalla de facturación para activar el descuento. Es un código corto y fácil de recordar.

**Ejemplos de alias:**
- `DESC10` → voucher de 10% de descuento
- `PROMO2026` → voucher de promoción especial
- `VIP500` → voucher de $500 para clientes VIP

El cliente recibe este alias (por mensaje, impreso, etc.) y lo presenta al vendedor al momento de comprar.

---

### Voucher de uso único vs. Multiuso

| Tipo | Comportamiento |
|---|---|
| **Uso único** (MULTIUSO = NO) | Una vez aplicado en una factura, el voucher queda marcado como "utilizado" y no puede volver a usarse. Ideal para promociones personalizadas. |
| **Multiuso** (MULTIUSO = SI) | El voucher puede usarse en tantas facturas como se desee, sin restricción de cantidad de usos. Ideal para descuentos permanentes o por categoría de cliente. |

---

### Voucher editable vs. no editable

| Tipo | Comportamiento |
|---|---|
| **No editable** (EDITABLE = NO) | El descuento del voucher se aplica exactamente como fue configurado y no puede cambiarse al facturar. |
| **Editable** (EDITABLE = SI) | El operador puede modificar el monto del descuento en el momento de aplicarlo. Útil cuando el descuento varía según la situación. |

---

### Columna "Usado" en la grilla

La grilla del panel derecho muestra una columna **Usado** que indica si el voucher fue aplicado en al menos una factura. Un voucher con valor en esa columna **no puede eliminarse** del sistema.

---

## Grilla de vouchers (panel derecho)

La grilla muestra todos los vouchers individuales del sistema con las siguientes columnas:

| Columna | Descripción |
|---|---|
| **Voucher** | Código interno del voucher (ID del sistema) |
| **Vence** | Fecha de vencimiento |
| **Descuento** | Porcentaje de descuento configurado (si aplica) |
| **Importe** | Monto fijo de descuento (si aplica) |
| **Descripción** | Nombre largo del voucher |
| **Alias** | Código corto para aplicarlo en facturación |
| **Editable** | SI / vacío (si es editable por el operador) |
| **Multiuso** | SI / vacío (si puede usarse más de una vez) |
| **Usado** | Cantidad de veces que fue aplicado en facturas |

---

## Paso a paso: Crear un voucher nuevo

**Caso típico:** Crear un voucher de 15% de descuento para un cliente VIP, válido durante el mes de marzo.

**1. Ingresar la descripción**
- En el campo **DESCRIPCION**, escribí el nombre del voucher.
- Ejemplo: `Descuento VIP Marzo 2026`

**2. Definir el alias (código)**
- En el campo **ALIAS**, escribí el código corto que se usará al facturar.
- Ejemplo: `VIP15`
- Elegí un alias fácil de recordar y sin espacios ni caracteres especiales.

**3. Establecer la fecha de vencimiento**
- En el campo **VENCE**, ingresá la fecha hasta la cual el voucher será válido.
- Ejemplo: `31/03/2026`

**4. Configurar el descuento**
- Si el descuento es porcentual: completá **DTO %** con el porcentaje y dejá **IMPORTE** en `0.00`.
  - Ejemplo: DTO % = `15.00`, IMPORTE = `0.00`
- Si el descuento es de monto fijo: completá **IMPORTE** y dejá **DTO %** en `0.00`.
  - Ejemplo: DTO % = `0.00`, IMPORTE = `5000.00`

**5. Configurar multiuso**
- **MULTIUSO = NO** si el voucher es para uso único (el cliente solo puede usarlo una vez).
- **MULTIUSO = SI** si el voucher puede usarse en múltiples compras.

**6. Configurar editable**
- **EDITABLE = NO** en la mayoría de los casos (el descuento se aplica tal como fue configurado).
- **EDITABLE = SI** solo si querés permitir que el operador ajuste el monto al usarlo.

**7. Guardar**
- Hacé clic en **Guardar** (o presioná el botón de confirmar).
- El sistema pedirá confirmación con el mensaje "¿Ingresar el Registro?".
- Hacé clic en **Aceptar** para confirmar.
- El nuevo voucher aparecerá en la grilla del panel derecho.

> 💡 Una vez creado el voucher, comunicate con el cliente y pasale el **ALIAS** para que lo presente al momento de comprar.

---

## Paso a paso: Modificar un voucher existente

**1.** En la grilla del panel derecho, hacé clic en el botón **Modificar** (ícono de lápiz) en la fila del voucher que querés cambiar.

**2.** Los datos actuales del voucher se cargarán en el formulario del panel izquierdo.

**3.** Modificá los campos que necesités (descripción, alias, fecha de vencimiento, descuento, multiuso, editable).

**4.** Hacé clic en **Guardar** y confirmá el cambio.

> ⚠️ Podés modificar un voucher aunque ya haya sido usado. Tené en cuenta que si cambiás el alias, el alias anterior ya no funcionará en facturas futuras.

---

## Paso a paso: Eliminar un voucher

**1.** En la grilla del panel derecho, hacé clic en el botón **Eliminar** (ícono de papelera) en la fila del voucher que querés borrar.

**2.** El sistema pedirá confirmación con el mensaje "¿Eliminar este registro?".

**3.** Hacé clic en **Aceptar** para confirmar.

> ⚠️ **No se puede eliminar** un voucher que ya fue aplicado en una **factura** o en un **presupuesto**. Si intentás hacerlo, el sistema mostrará un mensaje de error indicando dónde está asociado.

---

## Errores frecuentes y cómo resolverlos

| Error | Causa | Solución |
|---|---|---|
| "Debe ingresar una descripción" | El campo DESCRIPCION está vacío | Completá el campo DESCRIPCION |
| "Debe ingresar un Alias" | El campo ALIAS está vacío | Completá el campo ALIAS con un código corto |
| "Controle el Vencimiento" | El campo VENCE está vacío | Ingresá una fecha de vencimiento válida |
| "Debe ingresar un importe o un porcentaje de descuento" | Tanto DTO % como IMPORTE están en 0 | Completá uno de los dos campos con un valor mayor a 0 |
| "Se debe ingresar solo uno: Importe o Porcentaje de Descuento" | Tanto DTO % como IMPORTE tienen valores distintos de 0 | Dejá uno de los dos en 0.00 |
| "Voucher asociado a un Presupuesto" (al eliminar) | El voucher fue aplicado en un presupuesto | No se puede eliminar; podés modificar la fecha de vencimiento para que caduque |
| "Voucher asociado a una Factura" (al eliminar) | El voucher fue aplicado en una factura emitida | No se puede eliminar; dejarlo como registro histórico |

---

## Preguntas frecuentes

**¿Cuántos vouchers puedo crear?**
No hay límite en la cantidad de vouchers que podés crear.

**¿Puedo crear vouchers con el mismo alias?**
Técnicamente el sistema no bloquea aliases repetidos, pero se recomienda usar aliases únicos para evitar confusión al aplicarlos en facturación.

**¿Qué pasa si el voucher venció?**
Al intentar aplicarlo en una factura, el sistema lo rechazará informando que el voucher está vencido o no es válido.

**¿Un voucher aplica sobre artículos o sobre el total?**
El descuento del voucher se aplica sobre el **total de la factura** (no sobre artículos individuales).

**¿El voucher se combina con otras promociones o descuentos por forma de pago?**
No. Cuando hay un voucher activo en una factura, los descuentos automáticos por forma de pago (efectivo, débito, etc.) **no se aplican**.

**¿Cuál es la diferencia entre Vouchers Individuales y Vouchers Promociones?**
Los **Vouchers Individuales** tienen un único código (un solo alias) y pueden configurarse para uso único o multiuso. Los **Vouchers Promociones** son rangos de códigos generados en lote (por ejemplo, para campañas masivas). Esta pantalla gestiona exclusivamente los vouchers individuales.

---

## Referencia rápida de campos

| Campo | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| DESCRIPCION | Texto (máx. 30) | Sí | Nombre del voucher |
| ALIAS | Texto (máx. 20) | Sí | Código para aplicar en facturación |
| VENCE | Fecha | Sí | Fecha de vencimiento |
| DTO % | Número decimal | Uno de los dos | Porcentaje de descuento |
| IMPORTE | Número decimal | Uno de los dos | Monto fijo de descuento |
| MULTIUSO | SI / NO | Sí | Permite uso en múltiples facturas |
| EDITABLE | SI / NO | Sí | Permite editar el descuento al aplicarlo |

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Febrero 2026*
