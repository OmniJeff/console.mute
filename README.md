# console.mute
Temporarily mute console.log in node.js. Resume and retrieve logged data later. Useful for intercepting logged data from any module and when testing modules that insist on logging all the things. Based on [this gist](https://gist.github.com/pguillory/729616#file-gistfile1-js-L8). [Here's a gist](https://gist.github.com/karlpokus/473de03f769f39796d44d3014c979719) that works in the browser.

# Install
```
$ npm install console.mute
```

# Usage
```javascript
require('console.mute'); // adds mute and resume to console

console.log('a'); // will log
console.mute(); // mutes log
console.log('b'); // will not log
console.log('c'); // will not log
var data = console.resume(); // resumes log and returns logged data during mute
console.log('d'); // will log
console.log(data); // logs ['b', 'c']
```

# Test
```
$ npm test
```

# Todo
- mute console.error et al

# Licence
MIT
