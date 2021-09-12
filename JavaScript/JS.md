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
