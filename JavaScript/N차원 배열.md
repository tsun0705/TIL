# 2021-09-28 TIL

## N차원 배열
* 배열 안에 N개 만큼의 배열이 존재하는 객체
* 2/3차원 지도 정보, RGB를 저장하는 2차원 사진 파일 등을 표현할 때 활용 가능
* 2차원 배열은 array[N][M]으로 접근하며, 배열 전체를 push(), pop() 가능
~~~
let array = [
[101, 102, 103],
[201, 202, 203],
[301, 302, 303],
];

console.log(array);
console.log(array[0]);
console.log(array[1][0]);
console.log(array[2][2]);

let arr_2 = array.pop();
console.log(array.length);
console.log(arr_2);
console.log(array);

let array_num = array.push([401, 402, 403]);
console.log(array.length);
console.log(array_num);
console.log(array);

/* 출력 값 :
[ [ 101, 102, 103 ], [ 201, 202, 203 ], [ 301, 302, 303 ] ]
[ 101, 102, 103 ]
201
303

2
[ 301, 302, 303 ]
[ [ 101, 102, 103 ], [ 201, 202, 203 ] ]

3
3
[ [ 101, 102, 103 ], [ 201, 202, 203 ], [ 401, 402, 403 ] ]
*/
~~~

## 2차원 배열 반복문
✔ 이중 for loop를 사용한 2차원 배열 접근
~~~
let array = [
    [101, 102, 103, 104],
    [201, 202, 203, 204],
    [301, 302, 303, 304],
    [401, 402, 403, 404],
];

for (let i=0; i < array.length; i++) {
    for (let j=0; j < array[i].length; j++) {
        console.log(array[i][j]);
    }
}

let fruits = [
    ["strawberry", 50],
    ["banana", 100],
    ["ice", 150]
];

for (let i=0; i<fruits.length; i++) {
    console.log(`fruits: ${fruits[i][0]}, amount: ${fruits[i][1]}`);
}

/* 출력 값 :
101
102
103
104
201
202
203
204
301
302
303
304
401
402
403
404

fruits: strawberry, amount: 50
fruits: banana, amount: 100
fruits: ice, amount: 150
*/
~~~
