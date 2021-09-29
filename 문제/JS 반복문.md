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
    result += "*"
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
