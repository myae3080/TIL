Variable Declaration
========================
- var
- let
- const

Code
------------------------
### var
* var로 변수 선언 시, function-scoped 또는 global-scoped. (변수 재선언, 재할당 가능)
``` javascript
if(1) {
    var str = 'test';
}

console.log(str);
```

* function-scoped라 다음과 같은 경우에는 밖에서 function 내 var를 참조할 수 없다.
``` javascript
testFn = () => {
    if(1) {
        var str = "Hi";
    }

    console.log(str);
}

//function scope 밖이라 referenceError 발생
console.log(str);
```

* 재선언이 가능하여 사용에 유의하여야 한다.(modern script에서는 일반적으로 사용 안함)
``` javascript
    var str = 'a';
    console.log(str); // a

    var str = 'b';
    console.log(str); // b
```

* 해당 변수가 사용되는 코드보다 후에 선언될 수 있다. 
``` javascript
    console.log(str); // ok

    var str = 'ok';
```

### let
* let으로 변수 선언 시, block-scoped. (변수 재선언 불가, 재할당 가능)
``` javascript
if(1) {
    let str = 'test';
}

console.log(str);
// Uncaught ReferenceError: str is not defined error
```

* 재선언 시, error 발생.
``` javascript
let test;
let test; 
// Uncaught SyntaxError: Identifier 'test' has already been declared
```

### const
* const는 재할당이 되면 안되는 값을 선언할 때 사용. (변수 재선언, 재할당 불가)
``` javascript
const str; 
// Uncaught SyntaxError: Missing initializer in const declaration
```

``` javascript
const str = 'immutable';

str = 'assign';
// Uncaught TypeError: Assignment to constant variable
```

Reference
------------------------
- JAVASCRIPT.INFO
