# HTTP?

WEB 서버와 클라이언트 간에 통신 규약(프로토콜)이다. 기본적인 순서는 클라이언트가 서버에게 요청하고(Request) 요청을 받은 서버는 클라이언트에게 응답(Respnose)를 한다. 프로토콜의 내용에는 헤더(편지 봉투와 같은 역할, 메타데이터)와 바디(편지의 내용물, 실제 데이터)로 구성되있다.

Request(요청)과 Response(응답)의 구조는 서로 비슷하다.


## HTTP Request header
<img src="https://mdn.mozillademos.org/files/13821/HTTP_Request_Headers2.png">


## HTTP Respnose header
<img src="https://mdn.mozillademos.org/files/13823/HTTP_Response_Headers2.png">



----

출처 : https://developer.mozilla.org/ko/docs/Web/HTTP/Messages

------
# HTTP 에러 코드별 원인과 해결 방법

## 413 error : Request Entity Too Large 파일 용량이 너무 커요

Nginx에선 Client max body size라는 옵션이 있는데, request body의 길이를 제한하는 옵션이다. 즉 'Content-Length'를 제한한다.(413 에러 발생)

기본 값으로 1MB로 설정이 되어 있는데, 이렇게 되면 1MB이상의 파일을 업로드하지 못한다. 이러한 제한을 건 이유는, 외부의 사용자가 서버에 의도적으로 과부하를 걸 수 있는 위험이 존재하기 때문이라고 한다. ( https://www.tecmint.com/limit-file-upload-size-in-nginx/ )

이를 해결하기 위해서 /etc/nginx/nginx.conf 파일에 옵션을 수정하면 된다.

```
http {
  client_max_body_size 100M; # body size 즉 Content-Length를 100M로 늘리기. 0M로 지정한다면 제한없음
}
```

