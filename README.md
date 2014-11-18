C# like String Formatter for Javascript
================

Looking how to format string in the way [Node.js](http://nodejs.org/api/util.html#util_util_format_format) does, I found [this answer](http://stackoverflow.com/a/4673436) in StackOverflow.

Installation
-----

Download the [`string-formatter.js`](https://raw.githubusercontent.com/pandres95/string-formatter/master/string-formatter.js) file and put it at the top of the scripts chain in the HTML file. Or artenatively, if you use **bower**, you can add it as a dependency in your `bower.json` file:

```json
{
  "dependencies": {
    "string-formatter": "0.0.2"
  }
}
```

Usage
-----

Is really simple. Just write a C# formatting-like string, and use the `format` function indicating the parameters to be replaced, the magic is done by this library.

```javascript
console.log("How to {0} this {1}? Just {0} it!".format("use", "library"));
// --> How to use this library? Just use it!
```

Now, if you attempt to format using a parameter number which is lower than 0 or upper than the items' number, it will return the same {#} string:

```javascript
console.log("I will feed my {0} with {9} fish and {-1} bodies".format("cat", "fresh", "dead"));
// --> I will feed my cat with {9} fish and {-1} bodies
```
