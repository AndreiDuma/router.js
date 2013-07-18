router.js
=========

router.js - a tiny hash (#) router with redirects included

## Usage
Include `routes.js` in your code. A global `Router` object will be visible. Add routes:
```js
Router.routes(
    /^#\/$/, function() {alert('home');},
    /^#\/routes\/?$/, function() {alert('routes');}
);
```

You may also add redirects:
```js
Router.redirects(
    /^.*$/, "#/"
)
```
