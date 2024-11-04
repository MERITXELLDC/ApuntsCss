###  **Selectors CSS**

Els selectors són una part essencial del CSS perquè permeten seleccionar elements HTML de maneres molt variades.

#### Selectors bàsics:

- **Selector d'etiqueta**: S'aplica a tots els elements d'un tipus específic (com `p`, `h1`, `div`).
  ```css
  p {
    color: green;
  }
  ```

- **Selector de classe**: Selecciona tots els elements amb una classe específica, indicada amb un punt (`.`).
  ```css
  .classe {
    background-color: yellow;
  }
  ```

  ```html
  <p class="classe">Text amb classe</p>
  ```

- **Selector d'identificador**: Selecciona l'element amb un identificador específic, indicat amb `#`. Només hauria d’haver-hi un element amb el mateix `id` a la pàgina.
  ```css
  #identificador {
    font-weight: bold;
  }
  ```

  ```html
  <p id="identificador">Text amb identificador</p>
  ```

#### Selectors combinats:

- **Selectors de descendents**: Selecciona elements que són fills dins d’un altre element.
  ```css
  div p {
    color: purple;
  }
  ```

  En aquest exemple, els paràgrafs (`p`) dins de qualsevol `div` seran de color porpra.

- **Selectors de grup**: Aplica el mateix estil a diferents elements separant-los amb comes.
  ```css
  h1, h2, h3 {
    color: red;
  }
  ```

  Així, els títols `h1`, `h2`, i `h3` seran de color vermell.

#### Selectors avançats:

- **Selector de pseudo-classe**: Aplica estils a l'estat específic d'un element, com `:hover`, `:focus`, etc.
  ```css
  a:hover {
    color: orange;
  }
  ```

  Aquest exemple canvia el color de l'enllaç a taronja quan el ratolí està a sobre.

- **Selector d'atribut**: Selecciona elements amb un atribut específic, com `input[type="text"]`.
  ```css
  input[type="text"] {
    border: 1px solid black;
  }
  ```

Aquest són només alguns dels selectors bàsics i avançats, però hi ha molts més per explorar! Els selectors permeten molta flexibilitat per a aplicar estils a elements específics i situacions concretes dins d'un document HTML.
