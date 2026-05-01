# 3.67 POSICIÓN FISCAL FC
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Posicion Fiscal FC

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Posición Fiscal FC** permite configurar qué prefijo fiscal (posición) se asigna a cada tipo de comprobante en cada punto de venta o zona. También indica si el comprobante utiliza el servicio web de AFIP (WS AFIP) para la emisión electrónica. Desde aquí podés:

- Asignar la posición fiscal de cada tipo de comprobante por PDV o por zona
- Indicar si el comprobante se emite mediante el web service de AFIP
- Consultar y eliminar configuraciones existentes

---

<img src="imagenes/pantalla_posicion_fiscal_fc.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Posicion Fiscal FC**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de configuración y una grilla a la derecha con los registros existentes.

---

## Formulario de configuración

| Campo | Descripción |
|---|---|
| **EMPRESA** | Empresa a la que pertenece la configuración. Al seleccionarla, se actualiza la lista de PDV. |
| **PDV** | Punto de venta al que se aplica la configuración. Solo muestra PDV con depósito de artículos y sin factura por zona. |
| **ZONA** | Zona para la que se configura la posición fiscal (modo alternativo al PDV). |
| **TIPO FC** | Tipo de comprobante: TK, IA, EA, EB, EC, EE, A, PA, B, PB, IRM, RM, R, M, IV, RC |
| **PREFIJO** | Prefijo de 4 caracteres que identifica la posición fiscal del comprobante |
| **WS AFIP** | Indica si el comprobante se emite a través del web service de AFIP (SI / NO) |

---

## Grilla de configuraciones

Muestra las configuraciones ya guardadas. El contenido varía según el modo de búsqueda:

**Modo PDV:**

| Columna | Descripción |
|---|---|
| Factura Tipo | Tipo de comprobante |
| Posición Fiscal | Prefijo fiscal asignado |
| Usa WS_Afip | Si usa el web service de AFIP |
| Punto de Venta | PDV al que aplica |
| Empresa | Empresa asociada |
| Detalle | Datos del comprobante |

**Modo Zona:**

| Columna | Descripción |
|---|---|
| Factura Tipo | Tipo de comprobante |
| Posición Fiscal | Prefijo fiscal asignado |
| Usa WS_Afip | Si usa el web service de AFIP |
| Zona Posición | Zona a la que aplica |
| Empresa | Empresa asociada |
| Detalle | Datos del comprobante |

**Acciones disponibles:**
- **Borrar:** Elimina la configuración seleccionada

---

## Notas importantes

- La configuración por **PDV** aplica cuando el punto de venta no factura por zona.
- La configuración por **Zona** aplica cuando el PDV tiene activada la opción "Factura por Zona".
- El prefijo (posición fiscal) determina qué categoría impositiva se usa al emitir el comprobante.
- Si WS AFIP está en **SI**, el sistema intentará autorizar el comprobante online al momento de emitirlo.
