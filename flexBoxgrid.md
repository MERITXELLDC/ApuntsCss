**Flexbox** i **CSS Grid** per dissenyar layouts de pàgines web. 
Aquests dos sistemes són molt potents i flexibles i permeten disposar els elements de manera responsiva i eficient.

---

## 1. Flexbox

**Flexbox** és ideal per disposar elements en **una dimensió**: ja sigui en fila (horizontalment) o en columna (verticalment). És especialment útil per alinear elements i distribuir espais dins de contenidors.

### Com utilitzar Flexbox:

1. **Defineix el contenidor flex**: aplica `display: flex;` al contenidor pare per activar Flexbox.
2. **Propietats bàsiques del contenidor (eix principal)**:
    - **`flex-direction`**: defineix la direcció dels elements (per defecte és fila horitzontal).
      - `row`: horitzontal (per defecte).
      - `column`: vertical.
    - **`justify-content`**: alinea els elements al llarg de l'eix principal (fila o columna).
      - `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.
3. **Propietats d'alineació de l'eix transversal**:
    - **`align-items`**: alinea els elements en l'eix transversal (perpendicular).
      - `flex-start`, `flex-end`, `center`, `stretch`, `baseline`.
4. **Propietats dels elements flex**:
    - **`flex-grow`**: defineix com un element ocupa espai addicional.
    - **`flex-shrink`**: defineix com un element redueix la mida si hi ha menys espai.
    - **`flex-basis`**: especifica la mida inicial de l’element abans de distribuir l’espai.

### Exemple de Flexbox

```css
.container {
    display: flex;
    flex-direction: row; /* Direcció horitzontal */
    justify-content: space-between; /* Espaiat entre elements */
    align-items: center; /* Centrat en l'eix vertical */
}

.item {
    flex: 1; /* Cada element ocupa espai proporcionalment */
    padding: 10px;
    background-color: lightblue;
    margin: 5px;
}
```

```html
<div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
</div>
```

---

## 2. CSS Grid

**CSS Grid** és perfecte per a disposicions en **dues dimensions** (files i columnes). Ofereix un control total sobre com i on col·locar cada element dins de la quadrícula.

### Com utilitzar CSS Grid:

1. **Defineix el contenidor grid**: aplica `display: grid;` al contenidor pare per activar CSS Grid.
2. **Configura les files i columnes**:
    - **`grid-template-columns`** i **`grid-template-rows`**: defineixen el nombre i la mida de les columnes i files.
      - Exemple: `grid-template-columns: 1fr 1fr 1fr;` (tres columnes d'amplada igual).
3. **Espai entre cel·les**:
    - **`gap`** o **`grid-gap`**: defineix l'espai entre les files i les columnes.
4. **Col·loca elements dins de la quadrícula**:
    - **`grid-column`** i **`grid-row`**: col·loquen elements en posicions específiques (especificant el començament i el final de cada element).
      - Exemple: `grid-column: 1 / 3;` (l'element ocupa de la columna 1 a la 3).

### Exemple de CSS Grid

```css
.container {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr; /* Defineix 3 columnes de diferents amplades */
    grid-template-rows: auto 200px auto; /* Defineix 3 files */
    gap: 10px; /* Espai entre les cel·les */
}

.item1 {
    grid-column: 1 / 4; /* Ocupa les 3 columnes */
    grid-row: 1 / 2; /* Primera fila */
}

.item2 {
    grid-column: 2 / 3; /* Ocupa la segona columna */
    grid-row: 2 / 3; /* Segona fila */
}
```

```html
<div class="container">
    <div class="item1">Capçalera</div>
    <div class="item2">Contingut principal</div>
    <div class="item3">Sidebar</div>
    <div class="item4">Peu de pàgina</div>
</div>
```

---

### Comparativa Flexbox vs Grid

- **Flexbox** és més senzill i es recomana per a dissenys lineals en una sola direcció, com centrat de text, botons o llistes.
- **CSS Grid** és més avançat i ideal per a estructures més complexes que necessiten alineació en dues dimensions, com un disseny de pàgina complet amb capçaleres, barres laterals i peus de pàgina.

Aquests dos mètodes es poden combinar, utilitzant Flexbox dins d’una cel·la de Grid, per exemple, per a aconseguir dissenys flexibles i adaptables.
