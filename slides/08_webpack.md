<!-- .slide: data-background="assets/6990221148_dff14b0f90_k.jpg" -->
<div class="attribution">Bild: [flickr/rdecom](https://www.flickr.com/photos/rdecom/6990221148/)</div>

# Advanced Tools

- Webpack
- Browserify
- RequireJS (r.js)
- SystemJS

--

<!-- .slide: data-background="assets/5364128968_7e7d01de07_o.jpg" -->
<div class="attribution">Bild: [flickr/pennuja](https://www.flickr.com/photos/pennuja/5364128968/)</div>

# Webpack

Note:

Schweizer Messer des Webs

--

<img data-src="assets/webpack.png">

> <footer>[webpack.github.io](http://webpack.github.io/)</footer>

--

### Module in CommonJS-Style

```js
module.exports = function add(a, b) {
    return a + b;
}
```

```
var add = require('./add');

console.log(add(5, 4) === 9); // true
```

... aber ES2015 oder AMD gehen auch

--

### Mit loaders kann man alles

```js
var template = require('./views/templates/product.html');

console.log(template); // <h1>Product</h1><p>{{ placeholder }}</p>....

```

nicht nur JavaScript

--

## Am Ende wird gebundlet

- ein oder mehrere Bundles können gemacht werden
- UglifyJS minifiziert

--

<!-- .slide: data-background="assets/2599394171_12d33a2459_o.jpg" -->
<div class="attribution">Bild: [flickr/ainet](https://www.flickr.com/photos/ainet/2599394171/)</div>

# Unit Testing

--

# ESLint, Mocha und Karma

- ESLint
- Karma ist der Test-Runner 
- Mocha ist der Test-Framework
- Unit Tests laufen in PhantomJS...
- ...und echten Browsern

Note:
- Datei Speichern -> Tests laufen sofort

- Zukunft: Notification

--

```js
describe('Array', function(){
    describe('#indexOf()', function(){
        it('should return -1 when the value is not present', function(){
            [1,2,3].indexOf(5).should.equal(-1);
            [1,2,3].indexOf(0).should.equal(-1);
        });
    });
});
```