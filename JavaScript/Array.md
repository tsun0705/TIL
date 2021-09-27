# 2021-09-27 TIL

## 배열
* 여러 개체 값을 순차적으로 나열한 자료 구조
* 배열 내 값을 요소라고 하며, 배열 요소는 index로 접근

## 배열 선언/접근/속성
* 선언 - new Array() 혹은 []를 통해 선언하며, 사이즈 혹은 값을 입력하여 초기화도 가능
* 접근 방법 - Array[index]를 통해 index를 통하여 O(1) 접근
* 배열 속성 - Array.length를 통해 배열 요소의 개수 확인 가능
~~~
let arr_1 = new Array(10);
let arr_2 = [];

console.log(arr_1);
console.log(arr_2);

let fruits = ["apple", "orange", "melon"];
console.log(fruits);
console.log(fruits.length);
console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);

fruits[1]= "kiwi"; // orange > kiwi 교체
console.log(fruits);
/* 출력 값 :
[ <10 empty items> ]
[]

[ 'apple', 'orange', 'melon' ]
3
apple
orange
melon

[ 'apple', 'kiwi', 'melon' ] */
~~~
