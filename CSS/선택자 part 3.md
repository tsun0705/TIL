# 2021-09-04 Today I Learned

## 가상 요소 선택자

~~~
/* selector::_____ */

.favorite::before {
content: ' ';
}

.favorite::after {
content: ' ';
}

.lorem::first-letter {
}

.lorem::first-line {
}

.lorem::selection {
}
~~~
* 실제로 존재하지 않는 요소를 만들거나 범위를 만들어서 CSS를 적용한다.
* before, after는 클래스 명 앞, 뒤에 문자열을 추가할때 사용한다.
* first-letter는 첫 글자, first-line은 첫 번째 줄, selection은 드래그를 의미 한다. 
