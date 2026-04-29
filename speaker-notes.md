# Guion Oral

## Final 01 - Slide 01 - Portada

Presentar la charla como una demo practica centrada en OpenCode + Plannotator. Vamos a ver cómo construir QRGen paso a paso, asistidos por IA y con un control total sobre el plan de ejecución.

## Final 15 - Slide 07D - OpenCode: Inicializar Un Proyecto

Explicar que `/init` es el primer paso en un repo nuevo. Analiza el entorno y prepara OpenCode para entender el lenguaje y herramientas que vamos a usar.

## Final 18 - Slide 07G - OpenCode: Plugins y Plannotator

Aquí está el "secreto" para tener todo el poder:
1. **Instalación**: Plannotator se instala como una herramienta del sistema.
2. **Inicialización**: Una vez que el proyecto tiene su `/init`, debemos registrar el plugin.
3. **Registro Correcto (TIP TÉCNICO)**: OpenCode a veces puede intentar registrarlo como `plugins` (plural), pero la clave correcta en `.opencode/opencode.json` es `plugin` (en singular).
   * **Ejemplo del JSON**: `{ "plugin": ["@plannotator/opencode@latest"] }`.
Una vez guardado el archivo, OpenCode "aprende" automáticamente a usar las herramientas de planificación.

## Final 19 - Slide 07H - OpenCode + Plannotator: Primer Uso

Mostrar la dinámica interactiva sobre las slides. Abrimos Plannotator, anotamos una mejora, y OpenCode la aplica. Es un flujo de "Digo qué quiero -> La IA propone -> Yo apruebo -> La IA ejecuta".

## Final 31 - Slide 11 - Plannotator en QRGen

Ahora aplicamos el mismo rigor al proyecto real.
- **Carga**: Abrimos Plannotator sobre `fases-qrgen.md`.
- **Modo Plan**: Siempre verificar que estamos en Modo Plan antes de empezar, para que el asistente no se adelante a escribir código sin nuestra validación.
- **Control Humano**: Nosotros somos los directores de obra; OpenCode es el ingeniero que ejecuta. Marcamos hitos como "final" a medida que la demo avanza.
