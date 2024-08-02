# Props란

_부모 컴포넌트에서 자식 컴포넌트로 내려주는 속성값properties_

부모 컴포넌트로부터 자식 컴포넌트에 데이터를 보내는 일종의 방식이다.

## 리액트에서의 컴포넌트 재사용

리액트의 컴포넌트란, 어떠한 JSX를 return하는 함수를 말한다.

props를 컴포넌트에 전달한다는 것은 곧 컴포넌트에 어떠한 정보를 전달하는 것인데, 이에 따라 컴포넌트에 서로 다른 props를 전달하면 같은 컴포넌트라도 여러 곳에 다양한 방식으로 사용할 수 있게 된다.

위에서 말한대로 컴포넌트는 JSX를 반환하는 함수이므로, 컴포넌트에 무언가를 전달하려면 함수의 인자*argument*로서 전달해야 한다. 이 인자를 리액트에서는 **props**라고 부르는 것이다.

결국 리액트의 컴포넌트란, 컴포넌트라는 '함수'에 props라는 '값'을 넣어서 각기 다른 결과물이 나오도록 사용하는 것과 같다.

## Props의 형태

```js
// 부모 컴포넌트
function App() {
  return (
    <div>
      <Btn name="button" />
    </div>
  );
}

// 자식 컴포넌트
function Btn(props) {
  console.log(props); // {name : "button"}
  return <button>{props.name}</button>;
}
```

props를 자식 컴포넌트에게 전달할 때, 컴포넌트에 html 태그의 attribute 형태로 입력하지만, 실제로 리액트는 모든 props를 객체object에 담아 **key:value** 쌍으로 전달한다.

- props는 컴포넌트가 전달받는 첫 번째이자 유일한 인자이다.
- props는 object 형식으로 전달된다. object { } 안에 모든 property가 **key : value** 쌍으로 차례로 들어 있다.
- props에는 숫자, 문자, boolean, 그리고 **함수**도 인자로 전달될 수 있다. 즉, 이벤트리스너를 컴포넌트의 props로 전달하는 것이 가능하다.
