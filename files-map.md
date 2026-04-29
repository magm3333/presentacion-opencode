# Mapa De Archivos

## Presentacion

| Archivo | Rol |
|---|---|
| `slides-plan.md` | Plan vivo y corregible por slide |
| `slides.md` | Presentacion final en Markdown/Marp |
| `speaker-notes.md` | Guion oral separado |
| `demo-checklist.md` | Checklist operativo de demo |
| `commands.md` | Comandos relevantes |
| `files-map.md` | Mapa de archivos de presentacion y QRGen |
| `themes/qrgen.css` | Tema visual simple |
| `assets/images/` | Imagenes, capturas y diagramas |
| `.github/workflows/deploy.yml` | Deploy automatico a GitHub Pages |

## QRGen

| Archivo | Rol |
|---|---|
| `README.md` | Instalacion, uso, deploy y usuarios |
| `deploy.sh` | Automatizacion del deploy sin secretos |
| `vite.config.js` | Configuracion Vite y `base: '/qrgen/'` |
| `passwords` | Usuarios y hashes SHA256 |
| `public/passwords` | Copia publica consumible por la app estatica |
| `src/App.vue` | Layout general, login y orquestacion |
| `src/auth.js` | Autenticacion estatica con SHA256 |
| `src/main.js` | Entrada Vue |
| `src/style.css` | Estilos globales |
| `src/components/QRGenerator.vue` | Generacion y exportacion de QR |
| `src/components/TemplateEditor.vue` | Editor visual, fondo, transformaciones y exportacion |
