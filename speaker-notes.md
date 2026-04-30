# Guion Oral Técnico - Restauración Total de Fidelidad

## Slide 01 - Portada
Presentar la charla como una demo de ingeniería asistida: "OpenCode + Plannotator: Del plan al deploy con QRGen". Explicar que OpenCode es el motor de ejecución en la terminal y Plannotator el cerebro estratégico que garantiza el orden y el control.

## Slide 02 - Objetivo
Flujo lineal de la demo: Idea -> Decisiones -> Planificación -> Ejecución asistida -> QA -> Deploy automático. Resaltar que no es teoría aislada; es una aplicación real construida en vivo.

## Slide 03 - QRGen en una Frase
Definir el producto: Generador de QR estático (Vue 3 + Vite) con composición visual sobre plantillas. Un MVP que cubre desafíos de auth local, Canvas API y automatización de despliegue.

## Slide 04 - La Presentación También Es Un Proyecto
Meta-demo: Estamos en `/home/mariano/Documentos/proyectos/presentacion-opencode`. Estas slides son Markdown, el build es Marp y el despliegue es GitHub Actions. La documentación técnica debe ser versionada como el código.

## Slide 05 - Slides como Plan
Explicar el ciclo: Anotamos `slides-plan.md`, OpenCode lee el contexto y aplica cambios a `slides.md`. Es un flujo de "Digo qué quiero -> IA aplica -> Yo valido". El plan manda sobre la IA.

## Slide 06 - Desglose: Estado
Detallar los estados del plan para la audiencia:
- **idea**: Intención inicial.
- **borrador**: Primera versión no revisada.
- **anotada**: El usuario pidió cambios.
- **revisada**: La IA aplicó los cambios.
- **final**: Versión aprobada para la presentación.

## Slide 07 - Desglose: Objetivo
El objetivo de cada slide evita que la charla se disperse. Si el objetivo es "explicar la instalación", la slide no debe hablar de modelos. Es nuestro criterio de calidad innegociable.

## Slide 08 - Desglose: Anotaciones
El poder de la corrección humana. Escribimos notas ("poné esto en rojo", "agregá este comando") y la IA las procesa para actualizar el producto final sin intervención manual en el código Marp.

## Slide 09 - Desglose: Acción Final
El comando técnico que une el plan con el resultado. Es la instrucción exacta que le damos al agente para que materialice los cambios en las slides finales.

## Slide 10 - Que Es OpenCode en esta Demo
Definir OpenCode como un asistente embebido en el repo. No es un chatbot; lee contexto, propone planes, escribe código y ejecuta verificaciones sin salir de tu terminal.

## Slide 11 - Instalacion Y Ejecucion De OpenCode
Hoja de ruta para empezar: Instalación, Verificación de CLI, Autenticación, Inicialización y primer contacto con la TUI interactiva.

## Slide 12 - OpenCode: Instalacion
Comandos para traer la herramienta:
- `curl -fsSL https://opencode.ai/install | bash` (Recomendada).
- `npm install -g opencode-ai` (Ecosistema Node.js).
- `brew install anomalyco/tap/opencode` (macOS/Linux).

## Slide 13 - OpenCode: Verificacion Y Ayuda
Comprobar binario: `opencode --version`. Descubrimiento: `opencode --help`. Es el primer paso de cualquier ingeniero al validar su entorno de trabajo.

## Slide 14 - OpenCode: Autenticacion Y Modelos
Conexión con el cerebro de IA:
- `opencode auth login`: Para el proveedor.
- `opencode models --refresh`: Para actualizar la lista de motores.
- **SEGURIDAD**: Nunca mostrar claves en pantalla. El icono 🔒 nos recuerda proteger la privacidad.

## Slide 15 - OpenCode: Inicializar Un Proyecto
Fundamental: `/init` en la TUI. Esto genera `AGENTS.md`, la "personalidad" del repo que le indica a OpenCode qué reglas seguir y qué herramientas usar en este proyecto específico.

## Slide 16 - OpenCode: CLI No Interactiva
El poder de `opencode run`. Ideal para tareas rápidas como resúmenes de archivos o automatización por scripts. Podemos inyectar archivos de contexto con el flag `--file`.

## Slide 17 - OpenCode: Sesiones Desde CLI
Control del historial:
- `opencode session list -n 5`: Ver lo último.
- `opencode export <id> > session.json`: Persistir el conocimiento.
- `/rename`: Comando vital para no perderse entre fases (ej: `QRGen - Fase 1`).

## Slide 18 - OpenCode: Plugins y Plannotator
Cómo activar herramientas avanzadas:
1. Instalar Plannotator.
2. `/init` del proyecto.
3. Editar `.opencode/opencode.json`. 
**OJO**: La clave es `"plugin"` en singular. Si pones "plugins", fallará la carga. 

## Slide 19 - OpenCode + Plannotator: Primer Uso
Demo interactiva: Anotamos `slides-plan.md`, el agente aplica cambios a `slides.md`, y validamos con `npm run build`. Sincronía Plan -> Producto en tiempo real.

## Slide 20 - Dos Contextos, Una Misma Dinamica
Aclaración de entorno:
- Contexto A: Presentación (este repo).
- Contexto B: QRGen (demo real).
Desde acá, nos mudamos definitivamente a construir la App QRGen.

## Slide 21 - OpenCode: TUI Basica (Sintaxis @)
Referencias de contexto:
- `@src/App.vue`: Trae código al contexto.
- `@explore` / `@general`: **Subagentes**, no archivos. `@explore` lee código; `@general` resuelve lógica pura.
- `!comando`: Shell directo.

## Slide 22 - Tipos De Uso / UI
Mapa de interfaces: CLI para rapidez, TUI para desarrollo, Web para demos remotas con CORS e IDE para refinamiento de componentes Vue con resaltado visual.

## Slide 23 - Aclaracion: UI, Uso Y Modo
Desmitificar la tecla `Tab`: Solo alterna entre **Plan Mode** (seguridad, solo propuesta) y **Build Mode** (ejecución y escritura). No cambia entre interfaces físicas.

## Slide 24 - UI: CLI No Interactiva (Caso QRGen)
Antes de abrir la TUI pesada de desarrollo, le pedimos un resumen del descriptor con `opencode run`. Claridad mental instantánea antes de empezar a codear.

## Slide 25 - UI: TUI sobre QRGen
Abrimos el proyecto real: `opencode /home/mariano/Documentos/proyectos/qrgen_demo`. Iniciamos el desarrollo interactivo sobre el repo de la App, con el agente consciente del stack Vue 3.

## Slide 26 - UI: Web / Attach (CORS y Lab)
Comando: `opencode web --port 4096 --hostname 0.0.0.0 --cors "*"`. 
El flag `--cors "*"` permite que dispositivos externos (tablet, móvil) se conecten a la TUI web de la demo sin bloqueos de seguridad del navegador.

## Slide 27 - UI: IDE
Mencionar extensiones integradas (ej. VS Code). Complemento visual ideal para cuando OpenCode escribe componentes complejos y queremos revisar los diffs.

## Slide 28 - Modo Plan / Build
Disciplina de trabajo: Siempre empezamos en Plan. Acordamos estructura y librerías. Cuando el plan es sólido, pulsamos `Tab` y pasamos a Build para materializar los archivos.

## Slide 29 - Primer Prompt QRGen (Mando Senior)
Lanzamiento profesional: 
"Actúa como un Ingeniero de Software Senior experto en Vue 3. Vamos a trabajar en la carpeta local `/home/mariano/Documentos/proyectos/qrgen_demo`. Inicia el proyecto QRGen asociado al repo `magm3333/qrgen_demo`. Tecnología: Vue 3 + Vite. Despliega en GitHub Pages. Objetivo: Aplicación estática para generar códigos QR. Funcionalidad inicial: debe pedir un texto, generar el QR automáticamente y permitir descargarlo como JPG y PNG. Tu primera tarea: Generá el plan de fases completo (Fases 1 a 7) y guardalo en un archivo llamado `fases-qrgen.md` en la raíz del proyecto. No implementes código todavía."

## Slide 30 - Plannotator en QRGen
Cargamos el plan interactivo.
- **TIP**: Si hay conflicto de contexto, forzar path absoluto:
"Carga un NUEVO plan desde /qrgen_demo/fases-qrgen.md usando la herramienta Plannotator."

## Slide 31 - Metodo de Demo: QRGen
Hoja de ruta: 5 hitos reales. La Fase 1 incluye el deploy automático. No avanzamos sin validar que la "tubería" de entrega funciona en internet.

## Slide 32 - Fase 1: Estructura Base y Deploy
Ejecución de `npm create vite`. Configuración del `base URL` en `vite.config.js`. Setup de GitHub Actions. El resultado es la App vacía pero publicada en internet.

## Slide 33 - Fase 2: Generador QR Minimo
Instalación de `qrcode`. Creación de `QRGenerator.vue`. Lógica reactiva: Texto -> Canvas -> QR. Primer valor funcional visible para el usuario.

## Slide 34 - Fase 3: Login Estatico SHA256
Estrategia de seguridad pragmática:
- Generar hash: `echo -n "pass" | sha256sum`.
- Validar con `crypto.subtle.digest` en el navegador.
- Sin backend, app 100% estática y segura.

## Slide 35 - Fase 4: Editor Visual Basico
Composición visual. Área de trabajo Canvas. Carga de imagen local y QR flotante encima para crear el diseño final.

## Slide 36 - Fase 5: Interaccion Profesional
Refinamiento de UX: Handles para escalar y rotar el QR. Cursores dinámicos. Lógica matemática compleja resuelta con la asistencia del agente.

## Slide 37 - Fase 6: Proyectos Y Exportacion
Persistencia en JSON para "guardar y cargar". Exportación final a imagen PNG mediante Canvas API para que el usuario pueda usar el QR generado.

## Slide 38 - Mapa de Archivos QRGen
Arquitectura limpia: `App.vue` (orquestador), `auth.js` (seguridad), `QRGenerator.vue` (lógica core), `passwords` (hashes).

## Slide 39 - Checklist de Demo
Checklist del presentador: Repos limpios, imágenes listas, acceso GitHub verificado (SSH/gh). No depender de tokens pegados en pantalla.

## Slide 40 - Comandos Relevantes
Pantalla de referencia para la audiencia: comandos de build, generación de hashes y despliegue manual.

## Slide 41 - Publicacion de esta Presentacion
Cerrar el círculo: Mostrar que esta charla es transparente y vive en `magm3333/presentacion-opencode`.

## Slide 42 - Conclusiones
Los 3 pilares: Velocidad (OpenCode), Control (Plannotator) y Seguridad (Flujo Incremental).

## Slide 43 - Proximos Pasos
Escalabilidad: SVG export, PWA, plantillas dinámicas desde servidor.

## Slide 44 - Cierre
Despedida con un QR generado por la App real que apunta al repo. ¡Gracias por su atención!
