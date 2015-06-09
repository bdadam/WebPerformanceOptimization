<!-- .slide: data-background="assets/13.jpg" -->
<div class="attribution">Bild: [flickr/louish](https://www.flickr.com/photos/louish/5521251110/)</div>

# Bilder optimieren

---

<!-- .slide: data-background="assets/10.jpg" -->
<div class="attribution">Bild: [flickr/marcovdz](https://www.flickr.com/photos/marcovdz/4520986339/)</div>

## Bilder komprimieren

---

### Tools:

- grunt-contrib-imagemin
- pngcrush

---

<!-- .slide: data-background="assets/cache.jpg" -->
<div class="attribution">Bild: [flickr/picksfromoutthere](https://www.flickr.com/photos/picksfromoutthere/16642333284/)</div>

## Bilder richtig cachen

---

- caching header richtig setzen
- Hash code an URL anhängen und hash bei Bildänderung ändern

explain resource: https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching?hl=de

---

## Das richtge Format wählen

- JPEG: Bilder ohne Transparenz
- PNG: Bilder mit Transparenz
- WEBP: moderne Browser
- SVG: Icons

---

### Auflösung 2592 x 3456

<div>
	<div style="float: left; width: 32%">
		<p>JPEG</p>
		<img src="assets/image_formats/kitten.jpg" />
		<p>1.3 MB</p>
	</div>
	<div style="float: left; width: 32%">
		<p>PNG</p>
		<img src="assets/image_formats/kitten.png" />
		<p>12.7 MB</p>
	</div>
	<div style="float: left; width: 32%">
		<p>WEBP</p>
		<img src="assets/image_formats/kitten.webp" />
		<p>312 KB</p>
	</div>
</div>

---

<!-- .slide: data-background="assets/14.jpg" -->
<div class="attribution">Bild: [flickr/yukop](https://www.flickr.com/photos/yukop/7004565377/)</div>

## SVG für Icons

Note: (TODO: include infos in slides + SVG example code)
- Funktioniert für alle Auflösungen
- Text -> Gute Komprimierung
- Flexibel einsetzbar (CSS styling)

---

<!-- .slide: data-background="assets/grunticon.jpg" -->

---

<!-- .slide: data-background="assets/responsive.png" -->
<div class="attribution">Bild: [Wikipedia Commons](http://commons.wikimedia.org/wiki/File:Responsive_Web_Design_Logo.svg)</div>

## Responsive Images

---

### Bilder serverseitig resizen

http://pic.autoscout24.net/images-420x315/164/306/0269306164001.jpg

<img src="assets/pic_server_1.jpg" />

---

http://pic.autoscout24.net/images-big/164/306/0269306164001.jpg

<img src="assets/pic_server_2.jpg" />

---

### Tools:

- Imager.js
- PictureFill

---

<!-- .slide: data-background="assets/15.jpg" -->
<div class="attribution">Bild: [flickr/hmk](https://www.flickr.com/photos/hmk/2742398590/)</div>

## Lazy Loading von Bildern

---

### Tools:

- data Attributes
- Layzr.js

Note:
- Bilder nur laden wenn sie sichtbar sind