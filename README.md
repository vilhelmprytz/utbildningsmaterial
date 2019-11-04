# Vilhelm Prytz - Utbildningsmaterial

[![Build Status](https://travis-ci.org/VilhelmPrytz/utbildningsmaterial.svg?branch=master)](https://travis-ci.org/VilhelmPrytz/utbildningsmaterial) [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE) 

Innehåller dokument med diverse begreppslistor och andra utbildningsmaterial. Uppdelat i varje gymnasiekurs och arbetsområde (några enstaka grundskolematerial finns även).

## Introduktion

Källkod till sidan [utb.vilhelmprytz.se](https://utb.vilhelmprytz.se).

Använder sig av dokumentmotorn [Hugo](https://gohugo.io) och temat [hugo-book](https://github.com/alex-shpak/hugo-book) (finns som submodul i detta Github-projekt).

## Bygga projektet från källkoden

För att bygga projektet via källkoden krävs att du har Hugo installerat på din dator. Hugo kan installeras via [Homebrew](https://brew.sh/index_sv) på macOS, [Linuxbrew](https://docs.brew.sh/Homebrew-on-Linux) på Linux (Linuxbrew fungerar även på Windows i WSL, [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)) eller så går det att [ladda ner projektet](https://github.com/gohugoio/hugo/releases) som Windows Executable för Windows (lite krångligare installation).

Via `brew` installerar du Hugo enkelt.

```bash
brew install hugo
```

När du har installerat Hugo kan du sedan köra sidan lokalt på din dator med hjälp av `hugo serve` (sidan går då att nå på [http://localhost:1313](http://localhost:1313)) eller bara `hugo` för att bygga HTML-filer till `public` mappen. Endast administratörer med åtkomst kan bygga projektet och skicka det till den officiella webbservern.

Om du precis har klonat git-projektet kommer inte temat (som är lagrat som submodul) att finnas på din dator. Detta kommer leda till att `hugo` returnerar felmeddelanden. Du kan hämta alla submoduler med hjälp av git.

```
git submodule update --init
```

## Bidrag

Med hjälp av GitHub går det att skapa en s.k. `fork` av projektet. Där kan du göra ändringar (`commits`) och sedan skicka dessa som en `pull request`. Glöm inte att tydligt beskriva dina ändringar.