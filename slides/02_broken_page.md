<!-- .slide: data-background="assets/keyboard.jpg" -->
<div class="attribution">Bild: [flickr/jeroenbennink](https://www.flickr.com/photos/jeroenbennink/3382865257/)</div>

# Performance Optimierungen

Note:
- Wie wir die Performance bei AS24 verbessert haben
- Wie kann man Performance und perceived performance messen (WPT, Google pagespeed insights)

---

<!-- .slide: data-background="assets/06.jpg" -->
<div class="attribution">Bild: [flickr/wwarby](https://www.flickr.com/photos/wwarby/3296379139/)</div>

## Startpunkt: Messen

---

## webpagetest.org

<img data-src="assets/wpt.jpg" width="733px" height="555px" />

Note:
- Was ist WPT
- Was kann man mit WPT machen?

---

<img data-src="assets/webpagetest_result.jpg" -->

---

## Google Page Speed Insights

<img data-src="assets/gpsi.jpg" />

Note:
- Was ist GPSI? --> analysiert den Inhalt einer Webseite und erstellt Vorschläge zur Verbesserung der Geschwindigkeit dieser Seite.

---

<!-- .slide: data-background="assets/gpsi_result.jpg" class="empty" -->

---

## Das Performance Ziel

<div>
	<img src="assets/GPSI_goal.jpg" style="float: left; width: 48%;" />
	<img src="assets/wpt_goal.jpg" style="float: right; width: 48%;" />
	<div style="clear: both;"></div>
</div>

Messungen erfolgen mit 3G Verbindung

Note:
- Was ist das Ziel? -> GPSI score >= 95, WPT speed index <= 1000
- Warum haben wir dieses Ziel gewählt?

---

## Etappen zum Ziel

1. Quickwins: Komprimierung, Minifizierung, Caching
1. Bildoptimierungen
1. CSS Optimierungen
1. JavaScript Optimierungen
1. 3rd Party: Fonts, Tracking, Werbung

Note:
- BILD: Karte mit route darstellen und den Etappen
- einfache Sachen sind relative gerade linie, aufwändigere Sachen sind mit Kurven gestaltet

---

<!-- .slide: data-background="assets/07.jpg" -->
<div class="attribution">Bild: [flickr/92334668@N07](https://www.flickr.com/photos/92334668@N07/11123530043)</div>

## Technologie stack bei AutoScout24

<div style="background-color: white; padding: 20px; margin-left: -20px; width: 100%">
	<img src="assets/microsoft-net-logo.jpg" style="float: left; width: 180px; height: 180px" />
	<img src="assets/grunt.png" style="float: right; width: 180px; height: 180px" />
	<img src="assets/js.png" style="float: right; width: 180px; height: 180px" />
	<img src="assets/sass.png" style="float: right; width: 180px; height: 180px;" />
	<img src="assets/html.png" style="float: right; width: 180px; height: 180px;" />
	<div style="clear: both;"></div>
</div>

---

## Unterstüzte Browser

<style>
	.browsers img {
		width: 180px;
		height: 180px;
		
		background: none !important;
		border: none !important;
		margin-left: 15px;
	}
</style>

<div class="browsers">
	<img src="assets/ie.png"/>
	<img src="assets/chrome.png"/>
	<img src="assets/firefox.png"/>
	<img src="assets/android.png"/>
	<img src="assets/safari.png"/>
</div>
