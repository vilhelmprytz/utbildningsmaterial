---
weight: 2
---

# Git

Git är ett versionhanteringssystem som ofta används inom programmering. Denna sida använder sig av Git och tjänsten som kallas för [GitHub](https://github.com).

## Hur du gör en commit

Börja med att lägga till filerna som du ändrat i din commit.

```bash
git add filename.py
```

Om du vill lägga till alla filer som har modifierats i ett enda kommando kan det också göras.

```bash
git add .
```

När du lagt till ändringarna kan du sedan "stämpla ändringarna" med en version, kommentar och datum (alltså en commit). Försök att ha beskrivande men korta kommentarer. Ofta skrivs kommentaren på så sätt att den beskriver vad commiten gör, inte vad du har gjort.

```bash
git commit -m "Ett kort meddelande som beskriver vad denna commit gör"
```

Använder du en tjänst som t.ex. GitHub eller GitLab behöver du också publicera din commit till respektive plattform.

```bash
git push
```

## Koppla ett lokalt repository mot GitHub

Om du skapat en repository på din dator och vill länka mot den till t.ex. GitHub behöver du först kopiera `.git`-länken för ditt repository.

Lägg till den i git.

```bash
git remote add origin https://github.com/vilhelmprytz/utbildningsmaterial.git
```

Länka din lokala branch mot den som finns på GitHub.

```bash
git branch --set-upstream-to=origin/master master
```

Nu kan du använda `git pull` eller `git push` för att hämta respektive ladda upp ändringar.
