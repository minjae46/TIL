# label 태그에 대하여

label 태그의 `for` 속성 (React에서는 htmlFor)을 이용하여,  
input 등의 form 요소를 컨트롤 할 수 있다.

컨트롤 할 요소의 `id`와 label 태그의 `for` 속성이 같으면,  
label 태그로 `id`를 가진 요소를 컨트롤 할 수 있다.

```js
<!--
    # 매칭할 컨트롤 요소의 id 값인 "user-checking"을
    # label 태그의 for 속성의 값으로 지정
-->
<label for="user-checking">저를 클릭하세요.</label>
<input type="checkbox" id="user-checking">
```
