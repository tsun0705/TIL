# 2021-09-13 Today I Learned

## grid-template-areas
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
