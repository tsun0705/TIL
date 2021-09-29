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
/*** 3. 반 평균 ***/

/* user code */
function answer(score) {
  let average = 0;

  // 코드 구현 시작 영역
  for(let i=0; i<score.length; i++) {
    average += score[i];
  }

  // …

  // 코드 구현 종료 영역

  return (average/score.length).toFixed(2);
}

/* main code */
let input = [
  // TC: 1
  [80, 95, 65, 70, 100],
  // TC: 2
  [82, 77, 51, 64, 73, 90, 80],
  // TC: 3
  [100, 71, 59, 88, 72, 75, 91, 93],
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 : 
#1 82.00
#2 73.86
#3 81.13
*/
~~~

## 4번 핸드폰 판매
![image](https://user-images.githubusercontent.com/58898466/135201613-4349ccab-8352-43c9-ab70-f50fcf245282.png)
~~~
/*** 4. 헨드폰 판매 ***/

/* user code */
function answer(employee) {
  let employee_id;
  let max = 0;

  // 코드 구현 시작 영역
  for(let i = 0; i < employee.length; i++) {
    if (employee[i] > max) {
      max = employee[i];
      employee_id = i + 1;
    }
  }

  // …

  // 코드 구현 종료 영역

  return employee_id
}

/* main code */
let input = [
  // TC: 1
  [3, 7, 9, 6, 1],
  // TC: 2
  [2, 7, 1, 4, 3, 0, 5],
  // TC: 3
  [7, 5, 0, 1, 2, 12, 6],
];
for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 : 
#1 3
#2 2
#3 6
*/
~~~
***

## 5번 무한 
![image](https://user-images.githubusercontent.com/58898466/135202432-0a0d8c34-bcc0-49cf-8401-b9d6cb83bc14.png)

~~~
