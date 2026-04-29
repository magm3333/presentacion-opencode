# Slides

Este archivo es la fuente editable de la presentacion. Cada slide se corrige como una unidad de plan asistida por OpenCode: objetivo, contenido, demo, anotaciones, decisiones y accion para la version final.

Estados (solo para seguimiento interno): `borrador`, `anotada`, `final`.

## Indice De Slides

Nota: Los enlaces internos de Markdown sirven para navegacion. El flujo de trabajo se basa en anotar este archivo y pedirle a OpenCode que aplique los cambios a `slides.md`.

- 🟢 final - Slide 01 - `SLIDE-01` - [Portada](#slide-01)
- 🟢 final - Slide 02 - `SLIDE-02` - [Objetivo De La Demo](#slide-02)
- 🟢 final - Slide 03 - `SLIDE-03` - [QRGen En Una Frase](#slide-03)
- 🟢 final - Slide 04 - `SLIDE-04` - [La Presentacion Tambien Es Un Proyecto](#slide-04)
- 🟢 final - Slide 05 - `SLIDE-05` - [Slides como Guia de Trabajo](#slide-05)
- 🟢 final - Slide 10 - `SLIDE-06` - [Que Es OpenCode En Esta Demo](#slide-10)
- 🟢 final - Slide 11 - `SLIDE-07` - [Instalacion Y Ejecucion De OpenCode](#slide-11)
- 🟢 final - Slide 12 - `SLIDE-07A` - [OpenCode: Instalacion](#slide-12)
- 🟢 final - Slide 13 - `SLIDE-07B` - [OpenCode: Verificacion Y Ayuda](#slide-13)
- 🟢 final - Slide 14 - `SLIDE-07C` - [OpenCode: Autenticacion Y Modelos](#slide-14)
- 🟢 final - Slide 15 - `SLIDE-07D` - [OpenCode: Inicializar Un Proyecto](#slide-15)
- 🟢 final - Slide 16 - `SLIDE-07E` - [OpenCode: CLI No Interactiva](#slide-16)
- 🟢 final - Slide 17 - `SLIDE-07F` - [OpenCode: Sesiones Desde CLI](#slide-17)
- 🟢 final - Slide 18 - `SLIDE-07G` - [OpenCode: Plugins y Plannotator](#slide-18)
- 🟢 final - Slide 19 - `SLIDE-07H` - [OpenCode + Plannotator: Primer Uso (Meta-demo)](#slide-19)
- 🟢 final - Slide 20 - `SLIDE-20` - [Dos Contextos, Una Misma Dinamica](#slide-20)
- 🟢 final - Slide 21 - `SLIDE-07I` - [OpenCode: TUI Basica](#slide-21)
- 🟢 final - Slide 22 - `SLIDE-08` - [Tipos De UI De OpenCode](#slide-22)
- 🟢 final - Slide 23 - `SLIDE-08A` - [Aclaracion: UI, Uso Y Modo](#slide-23)
- 🟢 final - Slide 24 - `SLIDE-08B` - [CLI No Interactiva](#slide-24)
- 🟢 final - Slide 25 - `SLIDE-08C` - [TUI Sobre QRGen](#slide-25)
- 🟢 final - Slide 26 - `SLIDE-08D` - [Web / Attach](#slide-26)
- 🟢 final - Slide 27 - `SLIDE-08E` - [IDE](#slide-27)
- 🟢 final - Slide 28 - `SLIDE-08F` - [Modo Plan / Build](#slide-28)
- 🟢 final - Slide 29 - `SLIDE-09` - [Primer Prompt QRGen](#slide-29)
- 🟢 final - Slide 30 - `SLIDE-10` - [Manejo De Sesiones en QRGen](#slide-30)
- 🟢 final - Slide 31 - `SLIDE-11` - [Plannotator en el Flujo QRGen](#slide-31)
- 🟢 final - Slide 32 - `SLIDE-12` - [Metodo De Demo: QRGen](#slide-32)
- 🟢 final - Slide 33 - `SLIDE-13` - [Fase 1: Estructura Base y Deploy](#slide-33)
- 🟠 borrador - Slide 34 - `SLIDE-14` - [Fase 2: Generador QR Minimo](#slide-34)
- 🟠 borrador - Slide 35 - `SLIDE-15` - [Fase 3: Login Estatico SHA256](#slide-35)
- 🟠 borrador - Slide 36 - `SLIDE-16` - [Fase 4: Editor Visual Basico](#slide-36)
- 🟠 borrador - Slide 37 - `SLIDE-17` - [Fase 5: Interaccion Profesional](#slide-37)
- 🟠 borrador - Slide 38 - `SLIDE-18` - [Fase 6: Proyectos Y Exportacion](#slide-38)
- 🟠 borrador - Slide 39 - `SLIDE-19` - [Fase 7: Pulido Y Deploy Final](#slide-39)
- 🟠 borrador - Slide 40 - `SLIDE-20` - [Mapa De Archivos QRGen](#slide-40)
- 🟠 borrador - Slide 41 - `SLIDE-21` - [Checklist De Demo](#slide-41)
- 🟠 borrador - Slide 42 - `SLIDE-22` - [Comandos Relevantes](#slide-42)
- 🟠 borrador - Slide 43 - `SLIDE-23` - [Publicacion De La Presentacion](#slide-43)
- 🟠 borrador - Slide 44 - `SLIDE-24` - [Cierre](#slide-44)

<a id="slide-01"></a>

## Slide 01 - Portada

Estado: 🟢 final

Objetivo:
Presentar el tema: OpenCode + Plannotator aplicados al desarrollo completo de QRGen.

Contenido previsto:
- OpenCode + Plannotator.
- Construyendo QRGen desde cero hasta GitHub Pages.

<a id="slide-02"></a>

## Slide 02 - Objetivo De La Demo

Estado: 🟢 final

Objetivo:
Explicar que la charla no es teoria aislada, sino un flujo de trabajo completo.

Contenido previsto:
- Idea inicial.
- Planificacion por fases.
- Implementacion incremental.
- Refinamiento.
- Documentacion y deploy.

<a id="slide-05"></a>

## Slide 05 - Slides como Guia de Trabajo

Estado: 🟢 final

Objetivo:
Explicar como usamos este archivo Markdown para guiar el desarrollo de la presentacion.

Contenido previsto:
- El archivo Markdown como panel de control.
- Flujo: El usuario escribe notas, OpenCode lee el archivo (@) e implementa.
- Ventaja: El plan es versionable, humano y portable.

<a id="slide-18"></a>

## Slide 18 - OpenCode: Plugins y Plannotator

Estado: 🟢 final

Objetivo:
Enseñar a activar herramientas avanzadas mediante la configuracion de plugins.

Contenido previsto:
- Registro de Plannotator en `.opencode/opencode.json`.
- Clave correcta: `"plugin"` (singular).
- La importancia de la inicializacion con `/init`.

<a id="slide-19"></a>

## Slide 19 - OpenCode + Plannotator: Primer Uso (Meta-demo)

Estado: 🟢 final

Objetivo:
Mostrar Plannotator corrigiendo la propia presentacion.

Contenido previsto:
- Visual: plannotator-annotation-flow.svg (PLAN: slides-plan.md -> PRODUCTO: slides.md).
- Dinamica interactiva: Anotar -> OpenCode aplica -> Validar build.

<a id="slide-29"></a>

## Slide 29 - Primer Prompt QRGen

Estado: 🟢 final

Objetivo:
Lanzar el proyecto QRGen con un prompt profesional que defina el rol, el stack y el producto.

Contenido previsto:
- Rol: Ingeniero Senior.
- Stack: Vue 3 + Vite + Pages.
- Objetivo: Generador QR (texto -> QR) con descarga JPG/PNG.
- Tarea: Generar `fases-qrgen.md`.

<a id="slide-31"></a>

## Slide 31 - Plannotator en el Flujo QRGen

Estado: 🟢 final

Objetivo:
Mostrar Plannotator orquestando la construccion de QRGen.

Contenido previsto:
- Visual: qrgen-build-flow.svg (PLAN: fases-qrgen.md -> PRODUCTO: Site / App).
- Gestion de estados: idea -> anotada -> final.

<a id="slide-33"></a>

## Slide 33 - Fase 1: Estructura Base y Deploy

Estado: 🟢 final

Objetivo:
Detallar el primer hito: estructura base y despliegue inicial.

Contenido previsto:
- Bootstrap: `npm create vite@latest`.
- Config base path y GitHub Action.
- Resultado: App vacia publicada.

<a id="slide-34"></a>

## Slide 34 - Fase 2: Generador QR Minimo

Estado: 🟠 borrador

Objetivo:
Mostrar la implementación de la lógica core del QR.

Contenido previsto:
- Instalación de librería (`qrcode`).
- Creación de `QRGenerator.vue`.
- Input reactivo para texto.
- Renderizado en Canvas.

Accion para la version final:
Actualizar slide con captura del componente funcionando.

<a id="slide-35"></a>

## Slide 35 - Fase 3: Login Estatico SHA256

Estado: 🟠 borrador

Objetivo:
Agregar control de acceso sin backend.

Contenido previsto:
- Archivo `passwords`.
- Validacion con `crypto.subtle.digest`.
- Sesion en `localStorage`.

Accion para la version final:
Crear diagrama sutil de "Login Flow sin Backend".

<a id="slide-44"></a>

## Slide 44 - Cierre

Estado: 🟠 borrador

Objetivo:
Cerrar con aprendizajes y proximos pasos.

Contenido previsto:
- OpenCode acelera la ejecucion.
- Plannotator garantiza el orden.
- QRGen demuestra que el desarrollo asistido es real.
