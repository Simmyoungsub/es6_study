### ES6 문법
##### 변수

1. 선언
  + Naming rule
    + 보통 글자나 $, _ 기호로 시작해야함
    + 글자나 숫자,$,_ 만 사용할 수 있음
    + 유니코드 사용가능
    + 예약어는 사용 불가능
  + let나 const를 사용
    - var와 다르게 let, const는 선언된 block내에서만 사용가능
  + Example
            let foo = 'hello'; // 변수선언
            const bar = 'world'; // 상수 선언

2. 타입
  + premitive
    - immutable함
    - number, string, boolean, null, undefined, symbol이 해당됨
    - number, string, boolean은 각각에 대응하는 객체타입인 Number, String, Boolean이 있음
  + object
    - premitive 외의 타입

3. 리터럴
  + 프로그램안에서 직접 지정하는 값
    - 보통 string들
  + javascript는 quote를 통해 식별자와 리터럴을 구분함

4. 템플릿 문자열
  + 변수나 상수를 문자열 안에 쓰기 위해 도입
  + 변수는 ${}안에 기입, $를 문자열안에 쓰려면 \(escape)를 붙여서 사용
    - `(back tik)을 사용

              const a = "hello";
              const str = `${a} world!`;
              console.log(str);

5. expression
  + ...(spread 연산자)
    - 스프레드 구문을 사용하면 여러 인수 또는 여러 요소가 예상되는 위치에서
      표현식을 확장 할 수 있음
  + Distructuring
    - 배열 또는 객체에서 데이터를 별개로 추줄하여 할당
    - 값이 모자란경우 빈값 혹은 undfined를 할당
            let [a,b,c] = [1,2,3];
            console.log(a,b,c);
            [a,b,c,...d] = [1,2,3,4,5];
            console.log(a,b,c,d); // d = [4,5]
            [a,b] = [b,a]; // swap
            let [r1,r2] = function(){
              return [1,2];
            }();
            console.log(r1,r2);
  + for...of, for ...in
             const objs = [
               {
                 'chrome' : 10
               },
               {
                 'firefox' : 7
               },
               {
                 'safari' : 5
               },
               {
                 'opera' : 8
               }
             ];

             for(let item of objs) {
               for(let key in item) {
                 console.log(key, item[key]);
               }
             }
  + default parameter
    - es6에서는 함수의 헤더부분의 매개변수에 default값을 설정해줄수 있다.
  + instanceof 연산자
    - 객체 instanceof 클래스이름
  + 논리 연산자
    - &&
           if(a == b) {
             func();
           }

           (a == b) && func();
    - ||
           const value;
           const max = value || 10; // value가 거짓이라면 10을 할당

6. Hoisting
  + javascript는 함수 스코핑을 사용
