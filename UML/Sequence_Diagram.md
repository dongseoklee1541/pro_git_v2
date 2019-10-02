## Sequence Diagram

문제 해결을 위한 객체를 정의하고 객체간의 상호작용 메시지 시퀸스를 시간의 흐름에 따라 나타내는 다이어그램


## 구성요소

<img src="https://github.com/dongseoklee1541/programming_concept/pic/sequence-diagram-overview.png">

> 시퀸스 다이어그램을 구성하는 주요 요소

### Lifeline
Lifeline은 시퀸스 다이어그램 상의 독립적인 참여자를 나타낸다. 여러 구성 요소들과 달리 Lifeline은 2개 이상 다중으로 존재할 수 없는, 각각이
단 하나의 상호 작용 주체이다.

Lifeline의 symbol은 아래와 같이 사각형 형태에 수직선이 연결되어 있는 모습이고, 사각형 안에 Lifeline(참여자)에 대한 정보를 나타내고
수직선은 해당 참여자의 생명선을 나타낸다.

<img src="pic/object_lifeline.png">

> object와 Lifeline

### 메시지(Message)

서로 다른 객체간의 **상호작용 혹은 의사소통 통신을 정의하는 요소.** 하나의 객체 라이프라인으로 부터 다른 객체 라이프라인까지 선+화살표로 표시되며
메시지는 그 선의 위에 표시

<img src="pic/message.png">

> 메시지

#### 메시지 유형

<img src="pic/message_type.png">

메시지 유형에 따른 선 모양과 화살표 모양을 꼭 기억하자.

* 동기 메시지(Synchronous message) : 메시지 전송 객체가 계속하기 전까지 동기 메시지에 대한 응답을 기다림. 프로그램 내 일반적인 함수 호출과
동일한 동작 방식의 메시지를 표현

* 비동기 메시지(Async message) : 메시지 전송 객체가 계속하기 전까지 응답을 요구하지 않는 메시지. 전송 객체의 호출만을 표시. 보통 개별 쓰레드
간의 통신 및 새 쓰레드의 생성에 사용

* 자체 메시지(Self meesage) : 자신에게 보낸 메시지. 결과로 생성되는 실행 발생이 전송 실행 위에 나타남.

* 반환 메시지(Reply/Return message) : 이전 호출의 반환을 기다리는 객체에게 다시 반환되는 메시지.

### Gate
Gate는 (시퀀스 다이어그램 내부)Message의 끝으로, 시퀀스 다이어그램으로 보여지는 범위 외부의 message에 대한 연결점으로, 이를 사용하는 목적은
모든 message에 대한 발신자와 수신자를 구체화하기 위함이다.

### 활성 박스(Activation Box)

<img src="pic/activation_box.png">

> 활성 박스(Activation Box)

객체 라이프 라인 위에 그려지는 박스로 이 박스위에서 객체의 호출이 이루어진다. 객체의 특정 메소드 실행 혹은 정보 처리가 실행되고 있거나
다른 객체의 메소드가 종료되기를 기다린다는 것을 나타낸다.(동기 메시지)

### 작성
시퀸스 다이어 그램의 작성방법을 알아보자.

#### 작성 순서

* 유스케이스 정의서 분석을 통한 참여 객체 파악
* 액터와 참여 객체를 x축에 나열
* 객체의 메시지를 정의하고 메시지 호출을 시간 순서에 따라 표시



---
출처 : https://thinking-jmini.tistory.com/29
출처 : https://sswpgm.tistory.com/29
