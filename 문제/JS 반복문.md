# 2021-09-29 TIL

## 1번 별별별
![image](https://user-images.githubusercontent.com/58898466/135193255-df0540fc-fd62-47ef-97d5-bf2a28acd6f4.png)
~~~
/*** 1. 별별별 ***/

/* user code */
function answer(num) {
  let result = "";

  // 코드 구현 시작 영역
  for (let i=0; i < num; i++) {
    result += "*";
  }

  // …

  // 코드 구현 종료 영역

  return result;
}

/* main code */
let input = [
  // TC: 1
  5,
  // TC: 2
  7,
  // TC: 3
  12,
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 :
#1 *****
#2 *******
#3 ************
*/
~~~
***

## 2번 두 수 사이 숫자
![image](https://user-images.githubusercontent.com/58898466/135199446-c9b79d84-26d5-463c-8e87-7c14eb7c560e.png)
~~~
/*** 2. 두 수 사이 숫자 ***/

/* user code */
function answer(x, y) {
  let result = [];
  if (x > y) {
    let temp; 
    temp = x;
    x = y;
    y = temp;
  }
 
 /*
 if (x > y) {
    [x, y] = [y, x];
 }
 */ ES6에 추가된 자바스크립트 문법
 
  // 코드 구현 시작 영역
  for (let i=x; i <= y; i++) {
    result.push(i);
  }
  // …

  // 코드 구현 종료 영역

  return result;
}

/* main code */
let input = [
  // TC: 1
  [3, 7],
  // TC: 2
  [8, 3],
  // TC: 3
  [12, 10],
];
for (let i = 0; i < input.length; i++) {
  process.stdout.write(`#${i + 1} `);
  console.log(answer(input[i][0], input[i][1]));
}

/* 출력 값 : 
#1 [ 3, 4, 5, 6, 7 ]
#2 [ 3, 4, 5, 6, 7, 8 ]
#3 [ 10, 11, 12 ]
*/
~~~
***

## 3번 반 평균
![image](https://user-images.githubusercontent.com/58898466/135200696-814b5dd2-9c17-4003-b4cf-9838c416d219.png)
~~~

