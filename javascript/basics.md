# Basics

- Initial value of JavaScript variables is `undefined`
- Performing operations on `undefined` variables result in NaN
- Concatenate `undefined` variable will result in `"undefined"` a `string`
- Variables initialized without the `var` keyword are available in `global` scope
- Use bracket notation when accessing object has space `obj1["First Name];`

## JavaScript Constructors

Basic Syntax
```
var Person = function() {
  this.first_name =  "John";
  this.last_name = "Doe";
};

var somePerson = new Persion();
```

Public Method and Private Properties
```
var Person = function() {
  // private property
  var prop = "private";
  
  // public method
  this.stuff = function() {
    return prop;
  };
};
```


# Arrays
## map

```
var newArray = oldArray.map(function(val) {
  return val + 1;
});
```
# Anti-patterns

## if / else


Anti-pattern
```
function equal(x,y) {
  if (x === y) {
    return true;
  } else {
    return false;
  }
}
```

Much beter
```
function equal(x,y) {
  return x === y;
}
```
