# Semana 3: Página web hecha con IA

En esta semana se pedía una página web creada con ayuda de IA, trabajada en grupo. En esta carpeta hay dos trabajos:

1. **TeslaCode**, la página del grupo, hecha entre cuatro personas.
2. **Riwi Task Manager**, mi propia página, hecha por mí con IA.

---

## 1. Página del grupo: TeslaCode

Academia interactiva de programación en español. Combina rutas visuales, lecciones por etapas (aprender, practicar y comprobar), simuladores y proyectos. Incluye un tutor de IA opcional (conectado a Gemini mediante una función de servidor en Vercel).

**Integrantes** (grupo distinto al de la semana 1):

- Juan Manuel Cardona Betancur
- Christian Camilo Benitez Gomez
- Ramael Gonzalez Florez
- Juan David Quintero Lopez

**Repositorio del proyecto:** https://github.com/Juan98698/Tesla-Code

**Página desplegada:** https://teslacode-snowy.vercel.app/#/inicio

**IAs utilizadas:** Gemini y ChatGPT. (Además, la página incluye un tutor de IA opcional conectado a Gemini, que es una función del producto y no una herramienta de construcción.)

**Mi aporte al grupo:** el grupo tomó como base el proyecto que construyó otro integrante. Mi aporte fue sobre todo de ideas, además de dar el visto bueno a muchas decisiones visuales y de funcionalidad. Mi trabajo propio con IA es el Riwi Task Manager, que está en la sección siguiente.

### Prompts

**Prompt del video de introducción** (la intro de 10 segundos que abre el sitio, con Nikola Tesla como personaje):

```
TESLACODE — THE AWAKENING

Create a photorealistic, cinematic 16:9 introduction video for TeslaCode, a futuristic programming education platform.

Duration: 18–22 seconds.
Resolution: 1920 × 1080 or higher.
Frame rate: 24 FPS.
Style: Cinematic realism, science fiction, electrical energy, deep navy blue and electric blue neon.

CHARACTER CONSISTENCY

Use the first reference image as the definitive character design for Nikola Tesla.

Maintain the same face, hairstyle, mustache, facial proportions, black Victorian three-piece suit, white shirt and dark tie throughout every scene.

Tesla must look like the same person in every frame.

SCENE 1 — ELECTRICAL AWAKENING (0–4 SECONDS)

Begin in complete darkness.

Small electric-blue sparks gradually illuminate the environment.

Electrical currents travel through futuristic circuits and scientific instruments.

Reveal an enormous laboratory containing Tesla coils, electromagnetic devices and glowing blue electrical arcs.

The camera moves slowly forward through the darkness.

Lighting is atmospheric, physically realistic and cinematic.
```

**Prompts del sitio web:** el proyecto se hizo solo con inteligencia artificial. Se partió de un primer prompt y luego se refinó.

**Primer prompt:**

```
Quiero que construyas una aplicación funcional de aprendizaje en programacion, optimizada para dispositivos móviles y WEB (PWA) orientada a personas que no saben programar. para que tengas un mejor contexto quiero que te bases en paginas como roadmap y platzi


No quiero únicamente una landing page, un prototipo visual o una colección de pantallas estáticas. Quiero un producto con arquitectura escalable, lógica de negocio, y funcionalidades conectadas. y buenas practiucas UX/UI. El proyecto se llamará provisionalmente TeslaCode.

VISIÓN DEL PRODUCTO
Mi pagina permitirá aprender, algoritmia, programacion, frontenn, backend, IA. desde nivel basico a nivel avanzado
El usuario podrá:
Buscar temas Generales, temas especificos, rutas de aprendizaje, cada carrera tendra su ruta de aprendizaje, por ejemplo machine learning debe tener una ruta de aprendizaje de todo lo que el usuario necesita aprender y el orden en el que lo debe estudiar para llegar a ser un ingeniero en machine learning. la plataforma debera proveer todos los conocimientos que se requiera segun la ruta. no quiero que sea algo aburrido para el aprendiz, quiero que sea algo dinamico y entretenido para el aprendiz.
para que tengas un mejor contexto quiero que te bases en paginas como roadmap y platzi (pero sin videocursos por el momento).
puedes proponer ideas, y apoyarte en esta plataforma para tomar lo mejor de ambas hacer algo mucho mejor.
```

**Prompt refinado:**

```
Actúa como un equipo senior de ingeniería de software, diseño instruccional y UX. Construye "TeslaCode": una plataforma web en español para aprender programación desde cero hasta nivel profesional, pensada para personas sin experiencia que buscan empleo (por ejemplo, jóvenes de un programa como Riwi, en Medellín). Nunca asumas conocimientos previos del estudiante.

## Producto
- Rutas: Fundamentos y lógica, Algoritmia, Python, JavaScript, Frontend, Backend, Bases de datos e Inteligencia artificial.
- Cada ruta tiene niveles con las lecciones que su contenido exija (sin cuotas simétricas). Cada lección declara los conceptos que requiere y los que introduce, y tiene teoría, ejemplos, actividades, quiz y fuentes.
- El temario completo de cada ruta es navegable aunque sus lecciones no estén escritas; las pendientes dicen "en preparación". Nunca finjas que existe contenido que no existe.
- Las dependencias forman un grafo real (una lección puede requerir varias), no una cadena lineal.
- Las lecciones se desbloquean en orden al superar el 80 % del quiz. Los quizzes miden comprensión real: predecir salida, depurar, ordenar y completar código.
- Tecnologías y versiones actuales: verifícalas con fuentes vigentes, fecha cada revisión y cita las fuentes.

## Enseñanza
- Fundamentos usa un pseudocódigo en español, cercano a Python y JavaScript (mostrar, leer, si/sino si/sino, segun, mientras, hacer … mientras, para, funcion/devolver). Documenta el dialecto y la equivalencia con PSeInt.
- Práctica en cuatro formatos de datos, sin código nuevo por ejercicio: Aprende (ejemplo explicado con pseudocódigo y Python), Decide (elegir la herramienta adecuada), Traza (paso a paso con memoria visible), Predice, Arregla (tocar la línea con el error y elegir la corrección) y Ordena. Cada práctica tiene objetivo, tema, tiempo estimado y se filtra por tipo y tema.
- Python real en el navegador (Pyodide) dentro de un iframe aislado con Worker, límite de 3 s y de tamaño, y casos de prueba automáticos.
- Lectura en voz alta de la teoría con la Web Speech API: fragmentos cortos, solo voces en español, sin leer el código, con pausa, velocidad y aviso si el dispositivo no tiene voz.
- Tutor de IA socrático con contexto de la lección: da pistas, no resuelve ejercicios evaluados y reconoce cuando no sabe.
- Motivación sana: XP, rachas por días consecutivos reales, logros, mapa visual de habilidades, repaso espaciado y copia de seguridad del progreso. Sin castigos por romper la racha.

## Arquitectura
- Sitio estático para GitHub Pages: JavaScript con módulos ES, sin framework ni paso de compilación para el contenido.
- Capas: core (DOM, eventos, almacenamiento), domain (reglas puras: desbloqueo, corrección, XP), repositories (carga de contenido bajo demanda), features (interfaz) y widgets (simuladores). Patrones: Repository, Strategy, Observer y carga diferida.
- Contenido en JSON: un archivo por ruta (temario) y por lección. El progreso vive en localStorage, con esquema validado.
- El tutor usa una función serverless: la clave nunca llega al navegador; valida origen, tamaño, formato y roles; limita el uso con contadores atómicos y falla cerrado.
- Un validador de contenido bloquea el build si una lección usa un concepto antes de enseñarlo, si faltan archivos o si un quiz es inválido.

## Calidad y UX
- Móvil primero, con navegación inferior (Inicio, Rutas, Practicar, Progreso). Tema claro/oscuro, accesibilidad WCAG 2.2 AA, objetivos táctiles de 44 px y respeto a "reducir movimiento".
- Pruebas unitarias con cobertura alta, pruebas de accesibilidad y de navegador en 390 y 1440 px, formato automático y CI con acciones fijadas por hash y permisos de solo lectura.
- Seguridad: escapa todo HTML, usa política CSP, aísla la ejecución de código y no guardes secretos.
- Documenta arquitectura, guía de contenido, pruebas y licencias de cada asset. Respeta la ley colombiana de protección de datos.

## Forma de trabajar
1. Trabaja por fases, y al terminar cada una ejecuta todas las verificaciones y reporta resultados reales, incluido lo que no pudiste comprobar.
2. Prioriza pocas lecciones completas y profundas sobre muchas superficiales.
3. No inventes datos ni versiones: busca y cita.
4. Si algo es ambiguo, pregunta una sola cosa antes de continuar.

Primera fase: estructura del proyecto, validador, la ruta de Fundamentos con 10 lecciones completas y el centro de práctica. Entrega un resumen de lo hecho, lo pendiente y los riesgos.
```

---

## 2. Mi propia página: Riwi Task Manager

Plataforma para que los estudiantes de Riwi administren sus tareas, que están dispersas en distintos lugares y es difícil llevarlas en una sola línea de tiempo. Incluye panel, calendario, categorías, búsqueda, orden, modo claro y oscuro, y versión en español e inglés. Guarda los datos con `localStorage`.

- **Carpeta:** [`riwi-task-manager`](riwi-task-manager)
- **IA utilizada:** Claude (claude.ai)
- **Enlace para verla:** https://christian-b1998.github.io/entregables-IA/Trabajo-IA-Semana3/riwi-task-manager/
- **Cómo se hizo:** fue un proyecto de la materia de IA y prompts en Riwi, dentro de un concurso del mejor front. Las reglas no permitían editar el código a mano, así que todo el resultado salió de prompts.
- **Mi aporte:** definí la idea (una página para gestionar las tareas de los estudiantes de Riwi, con su identidad visual y en dos idiomas) y, con ayuda de la IA, la convertí en un prompt detallado con criterios de aceptación y un entregable final claro.
- **Prompt utilizado:** el prompt completo está en el [README de `riwi-task-manager`](riwi-task-manager/README.md).

---

## Qué aprendí

Aprendí a escribir mejores prompts para obtener un resultado más cercano a lo que espero. Para eso hay que incluir de entrada:

- Las reglas de negocio.
- El UX/UI.
- Las tecnologías.
- La paleta de colores.
