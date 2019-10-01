# Vilhelm Prytz - Utbildningsmaterial

## Introduktion

Källkod till sidan [utb.vilhelmprytz.se](https://utb.vilhelmprytz.se).

Använder sig av motorn [Hugo](https://gohugo.io) och temat [hugo-book](https://github.com/alex-shpak/hugo-book) (finns som submodul i detta Github-projekt).

## Bygga projektet från källkoden

För att bygga projektet via källkoden krävs att du har Hugo installerat på din dator. Hugo kan installeras via [Homebrew](https://brew.sh/index_sv) på macOS eller [Linuxbrew](https://docs.brew.sh/Homebrew-on-Linux) på Linux.

Sedan installerar du Hugo via brew.

```bash
brew install hugo
```

Du kan sedan köra sidan lokalt på din dator med hjälp av `hugo serve` eller bara `hugo` för att bygga HTML-filer till `public` mappen. Endast administratörer med åtkomst kan bygga projektet och skicka det till den officiella webbservern.