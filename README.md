# Préstamos de equipos - Ingeniería de Software II

Miniaplicación estática para la actividad individual de aseguramiento de calidad de software. No usa base de datos ni servidor, guarda los registros en el navegador mediante `localStorage`.

**Estudiante:** Lenin Smith Apaza Cuentas
**Ficha asignada:** 02 - Longitud máxima del solicitante
**Repositorio:** [02-IS2-Apaza-Cuentas](https://github.com/lsmithcovid19-gif/02-IS2-Apaza-Cuentas)
**Demo en vivo:** *(agregar aquí el link de GitHub Pages cuando esté activo)*

---

## Funcionalidad inicial

- Registra un préstamo de un equipo disponible.
- Evita registrar datos incompletos, una fecha de devolución anterior a la fecha de préstamo y el préstamo simultáneo del mismo equipo.
- Muestra los préstamos y permite registrar la devolución.
- Conserva los datos del navegador mientras no se restablezcan desde la aplicación.

## Mejora implementada

**Validación de longitud máxima del solicitante.** El campo "Solicitante" no acepta más de 50 caracteres: si el nombre ingresado supera ese límite, el sistema muestra un mensaje de error y no registra el préstamo.

**Criterios de aceptación:**
- Un nombre de hasta 50 caracteres se registra correctamente.
- Un nombre de 51 caracteres o más se rechaza, mostrando un mensaje claro y sin guardar el registro.

## Inicio rápido

1. Clone este repositorio.
2. Abra `index.html` en el navegador para probarlo localmente.
3. Complete el formulario y pruebe registrar un préstamo.

## Archivos principales

| Archivo | Contenido |
|---|---|
| `index.html` | Estructura y controles de la aplicación |
| `style.css` | Diseño visual |
| `app.js` | Catálogo, registros, validaciones y almacenamiento local |

## Casos de prueba de mi mejora

| Caso | Datos de entrada / acción | Resultado esperado | Resultado obtenido | Estado |
|:---|:---|:---|:---|:---:|
| **CP-01**<br>*(válido)* | Equipo disponible cualquiera. Solicitante: **"Lenin Smith Apaza Cuentas"** (≤ 50 caracteres). Fechas de préstamo y devolución válidas. Clic en "Registrar préstamo". | El sistema acepta el nombre, guarda el préstamo y lo muestra en la tabla con estado **Activo**. | El préstamo se registró correctamente y apareció en la tabla con estado "Activo". | Aprobado |
| **CP-02**<br>*(inválido / límite)* | Equipo disponible cualquiera. Solicitante: nombre de **51+ caracteres** (ej. "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"). Fechas válidas. Clic en "Registrar préstamo". | El sistema rechaza el registro, muestra el mensaje de error correspondiente y no agrega ninguna fila. | Apareció el mensaje "⚠ El nombre del solicitante no puede superar 50 caracteres." La tabla no agregó ninguna fila nueva. | Aprobado |

## Entrega

- **Repositorio individual:** https://github.com/lsmithcovid19-gif/02-IS2-Apaza-Cuentas
- **GitHub Pages:** *(agregar aquí una vez publicado)*
- README actualizado con los dos casos de prueba