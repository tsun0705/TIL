# 2021-09-09 Today I Learned

## ✔ Flexbox - container
* 행과 열 형태로 항목 무리를 배치하는 일차원 레이아웃 메서드다.
* 부모 자식간 관계여만 성립이 된다.
  - flex container : 아이템을 감싸고 있는 바깥족 부모 영역이다.
  - flex item : 내부의 정렬을 위해 담아 놓은 여러 개의 아이템이다.
  - main axis : 주축
  - cross axis : 교차축
* display inside(flex, grid)와 display-outside(inline, block)로 나뉜다.
* 컨테이너에서 정의한다.

## flex-direction
* 컨테이너 내의 아이템을 배치할 때 사용할 주축 및 방향을 지정한다.
* 컨테이너에서 정의한다.
* 주축의 위치를 수평, 수직으로 할지 주축의 방향을 정방향, 역방향으로 할지 설정한다.
  - row : 기본값이며, 글의 작성 방향과 주축이 동일하고 주축의 시작점과 끝점이 콘텐츠 방향과 동일하다.
  - row-reverse : row와 동일하게 작성되지만 시작점과 끝점이 반대다.
  - column : 주축이 불록 축과 동일하고 주축의 시작점과 끝점이 글 작성 모드의 이전 지점 및 이후 지점과 동일하다.
  - column-reverse : column과 동일하게 작성되지만 시작점과 끝점이 반대다.

## flex-wrap
* flex-item 요소들이 강제로 한줄에 배치되게 할 것인지, 여러 행으로 나누어 표현 할 것인지 결정하는 속성이다.
  - nowrap : 기본값이며, flex-item 요소들을 한 줄에 배치하고 시작점은 flex-direction에 의해 결정된 방향으로 적용한다.
  - wrap : 여러 행에 걸쳐서 배치된다. 시작점은 flex-direction에 의해 결정되고 일반적으로 위에서 아래로 쌓이는 순서다. (자기 자신의 width를 유지)
  - wrap-reverse : wrap과 동일하지만, 시작점과 끝점의 기준이 반대로 배치된다.
* 컨테이너에서 정의한다.

## flex-flow (단축 속성)
* flex-direction, flex-wrap 속성의 단축 속성이다.
* 스페이싱으로 구분하여 사용한다.
* 컨테이너에서 정의한다.

## justify-content
* 주축을 기준으로 아이템을 어떻게 정렬할지 정하는 속성이다.
  - flex-start : 주축이 시작되는 위치부터 정렬을 한다.
  - flex-end : 주축이 끝나는 위치에 정렬한다.  
  - center : 주축을 기준으로 가운데 정렬한다.
  - space-between : 시작과 끝부분은 붙어있고 나머지들은 동일한 간격으로 나눠진다.
  - space-around : 모든 부분을 동일한 간격으로 나눠진다. (시작과 끝부분도 공백을 가짐)

## align-items
* 교차축을 기준으로 컨테이너를 어디 부분에 위치 시킬지 정하는 속성이다.
  - stretch : 아이템이 차지할 수 있는 최대 값을 차지한다
  - flex-start : 교차축의 시작 부분에 위치한다.
  - flex-end : 교차축의 끝 부분에 위치한다.
  - center : 전체중 가운데에 위치한다.
* 한 줄일때 사용한다.

## align-content
* 교차축을 기준으로 어디에 위치 시킬지 정하며 여러 줄일때 사용한다.
* 키워드는 justify-content와 동일하다.
