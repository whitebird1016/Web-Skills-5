# Web-Skills(5)
![Shikamaru](https://github.com/whitebird1016/Web-Skills-with-Shikmamaru/blob/main/1_HTGSqvOc52yfMwyLhCMjVA.jpeg)
<h2>Object Skills</h2>
<h3>1: Clone object</h3>

```
const _obj = { a: 0, b: 1, c: 2 };
const obj = { ..._obj };
const obj = JSON.parse(JSON.stringify(_obj));
// obj => { a: 0, b: 1, c: 2 }
```
<h3>2: Merge objects</h3>

```
const obj1 = { a: 0, b: 1, c: 2 };
const obj2 = { c: 3, d: 4, e: 5 };
const obj = { ...obj1, ...obj2 };
// obj => { a: 0, b: 1, c: 3, d: 4, e: 5 }
```
<h3>3: Object Variable Properties</h3>

```
const flag = false;
const obj = {
    a: 0,
    b: 1,
    [flag ? "c" : "d"]: 2
};
// obj => { a: 0, b: 1, d: 2 }
```
<h3>4: Create a pure empty object</h3>

```
const obj = Object.create(null);
Object.prototype.a = 0;
// obj => {}
```
<h3>5: Delete object useless properties</h3>

```
const obj = { a: 0, b: 1, c: 2 }; 
const { a, ...rest } = obj;
// rest => { b: 1, c: 2 }
```
<h3>6: Destructuring object property nesting</h3>

```
const obj = { a: 0, b: 1, c: { d: 2, e: 3 } };
const { c: { d, e } } = obj;
// d e => 2 3
```

<h3>7: Destructuring object property aliases</h3>

```
const obj = { a: 0, b: 1, c: 2 };
const { a, b: d, c: e } = obj;
// a d e => 0 1 2
```

<h3>8:  Destructuring object property default values</h3>

```
const obj = { a: 0, b: 1, c: 2 };
const { a, b = 2, d = 3 } = obj;
// a b d => 0 1 3
```
