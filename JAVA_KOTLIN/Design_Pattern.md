

## [observer pattern](https://velog.io/@haero_kim/%EC%98%B5%EC%A0%80%EB%B2%84-%ED%8C%A8%ED%84%B4-%EA%B0%9C%EB%85%90-%EB%96%A0%EB%A8%B9%EC%97%AC%EB%93%9C%EB%A6%BD%EB%8B%88%EB%8B%A4)

- 단점: thread safe 하지않음, 알림 순서가 보장이 안됨

## [싱글톤 패턴](https://velog.io/@haero_kim/%ED%98%B9%EC%8B%9C-%EC%8B%B1%EA%B8%80%ED%86%A4%EC%9D%B4%EC%84%B8%EC%9A%94-%EC%A0%80%EB%8A%94-%EB%B2%99%EA%B8%80%ED%86%A4%EC%9D%B4%EC%97%90%EC%9A%94-%E3%85%8B%E3%85%8B%E3%85%8B)

        - 싱글턴 패턴의 단점은?

- [thread-safe 방법들](https://seunghyunson.tistory.com/28)

- Enum 방식은 Android 같이 Context 의존성이 있는 환경일 경우, Singleton의 초기화 과정에 Context라는 의존성이 끼어들 가능성이 있다.

- 싱글턴에 비해 static은 할 수 없는 일

        1. 다형성을 사용할 수 없다. -> 정적클래스는 상속이 불가능하다.

        2. 싱글턴에서 멀티턴 패턴(하나가 아닌 여러 개 반환 즉 객체 최대 n개 반환)으로 바꿀 수 없다.

        3.  객체의 생성 시점을 제어할 수 없다.

        Java의 static은 프로그램 실행 시에 초기화된다.
        싱글턴은 getInstance 호출할 때 객체를 만드므로 제어가 그나마 가능하다.


## builder pattern


## [템플릿 메소드(Template Method) 패턴](https://goodgid.github.io/What-is-Template-Method-Pattern/)


## [어댑터 패턴](https://velog.io/@haero_kim/%EC%9A%B0%EB%A6%AC%EB%8A%94-%EC%9D%B4%EB%AF%B8-%EC%96%B4%EB%8C%91%ED%84%B0-%ED%8C%A8%ED%84%B4%EC%9D%84-%EC%95%8C%EA%B3%A0-%EC%9E%88%EB%8B%A4#%EC%8B%A4%EC%83%9D%ED%99%9C%EC%97%90%EC%84%9C%EC%9D%98-%EC%96%B4%EB%8C%91%ED%84%B0)

        - 단점

                - 객체를 구성으로 결합하면 어댑터는 클라이언트에서 사용하는 인터페이스 방식으로 메서드를 새로 생성한다. 어댑터가 새로운 메서드를 재구성할 때 추가 코드가 필요하다.

                - 프로젝트에서 어댑터 패턴을 적용한다고 코드의 성능이 개선되지는 않는다. 오히려 어댑터를 통해야 하므로 속도가 저하된다.