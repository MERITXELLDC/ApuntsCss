Sintaxis CSS:

### 1. **Estructura bàsica de la sintaxi CSS**

Un bloc CSS consisteix en:

```css
selector {
    propietat: valor;
    propietat2: valor2;
    /* més propietats i valors */
}
```

#### Parts principals:
- **Selector**: Indica a quin element o elements HTML s’aplicarà l’estil.
- **Propietat**: És l’aspecte de l’element que volem modificar. Exemples comuns són `color`, `font-size`, `margin`, etc.
- **Valor**: És el valor que assignem a la propietat, que pot ser un color, una mida, una font, entre altres.

Cada línia dins del bloc és una **declaració** i ha de tenir una propietat i un valor separats per dos punts (`:`). Cada declaració acaba amb un punt i coma (`;`), que permet que el navegador interpreti correctament el codi.

#### Exemple bàsic:
```css
p {
    color: blue;
    font-size: 16px;
    margin: 10px;
}
```

En aquest exemple:
- El selector és `p` (s’aplica a tots els paràgrafs).
- Les propietats són `color`, `font-size` i `margin`.
- Els valors assignats són `blue`, `16px` i `10px`, respectivament.

### 2. **Selectors múltiples**
Pots aplicar els mateixos estils a diversos selectors separant-los amb comes.

```css
h1, h2, h3 {
    color: darkblue;
    font-weight: bold;
}
```

Aquest codi fa que els títols `h1`, `h2` i `h3` siguin de color blau fosc i tinguin la lletra en negreta.

---

### 3. **Unitats de mesura en CSS**

CSS permet utilitzar diferents unitats de mesura per definir mides, amplades, alçades, espais, etc. Les unitats més comunes són:

- **Pixels (`px`)**: Unitat fixa que és molt utilitzada per a dimensions precises.
  ```css
  font-size: 16px;
  ```

- **Percentatges (`%`)**: Unitat relativa, que s’utilitza per fer que les mides depenguin de les dimensions de l'element pare.
  ```css
  width: 50%;
  ```

- **Ems (`em`) i Rems (`rem`)**: Unitats relatives utilitzades per definir la mida de la font o altres dimensions relatives.
  - `em` és relativa a la mida de font de l’element pare.
  - `rem` és relativa a la mida de font de l'element `<html>`.
  
  ```css
  font-size: 1.5em; /* 1.5 vegades la mida de font de l’element pare */
  padding: 2rem;    /* 2 vegades la mida de font del <html> */
  ```

### 4. **Comentaris en CSS**
Els comentaris són útils per deixar notes al codi, fer-lo més comprensible o indicar seccions. No es mostren al navegador.

```css
/* Aquest és un comentari */
p {
    color: black; /* També pots afegir comentaris en línia */
}
```

### 5. **Declaracions múltiples en una sola línia**
Pots escriure diverses propietats en una sola línia, però només és recomanable per a estils molt senzills o quan vulguis mantenir el codi molt compacte.

```css
h1 { color: green; font-size: 20px; text-align: center; }
```

### 6. **Agrupació de propietats amb abreviatures (shorthand)**

CSS té abreviatures per a algunes propietats, cosa que fa que el codi sigui més concís. Per exemple:

- **Marges i Padding**: Pots definir els marges de tots els costats en una sola línia.
  ```css
  margin: 10px 15px 10px 15px; /* dalt, dreta, baix, esquerra */
  padding: 10px 20px;          /* dalt i baix, esquerra i dreta */
  ```

- **Font**: Permet agrupar diverses propietats de la font en una línia.
  ```css
  font: bold 16px Arial, sans-serif;
  ```

- **Background**: Permet definir color, imatge, posició, i més.
  ```css
  background: #f0f0f0 url('imatge.png') no-repeat center;
  ```

### 7. **Prioritat i especificitat en CSS**

Quan hi ha conflictes en els estils aplicats (per exemple, diferents estils que s’apliquen al mateix element), el navegador utilitza una jerarquia de prioritat:

1. **Estils en línia** (en el mateix HTML amb `style="..."`) tenen la prioritat més alta.
2. **Selectors d’identificador** (amb `#id`) són més específics que els de classe (amb `.classe`).
3. **Selectors de classe** són més específics que els selectores d’etiqueta (`h1`, `p`, etc.).

També es pot fer servir `!important` per forçar la prioritat d'un estil, però és recomanable evitar-ho perquè pot complicar el manteniment.

```css
p {
    color: red !important;
}
```

Aquest `color: red` s'aplicarà sempre al paràgraf, fins i tot si altres regles intenten canviar-lo.

---

### Exemple complet

```css
/* Estil per a tot el cos */
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    margin: 0;
    padding: 0;
}

/* Títol principal */
h1 {
    color: darkblue;
    font-size: 2em;
    text-align: center;
}

/* Estils per a un paràgraf amb identificador únic */
#paragraf-unique {
    color: darkred;
    margin: 20px;
}

/* Estils per a elements amb classe */
.box {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin: 10px auto;
}
```

Aquest codi aplica estils diferents a `body`, `h1`, un paràgraf amb `id="paragraf-unique"`, i elements amb la classe `.box`. La combinació de totes aquestes parts et permet crear dissenys visuals complets per a les teves pàgines web.
