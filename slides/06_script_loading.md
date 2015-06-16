<!-- .slide: data-background="assets/maps/map_final_4.jpg" class="bg-contain empty" -->

--

<!-- .slide: data-background="assets/8038102723_1f2a6de4ac_k.jpg" -->
<div class="attribution">[flickr/kingair42](https://www.flickr.com/photos/kingair42/8038102723/)</div>

# Script Loading

--

## Render Blocking

<pre><code class="lang-html">&lt;script src="render-blocking.js">&lt;/script></code></pre>

- blockiert DOM-Aufbau
- blockiert CSSOM-Aufbau
- daher blockiert Rendering

--

## Deferred

<pre><code class="lang-html">&lt;script src="deferred-1.js" defer>&lt;/script>
&lt;script src="deferred-2.js" defer>&lt;/script>
</code></pre>

- Garantie auf Reihenfolge
- Verzögert DOMContentLoaded Event
- wenn `deferred-1.js` langsam ist blockiert auch die Ausführung von `deferred-2.js`

--

## Async

<pre><code class="lang-html">&lt;script src="async-1.js" async>&lt;/script>
&lt;script src="async-2.js" async>&lt;/script>
</code></pre>


- keine Garantie auf DOMContentLoaded Event
- keine Garantie auf `onload` Event
- keine Garantie auf Reihenfolge

--

## Inlining

- keine Blockierung 
- nur, wenn das Skript klein ist