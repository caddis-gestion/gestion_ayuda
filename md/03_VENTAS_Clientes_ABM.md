# 3.42 CLIENTES A/B/M
### Módulo 3 — Ventas y Facturación

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Ventas y Facturación → Clientes A/B/M

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Clientes A/B/M** (Alta, Baja, Modificación) permite crear y editar los datos de los clientes del sistema. También se usa como **Clientes Consulta** para ver la ficha completa de un cliente existente. Desde aquí podés:

- Dar de alta un nuevo cliente
- Modificar los datos de un cliente existente
- Desactivar un cliente (marcarlo como INACTIVO)
- Consultar la ficha completa de un cliente

---

<img src="imagenes/pantalla_clientes_abm.png" style="width:100%; height:auto; display:block;">

<div style="page-break-after:always"></div>

## Cómo acceder

Desde el menú principal seleccioná:
**Ventas y Facturación → Clientes A/B/M**
o
**Ventas y Facturación → Clientes Consulta**

---

## Descripción general de la pantalla

La pantalla muestra el formulario completo de la ficha del cliente, organizado en tres secciones: datos generales, datos para factura, y datos de entrega.

---

## Sección — Datos generales

| Campo | Descripción |
|---|---|
| **CODIGO** | Código interno del cliente (asignado automáticamente, sólo lectura) |
| **Estado** | ACTIVO o INACTIVO. Los clientes inactivos no aparecen en los selectores de facturación. |
| **CUIT\|DNI** (o TAX ID) | Número de identificación fiscal del cliente. Al ingresarlo, el sistema puede consultar los datos de AFIP automáticamente. Botón **"Ver en AFIP"** para consultar la constancia de inscripción. |
| **NACIMIENTO** | Fecha de nacimiento del cliente |
| **SEXO** | MASCULINO o FEMENINO |
| **CLIENTE** | Razón social o nombre completo del cliente |
| **NOMBRE FANTASIA** | Nombre comercial (si difiere de la razón social) |
| **DOMICILIO** | Dirección del cliente |
| **LOCALIDAD** | Localidad |
| **C.POSTAL** | Código postal |
| **PAIS** | País |
| **PROVINCIA** | Provincia |
| **E-MAIL** | Correo electrónico del cliente |
| **TELEFONO** | Teléfono de contacto |
| **TELEFONICA** | Operadora telefónica (Claro, Movistar, etc.) |
| **CONTACTO** | Nombre de la persona de contacto |
| **RUBRO** | Rubro o categoría del cliente |

---

## Sección — Datos para Factura

| Campo | Descripción |
|---|---|
| **VENTA CTA CTE** | SI: el cliente puede comprar en cuenta corriente (crédito). NO: sólo contado. |
| **LISTA DE PRECIO** | Lista de precios asignada al cliente |
| **IVA** | Condición frente al IVA (Consumidor Final, Responsable Inscripto, Monotributista, etc.) |
| **IIBB** | Condición frente a Ingresos Brutos |
| **IIBB Nro** | Número de inscripción en IIBB |
| **FACTURA EN** | Moneda en la que se factura al cliente (pesos u otra moneda, en entornos multimoneda) |
| **VENDEDOR / ADMINISTRADOR** | Vendedor o administrador asignado al cliente |

---

## Sección — Datos de Entrega

| Campo | Descripción |
|---|---|
| **DOMICILIO** | Domicilio de entrega (puede diferir del domicilio fiscal) |
| **BARRIO** | Barrio del domicilio de entrega |
| **LOCALIDAD** | Localidad de entrega |
| **C.POSTAL** | Código postal de entrega |
| **PAIS** | País de entrega |
| **PROVINCIA** | Provincia de entrega |
| **LUGAR DE PAGO** | EN ORIGEN (el cliente paga el flete) o EN DESTINO |
| **VALOR DECLARADO** | Porcentaje del valor declarado para el seguro de envío |
| **TRANSPORTE** | Empresa de transporte asignada |
| **CON TURNO** | Indica si la entrega requiere coordinar un turno (SI/NO) |
| **Observaciones** | Notas para la entrega |

---

## Notas importantes

- La pantalla **Clientes Consulta** usa el mismo formulario que **Clientes A/B/M** pero puede estar configurada en modo sólo lectura según el perfil del usuario.
- Al ingresar el **CUIT/DNI** y hacer clic en **"Ver en AFIP"**, el sistema consulta la constancia de inscripción en línea y puede completar automáticamente algunos datos fiscales.
- El campo **VENTA CTA CTE = SI** habilita al cliente para aparecer en la pantalla de **Cta Cte Clientes** (3.31) y realizar compras con pago diferido.
- Los clientes **INACTIVOS** no aparecen en los selectores de venta pero se conservan sus datos históricos.
