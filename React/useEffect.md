# useEffect

_컴포넌트가 렌더링될 때마다 특정 작업을 실행할 수 있도록 하는 Hook_

컴포넌트가 마운트(create) 될 때, 언마운트(destroy) 될 때, 그리고 업데이트 될 때 코드를 실행시켜 특정 작업을 실행시키고 싶을 때 사용한다.

useEffect는 아래와 같이 두 개의 argument를 가지는 함수이다.

1. 첫 번째 인자로는 실행하고자 하는 코드를 받는다.
2. 두 번째 인자로는 의존성 배열이라고 하는 것을 받는데, 이 배열에는 검사하고자 하는 특정 값(state, props 등)을 넣거나, 비워둘 수도 있다.

useEffect는 맨 처음 컴포넌트 렌더링 때 첫 번째 인자로 받은 함수를 한 번 실행하고, 그 이후에는 리액트가 의존성 배열을 관찰하여 배열 안에 특정값이 있다면 그 값이 변할 때마다 첫 번째 인자로 받은 코드를 재실행한다.

따라서 첫 번째 컴포넌트 렌더링 때 단 한번만 실행하고 싶은 코드라면, useEffect의 첫 번째 인자로 코드를 전달하고 의존성 배열은 비워두면 된다.

#### Cleanup

useEffect는 기본적으로 맨 처음 컴포넌트가 create될 때 첫 번째 인자로 받은 함수를 한 번 실행한다.

반대로 컴포넌트가 destroy될 때에도 코드가 실행되게 할 수도 있는데, 이를 통해 컴포넌트가 사라짐과 동시에 특정 함수가 실행되도록 하는 것이 가능하다.

useEffect의 첫 번째 인자로 들어가는 함수가 특정 코드를 return 하면, 이 코드는 컴포넌트가 destroy될 때 실행된다.

```js
function Hello() {
  useEffect(() => {
    console.log("hi :)"); // create 시 실행
    return () => console.log("bye :("); // destroy 시 실행
  }, []);
  return <h1>Hello</h1>;
}
```

위와 같이, 컴포넌트가 사라질 때 실행하고자 하는 작업을 첫 번째 인자의 함수가 **return**해 주면 된다.

이것이 가능한 이유는 다음과 같다.  
함수는 기본적으로 return하면 종료된다. return하지 않은 함수는 코드가 실행된 채로 계속 켜져 있는 것이나 마찬가지이고, return을 하게 되면 함수는 return하는 코드를 실행시킨후 자기자신은 종료되는 것이다.  
return은 함수를 kill하는 주문 같은 것이라고 생각하자.

이 작업을 통해 우리는 컴포넌트가 언제 create되고, 언제 destroy되는지를 정확히 아는 것이 가능하다.
