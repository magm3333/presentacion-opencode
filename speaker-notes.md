# Guion Oral Técnico - Restauración de Élite

## Slide 01 - Portada
Presentar la charla como una demo de ingeniería asistida de alta fidelidad. "OpenCode + Plannotator: Del plan al deploy con QRGen". Explicar que OpenCode es el motor de ejecución en la terminal y Plannotator el cerebro estratégico que garantiza el orden y el control.

## Slide 04 - La Presentación También Es Un Proyecto
Meta-demo: Estamos en `/home/mariano/Documentos/proyectos/presentacion-opencode`. Las slides son Markdown, el build es Marp y el deploy es GitHub Actions. La documentación técnica debe seguir el mismo rigor de versionado que el código de producción.

## Slide 05 - Slides como Plan
Explicar el ciclo de trabajo: Anotamos `slides-plan.md`, OpenCode lee el contexto y aplica cambios a `slides.md`. Es un flujo de "Digo qué quiero -> IA aplica -> Yo valido". El plan es la fuente de verdad innegociable.

## Slide 14 - OpenCode: Autenticacion Y Modelos
Seguridad ante todo. 
- Comandos: `opencode auth login`.
- **PRO TIP**: Si ya usas `gh auth login` en tu sistema, OpenCode a menudo puede heredar ese contexto de identidad.
- **SEGURIDAD**: Nunca mostrar claves en la terminal si hay público. El icono 🔒 nos recuerda proteger la privacidad del desarrollador y evitar el commit de secretos.

## Slide 15 - OpenCode: Inicializar Un Proyecto
Ejecutar `/init` genera `AGENTS.md`. Es la personalidad del repositorio. Le dice a OpenCode: "Acá usamos Vue 3, seguí estas reglas de estilo, usá estos comandos de build y respetá estas restricciones de arquitectura". Es la base del contexto operativo.

## Slide 17 - OpenCode: Sesiones Desde CLI
Manejo del historial:
- `opencode session list -n 5`: Ver lo más reciente para no saturar la terminal.
- `opencode export <id> > session.json`: Persistir el conocimiento fuera de la terminal.
- `/rename`: Comando vital para no perderse entre fases (ej: `QRGen - Fase 1 - Bootstrap`). Ayuda a la trazabilidad y organización mental.

## Slide 18 - OpenCode: Plugins y Plannotator (Punto Crítico)
Cómo activar Plannotator en cualquier repo nuevo:
1. Instalar herramienta globalmente.
2. `/init` del proyecto para preparar el workspace.
3. Editar manualmente `.opencode/opencode.json`. 
**DETALLE TÉCNICO VITAL**: La clave del JSON debe ser `"plugin"` en singular. Si pones "plugins" (plural), OpenCode ignorará la configuración y Plannotator no aparecerá.
JSON: `{ "plugin": ["@plannotator/opencode@latest"] }`.

## Slide 19 - Primer Uso (Meta-demo de Sincronía)
Gráfico PLAN (Markdown) -> PRODUCTO (Slides). Demostración visual de que el plan escrito guía la generación del entregable final. Sincronía total entre intención y ejecución.

## Slide 21 - OpenCode: TUI Basica (Sintaxis @)
Diferenciar referencias de contexto:
- `@archivo.vue`: Trae código al contexto para ser analizado o editado.
- `@explore` / `@general`: **Subagentes**. Importante: No son archivos. `@explore` es experto en lectura de código; `@general` en lógica y resolución de dudas genéricas.
- `!comando`: Corre shell (ej: `!npm run build`) y la salida vuelve a la IA como contexto de error o éxito.

## Slide 23 - Aclaracion: UI, Uso Y Modo
Desmitificar la tecla `Tab`: Solo alterna entre **Plan Mode** (seguridad, solo propuesta) y **Build Mode** (permiso de escritura de archivos). No cambia de la terminal al navegador web ni entre interfaces físicas.

## Slide 26 - UI: Web / Attach (CORS y Lab)
Uso remoto: `opencode web --port 4096 --hostname 0.0.0.0 --cors "*"`. 
El flag `--cors "*"` es la llave que permite que dispositivos externos (tablet, móvil) se conecten a la TUI web de la demo sin que el navegador bloquee la conexión por seguridad de origen.

## Slide 29 - Primer Prompt QRGen (Mando Senior)
El prompt de oro para arrancar la demo real:
"Actúa como un Ingeniero de Software Senior experto en Vue 3. Vamos a trabajar en la carpeta local `/home/mariano/Documentos/proyectos/qrgen_demo`. Inicia el proyecto QRGen asociado al repo `magm3333/qrgen_demo`. Tecnología: Vue 3 + Vite. Despliega en GitHub Pages. Objetivo: Aplicación estática para generar códigos QR. Funcionalidad inicial: debe pedir un texto, generar el QR automáticamente y permitir descargarlo como JPG y PNG. Tu primera tarea: Generá el plan de fases completo (Fases 1 a 7) y guardalo en un archivo llamado `fases-qrgen.md` en la raíz del proyecto. No implementes código todavía."

## Slide 30 - Plannotator en QRGen (Troubleshooting)
Si Plannotator carga el plan equivocado (el de las slides):
Prompt: "Carga un NUEVO plan ignorando el anterior desde el path absoluto /home/mariano/Documentos/proyectos/qrgen_demo/fases-qrgen.md usando la herramienta Plannotator." Esto rompe el conflicto de contexto global en la máquina y fuerza al agente a mirar el archivo correcto.

## Slide 33 - Fase 2: Generador QR Mínimo
Ver la IA instalando `qrcode`. El componente reactivo toma el texto del input y lo renderiza en el canvas. Validamos con `!npm run dev` para ver el nacimiento de la App en tiempo real.

## Slide 34 - Fase 3: Login Estático SHA256
Estrategia de seguridad pragmática:
- Generar Hash: `echo -n "password" | sha256sum`.
- Validación: Usamos `crypto.subtle.digest` en el frontend. Sin base de datos ni backend, mantenemos la app 100% estática pero con control de acceso funcional.

## Slide 40 - Comandos Relevantes
Ayuda memoria final para la audiencia:
- `npm run build`: Generar producción.
- `sha256sum`: Hashear claves.
- `git push origin gh-pages`: Desplegar.
- `opencode --session <id>`: Retomar contexto específico.

## Slide 44 - Cierre
Despedida con un QR generado por la App real construida durante la charla. Enlace al repositorio de la presentación. ¡Muchas gracias por su atención!
