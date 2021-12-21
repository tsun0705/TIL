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
# 시각화 : ggplot2 => +
# 패키지는 설치 후 주석처리

# install.packages("ggplot2")
library(ggplot2)

x = c("a", "a", "b", "c")
x
qplot(x) # 시각화

# data에 mpg, x축에 hwy 변수 지정
# mpg (Mile Per Callon) : 미국 환경 보호국에서 공개한 자료로 99~08년 사이 미국에서 출시된 자동차 234종의 연비 관련 정보
qplot(data=mpg, x=hwy)
~~~
