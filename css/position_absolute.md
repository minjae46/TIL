# position : absolute;

요소를 페이지 layer에서 분리(html 문서 흐름에서 제거)시켜서 기준 요소를 기준으로 원하는 위치에 둘 수 있다.

**부모 요소**를 기준으로, top, bottom, left, right 속성으로 배치된다.

> top : 기준 요소로부터 위쪽에서의 거리  
> bottom : 기준 요소로부터 아래쪽에서의 거리  
> left : 기준 요소로부터 왼쪽 끝에서부터의 거리  
> right: 기준 요소로부터 오른쪽 끝에서부터의 거리

부모 ~ 조상 요소 중에 position 속성(static을 제외한 relative, absolute, fixed 중 하나)을 가진 요소가 있으면, 그 부모 요소를 기준으로 움직인다.

position을 가진 조상이 하나도 없을 경우, 가장 상위 html 태그인 body 태그를 기준으로 움직인다.
