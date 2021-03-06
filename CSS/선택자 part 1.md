# 2021-09-02 Today I Learned
## 범용 선택자   
~~~
*{
}

p.red {
}

p + * {
}
~~~
* 첫번째 코드는 모든 요소에 적용한다.
* 두번째 코드는 p태그의 red 클래스에 적용한다.  
* *도 선택자이기 때문에 다른 선택자와 결합이 가능하다. 

***

## 태그 선택자   
~~~
H1 {
}
~~~
* 태그를 사용하는 요소에 스타일을 적용한다.     
* 보통 CSS 상단에서 사용한다.   
***

## ID 선택자   
~~~
#id명 {
} 
~~~
* id속성을 가진 특정 부분에 스타일을 적용한다. (이름표를 달아주는 느낌)
* id 에 줄 경우 아래처럼 #을 맨 앞에 붙여 사용하며 원칙적으로 ***하나의 객체*** 에만 적용할 수 있다.   
* 전역 속성이기 때문에 모든 속성에 사용이 가능하다.
***

## Class 선택자   
~~~
.class명 {
}
~~~
* class 이름을 가진 특정 집단의 요소에 스타일을 적용한다.      
* class에 줄 경우 아래처럼 .을 맨 앞에 붙여 사용하며 ***여러 객체***에 적용할 수 있다.   
* 전역 속성이기 때문에 모든 속성에 사용이 가능하다.
* 스페이싱을 사용하여 두 개의 이름도 적용 가능하다.
* 캐스캐이딩 원칙에 의해 뒤에 나온 소스코드를 우선 순위로 적용한다.
***

## 그룹 선택자    
~~~ 
H1, P {
}
~~~
* 여러 개의 요소를 ,로 연결해 스타일을 적용한다.  
***

## 하위 선택자   
~~~
ul a {
}
~~~
* 하위의 모든 요소에 스타일을 적용, 띄어쓰기 사용한다.   
* id, class 요소 다 사용 가능하다.
***

## 자식 선택자    
~~~
ul > a {
}
~~~
* 바로 하위에 있는 자식요소에 스타일을 적용한다.  
