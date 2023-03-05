---
description: 이론에 자신없는 내가 실습을 통해얻는것들
---

# Django part 2

DRF를 사용할때  가장 많이 사용했던 내용들을 정리 하고싶었다.&#x20;





### Attribute error

설칭을 했을때,  변수명 또는 클래스 이름의 오타로 많이 나오는 오류 라고 한다 그래서 비슷한 변수명을 사용하고있었던 나는 당연히 오타  문제로 잘못된거같았는데. 알고보니 related\_name 부분을 까먹고 안썼다...&#x20;

\*\*\*  object has no attribute \*\*\*  해당 에러는 realte\_name 따라서 역참조를 해줘야되는 상황에서 필수존재이다,&#x20;

\[class\_name]_set 을 해주던, related\_name을 쓰던.._&#x20;

_난또 오타낸줄알았지..._&#x20;











