```js

(function (root, factory) {
    if (typeof define === 'function' && define.amd) {
        // AMD. Register as an anonymous module.
        define(['exports'], factory);
    } else if (typeof exports === 'object' && typeof exports.nodeName !== 'string') {
        // CommonJS
        factory(exports);
    } else {
        // Browser globals
        root.avama = typeof avama === "undefined" ? {} : avama;
        factory(root.avama);
    }
}(this, function (exports) {

    function returnHello() {
        return "hello";
    }

    // attach properties to the exports object to define
    // the exported module properties.
    exports.subModuleName = {
        returnHello: returnHello
    };
}));
```
