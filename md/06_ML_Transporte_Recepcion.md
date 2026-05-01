# 6.25 ML RECEPCIÓN DE TRANSPORTE
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Recepcion Transporte

---

## ¿Para qué sirve esta pantalla?

**ML Recepción de Transporte** permite registrar la recepción de paquetes en el depósito del vendedor, tanto los que llegan por transporte/correo como los que se ingresan manualmente por remito. Desde aquí podés:

- Registrar la recepción de envíos ingresando los IDs de shipping de ML
- Registrar recepciones por número de remito de Caddis
- Ver el listado de recepciones registradas con los datos de la venta y el comprador
- Eliminar registros de recepción si se ingresaron por error

---

<img src="imagenes/pantalla_ml_transporte_recepcion.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Recepcion Transporte**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Formulario para registrar recepciones.
- **Panel derecho (grilla):** Listado de recepciones registradas.

---

## Panel izquierdo: Registrar recepciones

### Por remito

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Se selecciona al cargar la pantalla y actualiza automáticamente la grilla. |
| **Remito** | Número del remito de Caddis. Ingresá el número y presioná Enter para registrar la recepción asociada a ese remito. |

### Por IDs de envío de ML

| Campo | Descripción |
|---|---|
| **ENVIOS RECEPCIONADOS** | Área de texto donde ingresás uno o varios IDs de shipping de ML (uno por línea). |
| **Ingresar** | Botón para procesar e ingresar los envíos listados en el área de texto. |

---

## Panel derecho: Grilla de recepciones

Muestra las recepciones ya registradas.

| Columna | Descripción |
|---|---|
| **Venta** | ID de la venta en ML |
| **Fecha** | Fecha de la recepción |
| **Cliente** | Nombre del comprador |
| **Borrar** | Botón para eliminar el registro de recepción (si fue un error) |

---

## Cómo registrar la recepción de un envío

### Por ID de shipping ML

1. Seleccioná el **USUARIO** ML.
2. En el área **ENVIOS RECEPCIONADOS**, ingresá los IDs de shipping (uno por línea):
   ```
   123456789
   987654321
   ```
3. Hacé click en **Ingresar**.
4. El sistema registra la recepción y las ventas aparecen en la grilla.

### Por remito

1. Ingresá el número del **Remito** en el campo correspondiente.
2. Presioná **Enter**.
3. El sistema registra la recepción del remito y lo muestra en la grilla.

---

## Uso típico

Esta pantalla se usa cuando el depósito del vendedor recibe de vuelta mercadería de ML (devoluciones, paquetes no entregados, etc.) o cuando se necesita registrar la entrada de paquetes provenientes del operador logístico.

---

> 📖 Para gestionar ventas y envíos consultá [**Ventas de MercadoLibre**](https://ayuda.caddis.com.ar/instructivos/06_ML_Ventas.pdf).
> 📖 Para armar envíos que salen del depósito consultá [**Armar Envíos ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Armar_Envios.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
