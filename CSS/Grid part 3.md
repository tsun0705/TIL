# 2021-09-13 Today I Learned

## Grid - item

### grid-row, grid-column
* grid-row-start 와 grid-row-end의 단축 속성이며, / 로 구분한다. 
* grid-column 도 동일하게 사용한다.
~~~
grid-row: 1 / 3;
/* 첫번째 선부터 세번째 선까지 차지한다. */

grid-row 1 / -1;
/* 첫번째 선부터 마지막 선까지 차지한다. */

grid-row 1 / -2;
/* 첫번째 선부터 마지막 선 바로 전의 선까지 차지한다. */
grid-row 1 / span 2;
/* 첫번째 선부터 2칸을 차지한다. */
~~~
***

### grid-area
* grid-area 속성은 grid-row-start, grid-column-start, grid-row-end, grid-column-end 값을 한번에 설정하는 단축 속성이다.
* 이름을 지정할때 사용하기도 한다.
* row-start / column-start / row-end / column-end 순으로 작성한다.
~~~
grid-area: a; 
/* a라는 이름을 지정 */

grid-area: 2 / 1 / 2 / 4;
~~~
***

### order
* 현재 요소의 배치 순서를 지정한다.
* 기본값은 0이며, 작은 숫자가 우선순위다.
* 동일한 숫자를 가지면, 마크업 코드 순서로 나타낸다.
***

### z-index
* 아이템의 Z축 순서를 지정한다.
* z-index의 숫자가 클수록 앞에 나타난다.
***

## Grid 단위
✔  fr, min-content, max-content, auto-fill, auto-fit, minmax(min, max)
* fr : 비율을 지정하며, 절대 길이와 같이 혼용이 가능하다.
* min-content : 컨텐츠의 내용 중에서 제일 긴 단어의 길이 만큼 바뀐다. (최소 길이만큼 줄어든다.)
* max-content : 컨텐츠의 내용을 자르지 않고 한 줄로 표시하여 그 길이를 유지한다. (최대 길이만큼 줄어든다.)
* auto-fill : 아이템의 지정한 크기만큼 공간이 남으면 아이템으로 컨테이너를 채운다.
* auto-fit : 남는 크기와 상관없이 남는 공간을 자동으로 전부 채운다.
* minmax(min, max) : min값, max값을 지정한다. 
