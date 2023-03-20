# http

- [ref](https://goodgid.github.io/HTTP-Communicate-Process/)

- [쿠키와 세션](https://goodgid.github.io/Cookie-vs-Session/)

- [request, response 메시지 구조]()

    - 메시지 바디에는 json 말고 다른 데이터가 들어가는 경우가 있나?

    - get 메소드 요청에는 바디를 담을 수 있는가?

## HTTP method

- [post vs put vs patch](https://goodgid.github.io/HTTP-Method-Post-vs-Put-vs-Patch/)
- [other concept](https://goodgid.github.io/REST-Method-Idempotent-Options-Head-Trace-Connect/)

    - HTTP Method의 멱등성에 대해 설명해 주세요.

    : 멱등성이란, 동일한 요청을 여러 번 보내더라도 서버의 상태가 변하지 않는 것을 의미한다. 
      예를 들어, GET 메소드는 멱등성을 가지고 있지만, POST 메소드는 멱등성을 가지고 있지 않다. 

      POST 메소드는 멱등성을 가지고 있지 않기 때문에, 동일한 요청을 여러 번 보내면 서버의 상태가 변할 수 있다. 
      (ex, post를 두번 사용하면, 같은 값의 두개의 리소스가 생기게됨. 리소스 생성말고도 다른 작업 수행할때도 post를 사용함)
      따라서, 멱등성을 가지고 있지 않은 메소드는 서버의 상태를 변경하는 메소드이다.

    - GET과 POST의 차이는 무엇인가요?

    : get은 url을 통해 리소스를 조회하는 메소드이고, 길이에 제한 있음, 캐시를 사용해서 시간 단축가능.
      post는 body를 통해 리소스를 생성하는 메소드이고, 길이에 제한없음. 

    - POST와 PUT, PATCH의 차이는 무엇인가요?

    : post는 리소스를 생성하는 메소드이고, put은 리소스를 수정하는(덮어씌워서) 메소드이다. 
      patch는 리소스의 일부를 수정할 수 있는 메소드이다.
      put은 멱등성을 가지고 있지만, patch는 멱등성을 가지고 있지 않을때도 있음(ex, 정수데이터를 10씩 더하게 할때).

    - HTTP 1.1 이후로, GET에도 Body에 데이터를 실을 수 있게 되었습니다. 그럼에도 불구하고 왜 아직도 이런 방식을 지양하는 것일까요?

    : GET은 리소스를 조회하는 메소드이기 때문에, Body에 데이터를 실어서 보내는 것은 권장하지 않는다. 

      기존 시스템에서 GET에 Body를 실어서 보내는 것을 지원하지 않을 때도 있기 때문이다.


## HTTPS

- [SSL(Secure Sockets Layer)](https://goodgid.github.io/TLS-SSL/)

    - SSL과 TLS의 차이는 무엇인가요?

    - 왜 HTTPS Handshake 과정에서는 인증서를 사용하는 것 일까요?

    - 공개키와 대칭키에 대해 설명해 주세요.

## HTTP 버전

 - [stateless, connectionless]()

### HTTP 1.1

- [ref](https://goodgid.github.io/HTTP-1.1/)

- [http keep alive](https://goodgid.github.io/HTTP-Keep-Alive/)

### HTTP 2.0

- [ref](https://goodgid.github.io/HTTP-2.0/)

### [HTTP 3.0](https://evan-moon.github.io/2019/10/08/what-is-http3/#%ED%81%B4%EB%9D%BC%EC%9D%B4%EC%96%B8%ED%8A%B8%EC%9D%98-ip%EA%B0%80-%EB%B0%94%EB%80%8C%EC%96%B4%EB%8F%84-%EC%97%B0%EA%B2%B0%EC%9D%B4-%EC%9C%A0%EC%A7%80%EB%90%A8)

## HTTP RESTFUL

- [rest api](https://goodgid.github.io/REST-API/)

- [url, uri, urn](https://goodgid.github.io/URL-URI-URN/)

## [HTTP 상태코드](https://goodgid.github.io/HTTP-Status-Code/)

    - 401 (Unauthorized) 와 403 (Forbidden)은 의미적으로 어떤 차이가 있나요?

    : 401은 인증이 필요하다는 뜻이고, 403은 감춰진 리소스에 접근하려 할 때이다.(인증 여부와 상관없이 보여주지 않음.)

    - 200 (ok) 와 201 (created) 의 차이에 대해 설명해 주세요.

    : 201은 새로운 리소스가 생성되었을 때 사용한다.(put, post 메소드를 사용할 때)