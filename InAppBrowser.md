## Build phonegap app

---

navigate to path

```
./app-name/www/js/index.js
```

append to the OnDeviceReady: function() {

```js
var ref = window.open(url, target, options);
ref.addEventListener('loadstart', function() { console.log('start: ' + event.url); });
ref.addEventListener('loadstop', function() { console.log('stop: ' + event.url); })
ref.addEventListener('exit', function() { console.log(event.type); });
```
