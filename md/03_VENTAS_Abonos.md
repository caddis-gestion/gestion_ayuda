# 3.36 ABONOS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Abonos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Abonos** permite registrar y gestionar la facturación mensual de los abonos del sistema a los agentes (clientes del servicio). Desde aquí podés:

- Seleccionar el mes de liquidación y el agente a facturar
- Ingresar los importes de cada módulo contratado (gestión, marketplaces, servicios, conexiones, etc.)
- Facturar el abono mensual del agente
- Imprimir o enviar por mail las facturas de abono
- Consultar el historial de abonos facturados

---

<img src="imagenes/pantalla_abonos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Abonos**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de carga del abono y un panel derecho con la grilla de abonos del mes seleccionado.

---

## Botones de acción principales

| Botón | Descripción |
|---|---|
| **Detalles** | Ver el detalle del abono seleccionado |
| **Facturar** | Genera la factura del abono para el agente |
| **Imprimir** | Imprime las facturas de abono |
| **Mails** | Envía las facturas por correo electrónico |
| **Fc Inicio** | Imprime la factura de inicio del período |
| **Mail Inicio** | Envía la factura de inicio por mail |
| **Aumentos** | Aplica aumentos de precios a los módulos |

---

## Panel izquierdo — Formulario de abono

### Filtros principales

| Campo | Descripción |
|---|---|
| **MES** | Mes de liquidación a procesar |
| **EMITE** | Persona que emite la factura (SEBASTIAN, EUGENIA, TOMAS, Z) |
| **PRESTATARIA** | Módulo de servicio: CLARO, MOVISTAR o FACTURACIÓN |
| **AGENTE** | Agente al que se le carga el abono. Al seleccionarlo se cargan sus datos. |

### Sección CELULARES (si aplica)

| Campo | Descripción |
|---|---|
| **CELULARES** | Importe del módulo de celulares |
| **ALTAS** | Cantidad de altas de celulares |
| **ROBOT** | Importe del módulo robot |
| **ALTAS** | Cantidad de altas de robot |

### Sección GESTION

| Campo | Descripción |
|---|---|
| **GESTION** | Importe del módulo de gestión |
| **FACTURAS** | Cantidad de facturas emitidas |

### Sección MARKETPLACES

Permite ingresar el importe y cantidad de ventas para cada plataforma de marketplace contratada:

| Plataforma | Campos |
|---|---|
| **M.LIBRE** | Importe + Ventas |
| **M.LIBRE.GS** | Importe + Ventas |
| **TIENDA NUBE** | Importe + Ventas |
| **E3ECOMMERCE** | Importe + Ventas |
| **FOODIE, MEGATONE, WOOCOMMERCE, SKULLCANDY, SHOPIFY, FRAVEGA, BNA, BAPRO, BBVA, ICBC, INFOBAE, GALICIA, MACRO, ROTAX** | Importe + Ventas (según módulos contratados) |

### Sección SERVICIOS

| Campo | Descripción |
|---|---|
| **SEGUROS\|TARJ** | Importe de seguros/tarjetas + cantidad de ventas |
| **REPARACIONES** | Importe de reparaciones + cantidad |
| **LOGISTICA** | Importe de logística + cantidad |

### Sección CONEXIONES

| Campo | Descripción |
|---|---|
| **TANGO** | Importe módulo Tango |
| **IRSA** | Importe módulo IRSA + cantidad |
| **WEB SERVICE** | Importe módulo Web Service |

### Sección CAPACITACIONES

| Campo | Descripción |
|---|---|
| **CAPACITACIONES** | Importe de capacitaciones |

### Sección TOTAL

| Campo | Descripción |
|---|---|
| **DTO MODULOS** | Descuento sobre módulos (en %) |
| **DTO BASES** | Descuento sobre bases (en %) |
| **PREMIUM** | Importe del servicio premium |
| **SIZE** | Tamaño de backup |
| **TOTAL** | Total calculado del abono |

### Sección USOS (informativa)

Muestra datos de uso del agente (sólo lectura):

| Campo | Descripción |
|---|---|
| **LOCALES** | Cantidad de puntos de venta activos |
| **FC CREDITO** | Indica si usa facturación de crédito (SI/NO) |
| **FC EXPORTACION** | Indica si usa facturación de exportación (SI/NO) |
| **OC PROVEEDORES** | Indica si usa órdenes de compra a proveedores (SI/NO) |
| **PERCEPCION IIBB** | Indica si actúa como agente de percepción de IIBB (SI/NO) |

---

## Panel derecho — Grilla de abonos del mes

Muestra todos los abonos registrados para el mes seleccionado:

| Columna | Descripción |
|---|---|
| FC | Persona que emite (S/E/T/Z) |
| Módulo | Módulo de servicio (CLARO/MOVI/GESTION) |
| Agente | Nombre del agente |
| Total | Total del abono |
| Premium, Celulares, Robot, Gestion... | Importe de cada módulo |
| Dto Modulos / Dto Bases | Descuentos aplicados |

**Acciones disponibles:**
- **Borrar:** Elimina el abono del mes
- **Detalle:** Ver detalle del abono
- **Imprimir:** Imprime el abono

---

## Notas importantes

- Los módulos disponibles dependen de lo contratado por cada agente.
- El botón **Facturar** genera la factura formal una vez completados todos los datos del abono.
- Los campos de la sección **USOS** son informativos y se obtienen automáticamente del sistema.
