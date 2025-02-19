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
>        - Utiliza etiquetas HTML5 semánticas (<header>, <nav>, <main>, <article>, <section>, <footer>) para estructurar el contenido de manera lógica.
>    - Texto Alternativo para Imágenes:
>        - Asegúrate de que todas las imágenes tengan atributos alt descriptivos y concisos.
>        - Si la imagen es decorativa, utiliza un atributo alt vacío (alt="").
>    - Jerarquía de Encabezados:
>        - Utiliza encabezados (<h1> a <h6>) para estructurar el contenido de manera jerárquica y lógica.
>        - Asegúrate de que los encabezados estén anidados correctamente (ej. <h1> seguido de <h2>, no de <h3>).
>    - Contraste de Color:
>        - Verifica que el contraste entre el texto y el fondo cumpla con los requisitos de WCAG 2.2 (mínimo 4.5:1 para texto normal y 3:1 para texto grande).
>    - Accesibilidad con Teclado:
>        - Asegúrate de que todos los elementos interactivos (enlaces, botones, formularios) sean accesibles y utilizables mediante el teclado.
>        - Utiliza indicadores visuales de enfoque para elementos interactivos.
>    - Formularios Accesibles:
>        - Asocia etiquetas (<label>) con sus respectivos campos de formulario (<input>, <textarea>, <select>).
>        - Utiliza atributos placeholder para proporcionar información adicional en campos de formulario.
>        - Utiliza el atributo required para indicar campos obligatorios.
>    - Idioma del Contenido:
>        - Especifica el idioma del contenido utilizando el atributo lang en la etiqueta <html>.
>    - Etiquetas de Título:
>        - Asegúrate de que cada página tenga una etiqueta <title> descriptiva y concisa.
>    - Enlaces:
>        - Utiliza texto descriptivo en los enlaces.
>        - Evita el texto de enlace genérico como "haz clic aquí".
>    - Tablas:
>        - Utiliza encabezados de tabla (<th>) para proporcionar información sobre las columnas y filas.
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
