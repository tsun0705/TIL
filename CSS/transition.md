# 2021-09-07 Today I Learned

## transition-property
~~~
#test {
  transition-property: none;
  transition-property: all;
  transition-property: margin-right;
  transition-property: margin-right, color;
)
~~~
* 일정 시간이 흐른 후 a의 CSS 상태가 b의 CSS 상태로 전환시켜준다.
***

## transition-duration
~~~
#test {
  transition-duration:3s, 100ms;
  transition-property: margin-right, color;
  /* margin-right는 3초, color는 0.1초 동안 바뀐다. */
}
~~~
* 얼마 만큼의 시간을 가지고 바뀌는지 설정한다.

***

## transition-delay
~~~
#test {
  transition-delay: 1s; /* 1초 뒤에 transition이 실행된다. */
}
~~~
* transition에 딜레이를 걸어 원하는 시간 만큼 늦게 실행 시킨다.

## transition-timing-function
* 바뀌는 과정의 순간을 어떻게 보일 것 인지 설정한다.
* https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function
***

## transition (단축 속성)
* 기본값
  - transition-delay: 0s
  - transition-duration: 0s
  - transition-property: all
  - transition-timing-function: ease
* property name - duration - timing function - delay
* 앞쪽에 있는 시간이 duration, 뒤쪽에 있는 시간 delay로 인식한다.
