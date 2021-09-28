# 2021-09-28 TIL

## Math
* 표준 Built-in 객체로써 수학적인 연산을 위한 속성값과 메서드를 제공하는 객체
* Math는 생성자 함수가 아니며, 모든 속성과 메서드 정적이기에 Math.function()으로 언제든지 호출 가능
* 오일러 상수 : Math.E
* PI : Math.PI
* 절대값 : Math.abs(x)
* 최대값 : Math.max(x)
* 최소값 : Math.min(x)
* 랜덤 난수 값 : Math.random()
* 제곱과 제곱근 : Math.pow(x, y), Math.sprt(x)
* 소수점 처리 : Math.round(x), Math.ceil(x), Math.floor(x)
***
✔ 최대/최소/절대값
~~~
console.log(Math.max(1,-1));
console.log(Math.min(1,-1));

console.log(Math.max(1, 5, 6, 0, -9, -1));
console.log(Math.min(1, 5, 6, 0, -9, -1));

let nums = [1, -1, 5, 23, 17, -4, 0]
// apply
console.log(Math.max.apply(null, nums));
console.log(Math.min.apply(null, nums));
// spread
console.log(Math.max(...nums));
console.log(Math.min(...nums));

console.log(Math.abs(1));
console.log(Math.abs(-1));
console.log(Math.abs(-Infinity));

/* 출력 값 :
1
-1

6
-9

23
-4

23
-4

1
1
Infinity
*/
~~~
***
✔ 속성 및 랜덤
~~~
console.log(Math.E);
console.log(Math.PI);

console.log(Math.random());
console.log(Math.random() * 10);
console.log(Number.parseInt(Math.random() * 10));

for (let i=0; i < 10; i++) {
    console.log(Number.parseInt(Math.random() * 10));
}

/* 출력 값 :
2.718281828459045
3.141592653589793

0.7422165169831074
4.31222112235716
0

9
2
5
0
0
4
8
8
8
7
*/
~~~
***
✔ 제곱/제곱근/소수점 처리
* 제곱 : Math.pow(x, y)
* 제곱근 : Math.sqrt(x)
* 소수점 이하 반올림 정수 : Math.round(x)
* 소수점 이하 올림 : Math.ceil(x)
* 소수점 이하 내림 : Math.floor(x)
~~~
console.log(Math.pow(2,3));
console.log(2 ** 3);

console.log(Math.sqrt(4));
console.log(Math.sqrt(9));
console.log(Math.sqrt(2));

console.log(Math.round(3.5));
console.log(Math.round(-2.3));
console.log(Math.round(-2.7));

console.log(Math.ceil(3.5));
console.log(Math.ceil(-2.3));
console.log(Math.ceil(-2.7));

console.log(Math.floor(3.5));
console.log(Math.floor(-2.3));
console.log(Math.floor(-2.7));  

/* 출력 값 :
8
8

2
3
1.4142135623730951

4
-2
-3

4
-2
-2

3
-3
-3
*/
~~~
