# 12.01 NUEVA REPARACIÓN
### Módulo 12 — Reparaciones

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Reparaciones → Nueva Reparacion

---

## ¿Para qué sirve esta pantalla?

**Nueva Reparación** permite registrar el ingreso de un equipo al servicio técnico. Al crear la orden, el sistema asigna un número de orden, registra los datos del cliente, el equipo entregado, las condiciones de recepción, el presupuesto y genera automáticamente un PDF con el código de la reparación.

---

<img src="imagenes/pantalla_nueva_reparacion.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Reparaciones → Nueva Reparacion**

---

## Configuración previa

Antes de poder operar con reparaciones es necesario configurar los siguientes elementos:

| Elemento | Dónde se configura | Qué hacer |
|---|---|---|
| **Habilitar reparaciones en el PDV** | Administración → Puntos de Venta | Activar el campo **REPARACIONES = SI** para los PDV que reciben equipos |
| **Artículos de reparación** | ABM → Artículos | Crear los repuestos/servicios con **TIPO = REPARACIONES**, **SERVICIO = SI** y **SIN CONTROL DE STOCK** |
| **Condiciones de recepción (checkboxes)** | Reparaciones → Checkboxs | Definir las casillas que aparecen al ingresar el equipo (ej. CON BATERIA, PANTALLA ROTA) |
| **Texto de condiciones de reparación y entrega** | Reparaciones → Condiciones | Editar el texto legal/operativo que figura en el PDF de la orden |
| **Modelos de equipos** | ABM → Equipos Modelos | Crear los modelos si el equipo no existe aún en el sistema |

---

## Campos del formulario

### Datos generales

| Campo | Descripción |
|---|---|
| **ORDEN ANT** | Número de una orden anterior relacionada. Opcional. Usá el botón **Buscar** para buscarla. |
| **PDV** | Punto de venta donde se recibe el equipo. Solo se muestran los PDV con REPARACIONES = SI. |
| **VENDEDOR** | Vendedor que recibe el equipo. Se filtra según el PDV seleccionado. |
| **CLIENTE** | Cliente que entrega el equipo. Se puede buscar entre los existentes o crear uno nuevo en el momento. |
| **EQUIPO** | Modelo del equipo a reparar. Si no existe, se puede crear desde **Equipos Modelos**. |
| **IMEI** | Número de IMEI del equipo (si se dispone del dato). |

> El estado inicial se asigna automáticamente como **TOMADO** al guardar la orden.

### Sección CONDICIONES

Casillas de verificación que describen el estado físico del equipo al momento de la recepción (ej. CON BATERIA, PANTALLA ROTA, NO FUNCIONA CAM, NO FUNCIONA ALTAVOZ). Las opciones disponibles se configuran desde **Reparaciones → Checkboxs**.

### Sección OBSERVACIONES

Texto libre para registrar detalles adicionales sobre el equipo o la falla reportada por el cliente.

### Sección SEÑA

| Campo | Descripción |
|---|---|
| **IMPORTE** | Monto de seña cobrado al momento de la recepción. Dejar en 0 si no se cobra seña. |

> La seña **no se cobra en esta pantalla**: solo se registra el importe. Para emitir el recibo, ir a [**Facturación**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf), usar el botón **Reparaciones** (muestra las señas no facturadas) y emitir un comprobante tipo **RC** (recibo). Al final del día, las señas se rinden desde **Cierre de Caja Diario**.

### Sección PRESUPUESTO

Permite cargar los ítems del presupuesto de reparación. Los artículos disponibles son los de **TIPO = REPARACIONES** cargados en el sistema.

| Campo / Botón | Descripción |
|---|---|
| **CÓDIGO** | SKU del repuesto o servicio. Ingresá el código o usá la **lupa** para buscarlo. |
| **IMPORTE** | Precio unitario del ítem (se completa automáticamente al seleccionar el artículo). |
| **CANTIDAD** | Cantidad de unidades. |
| **Ingresar** | Agrega el ítem a la grilla del presupuesto. |

### Grilla del presupuesto

| Columna | Descripción |
|---|---|
| Artículo | Nombre del repuesto o servicio |
| Cant. | Cantidad |
| Importe | Precio unitario con IVA |
| Total | Importe × Cantidad |
| Borrar | Elimina el ítem del presupuesto |

---

## Paso a paso — Registrar el ingreso de un equipo

1. Seleccioná el **PDV** y el **VENDEDOR**
2. Buscá o ingresá el **CLIENTE**
3. Seleccioná el **EQUIPO** (modelo); si no existe, crealo desde Equipos Modelos
4. Ingresá el **IMEI** si se dispone del dato
5. Marcá las **CONDICIONES** de recepción que correspondan
6. Agregá **OBSERVACIONES** sobre la falla reportada
7. Si cobrás seña, ingresá el importe en la sección **SEÑA**
8. Cargá los ítems del **PRESUPUESTO** usando la lupa para buscar los artículos de reparación
9. Guardá la orden — el sistema asigna el número de orden y emite automáticamente un **PDF** con el código de la reparación

---

## Circuito completo de reparaciones

| Paso | Pantalla | Acción |
|---|---|---|
| **1** | **Nueva Reparación** | **Ingreso del equipo, condiciones, presupuesto y seña** |
| 2 | [**Modificar Reparación**](https://ayuda.caddis.com.ar/instructivos/12_REP_Modificar_Reparacion.pdf) | Actualización del presupuesto y datos durante la reparación |
| 3 | [**Estados**](https://ayuda.caddis.com.ar/instructivos/12_REP_Estados.pdf) | Cambio de estado (ej. EN REPARACION → REPARACION TERMINADA) |
| 4 | [**Facturación**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Facturacion.pdf) | Cobro de la reparación terminada (tipo REPA) |
| 5 | [**Entrega a Cliente**](https://ayuda.caddis.com.ar/instructivos/12_REP_Entrega_Cliente.pdf) | Registro de la entrega física del equipo |

---

## Notas importantes

- Solo aparecen en **PDV** los puntos de venta habilitados con **REPARACIONES = SI**.
- Los artículos del presupuesto deben existir en el sistema con **TIPO = REPARACIONES** y **SERVICIO = SI**.
- El texto de las condiciones de reparación y entrega que figura en el PDF se configura desde **Reparaciones → Condiciones**.
- Para ver el historial completo de todas las reparaciones usá **Reportes → Informes → Reparaciones** (filtrable por estado y depósito).
