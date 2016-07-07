# openweathermap-js
Node.js module to simplify use of Openweathermap weather APIs in node.js projects.

## How it works
To use it, simply use the require function in your node.js app.
```
const weather = require('openweathermap-js');
```
You can then use the included functions :
```
weather.defaults({
  location: 'Muhlbach-sur-Munster',
  appid:    'xxxx',
  …
});

weather.current(function(data, err) {
  if (!err)
    console.log(data);
  else
    console.error(err.message());
});

weather.forecast({location: 'Paris'}, function(err, data) {…});
weather.daily({cnt: 5}, function(err, data) {…});
```
