# 15.19 BACKUP DEL SISTEMA
### Módulo 15 — Administración

> **Versión:** 1.0 — Marzo 2026
> **Audiencia:** Usuarios finales del sistema (sin conocimientos técnicos)
> **Pantalla en el sistema:** Menú → Administración → Backup del Sistema

---

## ¿Para qué sirve esta pantalla?

La pantalla de **Backup del Sistema** permite generar una copia de seguridad de la base de datos del sistema en el momento deseado. Desde aquí podés:

- Generar un backup manual de la base de datos

---

## ¿Cómo acceder?

**Menú → Administración → Backup del Sistema**

---

## Uso

La pantalla cuenta con un único botón:

| Botón | Descripción |
|---|---|
| **Generar BackUp** | Inicia la generación de una copia de seguridad completa de la base de datos del sistema. |

Al hacer clic, el sistema genera el backup y lo almacena en el servidor. El proceso puede tardar algunos segundos dependiendo del tamaño de la base de datos.

---

## Notas importantes

- El backup generado es una copia completa de la base de datos en ese instante. Se recomienda generarlo periódicamente y ante cualquier operación de mantenimiento importante.
- El servidor Caddis también realiza backups automáticos programados; este botón permite forzar un backup manual adicional cuando sea necesario.
- Ante cualquier duda sobre la frecuencia o almacenamiento de los backups, consultar al equipo de soporte técnico de Caddis.
