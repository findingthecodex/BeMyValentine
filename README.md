# BeMyValentine

En Blazor WebAssembly-app för Alla Hjärtans Dag! 💖

## 🌐 Live Demo
https://findingthecodex.github.io/BeMyValentine/

## 🚀 GitHub Pages Deployment

Denna app är deployad till GitHub Pages via **Deploy from a branch**.

### Hur deployment fungerar

1. **Source-koden** finns på `main`-branchen
2. **Byggda filer** finns på `gh-pages-deploy`-branchen
3. GitHub Pages serverar direkt från `gh-pages-deploy`-branchen

### Hur du uppdaterar sidan

När du vill deploya ändringar:

```bash
# 1. Gör ändringar på main-branchen
git checkout main
# gör dina ändringar...
git add .
git commit -m "Din ändring"
git push origin main

# 2. Bygg projektet
dotnet publish ./BeMyValentine/BeMyValentine.csproj -c Release -o publish

# 3. Byt till deploy-branchen
git checkout gh-pages-deploy

# 4. Kopiera de nya filerna
cp -r publish/wwwroot/* .

# 5. Uppdatera base href (om behövs)
sed -i '' 's|<base href="/" />|<base href="/BeMyValentine/" />|g' index.html

# 6. Commit och pusha
git add -A
git commit -m "Update deployment"
git push origin gh-pages-deploy

# 7. Byt tillbaka till main
git checkout main
```

### Första gången (redan gjort)

Gå till **Settings → Pages** på GitHub och konfigurera:
- **Source:** Deploy from a branch
- **Branch:** `gh-pages-deploy`
- **Folder:** `/ (root)`

Sidan kommer vara live inom 1-2 minuter efter push! 💖

