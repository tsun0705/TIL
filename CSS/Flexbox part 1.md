# 2021-09-09 Today I Learned

## Flexbox - 
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

