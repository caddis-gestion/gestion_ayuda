# 5.05 ARTÍCULOS EN TRÁNSITO
### Módulo 5 — Stock y Logística

> **Versión:** 1.1 — Abril 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Articulos en Transito

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Artículos en Tránsito** permite controlar la recepción de mercadería que fue enviada desde otro depósito y aún no fue confirmada como recibida. Desde aquí puedes:

- Ver los remitos de transferencia pendientes de recepción en tu depósito
- Confirmar la recepción completa o parcial de artículos
- Comparar la cantidad enviada vs. la cantidad pendiente de recibir

---

<img src="imagenes/pantalla_articulos_transito.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal selecciona:
**Stock → Articulos en Transito**

---

## Configuración previa

Para que esta pantalla esté activa, el parámetro **sArtTransito** debe estar habilitado en el sistema. Para activarlo:

[**Administración → Configuración → Propiedades del Sistema**](https://ayuda.caddis.com.ar/instructivos/15_ADMIN_Propiedades_Sistema.pdf)

Una vez habilitado, toda mercadería transferida de un punto de venta a otro quedará con estado **En Tránsito** hasta que el destino confirme su recepción.

---

## Cómo funciona el tránsito

1. El **Punto A** genera un remito de transferencia y envía el stock.
2. Mientras el **Punto B** no confirme la recepción, el stock figura como **En Tránsito** (no disponible en ninguno de los dos puntos).
3. El usuario del Punto B accede a esta pantalla y registra la mercadería recibida.
4. Al confirmar la recepción, el stock se acredita en el Punto B y el estado cambia a **Recibido**.
5. El remito permanece visible en la pantalla hasta que **todos** los artículos hayan sido recibidos.

---

## Descripción general de la pantalla

La pantalla tiene un panel izquierdo con los filtros y opciones de recepción, y un panel derecho con el detalle del remito seleccionado.

---

## Panel izquierdo

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta / depósito de destino. Al seleccionarlo se cargan los remitos pendientes. |
| **REMITOS** | Lista de remitos en tránsito dirigidos a este depósito. Muestra fecha, número y depósito de origen. |
| **RECIBIR** | Acepta la totalidad del remito seleccionado (aceptación completa) |
| **ACEPTAR** | Confirma la aceptación luego de presionar RECIBIR |

### Recepción parcial (si el parámetro sArtTransito está activo)

| Campo / Botón | Descripción |
|---|---|
| **ARTICULO** | Código del artículo a recibir parcialmente |
| **Q RECIBIDA** | Cantidad efectivamente recibida |
| **Ingresar** | Confirma la recepción parcial de esa cantidad |

---

## Panel derecho — Detalle del remito

Muestra el contenido del remito seleccionado:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Recibido | Cantidad ya confirmada como recibida |
| Transito | Cantidad todavía en tránsito (pendiente de confirmar) |
| Articulo | Descripción |
| Tipo / Grupo / Marca / Variante | Clasificación del artículo |

---

## Modos de recepción

### A — Aceptación completa del remito

Si se recibió toda la mercadería del remito:

1. Selecciona el PDV y el remito correspondiente.
2. Haz clic en **RECIBIR**.
3. Confirma con **ACEPTAR** en el cuadro de diálogo.

El stock se acredita en el Punto B y el estado del remito cambia a **Recibido**.

### B — Aceptación parcial

Si solo se recibió una parte de los artículos:

1. Selecciona el PDV y el remito.
2. Ingresa el **código del artículo** y la **cantidad recibida** en los campos del panel izquierdo.
3. Presiona **Ingresar**.
4. Confirma la aceptación parcial en el cuadro de diálogo.

La grilla del panel derecho se actualiza mostrando:
- La cantidad ya recibida en la columna **Recibido**
- La cantidad que continúa **En Tránsito** en la columna **Transito**

El remito permanece visible hasta que todos los artículos sean recibidos completamente.

---

## Notas importantes

- Solo aparecen remitos con estado de tránsito activo (no anulados).
- El usuario del Punto B debe tener permisos para acceder a esta pantalla y registrar la recepción.
- La opción de recepción parcial solo está disponible cuando el parámetro `sArtTransito` está habilitado.
- Mientras el stock está en tránsito, no está disponible ni en el Punto A ni en el Punto B.
