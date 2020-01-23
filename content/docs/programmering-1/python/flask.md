---
weight: 1
---

# Flask

Flask är ett webbramverk för Python. Det går alltså att skapa hemsidor/webbapplikationer i Flask.

## Installera Flask

Flask går att installera med hjälp av `pip`.

```bash
pip3 install flask
```

## En enkel applikation

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def index():
    return "Hello World!"

if __name__ == "__main__":
    app.run(host="0.0.0.0")
```

Om du kör applikationen kommer en webbserver att startas på din dator på port `5000`. Du kan nå webbapplikation genom att gå in på [http://localhost:5000](http://localhost:5000).

## Returnera JSON-data

Att returnera svar i JSON är enkelt med Flask. Först behöver du importera `jsonify` från Flask.

```python
from flask import Flask, jsonify
```

I dina applikationroutes kan du nu returnera JSON data.

```python
@app.route("/test")
def test():
    return jsonify({
        "car": "Alfa Romeo",
        "numbers": [1, 2, 3],
        "person": {
            "age": 17,
            "city": "Stockholm"
        }
    })
```

JSON-datan behöver alltså wrappas med en `jsonify()` runt sig (JSON-data du vill returnera lägger du mellan paranteserna). Detta är perfekt för att skriva backendapplikationer.

## Dela upp Flask routes i olika filer med hjälp av blueprints

Om du kodar en större webbapplikation i Flask kan det vara bra att dela upp applikationen i olika filer. Detta går att göra i Flask med hjälp av `blueprints`.

Om du utgår från startapplikationen ovan kan du importera `blueprints` från andra filer.

```python
from client import client_routes

app.register_blueprint(client_routes)
```

Filen `client.py` kan innehålla `routes` som är helt separerade med resten av applikationen.

```python
from flask import Blueprint

# blueprint init
client_routes = Blueprint(
    "client_routes",
    __name__,
    template_folder="../templates"
)

# routes
@client_routes.route("/client")
def client():
    return "Detta kommer från client_routes!`
```

## Rendera HTML

Flask kan rendera HTML-filer med Python data.

```python
from flask import render_template

version = "v1.0"

@app.route("/demo")
def demo():
    return render_template("index.html", version=version)
```

Alla HTML filer måste finnas i `templates` mappen (som standard).

Genom att definera variabler som argument till `render_template` funktionen kommer dessa att vara tillgängliga från HTML-filen, se exemplet nedan (`templates/index.html`). Det går att skicka in variabler, listor och dictionaries.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Demo</title>
    </head>
    <body>
        <p>{{ version }}</p>
    </body>
</html>
```

För att använda variabler används `{{ variablens_namn }}`. Det går också att göra for-loopar eller if-statements.

```html
{% if error %}
<p>Detta visas endast om "error" variablen är definierad (alltså inte None).</p>
{% endif %}
```

```html
{% for user in users %}
<p>Användare {{ user }}</p>
{% endfor %}
```
