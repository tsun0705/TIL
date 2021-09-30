# 2021-09-30

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
***

## 2번 제곱 구현
![image](https://user-images.githubusercontent.com/58898466/135395297-f99f287a-02d6-4e79-87c9-82c46c360b99.png)

~~~
/* 2. 제곱 구현 */

/* user code */
function answer(x, y) {
  let result = 1;

  for (let i=0; i < y; i++) {
    result *= x;
  }

  return result;
}

/* main code */
let input = [
  // TC: 1
  [2, 3],
  // TC: 2
  [4, 6],
  // TC: 3
  [1, 100],
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i][0], input[i][1])}`);
}

/* 출력 값 :
#1 8
#2 4096
#3 1
*/
~~~
***

## 3번 놀이기구 입장 제한
![image](https://user-images.githubusercontent.com/58898466/135395620-fe8b7869-22f4-42f1-a2b0-f2dcc4714964.png)
~~~
/* 3. 놀이기구 입장 제한 */

/* user code */
function answer(user) {
  let permit;

  if (user.height >= 150) {
    permit = true;
  } else {
    permit = false;
  }

  return permit;
}

/* main code */
let input = [
  // TC: 1
  { name: "john", age: 27, height: 181 },
  // TC: 2
  { name: "alice", age: 12, height: 148 },
  // TC: 3
  { name: "bob", age: 14, height: 156 },
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 :
#1 true
#2 false
#3 true
*/
~~~
✔ 모범 답안
~~~
permit = user.height >= 150;
~~~
***

## 4번 요일 구하기
![image](https://user-images.githubusercontent.com/58898466/135397066-8b03bfc3-760e-46c6-bc8d-ad8ed0461175.png)

~~~
/* 4. 요일 구하기 */

/* user code */
function answer(str) {
  let week = new Array(
    "일요일",
    "월요일",
    "화요일",
    "수요일",
    "목요일",
    "금요일",
    "토요일"
  );
  let day;

  day = new Date(str);
  day = day.getDay();
  day = week[day];

  return day;
}

/* main code */
let input = [
  // TC: 1
  "2021-01-27",
  // TC: 2
  "2021-02-27",
  // TC: 3
  "2021-03-14",
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 :
#1 수요일
#2 토요일
#3 일요일
*/
~~~
✔ 모범 답안
~~~
  let date = new Date(str);
  day = week[date.getDay()];
~~~
***

## 5번 중복 단어 제거
![image](https://user-images.githubusercontent.com/58898466/135398168-5ed1167d-90c8-4f1c-b39e-a5eb55c5d8bd.png)

~~~
/* 5. 중복 단어 제거 */

/* user code */
function answer(arr) {
  let new_arr = [];

  new_arr = new Set(arr);

  return new_arr;
}

/* main code */
let input = [
  // TC: 1
  ["john", "alice", "alice"],
  // TC: 2
  ["Hello", "hello", "HELLO", "hello"],
  // TC: 3
  ["kiwi", "banana", "mango", "kiwi", "banana"],
];

for (let i = 0; i < input.length; i++) {
  process.stdout.write(`#${i + 1} `);
  console.log(answer(input[i]));
}

/* 출력 값 : 
#1 Set(2) { 'john', 'alice' }
#2 Set(3) { 'Hello', 'hello', 'HELLO' }
#3 Set(3) { 'kiwi', 'banana', 'mango' }
*/
~~~
✔ 모범 답안
~~~
  new_arr = Array.from(new Set(arr));

  new Set(arr).forEach(function item) {
    new_arr.push(item);
  });
~~~
***

## 배열 내 최대값 구하기
![image](https://user-images.githubusercontent.com/58898466/135416850-d9a423c0-d2a4-4813-ae4c-f589221a7fbe.png)
~~~
/* 6. 배열 내 최대값 구하기 */

/* user code */
function answer(arr) {
  let max;
  let temp;
  max = arr[0]
  for (let i=1; i<arr.length; i++) {
    if (max < arr[i]) max = arr[i];
  }

  return max;
}

/* main code */
let input = [
  // TC: 1
  [1, 6, 5, 2, 3],
  // TC: 2
  [19, 41, 23, -4, 17],
  // TC: 3
  [-64, -27, -41, -33, -59],
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 :
#1 6
#2 41
#3 -27
*/
~~~

✔ 모범 답안
~~~
  max = Number.MIN_SAFE_INTEGER;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i];
    }
  }
  
  max = Math.max.apply(null, arr);
~~~
***

## 7번 스팸 메일
![image](https://user-images.githubusercontent.com/58898466/135419541-ac968364-7aa6-46ba-aba5-b31851f42e3c.png)

~~~
/* 7. 스팸 메일 */

/* user code */
function answer(str) {
  let spam_flag;

  let spam = str.toLowerCase()
  if (spam.includes("advert") == true) {
    spam_flag = "true"
  } else spam_flag = "false"


  return spam_flag;
}

/* main code */
let input = [
  // TC: 1
  "RE: Request documents",
  // TC: 2
  "[Advertisement] free mobile!",
  // TC: 3
  "50% off this week (advertising)",
];

for (let i = 0; i < input.length; i++) {
  console.log(`#${i + 1} ${answer(input[i])}`);
}

/* 출력 값 : 
#1 false
#2 true
#3 true
*/
~~~

✔ 모범 답안
~~~
spam_flag = str.toLowerCase().includes("advert");
~~~
***

## 8번 배열 회전
![image](https://user-images.githubusercontent.com/58898466/135422842-aaab3c49-41e5-4d50-bfd1-a59f10404492.png)

~~~
/* 8. 배열 회전 */

/* user code */
function answer(user) {
  let reverse = [];

  for (let i=user.length-1; i>=0; i--) {
    reverse.push(user[i]);
  }

  return reverse;
}

/* main code */
let input = [
  // TC: 1
  [1, 2, 3, 4],
  // TC: 2
  [-1, 6, "hello", -15],
  // TC: 3
  ["apple", "banana", "mango"],
];

for (let i = 0; i < input.length; i++) {
  process.stdout.write(`#${i + 1} `);
  console.log(answer(input[i]));
}

/* 출력 값 :
#1 [ 4, 3, 2, 1 ]
#2 [ -15, 'hello', 6, -1 ]
#3 [ 'mango', 'banana', 'apple' ]
*/
~~~
✔ 모범 답안
~~~
  let tmp;
  for (let i = 0; i < user.length / 2; i++) {
    tmp = user[i];
    user[i] = user[user.length - 1 - i];
    user[user.length - 1 - i] = tmp;
  }
  reverse = user;
~~~
***

## 9번 문자 교정
![image](https://user-images.githubusercontent.com/58898466/135425439-afbb1289-0e6d-46dc-9053-733542ad9b6e.png)

~~~

