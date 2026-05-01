# 3.64 MONEDAS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Monedas

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Monedas** permite administrar las monedas extranjeras disponibles en el sistema y mantener actualizado el tipo de cambio. Es relevante en entornos donde se factura o compra en divisas (dólar, euro, etc.). Desde aquí podés:

- Agregar una moneda al sistema con su alias, símbolo y cotización
- Actualizar la cotización de una moneda existente
- Eliminar monedas que ya no se usan

---

<img src="imagenes/pantalla_monedas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Monedas**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario y un panel derecho con la grilla de monedas configuradas.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **MONEDA** | Selector de moneda del catálogo general (USD, EUR, etc.) |
| **ALIAS** | Nombre descriptivo personalizado para la moneda (hasta 20 caracteres) |
| **SIMBOLO** | Símbolo de la moneda (hasta 3 caracteres, ej. U$D, EUR) |
| **COTIZACION** | Tipo de cambio actual respecto al peso (ej. si 1 dólar = 1000 pesos, ingresar 1000) |

---

## Panel derecho — Grilla de monedas

Muestra las monedas configuradas en el sistema:

| Columna | Descripción |
|---|---|
| Moneda | Nombre de la moneda |
| Simbolo | Símbolo de la moneda |
| Cotizacion | Tipo de cambio actual |

**Acciones disponibles:**
- **Modificar:** Carga la moneda en el formulario para editar su cotización u otros datos
- **Borrar:** Elimina la moneda del sistema

---

## Paso a paso — Actualizar la cotización

1. En la grilla, hacé clic en **Modificar** junto a la moneda que querés actualizar
2. Los datos se cargan en el formulario del panel izquierdo
3. Actualizá el campo **COTIZACION** con el nuevo tipo de cambio
4. Guardá los cambios

---

## Notas importantes

- La cotización se usa en tiempo real para convertir importes en operaciones multimoneda (cta. cte. de clientes, facturas en divisa, etc.).
- Actualizar la cotización regularmente es importante para que los cálculos de deuda en divisa sean correctos.
- En entornos sin facturación en divisas (moneda única), esta pantalla generalmente no se utiliza.
