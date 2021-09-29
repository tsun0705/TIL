# 2021-09-29 

## 1번 최소값 구하기
![image](https://user-images.githubusercontent.com/58898466/135207558-83fa5fcf-751e-420e-9505-e0ab49513f7f.png)
~~~
/* 1. 최소값 구하기 */

/* user code */
function answer(x, y) {
  let min;

  min = Math.min(x, y);

  return min;
}

/* main code */
let input = [
  // TC: 1
  [16, 3],
  // TC: 2
  [-3, 1],
  // TC: 3
  [1000, 525],
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i][0], input[i][1])}`);
}

/* 출력 값 : 
#1 3
#2 -3
#3 525
*/
~~~
