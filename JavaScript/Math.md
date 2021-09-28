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
