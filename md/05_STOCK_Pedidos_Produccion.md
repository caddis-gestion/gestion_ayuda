# 5.XX PEDIDOS DE PRODUCCIÓN
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Pedidos Producción

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Pedidos de Producción** permite emitir pedidos de producción a partir de una factura de venta que contiene artículos compuestos (fabricados a partir de otros). El sistema calcula automáticamente los componentes necesarios y permite asignar los envases para cada artículo. Desde aquí podés:

- Buscar una factura que contiene artículos con componentes de producción
- Ver el detalle de componentes requeridos por artículo
- Asignar envases y cantidades para cada artículo
- Emitir o reimprimir el pedido de producción

---

<img src="imagenes/pantalla_pedidos_produccion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Pedidos Producción**

---

## Formulario

| Campo | Descripción |
|---|---|
| **FACTURA** | Tipo y número de la factura de venta asociada. Botones **Buscar** (localiza la factura) y **Factura** (imprime el comprobante). |
| **FECHA** | Fecha de la factura (solo lectura) |
| **CLIENTE** | Nombre y CUIT del cliente (solo lectura) |
| **OBSERV** | Observaciones de la factura (solo lectura) |

---

## Detalle de componentes

Debajo del formulario el sistema muestra, por cada artículo compuesto de la factura:

- Nombre del artículo y cantidad total pedida
- Lista de componentes necesarios con cantidad por unidad, equivalencia (Kg/Lts) y total en kg
- Selector de **ENVASE** a utilizar para el artículo (tipo 40)
- Campo de **CANTIDAD** de envases

---

## Acciones

| Botón | Descripción |
|---|---|
| **Emitir Pedido** | Genera el pedido de producción. Aparece cuando no existe un pedido previo para la factura. |
| **Imprimir Pedido #N** | Imprime el pedido de producción ya emitido. Aparece cuando ya existe el pedido. |

---

## Notas importantes

- Esta pantalla aplica a empresas que fabrican productos compuestos (ej. alimenticia, cosmética, etc.).
- El pedido de producción detalla exactamente los materiales e insumos necesarios para cubrir la venta registrada.
- Una vez emitido el pedido, el botón cambia a **Imprimir Pedido** con el número asignado.
