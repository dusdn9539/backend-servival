# URI & MIME type

## 1. URI

* 리소스를 식별하는 방법 - 식별할 때는 식별자(Identifier = ID)를 사용

1\) URL(Uniform Resource Locator) → 리소스의 위치를 표현. 위치 변경에 취약함.

* [https://app.gitbook.com/](https://app.gitbook.com/)

2\) URN(Uniform Resource Name) → 리소스의 “유니크”한 이름. 사실상 쓰이지 않음.

* 종종 내부에서만 사용해야할때 사용하기도 함
* urn:<mark style="color:red;">isbn</mark>:9780141036144 - 도서, 음반 등에서 사용
* &#x20;urn:ietf:rfc:7230&#x20;

## 2. MIME Type (Content Type)

1. text/plain -> E-mail에서 자주 사용.
2. text/html -> 일반적인 웹 문서. HTML 문서.
3. text/css
4. text/javascript
5. application/xml -> 범용. 자기서술적이기 상대적으로 어렵다.
6. application/atom+xml ->범용, 각각이 어떤 의미를 가진다가 정해져있음, 트렌드가 아니라 사용하지는 않음
7. application/json -> 범용. 자기서술적이기 굉장히 어렵다.
8. application/dns+json
