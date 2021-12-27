~~~
a = 1
b = 2

c = a + b

var1 = c(1,2,5,7,8) # 배열
var1
var2 = c(1,1,1,1)
var2

var2 = c(1:5) # 배열 1~5
var2

var3 = seq(1,5) # 배열 1~5
var3

var4 = seq(1,10)
var4 = seq(1,10, by=2) # 배열 1~5, 2씩 
var4 = seq(1,10,by=2)

var1+var2

str1 = "a"
str1

str2 = "text"
str2

str3 = "Hello World!"
str3

str4 = c("a", "b", "c")
str4

str5 = c("Hello", "Wolrd", "is")
str5

x = c(1,2,3)
mean(x) # 중간값
max(x)
min(x)
str5 
paste(str5, collapse=",") # 합치기
paste(str5, collapse = " ") 

# 대표적인 패키지
# 데이터 : dplyr => %>% (체인 블록 : 연결 - 여러줄을 하나로 만듦)
# 시각화 : ggplot2 => + , 부수적으로 mpg 데이터를 포함하고 있음
# 패키지는 설치 후 주석처리

# install.packages("ggplot2")
library(ggplot2)

x = c("a", "a", "b", "c")
x
qplot(x) # 시각화

# data에 mpg, x축에 hwy 변수 지정
# mpg (Mile Per Callon) : 미국 환경 보호국에서 공개한 자료로 99~08년 사이 미국에서 출시된 자동차 234종의 연비 관련 정보
qplot(data=mpg, x=hwy)

## 데이터 목록 보기
data()

# x축 cty
qplot(data=mpg, x=cty)

# x축 drv, y축 hwy
qplot(data=mpg, x=drv, y=hwy)

# x축 drv, y축 hwy, 선 그래프 형태
qplot(data=mpg, x=drv, y=hwy, geom = "line")

# x축 drv, y축 hwy, 상자 그래프 형태
qplot(data=mpg, x=drv, y=hwy, geom = "boxplot")

# x축 drv, y축 hwy, 상자 그림형태, drv별 색 표현
qplot(data=mpg, x=drv, y=hwy, geom = "boxplot", colour=drv)

# Box Plot
# 1) MAX 2) MIN 3) 중앙값 4) 중심값 5) 25, 50, 75%, 이상치

~~~

