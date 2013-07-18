router.js
=========

router.js - a tiny hash (#) router with redirects included

## Usage
Include `routes.js` in your code. A global `Router` object will be visible. Add routes:
```js
Router.routes(
    /^#\/$/, function() {alert('home');},
    /^#\/routes\/?$/, function() {alert('routes');},
    /^#\/routes\/(\d+)\/?$/, function(id) {alert('route ' + id);},
    /^#\/message\/([a-zA-Z]+)\/?$/, function(msg) {alert(msg + '!');}
);
```

You may also add redirects:
```js
Router.redirects(
    /^#\/tracks\/?$/, "#/routes",    // Redirect #/tracks(/) to #/routes
    /^.*$/, "#/"    // Everything not yet matched redirects to #/
)
```
