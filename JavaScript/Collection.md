# 2021-09-28 TIL

## Collection
* 구조 혹은 비구조화 형태로 프로그래밍 언어가 제공하는 값을 담을 수 있는 공간
* Indexed Collection - Array, Typed Array
* keyed Collection - Object, Map, Set

## Map
* 다양한 자료형의 key를 허용하고, key-value 형태의 자료형을 저장할 수 있는 Collection
* Map은 Object 대비 비교하면 다양한 key의 사용을 허용하고, 값의 추가/삭제 시 메서드를 통해 수행이 필요
* 생성자 : new Map()
* 개수 확인 : Map.size()
* 요소 추가 : Map.set(key, value)
* 요소 접근 : Map.get(key)
* 요소 삭제 : Map.delete(key)
* 전체 삭제 : Map.clear()
* 요소 존재 여부 확인 : Map.has(key)

~~~
let map = new Map();

map.set("name", "john");
map.set(21, 21);
map.set(true, "bool_type");
console.log(map);

console.log(map.get("name"));
console.log(map.get(21));
console.log(map.get(true));
console.log(map.size);

map.delete(123);
console.log(map);
map.clear();
console.log(map);

map.set(123, 123).set(false, "bool_type").set("fruit", "banana");
console.log(map);

/* 출력 값 :
Map(3) { 'name' => 'john', 21 => 21, true => 'bool_type' } // Map(3) = 맵 사이즈

john
21
bool_type
3

Map(3) { 'name' => 'john', 21 => 21, true => 'bool_type' }

Map(0) {}

Map(3) { 123 => 123, false => 'bool_type', 'fruit' => 'banana' }
~~~

## Map 반복문
* Collection 객체인 Map이 가지고 있는 iterator 속성을 이용하여 for ... of 구문을 통해 반복문 수행 가능
~~~
let recipe_juice = new Map([
    ["strewberry", 50],
    ["banana", 100],
    ["ice", 150]
]);

for (let item of recipe_juice.keys()) {
    console.log(item);
};

for (let amount of recipe_juice.values()) {
    console.log(amount);
};

for (let entity of recipe_juice) {
    console.log(entity);
};

/* 출력 값 :
strewberry
banana
ice

50
100
150

[ 'strewberry', 50 ]
[ 'banana', 100 ]
[ 'ice', 150 ]
*/
~~~

## 
