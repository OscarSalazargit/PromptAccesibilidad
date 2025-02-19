# Prompt para Automatizar y Mejorar la Accesibilidad Web con Asistentes de Programación

## Trabajos Realizados

Se ha solicitado a varias IAs que nos ayudasen a generar un prompt para cumplir con los requerimientos de buenas prácticas para que esto fuera posible. Hemos obtenido varios prompts, hemos descartado los menos útiles y descriptivos, y hemos dejado finalmente solo tres, uno de ChatGPT, otro de Qwen, otro de Gemini y el último de Mistral.

## Video de Cómo se Realizan las Pruebas

Mismo HTML, mismo prompt.

## Proceso

### 1. Se Genera la Misma Pregunta para los Cinco Elegidos:

Se les pregunta a las IAs cuáles son las mejores para generar IA:

**Pregunta:** 
"Dime las tres mejores IAs para generar código de HTML y CSS que no sean de WordPress."

**Respuestas:**

- **Gemini:**
  - GitHub Copilot
  - Tabnine
  - CSS Scan

- **ChatGPT:**
  - ChatGPT
  - GitHub Copilot
  - Cedeium

- **Qwen:**
  - Jasper
  - Runway
  - DeepCode

- **Mistral:**
  - Easy-Peasy AI
  - MyMap AI
  - GitHub Copilot

**Conclusión:** 
Por deducción y mayoría absoluta, GitHub Copilot será quien de solución al mejor prompt.

### 2. Pruebas con GitHub Copilot

Tras las pruebas con los cuatro mejores prompts que hemos conseguido, estos son los resultados.

Pagina generada original con los estilos:
![Imagen foto original](/origen/webOrigenFront.jpg)
**Errores**
- Wave
![Errores de Wave](/origen/Errores%20en%20Wave%20sin%20samantica.jpg)
- Equals
![Errores de equals](/origen/errores%20sin%20semantica%20todo%20divs%20Equal.jpg)

### Test con ChatGPT 

- Prompt:
> Genera un código HTML completamente accesible según las WCAG 2.2 nivel AA. Debe cumplir con los siguientes requisitos:
> 
> Uso correcto de etiquetas semánticas de HTML5 para estructurar el contenido (header, main, nav, article, section, aside, footer).
> Compatibilidad con navegación por teclado (sin tabindex innecesarios, con un orden lógico de tabulación).
> Contrastes adecuados en colores y tipografía accesible (mínimo 4.5:1 para texto normal, 3:1 para UI).
> Elementos interactivos accesibles (botones con etiquetas claras, enlaces con descripciones significativas, formularios con etiquetas asociadas y mensajes de error accesibles).
> Uso de ARIA solo cuando sea estrictamente necesario y conforme a las mejores prácticas.
> Multimedia accesible (subtítulos en videos, descripciones en imágenes mediante alt, controles visibles para contenido multimedia).
> Compatibilidad con tecnologías de asistencia (lectores de pantalla, ampliadores de texto, comandos de voz).
> Validación con herramientas de accesibilidad como Lighthouse y axe DevTools.
> El código debe ser limpio, comentado cuando sea necesario y escrito bajo la metodología BEM para CSS.

Codigo generado por ChatGPT con su prompt
[Index.html](/chatgpt/solucionChatGPT.html)
- Respuesta de Wave
![Respuesta de Wave](/chatgpt/solucion%20chat%20gpt%20WAVE.jpg)
- Respuesta de EqualWEb
![Respuesta de Equalweb](/chatgpt/solucion%20chat%20gpt%20Equals.jpg)

### Test con Gemini

- Prompt:
>Tarea: Optimizar el código HTML para cumplir con las WCAG 2.2 (WAI) yDirectrices de Accesibilidad para el Contenido Web 2.2 (WCAG 2.2) y el uso adecuado de etiquetas ARIA.

>Nivel de Accesibilidad: A, AA (y opcionalmente AAA).

>Instrucciones:
>1. Analiza la estructura HTML proporcionada e identifica las áreas que requieren mejoras de accesibilidad.
>2. Aplica las siguientes modificaciones para cumplir con los criterios de accesibilidad:
>    - Atributos ARIA:
>        - Utiliza roles ARIA (ej. role="navigation", role="main") para definir la estructura y el propósito del contenido.
>        - Agrega atributos ARIA (ej. aria-label, aria-describedby, aria-labelledby) para proporcionar información adicional a tecnologías de asistencia.
>        - Utiliza propiedades ARIA (ej. aria-expanded, aria-hidden) para indicar el estado de elementos interactivos.
>    - Semántica HTML5:
>        - Utiliza etiquetas HTML5 semánticas (< header>, < nav>, < main>, < article>, < section>, < footer>) para estructurar el contenido de manera lógica.
>    - Texto Alternativo para Imágenes:
>        - Asegúrate de que todas las imágenes tengan atributos alt descriptivos y concisos.
>        - Si la imagen es decorativa, utiliza un atributo alt vacío (alt="").
>    - Jerarquía de Encabezados:
>        - Utiliza encabezados (< h1> a < h6>) para estructurar el contenido de manera jerárquica y lógica.
>        - Asegúrate de que los encabezados estén anidados correctamente (ej. < h1> seguido de < h2>, no de < h3>).
>    - Contraste de Color:
>        - Verifica que el contraste entre el texto y el fondo cumpla con los requisitos de WCAG 2.2 (mínimo 4.5:1 para texto normal y 3:1 para texto grande).
>    - Accesibilidad con Teclado:
>        - Asegúrate de que todos los elementos interactivos (enlaces, botones, formularios) sean accesibles y utilizables mediante el teclado.
>        - Utiliza indicadores visuales de enfoque para elementos interactivos.
>    - Formularios Accesibles:
>        - Asocia etiquetas (< label>) con sus respectivos campos de formulario (< input>, < textarea>, < select>).
>        - Utiliza atributos placeholder para proporcionar información adicional en campos de formulario.
>        - Utiliza el atributo required para indicar campos obligatorios.
>    - Idioma del Contenido:
>        - Especifica el idioma del contenido utilizando el atributo lang en la etiqueta < html>.
>    - Etiquetas de Título:
>        - Asegúrate de que cada página tenga una etiqueta < title> descriptiva y concisa.
>    - Enlaces:
>        - Utiliza texto descriptivo en los enlaces.
>        - Evita el texto de enlace genérico como "haz clic aquí".
>    - Tablas:
>        - Utiliza encabezados de tabla (< th>) para proporcionar información sobre las columnas y filas.
>        - Utiliza el atributo scope para asociar encabezados de tabla con sus respectivas celdas.
>3. Valida el código modificado utilizando herramientas de validación de accesibilidad como WAVE, Axe y Lighthouse.
>4. Ajusta el código y el prompt según sea necesario hasta que cumpla con los criterios de accesibilidad de nivel AA (y opcionalmente AAA).

>Código HTML a modificar:

Codigo generado por Gemini con su prompt
[Index.html](/gemini/solucionGemini.html)
- Respuesta de Wave
![Respuesta de Wave](/gemini/resultadoGeminiWave.jpg)
- Respuesta de EqualWEb
![Respuesta de Equalweb](/gemini/resultado%20Gemini%20con%20equal.jpg)

### Test con Mistral

- Prompt:
> Prompt para Mejorar la Accesibilidad Web según WCAG 2.2
> Objetivo
> Modificar el código HTML para cumplir con los estándares de accesibilidad web establecidos por la normativa WCAG 2.2 (WAI) y el uso adecuado de etiquetas ARIA. El código debe cumplir con los criterios de accesibilidad de nivel AA (y opcionalmente AAA).
> 
> Instrucciones
> Atributos ARIA:
> 
> Agrega atributos ARIA adecuados para formularios, botones, imágenes y enlaces.
> Ejemplo: `<button aria-label="Enviar formulario">Enviar</button>`.
> Semántica del Documento:
> 
> Utiliza etiquetas HTML5 semánticas como `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`, etc.
> Ejemplo: `<header><h1>Título Principal</h1></header>`.
> Textos Alternativos:
> 
> Asegúrate de que todas las imágenes tengan textos alternativos descriptivos.
> Ejemplo: `<img src="imagen.jpg" alt="Descripción de la imagen">`.
> Jerarquía de Encabezados:
> 
> Mantén una jerarquía adecuada de encabezados (h1, h2, h3, etc.).
> Ejemplo: `<h1>Título Principal</h1>`, `<h2>Subtítulo</h2>`.
> Contraste y Legibilidad:
> 
> Implementa controles de contraste adecuados entre texto y fondo.
> Ejemplo: Usa herramientas como WAVE para verificar el contraste.
> Navegación por Teclado:
> 
> Asegura que todos los elementos interactivos sean accesibles mediante teclado.
> Ejemplo: Usa tabindex cuando sea necesario.
> Formularios Accesibles:
> 
> Asocia correctamente las etiquetas con los campos de formulario.
> Ejemplo: `<label for="nombre">Nombre</label><input id="nombre" type="text">`.
> Validación de Accesibilidad:
> 
> Valida la accesibilidad utilizando herramientas como WAVE, Axe, Lighthouse, Accessibility Insights, Access Assistant, ANDI y ARC Toolkit.
> Documenta los resultados obtenidos antes y después de la aplicación del prompt.
> Ejemplo de Código HTML Inicial
> 
> `<!DOCTYPE html>`
> `<html lang="es">`
> `<head>`
>     `<meta charset="UTF-8">`
>     `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
>     `<title>Ejemplo de Accesibilidad</title>`
> `</head>`
> `<body>`
>     `<div>`
>         `<h1>Título Principal</h1>`
>         `<p>Este es un párrafo de ejemplo.</p>`
>         `<img src="imagen.jpg" alt="">`
>         `<form>`
>             `<input type="text" placeholder="Nombre">`
>             `<button>Enviar</button>`
>         `</form>`
>     `</div>`
> `</body>`
> `</html>`
> Ejemplo de Código HTML Optimizado
> 
> `<!DOCTYPE html>`
> `<html lang="es">`
> `<head>`
>     `<meta charset="UTF-8">`
>     `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
>     `<title>Ejemplo de Accesibilidad</title>`
> `</head>`
> `<body>`
>     `<header>`
>         `<h1>Título Principal</h1>`
>     `</header>`
>     `<main>`
>         `<section>`
>             `<p>Este es un párrafo de ejemplo.</p>`
>             `<img src="imagen.jpg" alt="Descripción de la imagen">`
>         `</section>`
>         `<section>`
>             `<form>`
>                 `<label for="nombre">Nombre</label>`
>                 `<input id="nombre" type="text" aria-required="true">`
>                 `<button aria-label="Enviar formulario">Enviar</button>`
>             `</form>`
>         `</section>`
>     `</main>`
>     `<footer>`
>         `<p>Pie de página</p>`
>     `</footer>`
> `</body>`
> `</html>`
> Validación y Ajustes
> Aplicación del Prompt:
> 
> Aplica el prompt en un IDE con un asistente de programación (GitHub Copilot, ChatGPT, u otro).
> Evalúa los cambios generados en el código HTML.
> Validación:
> 
> Utiliza al menos tres herramientas de validación (WAVE, Axe, Lighthouse, etc.) para verificar la accesibilidad del código.
> Documenta los resultados obtenidos antes y después de la aplicación del prompt.
> Ajustes Iterativos:
> 
> Si el código no cumple con los criterios, ajusta el prompt y repite el proceso hasta lograr un resultado óptimo.
> Este prompt está diseñado para ser claro y efectivo, guiando al asistente de programación para realizar las modificaciones necesarias y cumplir con los estándares de accesibilidad WCAG 2.2.


Codigo generado por Mistral con su prompt
[Index.html](/mistral/solucionMistral.html)
- Respuesta de Wave
![Respuesta de Wave](/mistral/resultado%20mistral%20con%20wave.jpg)
- Respuesta de EqualWEb
![Respuesta de Equalweb](/mistral/resultado%20mistral%20con%20equals.jpg)

### Test con Qwen

- Prompt:

> "Refactoriza este código HTML para cumplir con los estáandares de accesibilidad WCAG 2.2 nivel AA (y opcionalmente AAA). Las modificaciones deben incluir:
> 
> 1. Semántica:
> - Reemplaza divs genéricos por etiquetas semánticas apropiadas (`<header>`, `<footer>`, `<main>`, `<section>`, `<article>`, etc.)
> - Asegura una estructura lógica y jerarquía correcta de encabezados (h1, h2, h3, etc.)
> 
> 2. Imágenes:
> - Agrega atributos alt descriptivos a todas las imágenes significativas
> - Usa alt="" para imágenes decorativas
> - Considera la relación entre el texto alternativo y el contexto del contenido
> 
> 3. Formularios:
> - Asocia cada campo de entrada con su etiqueta correspondiente usando el atributo 'for'
> - Incluye atributos ARIA relevantes como aria-labelledby o aria-describedby cuando sea necesario
> - Proporciona indicaciones claras sobre requisitos de campos obligatorios
> - Implementa mensajes de error accesibles mediante roles ARIA adecuados
> 
> 4. Enlaces:
> - Usa textos descriptivos en lugar de "Haz clic aquí" o "Leer más"
> - Asegura que los enlaces sean distinguibles sin depender únicamente de color
> 
> 5. Botones:
> - Etiqueta correctamente los botones con texto descriptivo
> - Usa atributos ARIA si es necesario para mejorar comprensión
> 
> 6. Tablas:
> - Define cabeceras de tabla usando `<th>` con scope adecuado
> - Usa atributos ARIA si es necesario para mejorar navegación
> 
> 7. Navegación por teclado:
> - Asegura que todos los elementos interactivos sean accesibles mediante teclado
> - Mantiene un orden lógico de tabulación
> 
> 8. Contraste:
> - Garantiza un contraste suficiente entre texto y fondo (al menos 4.5:1 para texto normal)
> 
> 9. Otros:
> - Añade landmarks ARIA si es necesario para mejorar navegación asistida
> - Elimina cualquier contenido parpadeante o que pueda causar problemas de accesibilidad
> - Asegura que todo el contenido sea accesible mediante múltiples formas (no solo dependiendo de un único sentido)
> 
> Genera el código modificado completo manteniendo la funcionalidad original pero mejorando la accesibilidad."

Codigo generado por Mistral con su prompt
[Index.html](/qwen/resultadoQwen.html)
- Ojo que tambien ha cambiado el diseño
![Cambio en el diseño](/qwen/cambio%20de%20diseño%20con%20qwen.jpg)
- Respuesta de Wave
![Respuesta de Wave](/qwen/errores%20de%20wave%20con%20qwen.jpg)
- Respuesta de EqualWEb
![Respuesta de Equalweb](/qwen/errores%20de%20qwen%20con%20equal.jpg)


Conclusion:
<h1>La IA no nos quitará el Trabajo!!</h1>
