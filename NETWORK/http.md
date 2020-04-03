# HTTP?

WEB 서버와 클라이언트 간에 통신 규약(프로토콜)이다. 기본적인 순서는 클라이언트가 서버에게 요청하고(Request) 요청을 받은 서버는 클라이언트에게 응답(Respnose)를 한다. 프로토콜의 내용에는 헤더(편지 봉투와 같은 역할, 메타데이터)와 바디(편지의 내용물, 실제 데이터)로 구성되있다.

Request(요청)과 Response(응답)의 구조는 서로 비슷하다.


## HTTP Request header
<img src="https://mdn.mozillademos.org/files/13821/HTTP_Request_Headers2.png">


## HTTP Respnose header
<img src="https://mdn.mozillademos.org/files/13823/HTTP_Response_Headers2.png">



----

출처 : https://developer.mozilla.org/ko/docs/Web/HTTP/Messages


## Client max body size?
Nginx에선 Client max body size라는 옵션이 있는데, request body의 길이를 제한하는 옵션이다. 즉 'Content-Length'를 제한한다.(413 에러 발생) 
