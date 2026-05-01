# 3.53 EXCEPTUAR IIBB
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Exceptuar IIBB

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Exceptuar IIBB** (también llamada **Clientes con Percepción IIBB**) permite configurar excepciones a la percepción y retención de Ingresos Brutos (IIBB) para clientes o puntos de venta específicos. Desde aquí podés:

- Exceptuar a un CUIT del régimen de percepción o retención de IIBB de una provincia
- Asignar tasas especiales (distintas al padrón) para un CUIT específico
- Establecer el período de vigencia de la excepción (DESDE / HASTA)
- Consultar y eliminar excepciones existentes

---

<img src="imagenes/pantalla_exceptuar_iibb.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Exceptuar IIBB**

---

## Cuándo se calculan percepciones de IIBB

Las percepciones de IIBB se calculan al facturar cuando se cumplen **ambas** condiciones:

- El **vendedor** es agente de percepción de IIBB
- El **cliente** es Responsable Inscripto o Monotributista

---

## Lógica de cálculo según padrón y domicilio

El sistema determina el porcentaje a aplicar cruzando tres datos: si el cliente figura en el padrón, si su domicilio fiscal coincide con la provincia agente, y si el domicilio de facturación coincide.

### Agente de percepción en una sola provincia

**Caso 1 — El cliente NO figura en el padrón**

| Situación | ARBA |
|---|---|
| CLIENTE EN PADRON | NO |
| DOMICILIO DEL CLIENTE | SI/NO |
| DOMICILIO DE FACTURACION | SI |
| PORCENTAJE A CALCULAR | **APLICA % MAXIMO** |

**Caso 2 — El cliente figura en el padrón**

| Situación | ARBA |
|---|---|
| CLIENTE EN PADRON | SI |
| DOMICILIO DEL CLIENTE | SI |
| DOMICILIO DE FACTURACION | SI |
| PORCENTAJE A CALCULAR | **APLICA % PADRON** |

---

### Agente de percepción en dos provincias (ej. ARBA y CABA)

**Caso 3 — El cliente no figura en los padrones y su provincia coincide con la de facturación**

| Situación | ARBA | CABA |
|---|---|---|
| AGENTE RECAUDADOR | SI | SI |
| CLIENTE EN PADRON | NO | NO |
| DOMICILIO DEL CLIENTE | SI | NO |
| DOMICILIO DE FACTURACION | SI | NO |
| PORCENTAJE A CALCULAR | **APLICA % MAXIMO** | **NO PERCIBE** |

**Caso 4 — El cliente no figura en los padrones y su provincia NO coincide con la de facturación**

| Situación | ARBA | CABA |
|---|---|---|
| AGENTE RECAUDADOR | SI | SI |
| CLIENTE EN PADRON | NO | NO |
| DOMICILIO DEL CLIENTE | NO | SI |
| DOMICILIO DE FACTURACION | SI | NO |
| PORCENTAJE A CALCULAR | **APLICA % MAXIMO** | **APLICA % MAXIMO** |

**Caso 5 — El cliente figura en un solo padrón y su provincia coincide con la de facturación**

| Situación | ARBA | CABA |
|---|---|---|
| AGENTE RECAUDADOR | SI | SI |
| CLIENTE EN PADRON | SI | NO |
| DOMICILIO DEL CLIENTE | SI | NO |
| DOMICILIO DE FACTURACION | SI | NO |
| PORCENTAJE A CALCULAR | **APLICA % PADRON** | **NO PERCIBE** |

**Caso 6 — El cliente figura en un solo padrón y su provincia NO coincide con la de facturación**

| Situación | ARBA | CABA |
|---|---|---|
| AGENTE RECAUDADOR | SI | SI |
| CLIENTE EN PADRON | NO | SI |
| DOMICILIO DEL CLIENTE | NO | SI |
| DOMICILIO DE FACTURACION | SI | NO |
| PORCENTAJE A CALCULAR | **APLICA % MAXIMO** | **APLICA % PADRON** |

**Caso 7 — El cliente figura en ambos padrones**

| Situación | ARBA | CABA |
|---|---|---|
| AGENTE RECAUDADOR | SI | SI |
| CLIENTE EN PADRON | SI | SI |
| DOMICILIO DEL CLIENTE | SI/NO | SI/NO |
| DOMICILIO DE FACTURACION | SI/NO | SI/NO |
| PORCENTAJE A CALCULAR | **APLICA % PADRON** | **APLICA % PADRON** |

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con el formulario y un panel derecho con la grilla de excepciones configuradas.

---

## Panel izquierdo — Formulario

| Campo | Descripción |
|---|---|
| **PROVINCIA** | Provincia de IIBB a la que aplica la excepción. Al cambiarla, la grilla se actualiza. |
| **CUIT** | CUIT del cliente o PDV que se exceptúa |
| **PERCEPCION** | Tasa especial de percepción de IIBB (en %). Ingresar 0 si se exceptúa totalmente. |
| **RETENCION** | Tasa especial de retención de IIBB (en %). Ingresar 0 si se exceptúa totalmente. |
| **EXCEPTUAR** | **SI**: el CUIT queda exceptuado del régimen general del padrón. **NO**: se le aplican las tasas especiales ingresadas sin exceptuarlo totalmente. |
| **DESDE** | Fecha de inicio de la vigencia de la excepción |
| **HASTA** | Fecha de fin de la vigencia de la excepción |

---

## Panel derecho — Grilla de excepciones

Muestra los CUITs con excepción registrada para la provincia seleccionada:

| Columna | Descripción |
|---|---|
| Cuit | CUIT exceptuado |
| Nombre | Nombre del cliente o PDV |
| Fecha | Fecha del registro |
| Tasa Percepcion | Tasa de percepción del padrón general |
| Tasa Retencion | Tasa de retención del padrón general |
| Excepcion Percepcion | Tasa especial de percepción asignada |
| Excepcion Retencion | Tasa especial de retención asignada |
| Exceptuar | SI = totalmente exceptuado; NO = tasa especial |
| Provincia | Provincia de la excepción |

**Acciones disponibles:**
- **Borrar:** Elimina la excepción

---

## Paso a paso — Exceptuar totalmente a un cliente

Si el cliente no figura en el padrón y se quiere que el sistema **no calcule percepciones** al facturarle:

1. Seleccioná la **PROVINCIA**
2. Ingresá el **CUIT** del cliente
3. Dejá **PERCEPCION** y **RETENCION** en **0**
4. Seleccioná **EXCEPTUAR = SI**
5. Completá **DESDE** y **HASTA** para la vigencia
6. Guardá el registro

> De esta manera el cliente queda exceptuado todos los meses mientras la fecha actual esté dentro del rango configurado. Para revertirlo, eliminá la excepción desde la grilla.

## Paso a paso — Asignar tasa especial a un cliente

Si el cliente debe tributar una tasa diferente a la del padrón:

1. Seleccioná la **PROVINCIA**
2. Ingresá el **CUIT** del cliente
3. Completá **PERCEPCION** y/o **RETENCION** con la tasa especial
4. Seleccioná **EXCEPTUAR = NO**
5. Completá **DESDE** y **HASTA** para la vigencia
6. Guardá el registro

---

## Notas importantes

- Esta configuración aplica cuando el sistema calcula las percepciones y retenciones de IIBB al facturar.
- Los CUITs sin excepción siguen la lógica del padrón de IIBB importado (ver [**Importar Padrones IIBB**](https://ayuda.caddis.com.ar/instructivos/03_VENTAS_Importar_Padrones_IIBB.pdf), 3.57).
- Para que la excepción sea válida, la fecha actual debe estar dentro del rango DESDE/HASTA configurado.
- La excepción aplica según el criterio de cada empresa; no es una obligación fiscal sino una herramienta de gestión.
