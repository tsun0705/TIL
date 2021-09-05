# 2021-09-05 Today I Learned

## font의 단축속성
~~~
.text {
  font: italic bold 24px/1.5 serif
}
~~~
* 폰트의 여러 가지 속성을 한 줄로 작성하는 방법이다.
* font-size, font-family는 필수로 작성하고 font-style, font-weight, line-height, font-variant는 옵션이다.
* font-style, font-weight는 font-size 코드 보다 앞에 있어야 한다.
* line-height는 font-size 뒤에 / 한 후 작성한다.
* font-family는 맨 뒤에다가 작성 해야한다.
* 공백으로 할 경우 기본값으로 적용된다.
* style - weight - size/height - family
***

## letter-spacing, word-spacing
~~~
.text {
  letter-spacing: 5px;  /* 글자간의 간격을 기본값에 +5px */
  word-spacing: -1rem;  /* 글자간의 간격을 기본값에 -1rem */
}
~~~
* letter-spacing은 글자간 간격을 지정한다.
* word-spacing은 단어 사이의 간격을 지정한다.
* 음수도 가능하다.
* word-spacing은 %값도 사용이 가능하다.
* https://developer.mozilla.org/ko/docs/Web/CSS/word-spacing
***

## text-align
~~~
.text {
  text-align: left;
}
~~~
* left, right, center 속성이 대표적이다.
* 블록 요소에서만 사용이 가능하다.
***

## text-indent
~~~
.text {
  text-indent: 20px;
}
~~~
* 들여쓰기, 내어쓰기를 지정한다.
* 블록 요소에서만 사용이 가능하다.
* https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent

***

## text-decoration
~~~
.text {
  text-decoration: underline red 3px double;
}
~~~
* text-decoration은 라인에 대한 단축 속성으로 line, color, style, thickness를 지정한다.
* line은 필수 요소이다.
  - underline, overline, line-through (취소선)
  - 여러 가지 선 종류를 중첩해서 사용이 가능하다.
* style 요소
  - solid, double, dotted, dashed, wavy
* 사용 빈도가 높다.
* 순서는 상관없이 작동한다.
***

## word-break
~~~
p[lang="en"] {
  word-break: break-all
}

p[lang="ko"] {
  word-break: keep-all
}
~~~
* 텍스트가 자신의 콘텐츠 박스 밖으로 오버플로 할 때 줄을 바꿀 지 지정합니다.
* break-all은 콘텐츠 박스 밖으로 오버플로 할 때 줄을 바꾼다.
* keep-all은 콘텐츠 박스 밖으로 오버플로 할 때 줄을 바꾸지 않는다.
***

## text-transform
~~~
.container p:last-of-type {
  text-transform: uppercase;
}
~~~
* 영문자에 사용이 가능하다
* uppercase : 대문자, lowercase : 소문자, capitalize : 단어 첫 글자만 대문자로 변경한다.
