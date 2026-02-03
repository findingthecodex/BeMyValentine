# BeMyValentine

En Blazor WebAssembly-app för Alla Hjärtans Dag! 💖

## Deployment

Denna app är konfigurerad för automatisk deployment till GitHub Pages med GitHub Actions.

### Live Demo
🔗 https://findingthecodex.github.io/BeMyValentine/

### Hur det fungerar

Varje push till `main`-branchen triggar automatiskt:
1. Bygger Blazor-projektet
2. Justerar base href för GitHub Pages
3. Deplojar till `gh-pages` branch
4. Publicerar på GitHub Pages

Du kan också trigga deployment manuellt från Actions-fliken.
