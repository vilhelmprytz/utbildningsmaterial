---
weight: 2
title: pygame
---

# pygame

Pygame är ett pythonbibliotek som används för att skapa spel.

## Installera pygame

Pygame kan installeras med hjälp av `pip`.

```bash
pip3 install pygame
```

## En enkel applikation

```python
import pygame

pygame.init()
display = pygame.display.set_mode((800, 600))
clock = pygame.time.Clock()

isRunning = True

while isRunning:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            isRunning = False

    # rita en rektangel på skärmen
    pygame.draw.rect(display, (0, 128, 255), pygame.Rect(30, 30, 60, 60))

    pygame.display.flip()
    clock.tick(60)
```