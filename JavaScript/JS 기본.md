# 2021-09-12

## 자바스크립트란? 
* 정적인 HTML 문서와 달리 동적인 화면을 웹페이지에 구현하기 위해 사용하는 스크립트 언어다.



## 자바스크립트에서 변수를 선언할 때 사용하는 단어는 3가지가 있다.
* const : 처음 선언할 때 값을 무조건 대입해야 하고 재선언 및 재할당이 불가능하다.
~~~
const a = 1;
a = 2; // 오류
const a = 2 // 오류
~~~


* let : 재선언은 불가능하지만 재할당은 가능하다.
~~~
let a = 1;
a = 2; 
let a = 2; // 오류
~~~
* var :재선언 및 재할당 모두 가능하다. 자바스크립트 초기에 사용되었지만 현재 권장하지 않는다.

## Array이란?
* 인덱스를 가지는 복수의 자료를 저장할 수 있는 자료구조이다.
* 어떤 데이터 타입이든 상관없이 저장이 가능하다.


~~~
const daysOfWeek = ["mon", "tue", "wed", "thu", "fri", "sat"]; // 배열 선언
consol.log(daysOfWeek); // 배열 출력
daysOfWeek.push("sun"); // 배열값 추가
daysOfWeek[0] = "MON" // 배열의 첫번째 값 변경
consol.log(daysOfWeek); // sun값이 추가되고 배열의 첫번째 값이 변경된 배열 출력

Object
const player = {
name : "sky",
points : 10,
fat : false,
};

consol.log(player);
player.points = player.points + 10; // 합계 포인트 20점으로 업데이트
player.lastname = "kwon"; // lastname이란 property 추가 후 값 지정
consol.log(player); // points 업데이트, lastname 추가 한 플레이어 객체 출력

Array, Object, Function을 활용한 예제
const calculator = {
add: function(a,b){
  console.log(a+b);
},
minus: function(a,b){
  console.log(a-b);
},

divide: function(a,b){
  console.log(a/b);
},
  
powerOf: function(a,b){
  console.log(a**b); 
}
}
    calculator.add(4, 4)
    calculator.minus(6, 2)
    calculator.divide(20, 4)
    calculator.powerOf(2, 3)
~~~

## Document
* document 객체는 DOM 제어를 위한 다양한 메서드들을 담고 있다.
* 자바스크립트에서 HTML에 접근 및 선택, 생성, 이벤트 처리등의 작업이 가능하다.

~~~
document.getElementById("아이디"); // 해당 아이디의 태그(요소)에 접근
id값.innerText = ""; // 텍스트 업데이트
document.getElementsByClassName("클래스명"); // 해당 클래스명의 태그(요소)에 접근
document.getElementsByTagName("태그명"); // 해당 태그명에 접근
document.querySelector(".클래스명 태그명"); // 엘리먼트를 CSS 방식으로 검색, 단 하나의 엘리먼트를 리턴, 동일한 조건 시 첫번째 엘리먼트를 보여준다.
ducumnet.querySelector("#id"); // 해당 아이디의 태그에 접근
document.querySelectorAll(".클래스명 태그명"); // 조건에 부합하는 모든 엘리먼트를 가져온다.
Event (document를 이용하여 사용)
변수명(HTML Element).addEventListener("이벤트명", 이벤트 활성화 시 실행할 함수명);  // 함수명에 () 제외
HTML element.이벤트명 = 함수명; // 위와 동일하게 동작하는 코드, 함수명에 ()제외
console.dir(HTML Element); // 사용가능한 이벤트 볼 수 있음
~~~
