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
