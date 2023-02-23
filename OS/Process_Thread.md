## 프로세스 vs [스레드](https://goodgid.github.io/What-is-Thread/)

    - 프로그램과 프로세스, 스레드의 차이에 대해 설명해 주세요.

    - 리눅스에서, 프로세스와 스레드는 각각 어떻게 생성될까요?

    - 자식 프로세스가 상태를 알리지 않고 죽거나, 부모 프로세스가 먼저 죽게 되면 어떻게 처리하나요?

    - 리눅스에서, 데몬프로세스에 대해 설명해 주세요.


## 멀티프로세스 vs 멀티스레드

- [Multi Processing, Multi Core, Multi Tasking, Multi Programming 개념](https://goodgid.github.io/OS-Concepts-Starting-with-Multi/)


- [?멀티스레드](https://goodgid.github.io/What-is-Multi-Thread/)

## PCB

- [?인터럽트](https://goodgid.github.io/OS-The-Principle-Of-Interrupt/)

    - 인터럽트는 어떻게 처리하나요?

    - Polling 방식에 대해 설명해 주세요.

    - HW / SW 인터럽트에 대해 설명해 주세요.

    : HW - 각 하드웨어 장치에 대한 I/O 큐에 줄서게 된다. I/O가 완료되면, 디스크 컨트롤러가 인터럽트가 발생시켜 해당 프로세스는 CPU 준비큐에 줄서게 된다. 


- [PCB / context switching](https://velog.io/@haero_kim/PCB-%EC%99%80-Context-Switching-%EC%95%8C%EC%95%84%EB%B3%B4%EA%B8%B0)

    - PCB가 무엇인가요?

    : 위의 링크 참고.

    - 그렇다면, 스레드는 PCB를 갖고 있을까요?

    : 스레드는 TCB(Thread Control Block)를 따로 갖고있음. PCB보다 적은 정보를 가지고 있음.

    - 프로세스와 쓰레드는 컨텍스트 스위칭이 발생했을 때 어떤 차이가 있을까요?

    : TCB는 커널 레벨에서 Context Switching의 기본 단위가 되며, 같은 프로세스에서의 스위칭에 대해서는 TCB 정보만 저장하면 된다.
      하지만 다른 프로세스 간의 스위칭을 할 때에는 PCB / TCB 정보를 모두 저장해야 한다.

    - 컨텍스트 스위칭이 발생할 때, 기존의 프로세스 정보는 커널스택에 어떠한 형식으로 저장되나요?

    : 링크드리스트, 주소값으로 연결되는 형태.

    - 컨텍스트 스위칭은 언제 일어날까요?

    : 스케줄링의 선점 허용 기간을 모두 소모, 인터럽트 발생, I/O 응답대기 등.

## 스케줄링

- [스케줄러의 종류]()

    - 현대 OS에는 단기, 중기, 장기 스케쥴러를 모두 사용하고 있나요?

    - 프로세스의 스케쥴링 상태에 대해 설명해 주세요.

    - preemptive/non-preemptive 에서 존재할 수 없는 상태가 있을까요?

    - Memory가 부족할 경우, Process는 어떠한 상태로 변화할까요?


- [스케줄링 알고리즘 종류]()

    - RR을 사용할 때, Time Slice에 따른 trade-off를 설명해 주세요.

    - 싱글 스레드 CPU 에서 상시로 돌아가야 하는 프로세스가 있다면, 어떤 스케쥴링 알고리즘을 사용하는 것이 좋을까요? 또 왜 그럴까요?

    - 동시성과 병렬성의 차이에 대해 설명해 주세요.

    - 타 스케쥴러와 비교하여, Multi-level Feedback Queue는 어떤 문제점들을 해결한다고 볼 수 있을까요?