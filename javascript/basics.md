# Basics

- Initial value of JavaScript variables is `undefined`
- Performing operations on `undefined` variables result in NaN
- Concatenate `undefined` variable will result in `"undefined"` a `string`
- Variables initialized without the `var` keyword are available in `global` scope
- Use bracket notation when accessing object has space `obj1["First Name];`

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
