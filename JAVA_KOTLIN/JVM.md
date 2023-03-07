# [?Java Virtual Machine](https://goodgid.github.io/Java-JVM/)

    - 안드로이드에서 JVM 원리에 대해서 설명

    - jvm 외에도 여러 플랫폼에서 호환되는게 뭐가 있는지 말해주세요
## [메모리구조]()

    - 메모리 구조에서 스택과 힙의 차이

    - 힙 영역의 데이터는 어떻게 삭제가 될까?

    : GC가 힙 영역의 데이터를 삭제한다.

# JAVA파일의 컴파일 과정

- [간단한 요약](https://yang-droid.tistory.com/48)

## Garbage Collection

- 안드로이드 컴파일에서 Dalvik은 GC 방법으로 CMS 알고리즘을 사용하고, ART는 Customed CMS 알고리즘을 사용한다.

- [GC 기초, minor GC 위주](https://velog.io/@haero_kim/Garbage-Collection-%EA%B8%B0%EC%B4%88-%EA%B3%B5%EB%9E%B5%ED%95%98%EA%B8%B0)

    - GC가 어떻게 객체가 더이상 사용되지 않는지 알수있는가?

- [major GC: 4가지 알고리즘](https://goodgid.github.io/Java-Garbage-Collection-(2)/)

- [GC 총 정리](https://s2choco.tistory.com/14)

        - Young 영역에서 Old 영역으로 객체가 이동하는 것을 Promotion 되었다고 표현한다.

        - Old 영역에서도 GC에서 오래 살아남은 객체들은 Permanent Generation으로 이동하게 되는데, 이 영역에서도 Major GC로 unreachable한 객체를 회수한다. Major GC이기 때문에 STW(stop the world)가 발생한다.

        - Old 영역에 512 바이트 chunk의 card table이 존재한다.

            - old 객체에서 young 객체로의 참조 정보를 담고 있어 Minor GC 실행 시 메모리 회수 대상인지 아닌지를 빠르게 판단한다.

            - 약간의 overhead가 발생하지만 전반적인 GC시간을 줄여준다.

## 프로그램 실행의 일련과정
