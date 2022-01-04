## 파일 I/O
~~~
>>> f=open("C:/PYTHON/temp.txt",'w')

>>> f.close()

>>>
~~~
* 위의 예제는 C드라이브 바로 아래에 PYTHON이라는 폴더를 만들고, temp.txt 파일을 생성하라는 코드
* close() 함수는 파일을 닫아주는 역할

| 파일 열기 모드 | 설명 |
| ------ | ------ |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;r | 읽기모드, 파일을 읽을 수 만 있음 |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;w | 쓰기모드, 파일의 내용을 입력할 때 사용|
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a | 추가모드, 파일의 마지막에 내용을 추가할 때 사용|
***

~~~
PATH = "C:/PYTHON/temp.txt"

f=open(PATH,'w')
for i in range(1,6):
  line = "%d번째 줄.\n" %i
  f.write(line)
f.close()
~~~
~~~
실행 결과 : 
1번째 줄.
2번째 줄.
3번째 줄.
4번째 줄.
5번째 줄.
~~~
***
### 파일을 읽을 때 사용할 수 있는 함수
~~~
>>> f=open("C:/PYTHON/temp.txt", 'r')
>>> line=f.readlines()
>>> for i in line:
      print(i)


1번째 줄.

2번째 줄.

3번째 줄.

4번째 줄.

5번째 줄.

>>> f.close()
>>>
~~~
* readline() - 모든 줄을 한 줄씩
* readlines() - 한 줄을 한 글자씩
* read() - 모든 줄을 한 글자씩
***

### 기존 파일에 새로운 내용 추가
~~~
f=open("C:/PYTHON/temp.txt", 'a')

for i in range(6,11):
  line = "%d번째 줄.\n" %i
  f.write(line)
  
f.close()
~~~
~~~
실행 결과 : 

1번째 줄.
2번째 줄.
3번째 줄.
4번째 줄.
5번째 줄.
6번째 줄.
7번째 줄.
8번째 줄.
9번째 줄.
10번째 줄.
~~~
