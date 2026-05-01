# 5.37 EQUIPOS — INGRESOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Equipos Ingresos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Equipos Ingresos** permite registrar el ingreso de equipos (con NSE/IMEI) provenientes de proveedores. A diferencia de los artículos sin serie, los equipos se ingresan de a uno por número de serie. Desde aquí podés:

- Registrar un remito de ingreso de equipos con todos los datos del proveedor
- Ingresar equipos de forma individual, múltiple o por rango de NSE
- Asociar el ingreso a una Orden de Compra
- Registrar observaciones

---

<img src="imagenes/pantalla_equipos_ingresos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Equipos Ingresos**

---

## Formulario

| Campo | Descripción |
|---|---|
| **FECHA** | Fecha del ingreso. El número de remito interno se asigna automáticamente (solo lectura) |

**Datos del proveedor:**

| Campo | Descripción |
|---|---|
| **PEDIDO** | Número de pedido del proveedor |
| **REMITO** | Número de remito del proveedor |
| **FC.NUMERO** | Número de factura del proveedor |
| **FC.FECHA** | Fecha de la factura del proveedor |
| **DOC.ASOC** | Documento asociado (específico de operadoras) |

**Datos del depósito:**

| Campo | Descripción |
|---|---|
| **ALMACEN** | Almacén de recepción |
| **ORIGEN** | Proveedor de origen |
| **DESTINO** | PDV destino donde se registra el ingreso |

**Datos del equipo:**

| Campo | Descripción |
|---|---|
| **O. DE COMPRA** | Orden de compra a la que aplica este ingreso (en modo gestión) |
| **EQ.TIPO** | Tipo de equipo (en modo prestataria) |
| **DESPACHO** | Número de despacho de importación |
| **EQUIPO** | Modelo/código del equipo. Botón **Agregar** para sumar uno a la vez |
| **OBSERVACIONES** | Notas adicionales |

**Acciones de carga masiva:**
- **Multiple:** Ingresa múltiples NSE de una vez
- **Rango:** Ingresa un rango continuo de NSE

---

## Panel derecho — Grilla de equipos ingresados

| Columna | Descripción |
|---|---|
| Codigo | Código del equipo |
| Equipo | Marca y modelo |
| Cantidad | Unidades ingresadas |
| OC | Orden de compra asociada |
| Error | Cantidad con error de ingreso |

**Acciones:**
- **Borrar:** Elimina el equipo del remito en curso
- **Detalle:** Muestra el detalle de los NSE del equipo

---

## Notas importantes

- Cada equipo ingresado queda identificado individualmente por su NSE/IMEI.
- Al asociar una Orden de Compra, el sistema descuenta automáticamente las cantidades de la OC pendiente.
- El modo de ingreso (gestión vs. prestataria) puede variar según la configuración de la empresa.
