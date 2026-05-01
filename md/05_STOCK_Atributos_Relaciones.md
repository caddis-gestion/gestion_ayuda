# 5.17 ATRIBUTOS RELACIONES
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Atributos Relaciones

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Atributos Relaciones** permite asociar atributos a tipos de artículo. Esto define qué características son aplicables a cada tipo de producto (ej. el tipo "Teléfono" puede tener atributos como "Color" y "Capacidad"). Desde aquí podés:

- Seleccionar el tipo de artículo
- Asignar el atributo que aplica para ese tipo
- Ver y eliminar las relaciones ya configuradas

---

<img src="imagenes/pantalla_atributos_relaciones.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Atributos Relaciones**

---

## Formulario

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de artículo al que se asigna el atributo (solo tipos con código > 100) |
| **ATRIBUTO** | Atributo (clase) a asociar al tipo seleccionado |

Al seleccionar el atributo se guarda automáticamente la relación.

---

## Panel derecho — Grilla de relaciones

Muestra los atributos ya asociados al tipo seleccionado:

| Columna | Descripción |
|---|---|
| Categoria | Nombre del tipo de artículo |
| Atributo | Nombre del atributo asociado |

**Acciones:**
- **Borrar:** Elimina la relación tipo-atributo

---

## Notas importantes

- Esta pantalla complementa a **Atributos Variantes**: primero definís las variantes y luego las asociás al tipo de artículo aquí.
- Un tipo de artículo puede tener múltiples atributos asociados.
