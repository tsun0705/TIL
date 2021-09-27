# 2021-09-27 

## String
* 텍스트 길이에 상관없이 문자열 형태로 저장되는 자료형
* 자바스크립트에는 글자 하나만 저장할 수 있는 char 자료형이 없다.
 
## 정의 방법
* 큰 따옴표, 작은 따옴표, String()
* 문자열 + 변수 : 
~~~ 
`Hello_${변수}` 
~~~
 
## 문자 표기
~~~
console.log("linefeed");
console.log("line\nfeed");
console.log("line\rfeed");
console.log("line\tfeed");
console.log("line\\feed");
console.log("line\u{1F60D}");
/* 출력 값 :
linefeed

line
feed

line
feed

line	feed

line\feed

line😍
~~~

## 문자열 길이, 문자 접근
* String.length - 문자열 길이 
* 공백도 포함
~~~
let str = "hello, world!!!"

console.log(str.length);

console.log(str.charAt(0));
console.log(str.charCodeAt(0));
console.log(str[0]);
/* 출력 값 :
15

h
104
h */
~~~

## 문자열 검색
* 문자열 검색(index) : String.indexOf(substr, pos), String.lastIndexOf(substr, pos)
* 문자열 검색(bool) : String.includes(substr, pos), String.startsWith(substr, pos), String.endsWith(substr, pos)
~~~
let text = "hello, world!!!";

console.log(text.indexOf("l"));
console.log(text.indexOf("l",3)); // l을 4번째 부터 검색
console.log(text.lastIndexOf("l")); // l을 뒤에서 검색
console.log(text.lastIndexOf("l",5)); // l을 뒤에서 5번째 부터 검색

console.log(text.includes("Hello")); // 대 소문자 구분
console.log(text.startsWith("ello",1)); // 1번째 부터 ello로 시작하는지 검색
console.log(text.endsWith("wolrd")); // world로 끝에서 부터 검색

/* 출력 값 : 
2
3
10
3

false
true
false */
~~~

## 문자열 대 소문자 변환
~~~
let text = "hello, world!!!";

console.log(text.toUpperCase());
console.log(text.toLowerCase());

/* 출력 값 :
HELLO, WORLD!!!
hello, world!!! /*
~~~

## 문자열 치환
* 문자열 치환 : String.replace(orgin_str, change_str)
* 정규 표현식 활용 문자열 치환 : /치환문자열/g(전체)i(대 소문자 구분X)
~~~
let text = "hello, world!!!";
let changed_text = "";

changed_text = text.replace("world", "earth");

console.log(changed_text);
console.log(text);

console.log(text.replace("!", "?"));
console.log(text.replace("l", "i"));

console.log(text.replace(/l/g, "i"));
console.log(text.replace(/l/gi, "i"));

/* 출력 값 : 
hello, earth!!!
hello, world!!!

hello, world?!!
heilo, world!!!

heiio, worid!!!
heiio, worid!!! */
~~~

## 문자열 추출
* 위치 기반 문자열 추출 : String.slice(start, end), String.substring(start, end)
* 길이 기반 문자열 추출 : String.substr(start, length)
~~~
let text = "hello, world!!!";

console.log(text.slice(0,5));
console.log(text.slice(4,5));
console.log(text.slice(4));
console.log(text.slice(-4));

console.log(text.slice(2,6));
console.log(text.slice(6,2));
console.log(text.substring(2,6));
console.log(text.substring(6,2)); // substring: end > start -> start > end

console.log(text.substr(2,6));
console.log(text.substr(-5,3));
/* 출력 값 :
hello
o
o, world!!!
d!!!
llo,

llo,
llo,
llo, w
ld! /*
~~~

## 문자열 분할
* 배열로 문자열 분할 : String.split(Separator, limit)
~~~
let fruits = "apple banana melon";

result = fruits.split(" ");
console.log(result);
console.log(result[0]);
console.log(result[1]);
console.log(result[2]);

let fruits2 = "apple,banana,melon";

result2 = fruits2.split(",");
console.log(result2);
console.log(result2[0]);
console.log(result2[1]);
console.log(result2[2]);

let text = "hello";
reuslt = text.split("");
console.log(result);

let text = "hello";
reuslt = text.split("",3);
console.log(result);

/* 출력 값 : 
[ 'apple', 'banana', 'melon' ]
apple
banana
melon

[ 'apple', 'banana', 'melon' ]
apple
banana
melon

[ 'h', 'e', 'l', 'l', 'o' ]

[ 'h', 'e', 'l' ]
~~~
