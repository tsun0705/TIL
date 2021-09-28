# 2021-09-28 TIL

## Set
* value 값만 저장하며 증복을 허용하지 않는 Collection
* 생성자 : new Set()
* 개수 확인 : Set.size
* 요소 추가 : Set.add(value)
* 요소 삭제 : Set.delete(value)
* 전체 삭제 : Set.clear()
* 요소 존재 여부 확인 : Set.has(key)

~~~
let set = new Set();
let num = new Set([1, 2, 3, 4, 5]);
let str = new Set("Hello!");

console.log(set);
console.log(num);
console.log(str);

set.add(1).add(1).add(10).add(20);
console.log(set);

console.log(set.has(10));
console.log(set.has(2));

set.delete(1);
set.delete(-1);
console.log(set);

/* 출력 값 :
Set(0) {}
Set(5) { 1, 2, 3, 4, 5 }
Set(5) { 'H', 'e', 'l', 'o', '!' }

Set(3) { 1, 10, 20 }

true
false

Set(2) { 10, 20 }
*/
~~~

## Set 반복문
* Collection 객체인 Set이 가지고 있는 iterator 속성을 이용하여 for .. of 구문을 통해 반복문 수행 가능
~~~
let str = new Set("Hello!");
console.log(str);

for (let item of str) {
    console.log(item);
};

for (let item of str.keys()) {
    console.log(item);
};

for (let item of str.values()) {
    console.log(item);
};

for (let item of str.entries()) {
    console.log(item);
};

/* 출력 값 :
Set(5) { 'H', 'e', 'l', 'o', '!' }

H
e
l
o
!

H
e
l
o
!

H
e
l
o
!

[ 'H', 'H' ]
[ 'e', 'e' ]
[ 'l', 'l' ]
[ 'o', 'o' ]
[ '!', '!' ]
*/
~~~
