# 5.44 ETIQUETAS DE ARTÍCULOS
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Etiquetas Artículos

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Etiquetas Artículos** permite generar e imprimir etiquetas de precios o identificación para artículos del inventario. Podés configurar el tamaño, la disposición y la cantidad de etiquetas a imprimir. Desde aquí podés:

- Agregar artículos a la lista de etiquetas con la cantidad deseada
- Configurar las medidas de la hoja y la etiqueta
- Imprimir etiquetas con código de barras y descripción del artículo

---

<img src="imagenes/pantalla_etiquetas_articulos.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Etiquetas Artículos**

---

## Formulario — Artículos

| Campo | Descripción |
|---|---|
| **ARTICULO** | Artículo a incluir en la lista de etiquetas |
| **CANTIDAD** | Cantidad de etiquetas a imprimir para ese artículo |
| Botón **Ingresar** | Agrega el artículo con la cantidad indicada a la lista |
| Botón **Multiple** | Permite agregar múltiples artículos de una sola vez |

---

## Formulario — Medidas de la etiqueta

| Campo | Descripción |
|---|---|
| **HOJA** | Tamaño de la hoja: A4, Carta u Oficio |
| **POSICION** | Orientación: Vertical (Portrait) u Horizontal (Landscape) |
| **MARGEN TOP** | Margen superior de la hoja (en mm) |
| **ANCHO** | Ancho de cada etiqueta (en mm) |
| **ALTO** | Alto de cada etiqueta (en mm) |
| **COLUMNAS** | Cantidad de columnas de etiquetas por hoja |
| **FILAS** | Cantidad de filas de etiquetas por hoja |
| **SEPARACION** | Separación entre etiquetas (en mm) |
| **TEXTO** | Tamaño del texto en la etiqueta |

El botón **Modificar** guarda la configuración de medidas para futuras impresiones.

---

## Panel derecho — Lista de etiquetas

Muestra los artículos listos para imprimir:

| Columna | Descripción |
|---|---|
| Codigo | Código del artículo |
| Cantidad | Cantidad de etiquetas (editable) |
| Articulo | Descripción del artículo |
| Tipo | Tipo de artículo |
| Grupo | Grupo del artículo |
| Marca | Marca del artículo |
| Variante | Variante del artículo |

**Acciones:**
- **Borrar:** Quita el artículo de la lista

---

## Notas importantes

- Las medidas configuradas se guardan automáticamente en los parámetros del sistema.
- La cantidad de etiquetas en la grilla es editable directamente.
