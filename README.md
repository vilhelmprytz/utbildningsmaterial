# Vilhelm Prytz - Utbildningsmaterial

Innehåller dokument med diverse begreppslistor och andra utbildningsmaterial. Uppdelat i varje gymnasiekurs och arbetsområde (några enstaka grundskolematerial finns även).

## Introduktion

Källkod till sidan [utb.vilhelmprytz.se](https://utb.vilhelmprytz.se).

Använder sig av dokumentmotorn [Hugo](https://gohugo.io) och temat [hugo-book](https://github.com/alex-shpak/hugo-book) (finns som submodul i detta Github-projekt).

## Bygga projektet från källkoden

För att bygga projektet via källkoden krävs att du har Hugo installerat på din dator. Hugo kan installeras via [Homebrew](https://brew.sh/index_sv) på macOS eller [Linuxbrew](https://docs.brew.sh/Homebrew-on-Linux) på Linux.

Sedan installerar du Hugo via brew.

```bash
brew install hugo
```

Du kan sedan köra sidan lokalt på din dator med hjälp av `hugo serve` eller bara `hugo` för att bygga HTML-filer till `public` mappen. Endast administratörer med åtkomst kan bygga projektet och skicka det till den officiella webbservern.

## Bidrag

Med hjälp av GitHub går det att skapa en s.k. `fork` av projektet. Där kan du göra ändringar (`commits`) och sedan skicka dessa som en `pull request`. Glöm inte att tydligt beskriva dina ändringar.