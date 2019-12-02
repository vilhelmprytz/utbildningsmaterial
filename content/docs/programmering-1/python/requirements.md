---
weight: 3
---

# Requirements

Om du jobbar i ett större Python projekt med flera olika moduler an det vara bra att skapa en s.k. requirements-fil. En requirements-fil innehåller en lista på alla moduler/bilbiotek som används i projektet. Oftast brukar man kalla filen för `requirements.txt`.

En `requirements.txt` fil för ett projekt som använder sig av `pygame` kan t.ex. se ut så här.

```text
pygame
```

De som vill använda ditt program kan då installera alla bibliotek från din `requirements.txt` med hjälp av ett enda kommando.

```bash
pip install -r requirements.txt
```

På så sätt slipper användare gissa sig till vad som behöver installeras för just ditt projekt.

## Definiera specifika versioner

Det går även att definiera specifika versioner av moduler i din `requirements.txt`.

```text
pygame==1.9.6
```

`pip` kommer då att installera den specifika versionen `1.9.6` i detta fall. Definieras ingen version används den senaste.
