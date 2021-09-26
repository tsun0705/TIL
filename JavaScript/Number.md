# 2021-09-26 TIL

## 지수 표기법
* 아주 큰 숫자나 아주 작은 숫자를 표기하기 위해 지수 표기법(e)으로 0의 개수를 대체 표기 가능
~~~
/* 지수 표기법 */
let billion_1 = 1000000000; // 10억
let billion_2 = 1e9; // 1 + 0 9개
let us = 1e-6; // 왼쪽으로 6번 소수점 이동

console.log(billion_1); // 출력 값 : 1000000000
console.log(billion_2); // 출력 값 : 1000000000
console.log(us); // 출력 값 : 0.000001
~~~

## 진법 표기
* 진법 표기를 지원하기 위해 0x(16진수), 0o(8진수), 0b(2진수)로 N 진수 표기 가능
~~~
/* N 진법 */
console.log(0x0f); // 출력 값 : 15
console.log(0o17); // 출력 값 : 15
console.log(0b1111); // 출력 값 : 15
~~~

## 상수 값
~~~
console.log(Number.MAX_VALUE); // 지수로 표기되는 양수 최댓값
console.log(Number.MIN_VALUE); //지수로 표기되는 양수 최솟값

console.log(Number.MAX_SAFE_INTEGER); // 안전하게 표기되는 최댓값
console.log(Number.MIN_SAFE_INTEGER); // 안전하게 표기되는 최솟값

console.log(Number.POSITIVE_INFINITY); // 무한대 양수
console.log(Number.NEGATIVE_INFINITY); // 무한대 음수

console.log(Number.NaN); // 정의되지 않은 숫자 데이터 유형
console.log(NaN); // 정의되지 않은 숫자 데이터 유형

/* 출력 값 :
1.7976931348623157e+308
5e-324
9007199254740991
-9007199254740991
Infinity
-Infinity
NaN
NaN */
~~~

## 형 변환
* 변수.toString(), String(변수), 변수 + ""를 통해 변환 가능
~~~
let us = 1e-6
console.log(us.toString());
console.log(typeof us.toString());
console.log(typeof String(us));
console.log(typeof (us+ ""));
/* 출력 값 :
0.000001
string
string
string */
~~~

## 자리 수 표현
* 소수의 자리 수 길이를 제한 - Number.toFixed(pos)
* 정수와 소수의 자리 수를 합한 길이로 제한 - Number.toPrecision(pos)
~~~
let num_1 = 125.0;
let num_2 = 123.456;
console.log(num_1 - num_2);
console.log((num_1 - num_2).toFixed(3));
console.log((num_1 - num_2).toPrecision(3));
/* 출력 값 : 
1.543999999999997
1.544
1.54 */
~~~
