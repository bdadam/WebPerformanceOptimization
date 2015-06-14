<!-- .slide: data-background="assets/08.jpg" -->
<div class="attribution">Bild: [flickr/worldseriesboxing](https://www.flickr.com/photos/worldseriesboxing/8434284565/)</div>

# Quickwins

Note:
- Einfach und schnell umzusetzen

---

<!-- .slide: data-background="assets/10.jpg" -->
<div class="attribution">Bild: [flickr/marcovdz](https://www.flickr.com/photos/marcovdz/4520986339/)</div>

## GZIP aktivieren

Note:
- Nur für text dateien (CSS, JS, HTML)
- Automatisierte Tests schreiben um Gziping zu testen

---

### GZIP Komprimierung auf dem Server aktivieren

<div style="font-family: monospace; color: #DCDCDC; background: #3F3F3F; text-align: left; font-size: 30px; padding: 10px;">
HTTP/1.1 200 OK  
Content-Type: text/html; charset=utf-8  
<span style="color: red;">Content-Encoding: gzip</span>  
Vary: Accept-Encoding  
Server: Microsoft-IIS/7.5  
X-AspNetMvc-Version: 4.0  
X-AspNet-Version: 4.0.30319  
X-Powered-By: ASP.NET  
Date: Thu, 11 Jun 2015 19:27:44 GMT  
Content-Length: 35433
</div>

Kann mit automatisierten Tests getestet werden

---

<!-- .slide: data-background="assets/09.jpg" -->
<div class="attribution">Bild: [flickr/96828128@N02](https://www.flickr.com/photos/96828128@N02/14448381336/)</div>

## Dateien minifizieren

Note:
- kleiner Dateigrösse durch löschen von unnötigen Inhalten (Kommentare, whitespace, ...)

---

### Auswirkungen von GZIP und Minifizierung

<table>
  <thead>
    <tr>
      <th style="text-align: right">&nbsp;</th>
      <th style="text-align: center">Vorher</th>
      <th style="text-align: center">Nachher</th>
      <th style="text-align: center">Einsparung</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: right"><strong>CSS</strong></td>
      <td style="text-align: center">131 KB</td>
      <td style="text-align: center">27 KB</td>
      <td style="text-align: center">79.4%</td>
    </tr>
    <tr>
      <td style="text-align: right"><strong>JS</strong></td>
      <td style="text-align: center">159 KB</td>
      <td style="text-align: center">55.6 KB</td>
      <td style="text-align: center">65%</td>
    </tr>
  </tbody>
</table>

---

Tools:

- grunt-contrib-cssmin - CSS minifizieren
- grunt-contrib-uglify - JS minifizieren
- grunt-contrib-htmlmin - HTML minifizieren

---

<!-- .slide: data-background="assets/11.jpg" -->
<div class="attribution">Bild: [flickr/marcovdz](https://www.flickr.com/photos/ruthanddave/8530905481/)</div>

## Requests reduzieren durch Bundeling von JS / CSS

Note:
- Erklaren warum wenige requests wichtig sind

---

Nicht:
```
<head>
	...
	<link rel="stylesheet" href="home.css">
	<link rel="stylesheet" href="list.css">
	<link rel="stylesheet" href="detail.css">
	...
</head>
```

Sondern:
```
<head>
	...
	<link rel="stylesheet" href="main.css">
	...
</head>
```

---

Tools:

- grunt-contrib-concat

---

<!-- .slide: data-background="assets/12.jpg" -->
<div class="attribution">Bild: [flickr/joffi](https://www.flickr.com/photos/joffi/4966531636/)</div>

## Redirects reduzieren

---

<!-- .slide: data-background="assets/fetch.jpg" -->
<div class="attribution">Bild: [flickr/mshipp](https://www.flickr.com/photos/mshipp/14256166416)</div>

## DNS Prefetching

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