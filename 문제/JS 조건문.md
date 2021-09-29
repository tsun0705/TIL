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
