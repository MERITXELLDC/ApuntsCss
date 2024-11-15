Exemple on es combinen diversos conceptes de CSS i HTML, com ara selectors, unitats de mesura, abreviatures, estils en bloc i en línia, i altres conceptes clau.

---

### 1. **index.html**

Aquest és l’arxiu HTML principal, que inclou el contingut de la pàgina i enllaça amb el full d’estils extern (`style.css`).

```html
<!DOCTYPE html>
<html lang="ca">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemple de CSS amb HTML</title>
    <!-- Enllaça amb el full d'estils extern -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Encapsula tot el contingut dins d'un contenidor -->
    <div class="container">
        <!-- Títol principal -->
        <h1>Benvingut al meu exemple de pàgina web</h1>

        <!-- Paràgraf amb identificador únic -->
        <p id="paragraf-unique">Aquest paràgraf té un estil únic i està separat amb un marge especial.</p>

        <!-- Paràgrafs amb estils comuns mitjançant una classe -->
        <p class="text">Aquesta és una demostració d'estils aplicats a diversos elements HTML.</p>
        <p class="text">Amb CSS podem modificar colors, mides de font, marges, padding, i molt més.</p>

        <!-- Exemple d'una caixa amb estils aplicats mitjançant una classe -->
        <div class="box">Caixa amb estil</div>
        
        <!-- Exemple de botó amb estils en línia (inline) -->
        <button style="background-color: orange; color: white; padding: 10px; border: none;">
            Botó amb estil inline
        </button>
    </div>

</body>
</html>
```

---

### 2. **style.css**

Aquest és el fitxer CSS que conté tots els estils per als elements HTML definits en `index.html`.

```css
/* Estil general del cos de la pàgina */
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

/* Contenidor principal per centrar el contingut */
.container {
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
    background-color: white;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Estil per al títol */
h1 {
    color: darkblue;
    font-size: 2.5em;
    text-align: center;
    margin-bottom: 20px;
}

/* Paràgraf amb un identificador únic */
#paragraf-unique {
    color: darkred;
    font-size: 1.2em;
    margin: 20px 0;
    padding: 10px;
    background-color: #f0e0e0;
    border-left: 4px solid darkred;
}

/* Estil per a paràgrafs de classe 'text' */
.text {
    color: #333;
    font-size: 1em;
    margin: 10px 0;
    line-height: 1.5;
}

/* Estil per a una caixa amb classe 'box' */
.box {
    width: 120px;
    height: 120px;
    background-color: lightblue;
    margin: 20px auto;
    text-align: center;
    line-height: 100px; /* Per centrar el text verticalment */
    border-radius: 8px;
}

/* Botó per a estats de pseudo-classe (hover) */
button:hover {
    background-color: #ff6600;
    cursor: pointer;
}
```

---

### Conceptes utilitzats

- **Selectors d'etiqueta**: `body`, `h1`, etc., per aplicar estils a tots els elements del mateix tipus.
- **Selector de classe**: `.container`, `.text`, `.box`, aplicat a elements amb les classes corresponents.
- **Selector d'identificador**: `#paragraf-unique`, aplicat a un element amb l’identificador `id`.
- **Unitats de mesura**: s'han utilitzat `px`, `%`, `em`, i `rem` per a definir mides i marges.
- **Abreviatures (shorthand)**: S’utilitza `margin`, `padding` i `background` per simplificar les propietats.
- **Estils en línia (inline)**: Definits directament en l’etiqueta HTML del botó.
- **Pseudo-classe `:hover`**: Aplicada al botó per canviar-ne l'estil quan el cursor està a sobre.
