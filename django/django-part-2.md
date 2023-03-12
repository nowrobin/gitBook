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

__

## 문제점들 .. 생각해야되는거...&#x20;

1. ~~deadline을 D-day로 주고싶은데, datefield 에서 integer로 바꾸는 방식?~~
   1. &#x20;~~받기전에 미리 가공해서 datefield 가 아닌 integerfield 로 저장 ?~~
   2. ~~Integer 변수를 하나더 선언해서 ,거기에 Dday를 저장하는 방식 ?~~ &#x20;
   3. 해결함, 문제는 retreive 메소드로 사용해서, 다시 불러올때 됨,... 이건  처음 만들어 질때부터 변경해야될듯...
2. Enum을 사용하고 싶은데 ,, 다중으로 사용하는 방법 ? 여러 타입으로 지정할수있지 않을까 ?&#x20;
   1. 예를 들어  frontend , deveops 둘다 선택??&#x20;









