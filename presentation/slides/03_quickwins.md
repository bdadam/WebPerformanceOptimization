<!-- .slide: data-background="assets/08.jpg" -->
<div class="attribution">Bild: [flickr/worldseriesboxing](https://www.flickr.com/photos/worldseriesboxing/8434284565/)</div>

# Quickwins

Note:
- Einfach und schnell umzusetzen

---

<!-- .slide: data-background="assets/09.jpg" -->
<div class="attribution">Bild: [flickr/96828128@N02](https://www.flickr.com/photos/96828128@N02/14448381336/)</div>

## Dateien minifizieren

Note:
- kleiner Dateigrösse durch löschen von unnötigen Inhalten (Kommentare, whitespace, ...)

---

TODO: savings before after in KB and %

---

Tools:

- grunt-contrib-cssmin - CSS minifizieren
- grunt-contrib-uglify - JS minifizieren
- grunt-contrib-htmlmin - HTML minifizieren

---

<!-- .slide: data-background="assets/10.jpg" -->
<div class="attribution">Bild: [flickr/marcovdz](https://www.flickr.com/photos/marcovdz/4520986339/)</div>

## Gzip aktivieren

Note:
- Vor allem wichtig für text dateien (CSS, JS, HTML)
- Automatisierte Tests schreiben um Gziping zu testen

---

TODO: savings before after in KB and %

---

### GZIP Komprimierung auf dem Server aktivieren

<div style="font-family: monospace; color: #DCDCDC; background: #3F3F3F; text-align: left; font-size: 30px; padding: 10px;">
HTTP/1.1 200 OK  
Date: Thu, 04 Dec 2003 16:15:12 GMT  
Server: Apache/2.0  
Vary: Accept-Encoding  
<span style="color: red;">Content-Encoding: gzip</span>  
Cache-Control: max-age=300  
Expires: Thu, 04 Dec 2003 16:20:12 GMT  
X-Guru: basic-knowledge=0, general-knowledge=0.2, complete-omnipotence=0.99  
Content-Length: 1533  
Content-Type: text/html; charset=ISO-8859-1
</div>

Kann mit automatisierten Tests getestet werden

---

<!-- .slide: data-background="assets/11.jpg" -->
<div class="attribution">Bild: [flickr/marcovdz](https://www.flickr.com/photos/ruthanddave/8530905481/)</div>

## Requests reduzieren durch Bundeling von JS / CSS

Note:
- Erklaren warum wenige requests wichtig sind

---

TODO: savings before after

---

Tools:

- grunt-contrib-concat

---

<!-- .slide: data-background="assets/12.jpg" -->
<div class="attribution">Bild: [flickr/joffi](https://www.flickr.com/photos/joffi/4966531636/)</div>

## Redirects reduzieren

---

<!-- .slide: data-background="assets/names.jpg" -->
<div class="attribution">Bild: [flickr/ontourwithben](https://www.flickr.com/photos/ontourwithben/7836307042/)</div>

## DNS lookups reduzieren

---

### DNS wird im Hintergrund aufgelöst, noch vor Anforderung.  

```
<head>
	...
	<link rel="dns-prefetch" href="//pic.autoscout24.net" />
	<link rel="dns-prefetch" href="//www.googletagmanager.com" />
	...
</head>
```

Vorteile:

- Reduzierung von Latenzzeiten
- Schnellere Ladezeit