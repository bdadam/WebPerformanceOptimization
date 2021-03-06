<!-- .slide: data-background="assets/maps/map_final_3.jpg" class="bg-contain empty" -->

---

<!-- .slide: data-background="assets/16.jpg" class="empty" -->
<div class="attribution">Bild: [flickr/quaelin](https://www.flickr.com/photos/quaelin/3571013052)</div>

---

<!-- .slide: data-background="assets/bloat.jpg" -->
<div class="attribution">Bild: [flickr/garlandcannon](https://www.flickr.com/photos/garlandcannon/4558340132/)</div>

## Bloat vermeiden

---

<img data-src="assets/unusedcss.png" style="width: 100%;" />

---

### Einen CSS preprocessor wie SASS benutzen

<img data-src="assets/sass.png" style="height: 250px; background: none; border: none; margin-top: 80px;" />

---

### Ein leichtgewichtiges Grid System wie susy benutzen

<img data-src="assets/susy.png" style="height: 250px; background: none; border: none; margin-top: 80px;" />

Note:
- "grid on demand" anstatt große lösung die alle möglichen szenarien abbildet

---

<!-- .slide: data-background="assets/components.jpg" -->
<div class="attribution">Bild: [flickr/jys07](https://www.flickr.com/photos/jys07/14915304913/)</div>

### Eine Seite wird in verschiedene CSS "Komponenten" unterteilt

---

<img data-src="assets/components_detail.jpg">

---

```
...
  <div class="vehicle-details">...</div>
  <div class="vehicle-equipments">
	<hr>
	<h2>Ausstattung</h2>
	<ul>
	  <li>...</li>
	</ul>
  </div>
  <div class="vehicle-description">
    <hr>
    <h2>Fahrzeugbeschreibung</h2>
    <div>Fahrzeug für Bastler, Motor Kopfdichtung defekt</div>
  </div>
...
```

---

```
.vehicle-equipments {
    @extend %detail-page-block;

    li {
        margin-top: $XS;

        @media only screen and (min-width: 400px) {
            &:nth-child(odd) {
                @include span(first 6);
            }
            &:nth-child(even) {
                @include span(last 6);
            }
        }
    }
}
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
<img data-src="assets/filmstrip_2.jpg" />

asynchron
<img data-src="assets/filmstrip_1.webp" />

---

### IPhone 5 - above the fold

<img data-src="assets/abovethefold.jpg" />

---

## Inline CSS

Style für "above the fold" Inhalte direkt im ```<head>``` integrieren

```
<head>
  <styles>
    /* inline styles */
  </styles>
</head>
```

---

<!-- .slide: data-background="assets/inline_styles.jpg" class="empty" -->

---

CSS Datei ansynchron laden mit loadCSS

<pre><code class="lang-html">
&#x3C;head&#x3E;
  &#x3C;script&#x3E;
   // inline the loadCSS script
   function loadCSS( href, before, media, callback ){ ... }
   // then load your stylesheet
   loadCSS(&#x22;/path/to/stylesheet.css&#x22;);
  &#x3C;/script&#x3E;
  &#x3C;style&#x3E;
    /* inline critical CSS */
  &#x3C;/style&#x3E;
  &#x3C;noscript&#x3E;
    &#x3C;link href=&#x22;/path/to/stylesheet.css&#x22; rel=&#x22;stylesheet&#x22;&#x3E;
  &#x3C;/noscript&#x3E;
&#x3C;/head&#x3E;
</code></pre>