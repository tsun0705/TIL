# 2021-09-28 TIL

## Date
* 표준 Built-in 객체로써 날짜와 시간을 위한 속성 값과 메서드를 제공하는 객체
* Date 객체 생성자 : new Date()
* 현재 시간 기준 문자열 : Date()
* 날짜 정보 얻기 (년/월/일) : Date.getFullYear(), Date.getMonth(), Date.getDate()
* 날짜 정보 얻기 (시/분/초) : Date.getHours(), Date.getMinutes(), Date.getSeconds()
* 날짜 정보 설정 (년/월/일) : Date.setFullYear(), Date.setMonth(), Date.setDate()
* 날짜 정보 설정 (시/분/초) : Date.setHours(), Date.setMinutes(), Date.setSeconds()
* 그 외 날짜 정보 얻기 : Date.getDay(), Date.getTime(), Date.getTimezoneOffset()
* 그 외 날짜 정보 설정 : Date.parse(string)

## Date 생성자
* new Date()
* new Date(miniseconds)
* new Date(datestring)
* new Date(year, month, date, hours, minutes, seconds, ms)
~~~
let date_now = new Date();
let date_str = Date();

console.log(date_now);
console.log(date_str);

let date_ms_1 = new Date(0);
console.log(date_ms_1);
let date_ms_2 = new Date(1000 * 3600 * 24);
console.log(date_ms_2);

let date_string = new Date("2021-01-01");
console.log(date_string);

// month: 1월(0) ~ 12월(11)
let date_params_1 = new Date(2021, 0, 1);
let date_params_2 = new Date(Date.UTC(2021, 0, 1));
console.log(date_params_1);
console.log(date_params_2);

/* 출력 값 :
2021-09-28T07:52:03.778Z
Tue Sep 28 2021 16:52:03 GMT+0900 (대한민국 표준시)

1970-01-01T00:00:00.000Z
1970-01-02T00:00:00.000Z

2021-01-01T00:00:00.000Z

2020-12-31T15:00:00.000Z
2021-01-01T00:00:00.000Z
*/
~~~

## 날짜 정보 얻기
* 날짜 정보 얻기 (년/월/일/요일) : Date.getFullYear(), Date.getMonth(), Date.getDate()
* 날짜 정보 얻기 (시/분/초/ms) : Date.getHours(), Date.getMinutes(), Date.getSeconds()
* 주어진 일시 - 1970/1/1 차분(ms) : Date.getTime()
* 현지 시간 - 표준 시간 차분(min) : Date.getTimezoneOffset()
~~~
let date = new Date(Date.UTC(2021, 0, 1));

console.log(date);
console.log(date.getFullYear());
console.log(date.getMonth());

// 일요일(0) ~ 토요일(6)
console.log(date.getDay()); // 5 - 금요알

console.log(date.getHours());
console.log(date.getUTCHours());

console.log(date.getTime());
console.log(date.getTimezoneOffset());

/* 출력 값 : 
2021-01-01T00:00:00.000Z
2021
0

5

9
0

1609459200000
-540
*/
~~~

## 날짜 정보 설정
* 날짜 정보 설정 (년/월/일) : Date.setFullYear(), Date.setMonth(), Date.setDate()
* 날짜 정보 설정 (시/분/초/ms) : Date.setHours(), Date.setMinutes(), Date.setSeconds()
~~~
let date = new Date();

console.log(date);

let ms_year = date.setFullYear(2020, 3, 15);

console.log(date);
console.log(ms_year);
console.log(new Date(ms_year));

date.setDate(1);
console.log(date);

date.setDate(0);
console.log(date);

date.setHours(date.getHours() + 2);
console.log(date);

/* 출력 값 :
2021-09-28T08:14:46.926Z

2020-04-15T08:14:46.926Z
1586938486926
2020-04-15T08:14:46.926Z

2020-04-01T08:14:46.926Z

2020-03-31T08:14:46.926Z

2020-03-31T10:14:46.926Z
*/
~~~

## parse
* 문자열 기반 날짜 정보 설정 : Date.parse(YYYY-MM-DDTHH:mm:ss.sssZ)
* 년-월-일 "T" (구분 기호) 시:분:초.밀리초
* Z - 미 설정 시 현재 로컬 기준 UTC로, 설정 시 UTC+0 기준으로 시간 설정
~~~
let ms_parse = Date.parse("2020-03-31T00:00:00.000");

console.log(ms_parse);
console.log(new Date(ms_parse));

console.log(new Date(Date.parse("2020-03-31T00:00:00.000Z")));

/* 출력 값 : 
1585580400000
2020-03-30T15:00:00.000Z

2020-03-31T00:00:00.000Z
*/
~~~

## benchmark
* 벤치마크 측정 대상 함수 전후로 시간을 비교하여 알고리즘 성능을 측정
~~~
function dateSub(old_date, new_date) {
    return new_date - old_date;
}

function getTimeSub(old_date, new_date) {
    return new_date.getTime() - old_date.getTime();
}

function benchmark(callback_func) {
    let date_1 = new Date("2020-01-01");
    let date_2 = new Date();

    let start = Date.now();
    for (let i=0; i<100000; i++) {
        callback_func(date_1, date_2);
    }
    return Date.now() - start;
}

console.log("dateSub: " + benchmark(dateSub) + "ms");
console.log("getTimeSub: " + benchmark(getTimeSub) + "ms");

/* 출력 값 : 
dateSub: 18ms
getTimeSub: 8ms
*/
~~~


