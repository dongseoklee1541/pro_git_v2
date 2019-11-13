## Thread
스레드는 프로세스처럼 프로세서를 사용하는 기본단위이면서 프로그램을 실행하는 프로세스 내의 개체, 즉 명령어를 독립적으로 실행할 수 있는 하나의 제어 흐름이다.

스레드의 특징
* 자원을 공유 : 제어를 제외한 코드 및 데이터
* 병렬로 수행
* 구성요소
  * Thread ID
  * Register Set (PC 등 제어를 위한 정보)
  * Stack (i.e. local data, 정보 저장용)
  

### 다중 처리(다중 프로세스) vs 다중 스레드
다중 프로세스 : 여러개의 프로세스가 동시에 작업, 각자 자신만의 제어와 자원을 가지고 작업한다.

다중 스레드 : 공통된 작업을 가지고 여러 쓰래드가 작업 , 자신만의 제어는 갖지만 공유된 자원을 사용한다.

즉 **자원 공유 여부**로 구분할 수 있다.

#### 스레드 장점
* 사용자 응답성(Responsiveness) : 일부 스레드의 처리가 지연되어도, 다른 스레드는 작업을 계속할 수 있다.
* 자원 공유(Resource sharing) : 자원을 공유해서 효율성 증가(커널의 개입을 피할 수 있음)
  * ex) 동일 address space에서 스레드 여러 개
* 경제성(Economy) : 스레드를 늘리는 것이 프로세스의 생성 및 프로세스 context switch에 비해 효율적
  * 쓰래드는 자원을 공유하기에, 프로세스의 context switch 보다 효율적이다.
* 멀티 프로세서 활용 : 병렬처리를 통해 성능이 향상됨

## 병행 프로세스와 동기화 및 상호배제

#### 용어 정리 
* Shared data(Critical data, 공유 데이터) : 여러 프로세스들이 공유하는 데이터
* Critical section(임계 영역) : 공유 데이터를 접근하는 코드 영역(code segment)
* Mutual exclusion(상호배제) : 둘 이상의 프로세스가 동시에 Critical section에 진입하는 것을 막는 것
* Primitive : 가장 기본이 되는연산

### Requirements for ME primitives
* Mutual exclusion(상호 배제) : Critical section(CS)에 프로세스가 있으면, 다른 프로세스의 진입을 금지
* Progress(진행) : CS 안에 있는 프로세스 외에는, 다른 프로세스가 CS에 진입하는 것을 방해하면 안됨
* Bounded waiting(한정대기) : 프로세스의 CS 진입은 유한시간 내에 허용되어야 함
