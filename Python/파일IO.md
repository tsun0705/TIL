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
