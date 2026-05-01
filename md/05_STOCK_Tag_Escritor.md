# 5.XX TAG ESCRITOR (RFID)
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Tag Escritor

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Tag Escritor** permite asociar etiquetas RFID a artículos del stock, registrando el código SKU en cada etiqueta para facilitar la gestión de inventario por radiofrecuencia. Desde aquí podés:

- Consultar las etiquetas RFID registradas por punto de venta
- Asignar un SKU a una etiqueta RFID específica
- Usar el lector RFID para identificar etiquetas en el depósito (función exclusiva para usuarios administradores)

---

<img src="imagenes/pantalla_tag_escritor.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Tag Escritor**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta. Al cambiar aplica el filtro de etiquetas automáticamente. |
| **SKU** | Código del artículo a asignar a la etiqueta RFID |

### Sección LECTURA Y ESCRITURA POR RFID *(solo administradores)*

Disponible únicamente para usuarios con perfil administrador:

| Botón | Descripción |
|---|---|
| **Leer** | Solicita la lectura de etiquetas mediante el dispositivo RFID |
| **Stock** | Obtiene el resultado de la última lectura solicitada |
| **Escribir** | Escribe el SKU en las etiquetas seleccionadas |

Campo adicional para identificar la sesión de lectura RFID.

---

## Panel derecho — Grilla de etiquetas

Muestra las etiquetas RFID registradas para el punto de venta seleccionado:

| Columna | Descripción |
|---|---|
| TID | Identificador único de la etiqueta RFID |
| SKU | Código de artículo asignado a la etiqueta |
| Articulo | Descripción del artículo |
| Deposito | Depósito asociado |

---

## Notas importantes

- Las funciones de lectura y escritura RFID solo están disponibles para usuarios administradores del sistema.
- Cada etiqueta RFID se identifica por su TID (identificador único de fábrica) y se le asocia el SKU del artículo correspondiente.
