# nodejs-best-practice
nodejs best practice

## large features should be seperated into another module.
## checking empty
```javascript
function isEmpty(obj) {
  if(obj === undefined || obj === null) {
    return true;
  }
  return false;
}
```
## convert object to string with `require('json-stringify-safe')` rather that `JSON.stringify(object)` to avoid circular object error
```javascript
require('json-stringify-safe');

```
## add type checking or conversion for input parameters
### use toString method before use split method
```javascript
var s = s && s.toString();
var sarr = s.split(':');
```

## prefer to use self rather than this
```javascript
function fun1() {
  var self = this;
  self.counter = 0;
  setInterval(function() {
     selft.count = (self.counter + 1) % 100;
  }, 1000);
}
```

