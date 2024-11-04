El **model de caixes en CSS3** (CSS Box Model) és la base per entendre com es distribueixen i es representen visualment els elements HTML en una pàgina. Cada element de la pàgina es considera una "caixa", i el model de caixes defineix l'espai ocupat per l'element dins de la pàgina.

### Parts del model de caixes CSS

Cada caixa té quatre parts principals:

1. **Content** (Contingut): L'espai on es mostra el text, les imatges o altres elements dins de la caixa.
2. **Padding** (Espai interior): L'espai entre el contingut i el límit de la caixa. Afegeix espai dins de l'element i manté el contingut separat de la vora.
3. **Border** (Vora): El contorn que envolta la caixa de contingut i el padding.
4. **Margin** (Espai exterior): L'espai fora de la vora, que separa l'element d'altres elements veïns.

Aquest model es pot visualitzar així:

```
+-------------------------------+
|           Margin              |
|   +-------------------------+  |
|   |         Border          |  |
|   |   +-------------------+ |  |
|   |   |     Padding       | |  |
|   |   |   +-----------+   | |  |
|   |   |   |  Content   |   | |  |
|   |   |   +-----------+   | |  |
|   |   |                   | |  |
|   |   +-------------------+ |  |
|   +-------------------------+  |
+--------------------------------+
```

### Propietats del model de caixes

A continuació es mostren les propietats CSS per gestionar cada part del model de caixes:

- **Content**: Controlat per propietats com `width` i `height`.
- **Padding**: Controlat per `padding`, `padding-top`, `padding-right`, `padding-bottom`, `padding-left`.
- **Border**: Controlat per `border`, `border-width`, `border-style`, `border-color`, o de manera individual per cada costat (`border-top`, `border-right`, etc.).
- **Margin**: Controlat per `margin`, `margin-top`, `margin-right`, `margin-bottom`, `margin-left`.

### Exemple bàsic d'aplicació del model de caixes

Aquí tens un exemple amb CSS i HTML per mostrar com aplicar i veure el model de caixes en acció:

```html
<!DOCTYPE html>
<html lang="ca">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemple del Model de Caixes CSS</title>
    <style>
        /* Definició de la caixa */
        .box {
            width: 200px;          /* Amplada del contingut */
            height: 100px;         /* Alçada del contingut */
            padding: 20px;         /* Espai interior entre el contingut i la vora */
            border: 5px solid blue;/* Vora de la caixa */
            margin: 15px;          /* Espai exterior per separar la caixa d'altres elements */
            background-color: lightgray;
        }
    </style>
</head>
<body>

    <!-- Aplicació de la classe box -->
    <div class="box">
        Contingut de la caixa
    </div>

</body>
</html>
```

- **width** i **height**: defineixen la mida del contingut dins de la caixa (`200px` d'amplada i `100px` d'alçada).
- **padding**: afegeix 20 píxels d’espai interior al voltant del contingut.
- **border**: afegeix una vora de 5 píxels de color blau.
- **margin**: afegeix 15 píxels d’espai exterior al voltant de la caixa per separar-la d'altres elements.

### Càlcul de la mida total de la caixa

La mida visual total de la caixa és el resultat de sumar:
- **Amplada total**: `width` + `padding-esquerra` + `padding-dreta` + `border-esquerra` + `border-dreta` + `margin-esquerra` + `margin-dreta`.
- **Alçada total**: `height` + `padding-dalt` + `padding-baix` + `border-dalt` + `border-baix` + `margin-dalt` + `margin-baix`.

**En aquest exemple, l'amplada total de la caixa serà:**
200px (width) + 20px (padding esquerra) + 20px (padding dreta) + 5px (border esquerra) + 5px (border dreta) = 250px.

**L'alçada total de la caixa serà:**
100px (height) + 20px (padding dalt) + 20px (padding baix) + 5px (border dalt) + 5px (border baix) = 150px.

---

### Model de caixes amb `box-sizing: border-box`

Per defecte, CSS no inclou `padding` i `border` en el càlcul de `width` i `height`, però amb `box-sizing: border-box` pots fer que `width` i `height` incloguin el padding i el border, facilitant el disseny.

```css
.box {
    box-sizing: border-box;
    width: 200px;
    height: 100px;
    padding: 20px;
    border: 5px solid blue;
    margin: 15px;
    background-color: lightgray;
}
```

Amb `box-sizing: border-box`, l’amplada i l’alçada de l’element es mantenen dins dels 200px i 100px especificats, sense sumar el `padding` i el `border`. Això facilita la disposició de les caixes dins d’una pàgina.
