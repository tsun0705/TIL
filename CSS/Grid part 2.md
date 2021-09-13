# 2021-09-13 Today I Learned
## Grid - Container
 
### grid-template-areas
* 지정된 그리드 영역 이름을 참조해 그리드 템플릿을 생성한다.
~~~
.a {
  grid-area: a;
}

.b {
  grid-area: b;
}

.c {
  grid-area: c;
}
/* 클래스 별로 이름 달기 */

grid-template-areas: 
            "a a ."
            "a a ."
            ". b c";
/* .은 공백 */
~~~
![image](https://user-images.githubusercontent.com/58898466/133034950-3129c2cc-29ff-4722-acc2-817cb68b0663.png)
***

### row-gap, column-gap, gap
* 행과 열간의 간격을 결정한다.
* gap: 20px 50px; - 단축 속성으로 작성이 가능하며, row - column 순으로 작성한다.
***

### grid-auto-rows, grid-auto-columns
* 템플릿의 범위를 넘치는 아이템들에게 높이와 너비를 지정한다.
***

### grid-auto-flow
* 아이템들이 자기 자리를 찾아가는 과정을 어떤 방향의 기준점으로 흘러가는지 결정한다.
* row, column, row dense, column dense 가 있다.
* dense를 추가 시 빈 영역없이 자리를 차지한다.
***

### grid (단축 속성)
* 명시적인 속성인 grid-template-rows, grid-template-columns, grid-template-areas 값과 암시적인 속성인 grid-auto-rows, grid-auto-columns, grid-auto-flow 값을 한번에 설정한다.
* / 로 구분지어 사용하며, 행과 열의 순서로 작성한다.
***

### justify-content (메인 축 기준), align-content (교차 축 기준)
* 내부의 컨텐츠를 어떻게 정렬할 것인지 지정한다.
* 컨텐츠의 크기보다 컨테이너의 크기가 커서 남는 여백에 있어야 사용할 수 있다.
* start가 기본값이며, end, space-around, space-between 사용 가능하다.
***

### justify-items (메인 축), align-items (교차 축)
* 하나의 틀 안에 하나의 아이템에 대한 정렬을 지정한다.
* stretch가 기본값이며, start, end 등이 있다.
* justify-self로 원하는 아이템에만 지정이 가능하다.
