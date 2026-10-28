# Auditoría y Rediseño UX/UI - Aplicación

## 1. Tabla de Heurísticas de Nielsen (Problema y Solución)

| Heurística                                | Problema detectado en la interfaz anterior                                                              | Solución aplicada en el rediseño                                                                                  |
| :---------------------------------------- | :------------------------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------------------------------------- |
| **1. Visibilidad del estado del sistema** | Al realizar acciones (como registrar o borrar), la interfaz no mostraba ningún mensaje de confirmación. | Se implementó un contenedor de mensajes dinámicos que avisa cuando se procesa o se completa una acción con éxito. |
| **2. Coincidencia con el mundo real**     | Uso de textos crudos o poco claros ("ok" o botones sin contexto claro).                                 | Se reemplazaron por lenguaje natural y orientativo para el usuario ("Inscribirme", "Limpiar formulario").         |
| **3. Control y libertad del usuario**     | El botón de borrado inmediato borraba los datos de golpe sin dar opción a marcha atrás.                 | Se agregó una ventana emergente de confirmación (`confirm`) antes de limpiar por completo los campos.             |
| **4. Prevención de errores**              | Permitía enviar datos vacíos o con formatos incorrectos sin restricciones previas.                      | Se añadieron validaciones de campos obligatorios y tipos de datos (como correo electrónico).                      |
| **5. Reconocimiento antes que recuerdo**  | Los campos carecían de etiquetas persistentes o usaban marcadores temporales que se borraban.           | Se integraron etiquetas semánticas (`<label>`) fijas y agrupaciones claras mediante `<fieldset>`.                 |

## 2. Leyes de UX Aplicadas

- **Ley de Fitts:** Los botones principales de acción se diseñaron con un área de clic grande (mínimo 44px de alto) y separados de los botones secundarios para evitar clics accidentales.
- **Ley de Hick:** La selección de opciones complejas se organizó y agrupó por categorías lógicas (mediante `<optgroup>`), reduciendo el tiempo de decisión del usuario.
- **Ley de Miller:** La información y los campos del formulario se fragmentaron en bloques numerados para no saturar cognitivamente al usuario.

## 3. Accesibilidad y Estilos

- Uso de variables CSS (`:root`) para mantener consistencia de colores.
- Foco visible accesible (`:focus-visible`) para navegación exclusiva por teclado (`Tab` y `Enter`).
- Contraste de color superior a 4.5:1 y textos alternativos (`alt`) en imágenes.
