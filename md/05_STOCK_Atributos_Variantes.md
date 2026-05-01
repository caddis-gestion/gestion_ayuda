# 5.16 ATRIBUTOS VARIANTES
### Módulo 5 — Stock y Logística

> **Versión:** 1.1 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Atributos Variantes

---

## ¿Para qué sirve esta pantalla?

Los **atributos** son parámetros que clasifican y describen a los artículos: color, talle, medida, material, modelo, etc. Cada artículo puede tener distintos atributos según su tipo.

Los atributos se organizan en dos niveles:

- **Atributo**: define el tipo de característica. Ej: Color, Talle, Resolución.
- **Variante**: define los valores posibles de ese atributo. Ej: el atributo "Color" tiene variantes "Rojo", "Azul", "Negro".

Los atributos se asignan por **Tipo de Artículo**, lo que facilita la carga porque todos los artículos de un mismo tipo comparten los mismos atributos.

**Ejemplos:**

| Camisa | Cubierta | Televisor |
|---|---|---|
| Talle | Diámetro | Tamaño |
| Color | Ancho | Resolución |
| Tela | Talón | Modelo |
| Marca | Velocidad | |
| | Carga | |

Y dentro de cada atributo, sus variantes:

| Talle | Diámetro | Resolución |
|---|---|---|
| SMALL | 16" | HD |
| LARGE | 17" | FULL HD |
| MEDIUM | 18" | 4K |

Desde esta pantalla podés:

- Crear y administrar los atributos del sistema
- Crear, modificar y eliminar variantes para cada atributo

---

<img src="imagenes/pantalla_atributos_variantes.png" style="width:100%; height:auto; display:block;">

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Atributos Variantes**

---

## Formulario — Crear variantes

| Campo / Botón | Descripción |
|---|---|
| **ATRIBUTO** | Selector del atributo al que pertenece la variante. Muestra todos los atributos creados en el sistema. |
| **Agregar** (ícono junto al selector) | Abre el popup **Alta de Atributos** para crear un nuevo atributo |
| **Borrar** | Elimina el atributo seleccionado |
| **VARIANTE** | Nombre del valor de la variante (máximo 30 caracteres). Ej: "Rojo", "128GB", "Grande" |
| **Guardar** | Guarda la nueva variante para el atributo seleccionado |

> Los atributos deben crearse **antes** de ingresar sus variantes.

### Popup — Alta de Atributos

Al hacer clic en el botón **Agregar** junto al selector de atributo, se abre el popup **Alta de Atributos**:

| Campo / Columna | Descripción |
|---|---|
| **ATRIBUTO** | Nombre del nuevo atributo a crear |
| **Guardar** | Guarda el nuevo atributo |
| Grilla (Id / Atributo) | Lista de todos los atributos existentes en el sistema con su código interno |
| Ícono Modificar | Edita el nombre del atributo seleccionado |
| Ícono Borrar | Elimina el atributo seleccionado |
| Ícono Orden | Permite reordenar los atributos en la lista |

---

## Grilla de variantes

Muestra todas las variantes del atributo seleccionado:

| Columna | Descripción |
|---|---|
| Id | Código interno de la variante |
| Variante | Nombre del valor de la variante |
| Atributo | Nombre del atributo al que pertenece |

**Acciones disponibles sobre cada fila:**
- **Modificar:** Edita el nombre de la variante
- **Borrar:** Elimina la variante

---

## Pantalla relacionada — Atributos por Tipo de Artículo

Una vez creados los atributos y sus variantes, el siguiente paso es **relacionar cada atributo al Tipo de Artículo** correspondiente. Esto se realiza desde la pantalla **Stock → Atributos por Tipo de Artículo**.

| Campo | Descripción |
|---|---|
| **TIPO** | Tipo de artículo al que se le asignarán atributos |
| **ATRIBUTO** | Lista desplegable con todos los atributos disponibles |

Al seleccionar un atributo de la lista desplegable, el sistema lo asocia automáticamente al Tipo de Artículo. La asociación aparece en la grilla con columnas **Categoría** y **Atributo**. Para eliminar una asociación, usá el cesto de basura en la grilla.

> Una vez definidos los atributos por tipo, al cargar un artículo en ABM Artículos se mostrarán automáticamente los atributos correspondientes según el tipo seleccionado.

---

## Asignar variantes a cada artículo

Con la estructura de atributos y variantes definida, se asignan los valores específicos a cada artículo desde **A/B/M → Artículos** (ABM Artículos).

En el formulario de ABM Artículos, al elegir el **TIPO** de artículo, se muestra el bloque **ATRIBUTOS** con un selector desplegable para cada atributo configurado para ese tipo. Desde cada selector se elige la variante que corresponde al artículo.

**Ejemplo:** Para un artículo de tipo PRENDAS, el bloque ATRIBUTOS mostrará los selectores COLOR, COSTUMER, ORIGEN, etc., con las variantes disponibles para cada uno.

---

## Visualización de variantes en grillas y comprobantes

Una vez asignadas las variantes a los artículos, la información se muestra en todo el sistema:

### En grillas de stock

Las grillas de artículos (por ejemplo, **Stock de Artículos**) muestran una columna **Variante** con todas las variantes del artículo concatenadas:

```
MARCA: WANAMA | MODELO: CAMISA BAMBULA | MEDIDA: MEDIUM | COLOR: VERDE | MATERIAL: CHENILLE
```

Al pasar el mouse por encima de un artículo, se despliega un tooltip con todas sus variantes listadas en detalle.

### En comprobantes

En las grillas de comprobantes (facturas, remitos, etc.), al pasar el mouse sobre un artículo se muestra un tooltip con el detalle completo de sus variantes:

```
Edge 1030 Bundle
TIPO: Varios
MARCA: Garmin
MARCA: WANAMA
MODELO: CAMISA BAMBULA
MEDIDA: MEDIUM
COLOR: VERDE
MATERIAL: CHENILLE
```

---

## Flujo completo

| Paso | Pantalla | Acción |
|---|---|---|
| 1. Crear atributos | **Atributos Variantes** | Usar el botón Agregar para crear cada atributo (Color, Talle, etc.) |
| 2. Crear variantes | **Atributos Variantes** | Para cada atributo, ingresar sus valores (Rojo, Azul, SMALL, etc.) |
| 3. Relacionar atributos a tipos | **Atributos por Tipo de Artículo** | Asignar qué atributos corresponden a cada Tipo de Artículo |
| 4. Asignar variantes a artículos | **ABM Artículos** | Al cargar cada artículo, completar el bloque ATRIBUTOS |

---

## Notas importantes

- Los **atributos** deben crearse antes de ingresar sus variantes.
- Los atributos se asignan por **Tipo de Artículo**: todos los artículos del mismo tipo comparten el mismo conjunto de atributos.
- Las variantes asignadas a los artículos se visualizan automáticamente en grillas y comprobantes de todo el sistema.
- No eliminés atributos ni variantes que estén en uso en artículos activos del catálogo.
