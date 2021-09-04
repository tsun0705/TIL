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
***

## 형제 선택자
~~~
/* 1. 일반 형제 선택자 결합 (~) */
code ~ selector {
}

/* 2. 인접 형제 선택자 결합 (+) */
code + selector {
}

~~~
* 1번은 앞에 있는 요소와 형제 관계인 셀렉터를 뒤에 표시한다.
* 1,2번은 앞에 있는 선택자는 뒤에 있는 선택자보다 위에 있어야 한다. 즉 code 선택자 보다 아래에 있어야 한다.
* 셀렉터는 class, id, 속성도 가능하다.
* 2번은 가장 인접한 선택자만 가능하다. 즉 code 선택자 바로 아래에 선택자만 사용이 가능하다.
