# 6.07 ML PROMOCIONES
### Módulo 6 — Mercado Libre

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Mercado Libre → ML Promociones

---

## ¿Para qué sirve esta pantalla?

**ML Promociones** permite gestionar las promociones de precio de MercadoLibre para las publicaciones activas. Desde aquí podés:

- Consultar todas las promociones disponibles en ML para la cuenta seleccionada
- Ver qué publicaciones están participando de cada promoción
- Activar o inactivar publicaciones en una promoción
- Actualizar el estado de las promociones desde la API de ML
- Ver el semáforo de estado de cada publicación en la promoción (candidata, pendiente, activa)

---

<img src="imagenes/pantalla_ml_promociones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Mercado Libre → ML Promociones**

---

## Descripción general de la pantalla

La pantalla se divide en dos paneles:

- **Panel izquierdo:** Filtros para seleccionar usuario, tipo y campaña de promoción, más los filtros de publicaciones.
- **Panel derecho (grilla):** Publicaciones con sus precios de promoción, estado y semáforo.

---

## Panel izquierdo: Filtros

### Selección de promoción

| Campo | Descripción |
|---|---|
| **USUARIO** | Cuenta de MercadoLibre. Obligatorio. |
| **TIPO** | Tipo de campaña de ML (ej: `DEAL`, `LIGHTNING`, `PRICE_DISCOUNT`). |
| **PROMO** | Promoción específica del tipo seleccionado. El dropdown se filtra según el TIPO elegido. |
| **ITEMS** | Estado de los ítems dentro de la promoción (`candidate`, `in_campaign`, `rejected`). |

### Filtro de publicaciones

| Campo | Descripción |
|---|---|
| **ESTADO** | Estado de la publicación (`active`, `paused`, etc.). |
| **MARCA** | Marca del artículo. |
| **ITEM** | ID de publicación ML. |
| **SKU** | Código del artículo en Caddis. |

### Detalle de la promoción seleccionada (solo lectura)

Cuando se selecciona una promoción, aparecen sus datos:

| Campo | Descripción |
|---|---|
| **ESTADO** | Estado actual de la campaña en ML |
| **INICIA** | Fecha y hora de inicio de la promoción |
| **FINALIZA** | Fecha y hora de fin de la promoción |

---

## Procesos disponibles

| Botón | Descripción |
|---|---|
| **Activar** | Activa en la promoción las publicaciones seleccionadas (checkbox) con el precio de descuento configurado |
| **Inactivar** | Retira las publicaciones seleccionadas de la promoción activa |
| **Actualizar Promociones** | Sincroniza el estado de las promociones con la API de ML |

---

## Panel derecho: Columnas de la grilla

| Columna | Descripción |
|---|---|
| **Item** | ID de la publicación ML |
| **SKU** | Código del artículo en Caddis |
| **Titulo** | Título de la publicación |
| **Precio Lista** | Precio regular de la publicación sin promoción |
| **Precio Descuento** | Precio con el descuento de la promoción aplicado |
| **Precio Destacado** | Precio destacado (precio tachado visible en ML) |
| **Promocion** | Nombre de la promoción a la que pertenece |
| **Promo Tipo** | Tipo de campaña de la promoción — fondo amarillo |
| **Estado Promo** | Estado de la publicación dentro de la promoción — fondo amarillo |
| **Precio Sugerido** | Precio mínimo sugerido por ML para participar |
| **Precio Minimo** | Precio mínimo permitido por ML para esta publicación |
| **Precio Maximo** | Precio máximo para la promoción |
| **Porcentaje Meli** | Porcentaje de descuento aplicado por ML |
| **Porcentaje Vendedor** | Porcentaje de descuento adicional del vendedor |
| **Stock ML** | Stock disponible en la publicación |
| **Stock FULL** | Stock en depósito FULL de ML |
| **Stock Minimo** | Stock mínimo para participar en la promoción |
| **Stock Maximo** | Stock máximo ofrecido en la promoción |
| **Estado Publicacion** | Estado de la publicación en ML |

---

## Semáforo de estado en la promoción

| Color | Estado | Significado |
|---|---|---|
| Rojo | `CANDIDATE` | La publicación puede participar pero aún no fue activada |
| Amarillo | `PENDING` | La activación está pendiente de confirmación por ML |
| Verde | `STARTED` | La publicación está activa en la promoción |

---

## Cómo activar publicaciones en una promoción

1. Seleccioná el **USUARIO** ML.
2. Elegí el **TIPO** de promoción y luego la **PROMO** específica.
3. Filtrá por **MARCA**, **ITEM** o **SKU** si querés ver solo algunas publicaciones.
4. Marcá el checkbox de las publicaciones a activar.
5. Hacé click en **Activar**.
6. Confirmá el aviso.
7. El estado de las publicaciones cambia a `PENDING` o `STARTED` según la respuesta de ML.

---

## Errores frecuentes y cómo resolverlos

| Situación | Causa | Solución |
|---|---|---|
| Publicación en rojo permanente | El precio no cumple con el mínimo requerido por ML | Ajustá el **Precio Descuento** para que sea igual o menor al **Precio Mínimo** |
| No aparecen promociones | No hay campañas vigentes para el usuario | Ejecutá **Actualizar Promociones** para sincronizar con ML |
| Error al activar | Stock insuficiente o precio inválido | Verificá el stock disponible y el precio mínimo de la promoción |

---

> 📖 Para ver los precios actuales de las publicaciones consultá [**Precios de Publicaciones**](https://ayuda.caddis.com.ar/instructivos/06_ML_Precios.pdf).
> 📖 Para gestionar la lista de precios de marketplace consultá [**Listas de Precios ML**](https://ayuda.caddis.com.ar/instructivos/06_ML_Listas_Precios.pdf).

---

*Instructivo generado con asistencia de IA — Revisión y aprobación: Equipo Caddis*
*Versión 1.0 — Marzo 2026*
