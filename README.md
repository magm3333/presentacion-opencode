# Presentacion OpenCode + Plannotator

Presentacion introductoria sobre OpenCode y Plannotator usando QRGen como demo central de desarrollo completo.

La fuente editable esta organizada en dos niveles:

- `slides-plan.md`: plan vivo de la presentacion, corregible slide por slide.
- `slides.md`: presentacion final en Markdown/Marp para publicar en GitHub Pages.

## Desarrollo local

```bash
npm install
npm run dev
```

Abrir la URL local que muestra Marp.

## Build

```bash
npm run build
```

El HTML queda en `dist/index.html`.

## Publicacion

El workflow `.github/workflows/deploy.yml` publica `dist/` en GitHub Pages al hacer push a `main`.

No guardar tokens en este repositorio. Usar autenticacion local, GitHub Actions o secrets del repositorio.

## Flujo de correccion

1. Editar o comentar `slides-plan.md`.
2. Pasar slides a estado `revisada` o `final`.
3. Actualizar `slides.md` con esas decisiones.
4. Actualizar `speaker-notes.md` si cambia el guion.
5. Ejecutar `npm run build`.
6. Publicar en GitHub Pages.
