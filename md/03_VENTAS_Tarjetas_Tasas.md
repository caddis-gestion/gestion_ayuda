# 3.72 TARJETAS TASAS
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Tarjetas Tasas

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Tarjetas Tasas** permite configurar las tasas y cuotas que aplica cada tarjeta de crédito según la plataforma de cobro y la promoción vigente. Estas configuraciones determinan el costo financiero que se aplica al facturar con tarjeta. Desde aquí podés:

- Definir la tasa (con IVA incluido) para cada combinación de plataforma, tarjeta, promoción y cuotas
- Activar o desactivar combinaciones de tasa sin eliminarlas
- Importar datos masivos desde un archivo
- Consultar, modificar y eliminar tasas existentes

---

<img src="imagenes/pantalla_tarjetas_tasas.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Tarjetas Tasas**

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario de configuración y una grilla a la derecha con las tasas existentes filtradas por los criterios seleccionados.

---

## Formulario de configuración

| Campo | Descripción |
|---|---|
| **PLATAFORMA** | Plataforma de cobro con tarjeta (POS terminal). Al cambiar, actualiza la grilla automáticamente. |
| **TARJETA** | Tarjeta de crédito (Visa, Mastercard, American Express, etc.). Al cambiar, actualiza la grilla. |
| **PROMO** | Promoción aplicable (definidas en la pantalla Tarjetas Promos). Al cambiar, actualiza la grilla. |
| **CUOTAS** | Número de cuotas. Solo editable para tarjetas con código menor a 500 (tarjetas de crédito estándar); para débito y otras se fija en 0. |
| **TASA** | Tasa financiera final con IVA incluido (porcentaje, hasta 6 dígitos) |
| **ACTIVA** | Estado de la tasa: ACTIVA o INACTIVA |

### Sección IMPORTAR

Permite cargar tasas masivamente desde un archivo externo:

| Campo | Descripción |
|---|---|
| **Archivo** | Archivo con los datos a importar |
| **Subir Archivo** | Carga el archivo y procesa la importación |

---

## Grilla de tasas

Muestra las tasas existentes filtradas por la plataforma, tarjeta y promo seleccionadas. Los resultados se ordenan por cantidad de cuotas:

| Columna | Descripción |
|---|---|
| Tarjeta | Nombre de la tarjeta |
| Promo | Nombre de la promoción |
| Cuotas | Número de cuotas |
| Tasa | Tasa financiera con IVA (porcentaje) |
| Activa | SI o NO |
| Plataforma | Plataforma de cobro |

**Acciones disponibles:**
- **Modificar:** Edita los datos de la tasa seleccionada
- **Borrar:** Elimina la tasa

---

## Notas importantes

- La **tasa** expresada es la tasa final con IVA incluido que se aplica sobre el importe cobrado con tarjeta.
- Si una combinación está **INACTIVA**, no aparece como opción disponible al facturar con esa tarjeta.
- Para el caso de tarjetas de débito u otras con código ≥ 500, las cuotas se fijan automáticamente en 0.
- Las promos disponibles se administran en la pantalla **Tarjetas Promos**.
- Las plataformas disponibles se administran en la pantalla **Plataformas Pago**.
