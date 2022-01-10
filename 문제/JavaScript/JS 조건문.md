# 2021-09-29 TIL

## 1번 대소 비교
![image](https://user-images.githubusercontent.com/58898466/135203810-d7b073c8-ebeb-43a7-9a65-746d1f1fd758.png)
~~~
/*** 1. 대소비교 ***/

/* user code */
function answer(x, y) {
  let result = "";

  if (x > y) {
    result = ">";
  } else if (x < y) {
    result = "<";
  } else {
    result = "=";
  }

  return result;
}

/* main code */
let input = [
  // TC: 1
  [3, 5],
  // TC: 2
  [7, 4],
  // TC: 3
  [2, 2],
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i][0], input[i][1])}`);
}

/* 출력 값 :
#1 <
#2 >
#3 =
*/ 
~~~
***

## 2번 나누기와 대소 비교
![image](https://user-images.githubusercontent.com/58898466/135204473-5af70de4-8348-412f-beda-e08e1886bb9f.png)

~~~
/*** 2. 나누기와 대소비교 ***/

/* user code */
function answer(a, b, c, d) {
  let result;

  if (a/b > c/d) {
    result = 1;
  } else if (a/b == c/d) {
    result = 0;
  } else {
    result = -1;
  }

  return result;
}

/* main code */
let input = [
  // TC: 1
  [14, 2, 6, 6],
  // TC: 2
  [6, 7, 8, 9],
  // TC: 3
  [18, 2, 36, 4],
];

for (let i = 0; i < input.length; i++) {
  console.log(
    `#${i + 1} ${answer(input[i][0], input[i][1], input[i][2], input[i][3])}`
  );
}

/* 출력 값 :
#1 1
#2 -1
#3 0
*/
~~~
***

## 3번 윤년 판별기
![image](https://user-images.githubusercontent.com/58898466/135205066-fe790dc5-3f5d-4272-8123-5008a36f02e1.png)

~~~
/*** 3. 윤년 판별기 ***/

/* user code */
function answer(year) {
  let result;

  if (year % 4 == 0 && year % 100 != 0) {
    result = true;
  } else if (year % 400 == 0) {
    result = true;
  } else {
    result = false;
  }

  return result;
}

/* main code */
let input = [
  // TC: 1
  4,
  // TC: 2
  100,
  // TC: 3
  124,
  // TC: 4
  247,
  // TC: 5
  400,
];
for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 :
#1 true
#2 false
#3 true
#4 false
#5 true
*/
~~~
***

## 4번 ATM 기기
![image](https://user-images.githubusercontent.com/58898466/135205542-8be48eae-2777-4247-a09c-f09bc5256202.png)

~~~
/*** 4. ATM 기기 ***/

/* user code */
function answer(withdraw, total) {
  let result;

  if(withdraw + 0.5 < total && withdraw % 5 == 0) {
    result = total - withdraw - 0.5;
  } else {
    result = total;
  }

  return result;
}

/* main code */
let input = [
  // TC: 1
  [40, 130.0],
  // TC: 2
  [33, 130.0],
  // TC: 3
  [300, 300.0],
];
for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i][0], input[i][1])}`);
}

/* 출력 값 : 
#1 89.5
#2 130
#3 300
*/
~~~
***

## 5번 네 번째 좌표
![image](https://user-images.githubusercontent.com/58898466/135206253-c8bec603-ab61-41b6-8bb0-8162d09d2d8a.png)

~~~
/*** 5. 네번째 좌표 ***/

/* user code */
function answer(x_arr, y_arr) {
  let result = [];

  if (x_arr[0] == x_arr[1]) {
    result[0] = x_arr[2] 
 } else if (x_arr[0] == x_arr[2]) {
   result[0] = x_arr[1]
 } else if (x_arr[1] == x_arr[2]) {
   result[0] = x_arr[0]
 };

 if (y_arr[0] == y_arr[1]) {
  result[1] = y_arr[2] 
} else if (y_arr[0] == y_arr[2]) {
 result[1] = y_arr[1]
} else if (y_arr[1] == y_arr[2]) {
 result[1] = y_arr[0]
};
  return result;
}

/* main code */
let input = [
  // TC: 1
  [
    [5, 5, 8],
    [5, 8, 5],
  ],
  // TC: 2
  [
    [3, 1, 1],
    [2, 1, 2],
  ],
  // TC: 3
  [
    [7, 7, 3],
    [4, 1, 1],
  ],
];
for (let i = 0; i < input.length; i++) {
  process.stdout.write(`#${i + 1} `);
  console.log(answer(input[i][0], input[i][1]));
}

/* 출력 값 : 
#1 [ 8, 8 ]
#2 [ 3, 1 ]
#3 [ 3, 4 ]
*/
~~~
