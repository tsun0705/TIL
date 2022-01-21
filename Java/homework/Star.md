~~~
package ex00.homework;

public class Star {

	public static void main(String[] args) {
		for(int j=0; j<10; j++) {
			for(int i=0; i<10; i++) {
				System.out.printf("%c", '☆');
			}
			System.out.println();
		}
		
		System.out.println();
		
		for(int j=0;j<10;j++) {
			for(int i=0;i<j+1;i++) {
				System.out.print('☆');
			}
			System.out.println();
		}
		
		System.out.println();
		
		for(int j=10;j>0;j--) {
			for(int i=0;i<j;i++) {
				System.out.print('☆');
			}
			System.out.println();
		}
	}
}
~~~
![image](https://user-images.githubusercontent.com/58898466/150492912-a5dfdcad-b0be-4b40-81da-7480dc4521ce.png)
