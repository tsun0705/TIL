# 2021-09-27 TIL

## 배열
* 여러 개체 값을 순차적으로 나열한 자료 구조
* 배열 내 값을 요소라고 하며, 배열 요소는 index로 접근

## 배열 선언/접근/속성
* 선언 - new Array() 혹은 []를 통해 선언하며, 사이즈 혹은 값을 입력하여 초기화도 가능
* 접근 방법 - Array[index]를 통해 index를 통하여 O(1) 접근
* 배열 속성 - Array.length를 통해 배열 요소의 개수 확인 가능
~~~
let arr_1 = new Array(10);
let arr_2 = [];

console.log(arr_1);
console.log(arr_2);

let fruits = ["apple", "orange", "melon"];
console.log(fruits);
console.log(fruits.length);
console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);

fruits[1]= "kiwi"; // orange > kiwi 교체
console.log(fruits);
/* 출력 값 :
[ <10 empty items> ]
[]

[ 'apple', 'orange', 'melon' ]
3
apple
orange
melon

[ 'apple', 'kiwi', 'melon' ] */
~~~

## 배열의 실체
* 자바스크립트에서 배열은 다른 언어에서 말하는 일반적인 배열이 아닌 Hash 기반의 객체
* 메모리가 연속적인 밀집 배열이 아니라 비 연속적인 희소 배열이다.
~~~
let nums = [];

nums[0] = "one";
nums[1] = "two";
console.log(nums.length);
console.log(nums);

nums["once"] = "once";
nums["twice"] = "twice";
console.log(nums.length);
console.log(nums);

console.log(Object.getOwnPropertyDescriptors(nums));

/* 출력 값 :
2
[ 'one', 'two' ]

2
[ 'one', 'two', once: 'once', twice: 'twice' ]

{
  '0': {
    value: 'one',
    writable: true,
    enumerable: true,
    configurable: true
  },
  '1': {
    value: 'two',
    writable: true,
    enumerable: true,
    configurable: true
  },
  length: { value: 2, writable: true, enumerable: false, configurable: false },
  once: {
    value: 'once',
    writable: true,
    enumerable: true,
    configurable: true
  },
  twice: {
    value: 'twice',
    writable: true,
    enumerable: true,
    configurable: true
  }
} */
~~~

## 배열 타입 확인 & 배열 요소 삭제
* Array.isArray(value)
* delete array[Index] (삭제해도 배열의 사이즈는 그대로)

~~~
let num = 123.456;
let str = "Hello";
let fruits = ["apple", "orange", "melon"];

console.log(Array.isArray(num));
console.log(Array.isArray(str));
console.log(Array.isArray(fruits));

console.log(fruits);
console.log(fruits.length);


delete fruits[1];
console.log(fruits);
console.log(fruits.length);

/* 출력 값 :
false
false
true

[ 'apple', 'orange', 'melon' ]
3

[ 'apple', <1 empty item>, 'melon' ]
3
~~~

## 배열 추가/삭제 (LIFO - Back)
* 추가 - Array.push(element)
* 삭제 - Array.pop()
~~~
let fruits = ["apple", "orange", "melon"];
let ret;

ret = fruits.push("watermelon"); // 사이즈 리턴
console.log(fruits);
console.log(fruits.length);
console.log(ret);

ret = fruits.pop(); // 삭제된 element 리턴
console.log(fruits);
console.log(fruits.length);
console.log(ret);

/* 출력 값 :
[ 'apple', 'orange', 'melon', 'watermelon' ]
4
4

[ 'apple', 'orange', 'melon' ]
3
watermelon
~~~

## 배열 추가/삭제 (LIFO - Front)
* 추가 - Array.unshift(element)
* 삭제 - Array.shift()
~~~
let fruits = ["apple", "orange", "melon"];
let ret;

ret = fruits.unshift("watermelon"); // 사이즈 리턴
console.log(fruits);
console.log(fruits.length);
console.log(ret);

ret = fruits.shift(); // 삭제된 element 리턴
console.log(fruits);
console.log(fruits.length);
console.log(ret);

/* 출력 값 :
[ 'watermelon', 'apple', 'orange', 'melon' ]
4
4

[ 'apple', 'orange', 'melon' ]
3
watermelon
~~~

## 배열 삭제/변경 (index)
* Array.splice(index[start Num, delete Count, ele1, eleN])
~~~
let fruits = ["apple", "orange", "melon"];
let ret;

ret = fruits.splice(1);
console.log(ret); // 삭제된 element 요소 리턴
console.log(fruits);

fruits = ["apple", "orange", "melon", "strawberry"];
ret = fruits.splice(1,1);
console.log(ret);
console.log(fruits);

fruits = ["apple", "orange", "melon", "strawberry"];
ret = fruits.splice(1, 1, "mango", "kiwi")
console.log(ret);
console.log(fruits);

/* 출력 값 :
[ 'orange', 'melon' ]
[ 'apple' ]

[ 'orange' ]
[ 'apple', 'melon', 'strawberry' ]

[ 'orange' ]
[ 'apple', 'mango', 'kiwi', 'melon', 'strawberry' ]
~~~
