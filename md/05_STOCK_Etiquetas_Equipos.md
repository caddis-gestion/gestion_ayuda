# 5.45 ETIQUETAS DE EQUIPOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Etiquetas Equipos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Etiquetas Equipos** permite generar e imprimir etiquetas para equipos (teléfonos y dispositivos con NSE) del inventario del usuario. Funciona de forma similar a Etiquetas Artículos pero trabaja con el stock de equipos identificados por número de serie. Desde aquí podés:

- Ver los equipos del inventario actual del usuario
- Configurar las medidas de las etiquetas
- Imprimir etiquetas con el NSE y descripción de cada equipo

---

<img src="imagenes/pantalla_etiquetas_equipos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Etiquetas Equipos**

---

## Formulario — Medidas de la etiqueta

| Campo | Descripción |
|---|---|
| **HOJA** | Tamaño de la hoja: A4, Carta u Oficio |
| **POSICION** | Orientación: Vertical u Horizontal |
| **MARGEN TOP** | Margen superior de la hoja (en mm) |
| **ANCHO** | Ancho de cada etiqueta (en mm) |
| **ALTO** | Alto de cada etiqueta (en mm) |
| **COLUMNAS** | Cantidad de columnas de etiquetas por hoja |
| **FILAS** | Cantidad de filas de etiquetas por hoja |
| **SEPARACION** | Separación entre etiquetas (en mm) |
| **TEXTO** | Tamaño del texto en la etiqueta |

El botón **Modificar** guarda la configuración.

---

## Panel derecho — Lista de equipos para etiquetar

Muestra los equipos del inventario del usuario actual:

| Columna | Descripción |
|---|---|
| NSE_Hexa | Número de serie del equipo (hexadecimal) |
| Detalle | Marca y modelo del equipo |

**Acciones:**
- **Borrar:** Quita el equipo de la lista de etiquetas

---

## Notas importantes

- La lista de equipos corresponde al inventario del usuario que inició sesión (tabla temporal de equipos).
- Las medidas configuradas se guardan en los parámetros del sistema para futuras sesiones.
- Para agregar equipos al inventario primero usá **Equipos Ingresos** o **Equipos Movimientos**.
