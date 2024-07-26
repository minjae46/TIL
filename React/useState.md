# useState

_데이터값 변경에 따라 리렌더링을 유발(trigger)시키기 위한 리액트의 훅._

**React.useState()**  
초기 데이터값, 데이터값을 바꿀 수 있는 함수(modifier)가 담긴 **배열**을 반환한다.

```JS
// 구조분해할당 적용
const [state, setState] = React.useState(0);
console.log(state); // 0
setState(1); // 리렌더링
console.log(state); // 1
```

setState(modifier) 함수를 이용해서 state를 바꾸면, 해당 컴포넌트의 리렌더링이 일어나고 바뀐 데이터값으로 UI가 업데이트된다.

## modifier 함수

modifier 함수는 비동기로 동작한다.

modifier 함수로 state 값을 변경하는 방법 2가지 :

1. modifier 함수에 직접 값을 넣어서 state를 변경 :
   ```js
   setState(3);
   ```
2. 기존 state값을 기반으로 값을 업데이트 :
   ```js
   setState((current) => current + 1);
   // setState(state + 1);처럼 사용하지 않는다 !
   ```

단, 2번의 방법을 사용할 때에는 반드시 '함수'를 사용하여 현재 state 값을 얻는 방식으로 업데이트해야 해야 안전하다.  
이전 state값을 그대로 사용하는 경우, 외부 요소로 인한 변경 위험을 다 막을 수 없기 때문이다.
