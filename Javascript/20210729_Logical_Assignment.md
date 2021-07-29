Logical Assignment
========================
- &&, ||, ??를 사용한 코드를 조금 더 줄여 사용할 수 있도록 지원되는 방식.(chrome 85 이후 지원)


Code
------------------------
### Logical AND Assignment
* 기존 코드
``` javascript
let a = true;

a = a && 3;     // a && (a = 3);
console.log(a);     // 3
```

* 최근 코드
``` javascript
let a = true;

a &&= 3;
console.log(a);     // 3

let b = 0;

b &&= 10;
console.log(b);     // 0
```

### Logical OR Assignment
* 기존 코드
``` javascript
let a = false;

a = a || 3;     // a || (a = 3);
console.log(a);     // 3
```

* 최근 코드
``` javascript
let a = '';

a ||= 10;
console.log(a);     // 10

let b = 5;

b ||= 10;
console.log(b);     // 5
```

### Logical Nullish Assignment
* 기존 코드
``` javascript
let a;

a = a ?? 3;     // a ?? (a = 3);
console.log(a);     // 3
```

* 최근 코드
``` javascript
let a;

a ??= 10;
console.log(a);     // 10

let b = null;

b ??= 10;
console.log(b);     // 10

let c = 'null';

c ??= 100;
console.log(c);     // 'null'
```

Reference
------------------------
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND_assignment
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR_assignment
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_nullish_assignment