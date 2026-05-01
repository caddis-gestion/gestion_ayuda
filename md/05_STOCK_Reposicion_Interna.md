# 5.27 REPOSICIÓN INTERNA
### Módulo 5 — Stock y Logística

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Stock → Reposición Interna

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Reposición Interna** permite gestionar los envíos de mercadería desde el depósito central hacia los locales (reposición interna de stock). Desde aquí podés:

- Consultar remitos de reposición interna por estado y período
- Asignar transportes integrados a los envíos
- Marcar remitos como entregados
- Imprimir remitos

---

<img src="imagenes/pantalla_reposicion_interna.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Stock → Reposición Interna**

---

## Formulario

| Campo | Descripción |
|---|---|
| **PDV** | Punto de venta destino de la reposición |
| **DESDE** | Fecha de inicio del período |
| **HASTA** | Fecha de fin del período |
| **ESTADO** | TODOS / A ENTREGAR / ENTREGADO |

### Sección TRANSPORTES (si hay transportes integrados configurados)

| Campo/Acción | Descripción |
|---|---|
| **ENVIO** | Número de envío actualmente seleccionado (solo lectura) |
| Botones de transporte | Asigna los remitos seleccionados al transporte (Envíopack, Rapiboy, etc.) |

---

## Panel derecho — Grilla de remitos

| Columna | Descripción |
|---|---|
| Checkbox | Selección de remitos (en estado A ENTREGAR) |
| Id Remito | Identificador interno del remito |
| Remito Fecha | Fecha del remito de movimiento |
| Remito Numero | Número del remito |
| Envio | Número de envío asignado |
| Envío Fecha | Fecha en que se envió |
| Guia | Número de guía del transporte |
| Transporte | Empresa de transporte asignada |
| Origen | Depósito de origen (central) |
| Destino | Depósito de destino (local) |

**Acciones:**
- **Imprimir:** Imprime el remito de reposición
- **Modificar:** Permite asignar o cambiar el envío del remito

---

## Notas importantes

- Solo se muestran remitos de tipo de movimiento 22 (reposición interna) que van desde el depósito central hacia locales con logística interna configurada.
- El checkbox para selección múltiple aparece únicamente en el estado **A ENTREGAR**.
- Los botones de transporte aparecen solo si la empresa tiene transportes integrados configurados.
