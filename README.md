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

## Use hippie and supertest for testing

## use nock to mock http test


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
## use `module.exports` rather than `export`

##  exports with functions or properties
```
//good
module.exports.function = function1
//bad
module.exports = function
```

## mocha unit test
use test folder rather than tests folder

add `--recursive` in file test/mocha.opts
```javascript
cat test/mocha.opts
--recursive
```








