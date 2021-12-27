## 데이터 시각화
* 히스토그램
* 선 그래프
* 산점도
* 바 그래프
* 상자 그래프

## 레이아웃 구조 이해
* 1단계 - 배경 설정 (축)
* 2단계 - 그래프 추가 (점, 막대, 선)
* 3단계 - 설정 추가 (축 범위, 색, 표식)

~~~
# 1단계 - x축은 displ, y축은 hwy로 지정해 배경 설정
ggplot(data=mpg, aes(x=displ, y=hwy))

# 2단계 - 배경에 산점도 추가
ggplot(data=mpg, aes(x=displ, y=hwy)) + geom_point()

# 3단계 - x축 범위 3~6으로 지정, y축 범위는 10~30으로 지정
ggplot(data=mpg, aes(x=displ, y=hwy)) + geom_point() + xlim(3,6) + ylim(10,30)
~~~
![image](https://user-images.githubusercontent.com/58898466/147439483-1c580cdc-e14e-4d5f-ab7b-272b652dce1a.png)
***

~~~
library(dplyr)

rm(mpg)

df_mpg = mpg %>% group_by(drv) %>% summarise(mean_hwy = mean(hwy)) 
df_mpg

ggplot(data=df_mpg, aes(x=drv, y=mean_hwy))+geom_col()
ggplot(data=df_mpg, aes(x=reorder(drv, -mean_hwy), y=mean_hwy))+geom_col()

# 빈도 막대 그래프
# x축만 지정하고, geom_col 대신에 geom_bar() 사용
ggplot(data=mpg, aes(x=drv)) + geom_bar()

ggplot(data=mpg, aes(x=hwy)) + geom_bar()

## 시계열 그래프 - 선 그래프
ggplot(data = economics, aes(x=date, y=unemploy)) + geom_line()

## 상자 그래프
ggplot(data = mpg, aes(x=drv, y=hwy)) + geom_boxplot()
~~~
