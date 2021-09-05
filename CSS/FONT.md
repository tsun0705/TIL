# 2021-09-02 Today I Learned

## font-size 폰트의 크기
~~~
#size {
  font-size: 16px
  }
~~~
* 글자의 크기를 지정한다.
* https://developer.mozilla.org/ko/docs/Web/CSS/font-size 폰트 사이즈 설정 유형
* rem   
  - html 태그에 적용된 font-size의 영향을 받는다. html 태그의 폰트 크기에 따라서 상대적으로 크기가 결정된다.

* px   
  - 모니터 상의 화소 하나의 크기에 대응되는 단위다. 고정된 값이기 때문에 이해하기 쉽지만, 사용자가 글꼴의 크기를 조정할 수 없기 때문에 가급적 사용을 하지 않는 것이 좋다. 

* em   
  - 부모 태그의 영향을 받는 상대적인 크기다. 부모의 크기에 영향을 받기 때문에 파악하기가 어렵다.   
  - rem이 등장하면서 이 단위 역시 사용이 권장되지 않는다.

*** 

## font-style
~~~
#style {
  font-style: italic
  }
~~~
* italic은 기울임꼴로 지정한다.
***

## text-align 텍스트 정렬
* left
* right
* center
* justify

*** 

## font-family 폰트의 서체
# font-family: "Times New Roman", Times, serif;

* serif (장식이 있는 폰트)
* sans-serif
* cursive (흘림체)
* fantasy
* monospace (고정폭)

*** 

## font-weight
~~~
.weight {
  font-weight: bold;
}
~~~
* 폰트의 두께를 지정한다.
* https://developer.mozilla.org/ko/docs/Web/CSS/font-weight

***

## line-height 
* 행과 행 사이의 간격
* line-height: 1.3;

## color
~~~
h1 {
  color:red;
  }
~~~
* 폰트의 색상을 지정한다.
* 폰트의 컬러
  - http://www.w3schools.com/css/css_colors.asp
