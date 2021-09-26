# 2021-09-26 TIL

## method
* 객체에 저장된 값이 함수인 경우, 메서드라고 부른다.
~~~
let user = {
  name: "john",
  age: 27,
  hello_func() {
    console.log("hello");
  },
};
~~~
~~~
function hello_func() {
    console.log("hello");
}

function hi_func() {
    console.log("hi");
}

let obj = {
    name: "john",
    age: 27,
    func: hello_func
};

hello_func();
hi_func();
obj.func();
console.log(hello_func == obj.func);

obj.func = hi_func
obj.func();
console.log(hi_func == obj.func);
/* 출력 값 : 
hello
hi
hello
true
hi
true */
~~~
## this
* 메서드에서 객체 내부의 속성 값을 접근할 수 있는 지시자
~~~
let obj = {
  name: "john",
  age: 27,
  hello_func() {
    console.log("hello " + this.name);
  }
};
// 출력 값 : hello john
~~~
~~~
~~~
