# 동기/비동기

- [concurrency and parallelism](https://goodgid.github.io/Concurrency-vs-Paraleelism/)

- [Blocking/Non-Blocking & Sync/Async](https://goodgid.github.io/Blocking-NonBlocking-Synchronous-Asynchronous/)

    - 그렇다면, 동기이면서 논블로킹이고, 비동기이면서 블로킹인 경우는 의미가 있다고 할 수 있나요?

    : 둘 다 잘 사용되지는 않는다.
    
    node.js+MYSQL은 node.js가 Async로 통신을 요청하지만, MYSQL에서 제공하는 드라이버는 BLOCKING이다.
    -> Async+NON-BLOCKING 방식을 쓰는데, 그 과정중에 하나라도 BLOCKING으로 동작하면, BLOCKING-Async
    

    - I/O 멀티플렉싱에 대해 설명해 주세요.

    : 하나의 쓰레드가 여러개의 소켓을 관리하는 방식이다. -> 이를 서버-클라이언트 모델에 적용해서, 하나의 서버가 여러개의 클라이언트 요청을 처리함.

     하나의 서버가 여러개의 클라이언트를 관리 -> 각 클라이언트에서 요청에 대한 응답을 순서신경안쓰고 함(async) + 클라이언트 요청 들어올떄까지 기다림(BLOCKing) -> 하지만 BLOCKing-async와 I/O멀티플렉싱이 같다고 하는건 애매함.

## 동기화 기법

- 동기화를 구현하기 위한 하드웨어적인 해결 방법

    - volatile 키워드는 어떤 의미가 있나요?

    - 싱글코어가 아니라 멀티코어라면, 어떻게 동기화가 이뤄질까요?

### [스핀락](https://goodgid.github.io/Spin-Lock/)


### 뮤텍스 vs 세마포어

- [임계영역(critical section) / 세마포어(semaphores)](https://velog.io/@haero_kim/%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4-%EB%8F%99%EA%B8%B0%ED%99%94-%EC%9D%B4%EC%95%BC%EA%B8%B0)

- ![뮤텍스 vs 세마포어](https://cdn.discordapp.com/attachments/396651873811169284/1036218392799092806/unknown.png)

    - 이진 세마포어와 뮤텍스의 차이에 대해 설명해 주세요.

    : 위의 이미지 참고.

### 모니터

- thread pool

- fork-join



### 어토믹