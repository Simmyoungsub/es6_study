## 자바스크립트 개요
 + 자바스크립트의 활용범위
   - 서버 & 클라이언트 모두 개발가능
     - 서버개발
       - Node.js의 등장으로 서버개발도 활발히 이루어지고 있음
       - express나 socket.io등의 라이브러리가 있음
    - 모바일에서도 많이 쓰이는 추세
  + 자바스크립트의 핵심 개념
    - 객체
      - boolean, number, string, null, undefined, symbol을 제외한 나머지는 모두 객체
    - 함수
      - 자바스크립트에서는 함수도 객체로 취급
    - 프로토타입
      - 모든 객체는 숨겨진 링크인 프로토타입을 가지고있음
    - 실행컨텍스트 & 클로저
      - 자바스크립트는 실행컨텍스트를 만들고 그안에서 실행을 함
      - scope
  + 자바스크립트를 이용하면 여러 패러다임을 적용할 수 있음
    - 객체지향, 절차지향 , 반응형 등등
  + 함수형 프로그래밍
    - 높은 수준의 모듈화를 가능케 함
    - 일급객체
      -  변수나 데이터 구조안에 담을 수 있다.
      -  파라미터로 전달 할 수 있다.
      -  반환값(return value)으로 사용할 수 있다.
      -  할당에 사용된 이름과 관계없이 고유한 구별이 가능하다.
      -  동적으로 프로퍼티 할당이 가능하다.
  + 자바스크립트의 단점
    - 느슨한 타입체킹
      - 컴파일타임에서 에러를 잡지 못하기에 런타임 오류로 번짐
    - 전역객체
      - 충돌위험성이 높음

## 자바스크립트 데이터 타입과 연산자
  + premitive
    - number, string, boolean, null, undefined
  + reference
    - object
      - array
      - function
      - Rexp
  + 숫자
    - 모든 숫자를 64비트로 지정(double)
    - 정수, 소수 모두 typeof 값으로 number가 나옴
  + 문자열
    - 자바스크립트는 한번 생성된 문자열은 수정이 불가능하다.
            var str = "test";
            console.log(str);
            str[0] = 'T';
            console.log(str);
  + boolean
    - true/false
  + null & undefined
    - 일반적으로 null은 메모리가 할당 되어있지않은 껍데기 개념(명시적으로 값이 비어있음을 나타냄)
    - undefined는 메모리 공간은 존재하지만 그 안이 비어있는 개념
      - undefined는 타입
    - null은 object로 취급, 고로 null을 체크할때는 === null 로 체크를 해야됨
      - null은 타입이 아니기때문
            var nullVal = null;
            var undefinedVal = undefined;
            console.log(typeof nullVal);
            console.log(typeof undefinedVal);
