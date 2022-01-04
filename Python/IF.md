## IF
~~~
a = "A"
if a=="A":
  print("합격")
else:
  print("불합격")
~~~
~~~
실행 결과 : 
합격
~~~

## x in s, x not in s
* in 키워드는 변수 s에 x 값이 포함되어 있다면 True를 반환하고, 포함되어 있지 않다면 False를 반환
* not in 키워드는 변수 s에 x 값이 포함되어 있지 않다면 True를 반환하고, 포함되어 있다면 False를 반환 
* 변수 s의 자료형은 리스트, 튜플, 문자열

~~~
>>> a in ['a','b','c']
False

>>> 'a' in ['a','b','c']
True

>>> 'a' not in ['a','b','c']
False
~~~

~~~
box =['candy','chocolate','coke']

if 'candy' in box:
  print("삼키다") #pass
else:
  print("뱉다")
~~~
~~~
실행 결과 :
삼키다
~~~
* 이때 print("삼키다") 대신에 pass 키워드를 넣는다면 아무런 결과도 출력되지 않고 if / else 문이 종료

## IF ELSIF ELSE
~~~
a=1
b=0

if a and b:
  print("AND")
elif a==0:
  print("a=0")
elif b==1:
  print("b=1")
elif not a:
  print("not a")
else:
  print("OR")
~~~
~~~
실행 결과 : 
OR
~~~
