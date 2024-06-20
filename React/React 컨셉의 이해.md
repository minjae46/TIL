# 왜 React인가?

## React의 핵심

> html을 먼저 구축한 후 자바스크립트로 DOM 요소들을 조작하는 방식이 아닌, 자바스크립트로 직접 DOM 요소(html)를 생성하는 것.

- **React.createElement()** : DOM 요소를 생성
- **ReactDOM.render()** : 생성한 요소를 html로 변환

모든 html 요소를 자바스크립트로 생성하기 때문에, DOM 요소를 찾아서 가져오고 직접 조작하는 복잡한 방식을 사용하지 않아도 된다.

리액트는 html elements를 직접 생성하며, 생성한 elements의 업데이트가 필요할 때에 자동으로 업데이트 해 준다.

## React와 event

_Interactive Web Application을 쉽게 만들기 위해 태어난 React_

웹사이트가 인터랙티브하다는 것은 곧 event를 감지한다는 것이다.  
자바스크립트의 addEvenetListener를 계속 추가하는 대신, React는 event를 property로 간단히 등록할 수 있도록 하였다.

## React의 UI 업데이트
