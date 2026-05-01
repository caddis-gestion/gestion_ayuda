# TASAS DE TARJETAS DE CRÉDITO Y DÉBITO
### Módulo 1 — Artículos

> **Versión:** 1.0 — Febrero 2026
> **Audiencia:** Administradores del sistema
> **Pantalla en el sistema:** Menú → Artículos → Tasas de Tarjetas de Crédito

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Tasas de Tarjetas de Crédito y Débito** permite configurar los intereses que el sistema aplica automáticamente cuando una venta se cobra con tarjeta de crédito en cuotas o con tarjeta de débito.

Cada combinación de **plataforma de cobro + tarjeta + tipo de promoción + cantidad de cuotas** puede tener su propia tasa de interés. Cuando el operador registra un pago con tarjeta en la pantalla de **Facturación**, el sistema busca la tasa correspondiente y recalcula el importe total antes de emitir el comprobante.

> ⚠️ Esta pantalla es de uso exclusivo del **administrador del sistema**. Una configuración incorrecta afecta directamente los importes que se cobran a los clientes.

---

## Cómo acceder

Desde el menú principal seleccioná:
**Artículos → Tasas de Tarjetas de Crédito**

---

## Descripción general de la pantalla

La pantalla está organizada en **dos paneles**:

![Pantalla Tarjetas Tasas](imagenes/pantalla_tarjetas_tasas.png)

- **Panel izquierdo (formulario):** Campos para cargar o editar una tasa: Plataforma, Tarjeta, Promo, Cuotas, Tasa y Activa. Incluye la sección **Importar** para carga masiva desde Excel.
- **Panel derecho (grilla):** Lista de tasas ya configuradas, con columnas Tarjeta, Promo, Cuotas, Tasa, Activa y Plataforma. Se filtra automáticamente por la Plataforma, Tarjeta y Promo seleccionadas en el formulario. Cada fila tiene botones para modificar o borrar.

> 💡 Al cambiar la **Plataforma** en el formulario, la grilla se actualiza automáticamente mostrando solo las tasas de esa plataforma.

---

## Campos del formulario

| Campo | Descripción |
|---|---|
| **PLATAFORMA** | Terminal de cobro donde se pasa la tarjeta (ej.: Lapos, Clover, MercadoPago, POS propio). Al cambiar este campo la grilla se actualiza automáticamente. |
| **TARJETA** | Marca de la tarjeta de crédito o débito (ej.: Visa, Mastercard, Cabal, Naranja, American Express, Visa Débito). |
| **PROMO** | Tipo de promoción (ej.: Contado, 3 Cuotas, 6 Cuotas, 12 Cuotas, Plan Z). Las opciones disponibles las configura el administrador en la tabla de promociones. |
| **CUOTAS** | Cantidad de cuotas de la promoción (valores entre 0 y 99). Para tarjetas de **débito**, siempre debe ser **0** y el campo queda bloqueado. |
| **TASA** | Porcentaje de interés total a aplicar, **con IVA ya incluido** (ej.: `5.00` equivale a 5%). Ver sección "Cómo calcular la tasa correcta" más abajo. |
| **ACTIVA** | Estado de esta tasa: **ACTIVA** (el sistema la usa al facturar) o **INACTIVA** (queda guardada pero no se aplica). |

---

## Botones y acciones disponibles

| Botón / Acción | Qué hace |
|---|---|
| **Guardar** | Guarda la tasa configurada en el formulario. Si ya existe una tasa para esa misma combinación de Plataforma + Tarjeta + Promo + Cuotas, la reemplaza automáticamente. |
| **Modificar** (grilla) | Carga los datos de una tasa existente en el formulario para editarla. El botón aparece en cada fila de la grilla derecha. |
| **Borrar** (grilla) | Elimina definitivamente una tasa. Pide confirmación antes de ejecutarse. |
| **Cancelar** | Limpia el formulario sin guardar cambios. |
| **Actualizar** | Recarga la grilla derecha con los datos actualizados según la selección del formulario. Se ejecuta automáticamente al cambiar la plataforma, pero puede usarse en cualquier momento. |
| **Importar** | Importa tasas masivamente desde un archivo Excel. Ver sección "Importar desde Excel" más abajo. |

---

## Conceptos clave

### Cómo calcular la tasa correcta

El campo **TASA** debe ingresarse como el **porcentaje final con IVA incluido**. Esto es así porque el IVA sobre intereses financieros se calcula dentro del sistema.

**Fórmula:**
```
Tasa a ingresar = Tasa financiera neta × (1 + IVA)
```

**Ejemplo práctico:**
- Tasa financiera que el banco nos cobra: `4,13%`
- IVA vigente: `21%`
- Tasa a ingresar: `4,13% × 1,21 = 5,00%` → se ingresa **`5.00`**

> ⚠️ Si ingresás la tasa sin el IVA, el sistema calculará un interés menor al real y el comprobante quedará con un importe incorrecto.

---

### Cómo aplica el sistema el interés al facturar

Cuando el operador selecciona una tarjeta de crédito con cuotas en la ventana de Pagos de Facturación, el sistema:

1. Busca la tasa configurada para esa combinación de Plataforma + Tarjeta + Promo
2. Calcula el interés: `Interés = Importe de venta × Tasa`
3. Suma el interés al importe original: `Total a facturar = Importe + Interés`
4. El comprobante se emite por el total con interés incluido

**Ejemplo:**

| Concepto | Monto |
|---|---|
| Precio de venta | $100.000 |
| Tasa configurada (con IVA) | 12% |
| Interés calculado | $12.000 |
| **Total facturado al cliente** | **$112.000** |

> 💡 El interés ya incluye el IVA en el cálculo, por eso la tasa se ingresa con IVA incluido.

---

### Tarjetas de débito

Las tarjetas de débito tienen comportamiento especial:

- El campo **CUOTAS** queda bloqueado en **0** automáticamente (el débito no tiene cuotas)
- La **tasa no puede ser negativa** (el sistema lo valida al guardar)
- Si el PDV no cobra recargo por débito, se ingresa `0.00` como tasa

> 💡 Por convención, las tarjetas de débito tienen un `Id_Tarjeta` de 500 o mayor en el sistema. El formulario las identifica automáticamente y aplica las restricciones correspondientes.

---

## Paso a paso: Agregar una nueva tasa

**Caso típico:** Configurar un interés del 15% para Visa crédito en 12 cuotas con terminal Lapos.

**1.** Seleccioná la **PLATAFORMA** donde se cobra con esa tarjeta (ej.: `Lapos`).

**2.** Seleccioná la **TARJETA** (ej.: `Visa`).

**3.** Seleccioná la **PROMO** correspondiente (ej.: `12 Cuotas`).

**4.** Ingresá la cantidad de **CUOTAS** (ej.: `12`).

**5.** Ingresá la **TASA** como porcentaje final con IVA incluido (ej.: `15.00`).

**6.** Verificá que **ACTIVA** esté en `ACTIVA`.

**7.** Hacé clic en **Guardar**.

La nueva tasa aparecerá en la grilla derecha.

> 💡 Si ya existía una tasa para esa misma combinación, el sistema la reemplazará con los nuevos valores sin advertencia. Verificá la grilla antes de guardar.

---

## Paso a paso: Modificar una tasa existente

**1.** En el formulario izquierdo, seleccioná la **PLATAFORMA**, **TARJETA** y **PROMO** de la tasa que querés modificar para que aparezca en la grilla.

**2.** En la grilla derecha, ubicá la fila con la tasa a modificar.

**3.** Hacé clic en el botón **Modificar** de esa fila. Los datos se cargarán en el formulario izquierdo.

**4.** Editá los campos que necesitás (tasa, cuotas, estado activa/inactiva).

**5.** Hacé clic en **Guardar** para confirmar los cambios.

> ⚠️ No es posible cambiar la Plataforma, Tarjeta o Promo de una tasa existente mediante Modificar. Si necesitás cambiarlas, borrá la tasa actual y creá una nueva.

---

## Paso a paso: Desactivar una tasa sin borrarla

Si necesitás dejar de aplicar un interés pero querés conservar la configuración para el futuro:

**1.** Cargá la tasa en el formulario usando el botón **Modificar**.

**2.** Cambiá el campo **ACTIVA** a `INACTIVA`.

**3.** Hacé clic en **Guardar**.

La tasa quedará guardada pero el sistema no la usará al facturar.

---

## Importar tasas desde Excel

Esta función permite cargar o actualizar múltiples tasas a la vez desde un archivo de planilla de cálculo.

> ⚠️ **Requisito importante:** Al importar, todos los valores de tasa en el archivo deben estar expresados como el **porcentaje total con IVA incluido** (igual que al ingresarlos manualmente). El sistema lo indica con un mensaje de confirmación antes de procesar.

**Pasos:**

**1.** Preparar el archivo Excel con el formato correcto. Hacé clic en el botón **Ayuda** (si está disponible) para ver el formato esperado.

**2.** Hacé clic en el botón **Importar**.

**3.** El sistema mostrará una alerta: *"Al importar el interés debe ser Total con Iva incluido"*. Confirmá que los datos del archivo cumplen ese requisito y continuá.

**4.** Seleccioná el archivo Excel desde tu equipo.

**5.** El sistema procesará el archivo y cargará las tasas automáticamente. Se mostrará el resultado de la importación indicando cuántos registros se procesaron.

> 💡 La importación usa el mismo mecanismo que el botón **Guardar** manual: si una combinación ya existe, la reemplaza; si no existe, la agrega.

---

## Cómo se usan estas tasas en la Facturación

Cuando un operador registra un pago con **tarjeta de crédito** en la ventana de **Pagos** de la pantalla de Facturación:

1. Selecciona la tarjeta y la promoción
2. El sistema busca automáticamente la tasa activa para esa combinación (Plataforma del PDV + Tarjeta + Promo)
3. El importe total de la factura se recalcula sumando el interés
4. El comprobante se emite por el nuevo total

Si no existe una tasa configurada para esa combinación, el sistema no agrega interés y el importe se mantiene sin cambios.

> 📖 Para ver cómo funciona el proceso completo de cobro con tarjeta desde la perspectiva del operador, consultá el instructivo [**Facturación (A / B / C / M)**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf), sección *"Intereses por cuotas en tarjetas de crédito y débito"*.

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| "Elija una Tarjeta" | Se intentó guardar sin seleccionar tarjeta | Seleccioná la tarjeta en el campo correspondiente |
| "Controle las Cuotas" | El valor de cuotas es negativo o mayor a 99 | Ingresá un valor entre 0 y 99 |
| "La Tasa no puede ser negativa para Tarjetas de Débito" | Se ingresó una tasa negativa para una tarjeta de débito | Para débito, la tasa debe ser 0 o positiva |
| La grilla no muestra registros | No hay tasas configuradas para la combinación seleccionada | Verificá que la Plataforma, Tarjeta y Promo sean correctas, o creá la tasa nueva |
| El interés en facturación no se aplica | La tasa para esa combinación está en INACTIVA | Cambiá el estado a ACTIVA en esta pantalla |
| El interés calculado es diferente al esperado | La tasa fue ingresada sin IVA | Corregí la tasa multiplicándola por `(1 + IVA)`, por ej.: `4.13 × 1.21 = 5.00` |

---

## Preguntas frecuentes

**¿Qué pasa si hay dos tasas para la misma tarjeta pero distinta cantidad de cuotas?**
Cada combinación de Tarjeta + Promo + Cuotas es independiente. El sistema aplica exactamente la tasa que coincide con lo que el operador seleccionó en la ventana de Pagos.

**¿Puedo tener la misma tarjeta configurada con diferentes tasas según la plataforma de cobro?**
Sí. Podés tener, por ejemplo, Visa 3 cuotas con 8% en terminal Lapos y Visa 3 cuotas con 10% en MercadoPago. El sistema distingue por plataforma.

**¿Qué pasa si el operador selecciona una tarjeta + promo para la que no hay tasa configurada?**
El sistema no agrega interés y el importe facturado es el original sin recargo. Es recomendable tener configuradas todas las combinaciones que se usan en el negocio.

**¿Puedo borrar todas las tasas y empezar de cero?**
Sí, podés borrar registro por registro desde la grilla. También podés usar la importación Excel para reemplazar todas las tasas en bloque.

**¿La tasa aplica también sobre descuentos o sobre el precio original?**
El interés se calcula sobre el **importe final de la venta** en el momento del cobro (después de descuentos, vouchers, etc.).

**¿Cuántas combinaciones puedo configurar?**
No hay límite. Podés tener tantas combinaciones de Plataforma + Tarjeta + Promo + Cuotas como necesites.

---

## Referencia rápida

| Elemento | Tipo | Descripción |
|---|---|---|
| PLATAFORMA | Lista desplegable | Terminal de cobro |
| TARJETA | Lista desplegable | Marca de tarjeta |
| PROMO | Lista desplegable | Tipo de promoción / plan |
| CUOTAS | Número (0-99) | Cantidad de cuotas (0 para débito) |
| TASA | Porcentaje | Interés total con IVA incluido |
| ACTIVA | Lista | ACTIVA o INACTIVA |
| Guardar | Botón | Guarda o reemplaza la tasa |
| Modificar | Botón (grilla) | Carga tasa en el formulario para editar |
| Borrar | Botón (grilla) | Elimina la tasa seleccionada |
| Cancelar | Botón | Limpia el formulario |
| Actualizar | Botón | Refresca la grilla según selección |
| Importar | Botón | Carga tasas masivamente desde Excel |

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Febrero 2026*
