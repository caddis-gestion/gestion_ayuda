# CADDIS ERP — Instructivo de Usuario
## Módulo: Clientes · Pantalla: Alta, Baja y Modificación de Clientes

> **Versión:** 1.0 — Febrero 2026
> **Módulo:** 2 — Clientes
> **Pantalla:** 2.01 — ABM Clientes
> **Nivel:** Básico — No se requieren conocimientos técnicos

---

## ¿Para qué sirve esta pantalla?

Esta pantalla es el lugar donde se registran y administran **todos los clientes** de la empresa. Desde aquí podés:

- Dar de alta un cliente nuevo
- Buscar un cliente ya existente
- Modificar los datos de un cliente
- Desactivar un cliente (no se puede eliminar si tiene facturas)
- Consultar o actualizar la información para facturación y entrega

Cada vez que se hace una venta, se emite una factura o se realiza un envío, el sistema utiliza los datos del cliente registrados en esta pantalla. **Es fundamental que los datos estén correctos**, especialmente el CUIT/DNI y la condición de IVA.

---

## Cómo llegar a esta pantalla

En el menú superior del sistema, navegá: **VENTAS → CLIENTES → CLIENTES ABM**

> 💡 También podés usar la barra de búsqueda del menú superior y escribir "Clientes" para encontrarla rápidamente.

---

## Cómo está organizada la pantalla

La pantalla se presenta en **un único panel**, organizado en tres zonas verticales:

```
┌──────────────────────────────────────────────────────────┐
│   BARRA DE HERRAMIENTAS                                  │
│   [Nuevo] [Guardar] [Eliminar] [Buscar]                  │
├──────────────────────────────────────────────────────────┤
│   BUSCADOR Y LISTA DE CLIENTES                           │
│   (filtro por nombre / CUIT + grilla de resultados)      │
├──────────────────────────────────────────────────────────┤
│   FORMULARIO DE DATOS DEL CLIENTE                        │
│   (se completa al seleccionar un cliente o al dar alta)  │
└──────────────────────────────────────────────────────────┘
```

- **Barra de herramientas:** contiene los botones principales de acción (Nuevo, Guardar, Eliminar, Buscar).
- **Buscador y lista:** permite filtrar clientes existentes por nombre, razón social o CUIT y seleccionar uno para ver o editar sus datos.
- **Formulario:** muestra todos los campos del cliente seleccionado o limpio para ingresar uno nuevo.

---

## Botones principales

| Botón | Qué hace |
|---|---|
| **Nuevo** | Limpia el formulario para ingresar un cliente nuevo |
| **Guardar** | Guarda los datos del formulario (tanto para nuevo como para modificación) |
| **Eliminar** | Elimina el cliente (solo si no tiene comprobantes registrados) |
| **Buscar** | Filtra la lista de clientes según lo escrito en el buscador |

---

## Sección 1 — Datos Generales del Cliente

Esta es la primera sección del formulario. Contiene la información básica e identificatoria del cliente.

---

### Campo: CODIGO

- **Qué es:** Número de identificación interno que Caddis asigna automáticamente al cliente.
- **Lo completa:** El sistema solo. **No se puede modificar a mano.**
- **Para qué sirve:** Es el número único que identifica al cliente en todo el sistema (facturas, remitos, cuenta corriente, etc.)
- **Cuando es "0" o está vacío:** Significa que es un cliente nuevo que todavía no fue guardado.

---

### Campo: ACTIVO / INACTIVO

- **Qué es:** Indica si el cliente está habilitado para operar en el sistema.
- **Opciones:**
  - **ACTIVO:** El cliente puede ser usado en ventas, facturas y remitos.
  - **INACTIVO:** El cliente no aparece en las búsquedas al facturar. Se usa para dar de baja clientes que ya no operan sin perder su historial.
- **Cuándo usarlo:** Cambiá a INACTIVO cuando un cliente dejó de comprar o se detectó un error en su carga, pero ya tiene comprobantes asociados que no podés borrar.

> ⚠️ **Importante:** No elimines un cliente que tiene facturas o remitos. En su lugar, ponelo como INACTIVO.

---

### Campo: CUIT / DNI

- **Qué es:** El número de documento fiscal del cliente.
  - Para **personas físicas** en Argentina: puede ser el **DNI** (7 u 8 dígitos) o el **CUIT** (11 dígitos con formato XX-XXXXXXXX-X).
  - Para **personas jurídicas** (empresas): siempre el **CUIT** (11 dígitos).
  - Para clientes del **exterior**: el número de identificación fiscal del país correspondiente.
- **Formato:** Solo números, **sin guiones ni puntos**. El CUIT debe ingresarse obligatoriamente sin guiones.
  - Ejemplo correcto: `20123456789`
  - Ejemplo incorrecto: `20-12345678-9`
- **Es obligatorio:** ✅ Sí. No se puede guardar un cliente sin este dato.
- **El sistema verifica duplicados:** Si ingresás un CUIT que ya existe en otro cliente, el sistema te avisa el nombre del cliente duplicado antes de guardar.

#### Botón: VER EN AFIP

Aparece a la derecha del campo CUIT (solo para empresas Argentina).

- **Qué hace:** Abre la **Constancia de Inscripción** del cliente en el sitio oficial de AFIP.
- **Para qué sirve:** Verificar que el CUIT es válido, ver la razón social oficial, la condición de IVA y el domicilio fiscal registrado ante AFIP.
- **Cuándo usarlo:** Siempre que tengas dudas sobre el CUIT de un cliente nuevo o cuando necesitás confirmar su condición impositiva.

> 💡 **Consejo:** Usá el botón "Ver en AFIP" antes de cargar un cliente nuevo para copiar la razón social exactamente como figura en AFIP. Esto evita errores en las facturas.

---

### Campo: NACIMIENTO y SEXO

- **Qué es:** Fecha de nacimiento del cliente y su sexo biológico.
- **Formato de fecha:** DD/MM/AAAA (día/mes/año). Ejemplo: `15/03/1985`
- **Opciones de sexo:** MASCULINO / FEMENINO
- **¿Es obligatorio?** No. Se recomienda completar para personas físicas, especialmente en rubros de telecomunicaciones donde las operadoras lo requieren.

---

### Campo: CLIENTE (Razón Social o Nombre)

- **Qué es:** El nombre completo del cliente.
  - Para personas físicas: Apellido y Nombre (Ej: `García Juan Carlos`)
  - Para empresas: Razón Social completa (Ej: `Distribuidora Norte S.R.L.`)
- **Es obligatorio:** ✅ Sí. No se puede guardar sin nombre.
- **Límite:** Hasta 50 caracteres.

> 💡 **Consejo:** Ingresá siempre el nombre en **MAYÚSCULAS** y sin abreviaturas para facilitar las búsquedas y que quede uniforme en los documentos.

---

### Campo: NOMBRE FANTASÍA

- **Qué es:** El nombre comercial o de marca con el que se conoce al cliente en el mercado (puede diferir de la razón social).
  - Ejemplo: Razón social = `Martínez Hermanos S.A.`, Nombre fantasía = `El Rincón del Celular`
- **¿Es obligatorio?** No. Solo completarlo si es relevante para identificar al cliente.
- **Para qué sirve:** Aparece en algunas vistas de búsqueda y reportes internos como nombre alternativo.

---

### Campo: DOMICILIO

- **Qué es:** La dirección fiscal o de facturación del cliente (calle y número).
- **Ejemplo:** `San Martín 1234`
- **¿Es obligatorio?** No técnicamente, pero se recomienda completarlo.

> ⚠️ Este domicilio es el que figura en los comprobantes fiscales (facturas). Si el cliente tiene una dirección de entrega diferente, completá la sección **Datos de Entrega** más abajo.

---

### Campo: LOCALIDAD

- **Qué es:** La ciudad o localidad del domicilio fiscal.
- **Ejemplo:** `Buenos Aires`, `Rosario`, `Córdoba`

---

### Campo: C. POSTAL (Código Postal)

- **Qué es:** El código postal del domicilio fiscal.
- **Ejemplo:** `1425` o `C1425ACA`

---

### Campo: PAÍS

- **Qué es:** El país del domicilio fiscal del cliente.
- **Por defecto:** Argentina (AR). Cambiarlo solo para clientes del exterior.
- **Importante:** Al cambiar el país, el sistema actualiza las provincias disponibles en el campo siguiente.

---

### Campo: PROVINCIA

- **Qué es:** La provincia o estado del domicilio fiscal.
- **Selección:** Se elige de una lista desplegable. Las opciones se filtran automáticamente según el país seleccionado.
- **Para Argentina:** Seleccioná la provincia correspondiente (Buenos Aires, Córdoba, Santa Fe, etc.)

---

### Campo: E-MAIL

- **Qué es:** Dirección de correo electrónico del cliente.
- **Formato válido:** `nombre@dominio.com`
- **Para qué sirve:** El sistema puede enviar facturas, remitos y notificaciones automáticas al correo del cliente.

---

### Campo: TELÉFONO

- **Qué es:** Número de teléfono de contacto del cliente.
- **Recomendación:** Ingresá el código de área y el número sin espacios ni guiones.
- **Ejemplo:** `1155551234` o `01155551234`

---

### Campo: TELEFÓNICA

- **Qué es:** La operadora de telefonía (prestataria) asociada al cliente.
- **Opciones:** Claro, Movistar, Personal, Telecom, etc. (según las operadoras configuradas en el sistema)
- **Para qué sirve:** En empresas distribuidoras de telefonía, este dato vincula al cliente con la operadora para la que se realizó la activación o el servicio.
- **¿Es obligatorio?** Solo en empresas con módulo de telefonía habilitado.

---

### Campo: CONTACTO

- **Qué es:** Nombre de la persona de contacto dentro de la empresa cliente (útil para clientes corporativos o distribuidores).
- **Ejemplo:** `María López (Administración)` o `Juan (Compras)`
- **¿Es obligatorio?** No.

---

### Campo: RUBRO

- **Qué es:** La categoría o rubro comercial al que pertenece el cliente.
- **Ejemplo:** Distribuidora, Minorista, Mayorista, Franquiciado, etc.
- **Para qué sirve:** Permite segmentar la cartera de clientes y aplicar condiciones comerciales diferenciadas.
- **¿Es obligatorio?** Depende de la configuración de la empresa.

---

## Sección 2 — Datos para Factura

Esta sección define las condiciones fiscales y comerciales que se aplican automáticamente al momento de emitir un comprobante al cliente.

> ⚠️ **Es muy importante completar correctamente esta sección.** Un error en la condición de IVA puede generar facturas incorrectas desde el punto de vista impositivo.

---

### Campo: VENTA CTA CTE (Venta en Cuenta Corriente)

- **Qué es:** Indica si este cliente puede comprar a crédito (en cuenta corriente), es decir, sin pagar en el momento.
- **Opciones:**
  - **NO:** El cliente paga al contado en cada operación. Es la opción predeterminada para clientes minoristas.
  - **SÍ:** El cliente es mayorista o tiene habilitada una línea de crédito. Sus compras se registran en cuenta corriente y paga según las condiciones pactadas.
- **Consecuencias de seleccionar SÍ:** Al facturarle a este cliente, el sistema permite registrar la venta sin cobro inmediato, generando un saldo en su cuenta corriente.

> 💡 **Importante:** Para activar "SÍ" en este campo, generalmente se requiere que el usuario tenga los permisos correspondientes. Consultá con tu supervisor si no podés modificarlo.

---

### Campo: LISTA DE PRECIO

- **Qué es:** La lista de precios que se aplica automáticamente a este cliente cuando se realiza una venta.
- **Selección:** Se elige de las listas de precios configuradas en el sistema (Lista 1, Lista 2, Lista Mayorista, etc.)
- **Por defecto:** Lista 1 (lista general minorista).
- **Para qué sirve:** Permite asignarle a un cliente mayorista o de canal una lista con precios especiales sin tener que modificarlos manualmente en cada venta.

> 💡 **Consejo:** Si el cliente tiene un precio especial de manera permanente, asignale la lista que corresponda. Si el descuento es eventual, hacelo directamente en la venta.

---

### Campo: IVA (Condición frente al IVA)

- **Qué es:** La situación fiscal del cliente ante el Impuesto al Valor Agregado (IVA).
- **Opciones más comunes:**
  | Opción | A quién corresponde |
  |---|---|
  | **Consumidor Final** | Personas físicas que no están inscriptas en AFIP como responsables. Es el cliente de a pie. |
  | **Responsable Inscripto** | Empresas o personas físicas inscriptas en IVA. Reciben Factura A. |
  | **Exento** | Entidades exentas del IVA (hospitales, escuelas, etc.) |
  | **Monotributista** | Personas inscriptas en el régimen simplificado. |
  | **No Responsable** | No están obligados a inscribirse en IVA. |
- **Es obligatorio:** ✅ Sí. Este dato determina el **tipo de factura** que se emite:
  - Responsable Inscripto → **Factura A**
  - Consumidor Final / Monotributista / Exento → **Factura B** (o C si el emisor es monotributista)

> ⚠️ **Error frecuente:** Seleccionar "Consumidor Final" para una empresa que es Responsable Inscripto. Esto hace que se emita Factura B en lugar de Factura A, lo cual genera un problema impositivo para ambas partes.

---

### Campo: IIBB (Condición IIBB)

- **Qué es:** La situación del cliente frente al Impuesto a los Ingresos Brutos (IIBB).
- **Solo aplica para Argentina.**
- **Opciones más comunes:** Exento, Convenio Multilateral, Local (por provincia).
- **Para qué sirve:** En algunos casos, permite calcular automáticamente las **percepciones de IIBB** que deben ser retenidas al cliente en la factura.

---

### Campo: IIBB N° (Número de IIBB)

- **Qué es:** El número de inscripción en Ingresos Brutos del cliente.
- **Solo completar si el cliente está inscripto en IIBB y lo requiere.**
- **Ejemplo:** `901-123456-7`

---

### Campo: FACTURA EN (Moneda)

- **Qué es:** La moneda en que se emiten las facturas para este cliente.
- **Opciones:** Pesos Argentinos (ARS), Dólares (USD), u otras divisas configuradas.
- **Por defecto:** Pesos Argentinos.
- **Cuándo cambiarlo:** Solo para clientes del exterior o cuando por acuerdo comercial específico las facturas se emiten en moneda extranjera.

---

### Campo: VENDEDOR (o ADMINISTRADOR)

- **Qué es:** El vendedor de la empresa que tiene asignado este cliente en su cartera.
- **Para qué sirve:**
  - Aparece predeterminado al facturar a este cliente.
  - Se utiliza para el cálculo de comisiones.
  - Permite segmentar reportes de ventas por vendedor.
- **¿Es obligatorio?** Recomendable pero no siempre obligatorio. Consultá con tu supervisor.

---

## Sección 3 — Datos de Entrega

Esta sección define a dónde se envían los productos cuando se hace un despacho o remito para este cliente.

> 💡 **Importante:** Si el domicilio de entrega es **el mismo** que el domicilio fiscal (sección 1), podés dejar esta sección vacía. El sistema usará automáticamente la dirección del cliente.
> Si son **diferentes**, completá esta sección con la dirección donde realmente se entrega la mercadería.

---

### Campo: DOMICILIO (de entrega)

- **Qué es:** La dirección física donde se entregan los productos (calle y número).
- **Puede ser diferente** al domicilio fiscal (por ejemplo: un depósito, una sucursal, un local comercial).

---

### Campo: BARRIO

- **Qué es:** El barrio o zona específica dentro de la localidad de entrega.
- **Útil para:** Empresas de delivery o logística que organizan los envíos por zonas.

---

### Campo: LOCALIDAD (de entrega)

- **Qué es:** Ciudad o localidad donde se realiza la entrega.

---

### Campo: C. POSTAL (de entrega)

- **Qué es:** Código postal del domicilio de entrega.

---

### Campo: PAÍS y PROVINCIA (de entrega)

- **Misma lógica que los campos de domicilio fiscal.** Seleccionar país y provincia de entrega.

---

### Campo: LUGAR DE PAGO

- **Qué es:** Define quién paga el flete del envío.
- **Opciones:**
  - **EN ORIGEN:** El flete lo paga el remitente (la empresa que envía). El costo del envío corre por cuenta de tu empresa.
  - **EN DESTINO:** El flete lo paga el destinatario (el cliente). El cliente paga el envío al recibirlo.
- **Por defecto:** EN ORIGEN.

---

### Campo: VALOR DECLARADO

- **Qué es:** El porcentaje del valor de la mercadería que se declara ante la transportista para el seguro del envío.
- **Se expresa en porcentaje (%).**
- **Ejemplo:** Si el pedido vale $100.000 y el valor declarado es `80%`, se declara un valor de $80.000 a la transportista.
- **Para qué sirve:** Determina el valor asegurado en caso de pérdida o rotura durante el transporte.
- **Dejar en 0:** Si no se requiere seguro de envío para este cliente.

---

### Campo: TRANSPORTE

- **Qué es:** La empresa de transporte o logística predeterminada para los envíos a este cliente.
- **Selección:** Lista de transportistas configurados en el sistema (Envíopack, OCA, Correo Argentino, transporte propio, etc.)
- **Para qué sirve:** Al armar un envío para este cliente, el sistema sugiere automáticamente el transporte asignado.

---

### Campo: CON TURNO

- **Qué es:** Indica si el cliente requiere un turno previo para recibir mercadería.
- **Opciones:** SÍ / NO
- **Cuándo usar SÍ:** Para clientes (generalmente empresas grandes o supermercados) que no aceptan entregas sin turno acordado previamente. Esto sirve como recordatorio para el equipo de logística.

---

### Campo: OBSERVACIONES (de entrega)

- **Qué es:** Un campo libre de texto para anotar cualquier indicación especial sobre la entrega.
- **Ejemplos de uso:**
  - `Entregar solo de lunes a viernes de 9 a 17 hs`
  - `Tocar timbre piso 3`
  - `Ingresar por puerta lateral - preguntar por Juan`
  - `No entregar sin nota de pedido firmada`
- **Estas observaciones** aparecen en los remitos y documentos de despacho para que el equipo de logística las tenga en cuenta.

---

## Paso a paso: Cómo dar de alta un cliente nuevo

1. Hacé clic en el botón **Nuevo** en la barra de herramientas.
2. El formulario se limpia y queda listo para ingresar datos.
3. **Completá el CUIT o DNI** primero. El sistema verifica si ya existe un cliente con ese número.
   - Si existe, te avisa con un mensaje mostrando el nombre del cliente duplicado. Decidí si continuar o buscar el existente.
4. **Completá el nombre** del cliente (Razón Social o Apellido y Nombre).
5. Completá los datos de domicilio, contacto y ubicación.
6. **En la sección "Datos para Factura"**, seleccioná:
   - Condición de IVA (Consumidor Final, Responsable Inscripto, etc.)
   - Lista de Precios
   - Vendedor asignado
7. Si el domicilio de entrega es diferente al domicilio fiscal, completá la sección **"Datos de Entrega"**.
8. Hacé clic en **Guardar**.
9. El sistema asigna un código automático al nuevo cliente y queda registrado.

---

## Paso a paso: Cómo buscar y modificar un cliente existente

1. En el **buscador**, escribí el nombre, razón social o CUIT del cliente.
2. Hacé clic en **Buscar** o presioná **Enter**.
3. En la lista de resultados, hacé clic sobre el cliente que querés modificar.
4. Los datos del cliente aparecen automáticamente en el formulario.
5. Modificá los campos que necesitás cambiar.
6. Hacé clic en **Guardar** para confirmar los cambios.

---

## Paso a paso: Cómo dar de baja (desactivar) un cliente

1. Buscá el cliente siguiendo el paso a paso anterior.
2. En el campo **ACTIVO / INACTIVO**, seleccioná **INACTIVO**.
3. Hacé clic en **Guardar**.
4. El cliente queda desactivado y ya no aparecerá en las búsquedas al facturar.

> 💡 El cliente puede reactivarse en cualquier momento volviendo a seleccionar ACTIVO.

---

## Paso a paso: Cómo eliminar un cliente

1. Buscá el cliente y seleccionalo.
2. Hacé clic en el botón **Eliminar**.
3. El sistema verifica si el cliente tiene comprobantes (facturas, remitos, etc.) registrados.
   - **Si NO tiene comprobantes:** Se elimina definitivamente y no puede recuperarse.
   - **Si SÍ tiene comprobantes:** El sistema no permite eliminarlo y muestra un mensaje de error. En este caso, usá la opción de desactivar (INACTIVO).

> ⚠️ **La eliminación es permanente e irreversible.** Antes de eliminar, asegurate de que realmente no tiene historial en el sistema.

---

## Errores frecuentes y cómo resolverlos

| Mensaje o Situación | Causa | Solución |
|---|---|---|
| "Datos ya ingresados para: [Nombre]" | El CUIT/DNI ya existe en otro cliente | Buscá el cliente existente en lugar de crear uno nuevo. Si el cliente ya existe pero con datos incorrectos, modificalo. |
| "Se esperaba un Nro. de Documento" | El campo CUIT/DNI está vacío | Ingresá el CUIT o DNI del cliente. |
| "Documento mal ingresado" | El CUIT/DNI no tiene la cantidad correcta de dígitos | Para Argentina: DNI = 7 u 8 dígitos / CUIT = 11 dígitos (sin guiones). |
| No se puede eliminar el cliente | Tiene facturas, remitos u otros comprobantes asociados | Desactivá el cliente (INACTIVO) en lugar de eliminarlo. |
| La factura salió como tipo B en lugar de A | La condición de IVA está mal cargada | Verificá la condición de IVA con el botón "Ver en AFIP" y corregí el campo IVA del cliente. |
| El vendedor no aparece en la lista | El vendedor está inactivo o no está configurado | Contactá al administrador del sistema para verificar el alta del vendedor. |

---

## Preguntas frecuentes

**¿Puedo cargar clientes del exterior?**
Sí. Seleccioná el país correspondiente en el campo PAÍS y el sistema adapta los campos de provincia y el formato del documento fiscal.

**¿Qué pasa si el cliente no tiene CUIT?**
Para clientes argentinos, el CUIT o DNI es obligatorio. Si el cliente es una persona física sin CUIT, usá el DNI (8 dígitos). Si no tiene ninguno, consultá con el área contable de tu empresa.

**¿Puedo tener dos clientes con el mismo nombre pero diferente CUIT?**
Sí. El sistema solo verifica duplicados por CUIT/DNI, no por nombre. Sin embargo, se recomienda evitar nombres muy similares para no confundirse al buscar.

**¿Puedo cambiar la lista de precios de un cliente en cualquier momento?**
Sí. Simplemente buscá el cliente, modificá el campo "Lista de Precio" y guardá. A partir de ese momento, las nuevas ventas usarán la nueva lista.

**¿Dónde veo el historial de compras de un cliente?**
Depende del tipo de cliente:
- Si es un cliente **Mayorista** (con venta en cuenta corriente habilitada): buscalo en la pantalla **Cuenta Corriente de Clientes** (Módulo 2 → Opción 2.03), donde podés ver todos sus comprobantes y el saldo.
- Si es un cliente **minorista**: sus compras se consultan desde el informe **Ventas por Cliente** (Módulo Informes).

**¿Qué es el límite de crédito y cómo se configura?**
Es el monto máximo de deuda que puede tener un cliente en cuenta corriente. Se configura en la pantalla **Límites de Crédito** (Módulo 2 → Opción 2.02).

---

## Campos de referencia rápida

| Campo | ¿Obligatorio? | Sección |
|---|---|---|
| CUIT / DNI | ✅ Sí | Datos Generales |
| CLIENTE (Nombre) | ✅ Sí | Datos Generales |
| IVA | ✅ Sí (para facturar) | Datos para Factura |
| Nombre Fantasía | No | Datos Generales |
| Nacimiento / Sexo | No | Datos Generales |
| Domicilio | No (recomendado) | Datos Generales |
| Localidad | No (recomendado) | Datos Generales |
| C. Postal | No | Datos Generales |
| País / Provincia | No (recomendado) | Datos Generales |
| E-mail | No (recomendado) | Datos Generales |
| Teléfono | No (recomendado) | Datos Generales |
| Telefónica | Solo telco | Datos Generales |
| Contacto | No | Datos Generales |
| Rubro | Depende | Datos Generales |
| Venta Cta Cte | ✅ Revisar | Datos para Factura |
| Lista de Precio | ✅ Sí | Datos para Factura |
| IIBB | Solo si aplica | Datos para Factura |
| Moneda | ✅ Sí | Datos para Factura |
| Vendedor | Recomendado | Datos para Factura |
| Domicilio de entrega | Solo si difiere | Datos de Entrega |
| Transporte | Recomendado | Datos de Entrega |

---

## Resumen de los puntos clave

- El **CUIT/DNI** y el **Nombre** son los únicos campos obligatorios para guardar.
- La **condición de IVA** es crítica: determina el tipo de comprobante que se emite.
- Si tenés dudas del CUIT de un cliente, usá el botón **"Ver en AFIP"** para verificarlo.
- Antes de cargar un cliente nuevo, el sistema **detecta si ya existe** el mismo CUIT/DNI.
- Un cliente **con facturas no puede eliminarse**: usá la opción INACTIVO.
- El **domicilio de entrega** puede ser diferente al domicilio fiscal y se usa en los remitos.
- El **transporte predeterminado** agiliza el proceso de despacho al no tener que seleccionarlo en cada envío.

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Febrero 2026*
