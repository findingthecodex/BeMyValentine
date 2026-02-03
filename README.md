# BeMyValentine

En Blazor WebAssembly-app för Alla Hjärtans Dag! 💖

## GitHub Pages Deployment

Denna app är konfigurerad för automatisk deployment till GitHub Pages med GitHub Actions.

### Hur det fungerar

1. När du pushar till `main`-branchen triggas workflow:en automatiskt
2. GitHub Actions bygger Blazor-projektet med `dotnet publish`
3. Base href i `index.html` uppdateras automatiskt för GitHub Pages
4. Den färdiga siten deployas till `gh-pages`-branchen
5. Siten publiceras på: `https://<username>.github.io/BeMyValentine/`

### Manuell deploy

Du kan också köra workflow:en manuellt från Actions-fliken i GitHub.

### Första gången

Efter första deploy:en, gå till Repository Settings → Pages och verifiera att:
- Source är satt till `gh-pages` branch
- Root är vald som mapp

GitHub kommer vanligtvis att auto-konfigurera detta när `gh-pages`-branchen skapas.
