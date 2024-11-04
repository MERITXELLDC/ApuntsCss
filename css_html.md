Existeixen 3 maneres principals d’inserir CSS a HTML:

* **Full extern** és ideal per a projectes grans o amb diverses pàgines.
* **Estils interns** poden ser útils per a estils específics en una única pàgina.
* **Estils en línia** són útils per a modificacions ràpides o puntuals.

Sempre que sigui possible, el full extern és la millor opció per mantenir el codi CSS net, reutilitzable i fàcil de mantenir.

### 1. **Full d'estils extern**
   - És la manera més organitzada i recomanada, ja que separa el CSS de l'HTML.
   - Es crea un fitxer CSS separat (per exemple, `estils.css`) i es vincula a l'HTML amb l'etiqueta `<link>` dins de la secció `<head>`.
   - Exemple:
     ```html
     <!-- dins de l'HTML -->
     <head>
       <link rel="stylesheet" href="estils.css">
     </head>
     ```
   - Aquest mètode facilita el manteniment del codi, ja que permet reutilitzar el CSS en diverses pàgines HTML.

### 2. **Estils interns (CSS inline a la secció `<style>`)**
   - Els estils interns es defineixen dins d’una etiqueta `<style>` a la secció `<head>` de l'HTML.
   - Són útils per aplicar estils específics només en aquesta pàgina, però poden fer que el codi sigui més difícil de mantenir si es fan servir en excés.
   - Exemple:
     ```html
     <!-- dins de l'HTML -->
     <head>
       <style>
         body {
           background-color: #f0f0f0;
         }
         h1 {
           color: darkblue;
         }
       </style>
     </head>
     ```

### 3. **Estils en línia (CSS dins de les etiquetes HTML)**
   - Els estils en línia s’apliquen directament a les etiquetes HTML amb l’atribut `style`.
   - Són útils per a modificacions puntuals o ràpides, però no és recomanable abusar-ne perquè fan que el codi sigui difícil de mantenir i no reutilitzable.
   - Exemple:
     ```html
     <h1 style="color: red; font-size: 24px;">Títol amb CSS en línia</h1>
     ```


