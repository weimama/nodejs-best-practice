# nodejs-best-practice
nodejs best practice

## checking empty
```javascript
function isEmpty(obj) {
  if(obj === undefined || obj === null) {
    return true;
  }
  return false;
}
```
## use toString method before use split method
```javascript
var s = s && s.toString();
var sarr = s.split(':');
```
