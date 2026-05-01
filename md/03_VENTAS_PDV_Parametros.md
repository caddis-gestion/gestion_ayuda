# 3.65 PDV PARÁMETROS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Abril 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → PDV Parametros

---

## ¿Para qué sirve esta pantalla?

La pantalla de **PDV Parámetros** permite configurar los parámetros de funcionamiento de cada punto de venta. Desde aquí podés:

- Asignar la empresa facturante y la empresa de "cuenta y orden" a cada PDV
- Configurar la cantidad de cajas disponibles
- Asignar la lista de precios predeterminada del PDV
- Definir si se muestra la lista de precios al cliente
- Configurar si el PDV usa facturación por zona
- Elegir el formato de impresión de facturas (A4 o ticket)

> ⚠️ Esta pantalla es de uso administrativo. Modificar los parámetros incorrectamente puede afectar el funcionamiento de la facturación.

---

<img src="imagenes/pantalla_pdv_parametros.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → PDV Parametros**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de parámetros y un panel derecho con la grilla de todos los PDV configurados.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta a configurar (sólo muestra PDV con artículos habilitados) |
| **EMPRESA** | Empresa que factura desde este PDV |
| **FC CTA y ORDEN** | Empresa de "cuenta y orden" (para facturas emitidas en nombre de otra empresa). Sólo aplica en entornos multi-empresa con ese modelo de facturación. |
| **CAJAS** | Cantidad de cajas (terminales de venta) habilitadas en este PDV |
| **LISTA** | Lista de precios predeterminada para las ventas en este PDV |
| **LISTA CLIENTE** | **MOSTRAR**: muestra el precio de lista al cliente en pantalla. **NO MOSTRAR**: oculta la lista. |
| **FC ZONA** | **SI**: el PDV factura por zona (usa talonarios de zona). **NO**: facturación normal. |
| **FACTURA** | Formato de impresión del comprobante: **A4** para impresoras comunes (hoja completa 210×297mm) o **Ticket** para impresoras tickeadoras térmicas de 80mm. Determina el diseño del comprobante generado. |

---

## Panel derecho — Grilla de PDV

Muestra todos los PDV con su configuración actual:

| Columna | Descripción |
|---|---|
| PDV | Nombre del punto de venta |
| Cajas | Cantidad de cajas |
| Lista Precio | Lista de precios asignada |
| Mostrar Lista Cliente | SI o NO |
| ... | Otros parámetros configurados |

---

## Notas importantes

- Cada PDV debe tener asignada una **EMPRESA** para poder facturar. Sin empresa asignada, la facturación no funciona.
- El parámetro **FC ZONA** afecta qué talonario de comprobantes se usa: si es por zona, el contador de facturas es por zona geográfica y no por PDV.
- La cantidad de **CAJAS** determina cuántas sesiones de facturación pueden estar abiertas simultáneamente en el PDV.

### Formato de impresión de comprobantes

El campo **FACTURA** define cómo se imprime cada comprobante (facturas, remitos, notas de crédito) generado desde ese PDV:

| Formato | Tipo de impresora | Descripción |
|---|---|---|
| **A4** | Impresora común (láser, chorro de tinta) | Genera el comprobante en hoja completa A4 (210×297mm). Es el formato habitual para locales que imprimen en papel normal. |
| **Ticket** | Impresora tickeadora térmica (80mm) | Genera el comprobante en formato angosto, optimizado para rollo de papel térmico de 80mm. Es el formato usado en cajas rápidas con impresoras de tickets. |

> Cada PDV puede tener su propio formato configurado de forma independiente. Un comercio puede tener, por ejemplo, un PDV principal con impresora A4 y una caja rápida con impresora tickeadora, cada uno configurado con su formato correspondiente.
