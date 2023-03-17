# 졸업작푼 난

Vite로 구동 시켜서, React 와  Node를 실행 시키고. Flask는 따로 AI Server를 이용해서 연결 시켰다.&#x20;

아직까지 로컬에서 진행해서  따로 도커라이징 필요가 없지만 다른게 사용될것같아서 진행하였다.&#x20;



계획없이 무작전 실행시키기만 위해서 코드를 짜다보니..  문제가 발생했다. Node.js 서버를 따로 열지 않고

vite-react 폴더안에 모든거 구현해서 서버실행시킬때도  따로 폴더를 타고들어가서 실행시키는 대참사가 발생했다.





문제 해결 방법으로 두가지를 생각했다.

1.  다시 프로젝트 생성하여 폴더구성을 서버와 클라이언트를 따로해서 재생성 하는 방법&#x20;

    \- docker file을 작성할때 그냥 실행만 해주면 되는지 정확하게 모르겠다 &#x20;

    \-클라이언트와 서버 동시실행은 concurrently 로 해주면 된도 (이번에 처음알았다..)&#x20;
2. &#x20;아니면 따로 node.js는 따로 빼서 작업하는 방법








