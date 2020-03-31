# 무선 LAN과 네트워크 연결장치

## 무선 LAN 구조
무선 LAN은 BSS와 ESS라는 두 종류의 서비스를 지원한다.

#### AP(Access Point)
유무선 공유기, 무선 LAN과 직접적으로 관련된 장비를 AP라고 한다.

----

### BSS(Basic Service Set)
하나의 AP내에서의 서비스이며, 2개의 모드가 존재한다.

* Infrastructure 모드 : AP라는 중앙의 기지국을 사용하는 모드

* Ad hoc 모드 : AP가 없는 모드

-----

### ESS(Extended Service Set)
AP를 갖는 여러 BSS로 구성된 서비스, 회사와 같은 곳에서 주료사용한다. 영업 부서, 기술 부서등 AP를 사용해서 인터넷을 사용할 건데 그 과정에서
한 회사에서 정보를 주거니 받거니 하니까.


#### MAC 부계층
유선에서 앞서 말했던 MAC을 무선에서는 두개로 쪼갠다. PCF와 DCF로 나뉘는데, PCF는 선택사항으로 복잡한 접근제어를 수행하는 녀석이다.
무선에서의 MAC은 DCF라 생각하자. 

* Ad hoc에선 사용을 못하고 Infrastructure모드에서만 가능(AP가 있어야 한다)

#### DCF(Distributed Coordination Function
무선은 CSMA/CA 를 사용한다. 유선에서 사용하던
CSMA/CD는 무선에서 사용하기 어렵다. 신호가 점점 약해지기때문에 충돌이 난건지, 구별하기가 어렵기때문이다.

* Hidden Terminal 문제 : 데이터를 보내기전에 RTS(Request To Send),CTS(Clear To Send)을 주고받는 과정이 필요

즉 CTS를 받는다면, 다른 누군가가 데이터를 전송할려고 한다는 뜻으로 이해하면된다. 그리고 ACK가 올때까지 기다린 뒤 데이터를 전송하자.

### PCF(Point Coordination Function)
PCF는 선택사항으로 infrastructure 네트워크에서만 운용이 가능하다. 시간에 민감한 전송을 하고자 할때 사용한다. 

* 폴링 방법 : (야! 너 데이터 보낼거 있어?라고 물어보는 것)으로 내가 데이터를 마음대로 보내는게 아니라 먼저 물어본다.


### Blutetooth
서로 다른 기능의 기기들이 서로 연결하기 위한 무선 LAN기술, ad hoc 네트워크를 사용한다.

* 피코넷(Piconets) : 중앙의 통제가 있으면 거기에 블루투스 기기가 여러개 붙을 수 있는데, 이를 피코넷이라고 한다.
하나는 마스터(primary)가 되고 나머지는 종속 시스템(secondaries 또는 slaves)로 구성된다. 종속 시스템은 최대 7개까지 연결 즉 총 8대가 하나의
네트워크를 형성한다. 
  * 링크의 종류 : 피코넷은마스터와 종속시스템 사이에 2가지 형태의 링크가 존재한다.
    * SCO(Synchronous Connection-Oriented)링크 : 음성과 같이 지연이 에러보다 중요한 경우 사용
    * ACL(Asnchronous Connectionsless Link)링크 : 데이터 전송과 같이 데이터의 무결성이 중요한 경우 사용
    
