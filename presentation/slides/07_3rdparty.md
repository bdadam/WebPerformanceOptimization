# 3rd Party Content

--

#### aka.
# Cookie Monsters

<!-- .slide: data-background="assets/4592911516_4d8e73977c_o.jpg" -->
<div class="attribution">Photo: [flickr/x1brett](https://www.flickr.com/photos/x1brett/4592911516/)</div>

Note:
- 3rd party = cookie monster -> die setzen Cookies ohne Ende

--

Was sind die?
- Werbung (Google AdSense, Google DoubleClick)
- Tracking Pixels (Google Analytics, Piwik)
- Remarketing Pixels (Goodle AdWords Remarketing, Criteo)
- Comments (Disqus, Facebook)
- Social Network Plugins
- uvm.

--

# Separation of Concerns

1. Core Content
1. Enhancements
1. Leftovers

--

<!-- .slide: data-background="assets/separation-concerns.png" -->
<div class="attribution">Bild: [SmashingMagazine](http://www.smashingmagazine.com/2014/09/08/improving-smashing-magazine-performance-case-study/)</div>

--

# Core Content

- HTML (navigierbar, bedienbar)
- CSS
- Bild (wenn Teil des Contents)

--

# Enhancements

- JavaScript
- Webfonts
- Zusätzliche Bilder

--

# Leftovers

- Tracking
- Remarketing
- Werbung

Note:
- SmashingMagazin hat keinen Nachteil bei async Ads gesehen

--

# Strategie #0

### Braucht man wirklich so viele Tools?

--

# Startegie #1

```JavaScript
function loadLeftovers() {
    // Load ads
    // Load Google Analytics
    // ...
}

if (document.readyState === 'complete') {
    loadLeftovers();
} else {
    window.addEventListener('onload', loadLeftovers);
}
```

--

# Strategie #2

Asynchrone Scripts, wo es möglich ist

<pre><code class="lang-html">&#x3C;script src=&#x22;tracking-analytics-pixel-wow.js&#x22; async&#x3E;&#x3C;/script&#x3E;</code></pre>
