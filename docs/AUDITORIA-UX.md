# Auditoría de UX/UI - App de Notas

## Auditoría de Heurísticas de Nielsen

| Heurística                         | Problema Encontrado                                            | Solución Aplicada                                                            |
| :--------------------------------- | :------------------------------------------------------------- | :--------------------------------------------------------------------------- |
| **Visibilidad del estado**         | Al agregar o borrar una nota no había confirmación visual.     | Se añadió un mensaje de estado dinámico ("Nota guardada", "Nota eliminada"). |
| **Coincidencia con el mundo real** | Botones con íconos o textos crípticos del sistema.             | Se renombraron las acciones a lenguaje claro ("Guardar nota", "Eliminar").   |
| **Control y libertad**             | Al presionar borrar, la nota se eliminaba inmediatamente.      | Se incluyó una ventana de confirmación previa antes de eliminar.             |
| **Prevención de errores**          | Permitía crear notas completamente vacías al presionar enviar. | Se añadieron validaciones y el atributo `required` en los campos.            |
| **Reconocer, no recordar**         | No había etiquetas visibles en los campos de entrada.          | Se agregaron elementos `<label>` vinculados a cada `<input>` y `<textarea>`. |

## Leyes de UX Aplicadas

- **Ley de Fitts:** El botón principal para guardar la nota se diseñó con una altura mínima de 44px y abarca un área táctil amplia y accesible para facilitar el clic/tap.
- **Ley de Hick:** Se simplificó la interfaz clasificando o filtrando las notas por categorías simples para reducir el tiempo de decisión del usuario.
- **Ley de Miller:** Se dividió la creación de notas en bloques breves (Título, Categoría, Contenido) para no sobrecargar la memoria de trabajo.

## Accesibilidad

- **Contraste:** Cumple con la norma WCAG 2.2 AA (mínimo 4.5:1).
- **Teclado:** Se añadió el foco visible (`:focus-visible`) para navegación fluida con la tecla Tab.
- **Lighthouse:** Puntaje de accesibilidad obtenido $\ge$ 90.
