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

<!-- .slide: data-background="assets/webp.png" -->

---

<!-- .slide: data-background="assets/14.jpg" -->
<div class="attribution">Bild: [flickr/yukop](https://www.flickr.com/photos/yukop/7004565377/)</div>

## Inline SVG für Icons

---

<svg version="1.1" id="Ebene_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 fill="white" width="18px" height="18px" viewBox="0 0 18 18" style="enable-background:new 0 0 18 18;" xml:space="preserve">
<path style="fill-rule:evenodd;clip-rule:evenodd;" d="M9,11.9l-9-6C0,5.9,0,6,0,6v7.4C0,14.3,0.7,15,1.6,15h14.7
	c0.9,0,1.6-0.7,1.6-1.6V6c0-0.1,0-0.1,0-0.2L9,11.9z M9,10.3l8.5-5.9C17.2,4.2,16.6,4,16.2,4H1.8c-0.4,0-1,0.2-1.3,0.4L9,10.3z"/>
</svg>

```
<svg version="1.1" id="Ebene_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 fill="white" width="18px" height="18px" viewBox="0 0 18 18" style="enable-background:new 0 0 18 18;" xml:space="preserve">
<path style="fill-rule:evenodd;clip-rule:evenodd;" d="M9,11.9l-9-6C0,5.9,0,6,0,6v7.4C0,14.3,0.7,15,1.6,15h14.7
	c0.9,0,1.6-0.7,1.6-1.6V6c0-0.1,0-0.1,0-0.2L9,11.9z M9,10.3l8.5-5.9C17.2,4.2,16.6,4,16.2,4H1.8c-0.4,0-1,0.2-1.3,0.4L9,10.3z"/>
</svg>
```

---

### Vorteile von SVG

- Funktioniert für alle Auflösungen
- Sehr gute Komprimierung mit GZIP
- Flexibel einsetzbar

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