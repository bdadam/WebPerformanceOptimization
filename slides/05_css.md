<!-- .slide: data-background="assets/16.jpg" class="empty" -->
<div class="attribution">Bild: [flickr/quaelin](https://www.flickr.com/photos/quaelin/3571013052)</div>

---

<!-- .slide: data-background="assets/bloat.jpg" -->
<div class="attribution">Bild: [flickr/garlandcannon](https://www.flickr.com/photos/garlandcannon/4558340132/)</div>

## Bloat vermeiden

---

<img src="assets/unusedcss.png" />

---

### Einen CSS preprocessor wie SASS benutzen

<img src="assets/sass.png" style="height: 250px; background: none; border: none; margin-top: 80px;" />

---

### Ein leichtgewichtiges Grid System wie susy benutzen

<img src="assets/susy.png" style="height: 250px; background: none; border: none; margin-top: 80px;" />

---

<!-- .slide: data-background="assets/components.jpg" -->
<div class="attribution">Bild: [flickr/jys07](https://www.flickr.com/photos/jys07/14915304913/)</div>

### Eine Seite wird in verschiedene CSS Komponenten unterteilt

---

<img src="assets/components_detail.jpg">

---

```
...

  <div class="vehicle-details">...</div>
  <div class="vehicle-equipments">
	<hr>
	<h2>Ausstattung</h2>
	<ul>...</ul>
  </div>
  <div class="vehicle-description">
    <hr>
    <h2>Fahrzeugbeschreibung</h2>
    <div>Fahrzeug für Bastler, Motor Kopfdichtung defekt, Alle Angaben ohne Gewähr,</div>
  </div>
  
...
```

---

Tools:

- pleeease - Autoprefixer, fallbacks, etc.
- uncss - remove unused CSS

---

## CSS Asynchron laden

CSS files blockieren die Anzeige bis content heruntergeladen und verarbeitet wurde.

---

synchron
<img src="assets/filmstrip_2.jpg" />

asynchron
<img src="assets/filmstrip_1.webp" />

---

loadCSS

---

## Inlining CSS

TODO: explain how inlining works

---