# 2021-09-03 Today I Learned

## 속성 선택자 (Attribute Selector)
### 적용방법   
~~~
/* 1. 태그[속성] */
a[target] {
  color:red;
  }
  
/* 2. 태그[속성="값"] */
a[href="www.naver.com"] {
  color:green;
  }
  
/* 3. 태그[속성^="값"] */
a[href^="https://"] {
  color:silver;
  }
  
/* 4. 태그[속성$="값"] */
a[href$=".com"] {
  color:gold;
  }
  
/* 5. 태그[속성*="값"] */
a[href*="www"] {
  color:blue;
  }
~~~
* 태그안에 있는 속성을 사용하여 CSS를 적용한다.
* 두 번째 적용 방법은 보통 input 태그안에 type 속성에 따라 다른 CSS를 적용할때 사용한다.
* 세 번째 적용 방법은 밸류값으로 시작할 시 CSS를 적용한다.
* 네 번째 적용 방법은 밸류값으로 끝날 시 CSS를 적용한다.
* 다섯 번째 적용 방법은 밸류값을 포함할 시 CSS를 적용한다.
***

## 가상 클래스 선택자 (Psedu-Class Selector)
~~~
/* 1. first-child */
li:first-child {
  color:green;
}

.movie:first-child {
  font-size: 32px;
}

/* 2. last-child */
span:last-child {
  color:tomato;
}

/* 3. nth-child */
li:nth-child() {
  color:pink;
}
~~~
* 첫 번째 first-child는 해당 태그안에 있는 첫 번째 요소에 CSS를 적용한다. 단, 형제들 중에서 첫 번째 자식을 찾는다.
* 클래스 명도 이용이 가능하다. 단, 형제들 중에서 첫 번째 자식을 찾는다.
* 두 번째 last-child는 해당 태그안에 있는 마지막 요소에 CSS를 적용한다.
* 세 번째 nth-child는 괄호 안에 숫자 또는 even, odd, 식을 대입하여 그 값에 맞는 요소에 CSS를 적용한다.
