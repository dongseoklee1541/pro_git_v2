# RESTAPI?

## REST(REpresentational State Transfer)
RSET는 HTTP기반으로 필요한 자원에 접근하는 방식을 정해놓은 아키텍쳐. 기존 기술과 HTTP 프로토콜을 그대로 활용하기 때문에 웹의 장점을 최대한 활용할 수 있는 아키텍쳐 스타일. 다시말해 REST는 URI을 통해 **자원**을 표시하고, **HTTP METHOD(GET,POST..)** 를 이용하여 해당 **자원의 행위**를 정해주며 그 결과를
받는것을 의미한다.

* 자원(Resource) : 해당 소프트웨어가 관리하는 모든 것. 예를 들어 저장된 데이터(DBMS), 이미지/동영상과 같은 파일 또는 이메일 전송, 푸쉬 메시지와 같은 서비스를 모두 포함
* 자원의 표현(Representation) : 그 자원을 표현하기 위한 이름, DB의 학생 정보가 자원일 때, 'students'를 자원의 표현으로 정한다.
* 상태(정보) 전달 : 데이터가 요청되어지는 시점에서 자원의 상태(정보)를 전달한다. JSON 또는 XML을 통해 데이터를 주고 받는 것이 일반적이다.

### REST의 속성
* 서버에 있는 모든 자원은 각 자원 당 클라이언트가 바로 접근 할 수 있는 고유 URI 존재

* 모든 Request는 클라이언트가 요청할 때마다 필요한 정보를 주기에, 서버에서는 세션 정보를 보관할 필요가 없어 높은 자유도와 유연한 아키텍쳐 적응이
가능하다. 

* HTTP 메소드(GET, POST, PUT, DELETE) 메소드를 사용해 자원에 접근한다.

* 서비스 내에 하나의 자원이 주변에 연관된 리소스들과 연결되어 표현되어야 함

#### 자원(Resource)
REST에서는 자원에 접근할 때 URI(Uniform Resource Identifier)로 접근한다.


## REST API


## RESTFUL API?

정확한 정의는 없지만 RESTFUL이란 이해하기 쉽고 사용하기 쉬운 REST API를 만드는 것이다.


-------

https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html
https://medium.com/@dydrlaks/rest-api-3e424716bab
https://velog.io/@stampid/REST-API%EC%99%80-RESTful-API
