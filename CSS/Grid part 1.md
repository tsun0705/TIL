# 2021-09-10 Today I Learned

## Grid
✔ 콘텐츠를 주축과 교차축에 배치할 수 있게 해주는 기능이다.   
✔ rows, columns, 행과 열사이의 공백을 나타내는 gutters로 구성된다.

## Container
✔ display: inline-grid 또는 grid로 지정 가능하다.

***
✔ gird-template-rows : 몇 개의 행을 가질건지 정한다.   
✔ gird-template-columns : 몇 개의 열을 가질건지 정한다.
~~~
.container {
gird-template-columns : 100px 150px 100px; /* 100px 150px 100px 크기를 갖는 3개의 열을 만든다 */
}
~~~
✔ px은 절대적인 크기를 지정
✔ 1fr는 비율을 지정하여 컨테이너 크기를 비율에 상응하여 크기를 갖는다. ex) 1fr 1fr 1fr = 1:1:1 비율로 크기를 갖는다.
✔ 반복해서 사용할 때 repeat(4, 1fr); - 1fr을 4번 반복한다.
***

