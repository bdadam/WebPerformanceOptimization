<!-- .slide: data-background="assets/keyboard.jpg" -->
<div class="attribution">Bild: [flickr/jeroenbennink](https://www.flickr.com/photos/jeroenbennink/3382865257/)</div>

# Performance Optimierungen

Note:
- Wie wir die Performance bei AS24 verbessert haben
- Wir zeigen das anhand eines Beispiels
- WPT video zeigen auf dem man sieht wie die Seite lädt vor den optimierungen
- Was zeigt uns das Video?
- Probleme identifizieren: start render
- Wie kann man Performance und perceived performance messen (WPT, Google pagespeed insights)

---

<!-- .slide: data-background="assets/06.jpg" -->
<div class="attribution">Bild: [flickr/wwarby](https://www.flickr.com/photos/wwarby/3296379139/)</div>

## Startpunkt: Messen

---

## webpagetest.org

<img src="assets/wpt.jpg" width="733px" height="555px" />

Note:
- Was ist WPT
- Was kann man mit WPT machen?

TODO: screenshot WPT mit Ergebnissen von kaputter Seite

---

## Google Page Speed Insights

<img src="assets/gpsi.jpg" />

Note:
- Was ist GPSI? --> analysiert den Inhalt einer Webseite und erstellt Vorschläge zur Verbesserung der Geschwindigkeit dieser Seite.

TODO: screenshot GPSI mit Ergebnissen von kaputter Seite

---

## Das Performance Ziel

<div>
	<img src="assets/gpsi_goal.jpg" style="float: left;" />
	<img src="assets/wpt_goal.jpg" style="float: right; width: 50%;" />
	<div style="clear: both;"></div>
</div>

Note:
- Was ist das Ziel? -> GPSI score >= 95, WPT speed index <= 1000

---

<!-- .slide: data-background="assets/chess.jpg" -->
<div class="attribution">Bild: [flickr/jasonbrown2013](https://www.flickr.com/photos/jasonbrown2013/8589591025/)</div>

## Optimierungsstrategie

Was wird optimiert?

1. Anzahl der Requests
1. Kilobytes
1. Zeit für Page Rendering

---

## Etappen zum Ziel

1. Quickwins: Komprimierung, Minifizierung, Caching
1. Bildoptimierungen
1. CSS Optimierungen
1. JavaScript Optimierungen
1. 3rd Party: Fonts, Tracking, Werbung
1. Time-To-First-Byte reduzieren

Note:
- BILD: Karte mit route darstellen und den Etappen
- einfache Sachen sind relative gerade linie, aufwändigere Sachen sind mit Kurven gestaltet

---

<!-- .slide: data-background="assets/07.jpg" -->
<div class="attribution">Bild: [flickr/92334668@N07](https://www.flickr.com/photos/92334668@N07/11123530043)</div>

## Technologie stack bei AutoScout24

<div style="width: 138%; background-color: white; padding: 50px; margin-left: -250px;">
	<img src="assets/microsoft-net-logo.jpg" style="float: left; width: 235px; height: 225px" />
	<img src="assets/grunt.png" style="float: right; width: 235px; height: 225px" />
	<img src="assets/js.png" style="float: right; width: 235px; height: 225px" />
	<img src="assets/sass.png" style="float: right; width: 235px; height: 225px;" />
	<img src="assets/html.png" style="float: right; width: 235px; height: 225px;" />
	<div style="clear: both;"></div>
</div>