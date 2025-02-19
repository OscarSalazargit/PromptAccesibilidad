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

- Promopt:
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
[Respuesta de Equalweb](/chatgpt/solucion%20chat%20gpt%20Equals.jpg)