# TCP

- [TCP, UDP](https://goodgid.github.io/TCP-UDP/)


- [흐름/혼잡/오류 제어 기법](https://goodgid.github.io/Error-Flow-Control/)

## TCP vs UDP


    - 왜 HTTP는 TCP를 사용하나요?

    : 기본적으로 신뢰성을 필요로 하기 때문에 TCP를 기반으로 HTTP를 구현하게 됨.

    - 그렇다면, 왜 HTTP/3 에서는 UDP(QUIC) 를 사용하나요? 위에서 언급한 UDP의 문제가 해결되었나요?

    : UDP의 헤더크기가 가볍기 때문에, TCP 만큼의 신뢰성을 확보하기 위한 원하는 기능을 추가하였음
     -> 속도 지연을 최소화함.
     -> 첫 연결설정에서 데이터를 함께 전송, 연결 성공 시 설정을 캐싱하여 다음 연결때 바로 성립
     -> 그 외에 TLS를 사용하여 보안성을 확보함.

    - 본인이 새로운 통신 프로토콜을 TCP나 UDP를 사용해서 구현한다고 하면, 어떤 기준으로 프로토콜을 선택하시겠어요?

    : 신뢰성과 속도를 저울질 함. 속도의 중요성을 기준

    - Checksum이 무엇인가요?

    : 비트 데이터의 오류 검출을 하는 방법

    - TCP와 UDP 중 어느 프로토콜이 Checksum을 수행할까요?

    : 둘다, UDP는 오류 제어를 하지않기 때문에 간단함. 

    - 그렇다면, Checksum을 통해 오류를 정정할 수 있나요?

    : 오류를 검출하는 것임, 정정은 못함

    - TCP가 신뢰성을 보장하는 방법에 대해 설명해 주세요.

    : 위의 링크 참고

    - TCP의 혼잡 제어 처리 방법에 대해 설명해 주세요.

    : 위의 링크 참고


### 3-way-handshake, 4-way-handshake

- [3-way-handshake, 4-way-handshake](https://goodgid.github.io/TCP-IP-3Way-4Way/#tcp-3-way-handshake)

### [TCP,UDP 패킷의 구조](https://github.com/WeareSoft/tech-interview/blob/master/contents/network.md#tcp%EC%99%80-udp%EC%9D%98-%ED%97%A4%EB%8D%94-%EB%B6%84%EC%84%9D)

