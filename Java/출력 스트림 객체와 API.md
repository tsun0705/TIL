## 표준 입출력
* System.in: 표준 입력용 스트림
* System.out: 표준 출력용 스트림
* System.err: 표준 오류 출력 스트림

## 표준 입출력 Method
| 메소드 | 설명 |
| ------ | ------ |
|System.in.read() | 키보드로 입력된 값을 읽어들임, 더 이상 읽어들일 수 없으면 -1 리턴 |
|System.out.write() |( )안에 입력된 값을 화면(콘솔)에 출력 컴퓨터가 숫자로 저장하고 있는 것을 사람이 읽을 수 있는 문자로 디코딩해서 출력|
|System.out.flush()| 출력은 버퍼에 일정 용량 이상이 쌓여야 가능한데, 버퍼를 비워서 바로 출력하도록 하는 메소드 데이터를 일정 용량 쌓아두었다가 출력하는 이유는 입출력 성능 향상을 위함|
* 입출력 메소드 사용시 반드시 예외 처리를 해야함
~~~ 
	public static void main(String[] args) {
		System.out.write(3); // 3이라는 코드값을 가진 문자를 스트림 버퍼에 할당, 출력은 X
		System.out.flush(); // 버퍼를 바로 출력
		
		System.out.println();
		
		System.out.write('3'); // 3이라는 문자를 스트림 버퍼에 할당, 출력은 X
		System.out.flush(); // 버퍼를 바로 출력
	}
~~~
