currentTarget vs target
========================
- 이번 정리에서는, DOM 내 위치한 event를 뜻하는 Event interface 내 여러 속성 중, 다음 두 가지를 본다.
- currentTarget
- target

Code
------------------------
### HTML
* div에 click event를 붙이고 click을 했을 시, 차이점을 보면 다음 과 같다.
``` HTML
<div id="test">
  <span>
	Click!
  </span>
</div>
```

* currentTarget의 경우, event handler가 걸려 있는 해당 요소를 반환하고,
target은 event가 처음 발생한 요소를 반환한다.
``` javascript
const test = document.getElementById("test");

test.addEventListener("click", () => {
	console.log(event.currentTarget.tagName); 	// DIV
	console.log(event.target.tagName);	// SPAN
});
```


Reference
------------------------
- https://developer.mozilla.org/ko/docs/Web/API/Event
