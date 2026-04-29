# Comandos Relevantes

## Presentacion

```bash
cd /home/mariano/Documentos/proyectos/presentacion-opencode
npm install
npm run dev
npm run build
```

## QRGen - Desarrollo Local

```bash
npm install
npm run dev
npm run build
npx serve dist
```

## QRGen - Hash SHA256 Para Passwords

```bash
echo -n "password-del-usuario" | sha256sum
```

Formato del archivo `passwords`:

```text
usuario:hashSHA256
```

## QRGen - Deploy Manual Sugerido

```bash
npm run build
cp passwords dist/
cp -r dist/* ../qrgen-pages/
cd ../qrgen-pages
git add .
git commit -m "deploy"
git push origin gh-pages
```

## OpenCode

### Instalacion

```bash
curl -fsSL https://opencode.ai/install | bash
npm install -g opencode-ai
brew install anomalyco/tap/opencode
```

### Verificacion y ayuda

```bash
opencode --version
opencode --help
opencode auth list
opencode models
```

### Autenticacion y modelos

```bash
opencode auth login
opencode auth list
opencode models --refresh
```

En TUI:

```text
/connect
/models
```

### Inicializacion de proyecto

```bash
cd /ruta/del/proyecto
opencode
```

Dentro de la TUI:

```text
/init
```

### CLI no interactiva

```bash
opencode run "Resume el objetivo del proyecto"
opencode run --file descriptor-proyecto-qrgen.md "Propone fases de implementacion"
opencode run --continue "Continua con la fase siguiente"
opencode run --format json "Resume el estado actual"
```

### Sesiones

```bash
opencode session list
opencode session list -n 5
opencode --continue
opencode --session <session-id>
opencode export <session-id>
opencode export <session-id> > session.json
opencode import session.json
```

En TUI:

```text
/sessions
/rename
/compact
/summarize
```

### Plugins

Plugins locales:

```text
.opencode/plugins/
~/.config/opencode/plugins/
```

Plugins npm en `opencode.json`:

```json
{
  "plugin": ["opencode-helicone-session", "@org/plugin"]
}
```

### TUI basica

```bash
opencode
opencode /ruta/del/proyecto
```

Comandos dentro de la TUI:

```text
@archivo
!comando
/help
/init
/sessions
/new
/undo
/redo
/export
/share
```
