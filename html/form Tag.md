# form 태그에 대하여

form 태그의 기본 동작은 submit이다.

form 태그의 가장 강력하고 중요한 두 속성은 다음과 같다.

1. action : 어느 URL로 data를 보낼 것인가?
2. method : 어떤 방식으로 data를 보낼 것인가?
   - GET or POST?

<br/>

action 속성에 URL를 지정하고 submit 하면,  
input에 입력한 data가 URL로 전달된다.

즉, form 태그의 기능이란,  
사용자가 입력한 정보(data)들을 action 속성이 가리키는 서버 주소로, _쿼리스트링_ 형태로 전송해주는 것이다.
