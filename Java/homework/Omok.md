~~~
package homework;

public class Omok {

	public static void main(String[] args) {
		for(int y=1; y<=10; y++) {
			for(int x=1; x<=10; x++)
				if(x==4 && y==3)
					System.out.printf("%c",  '○');
				else if (x == 1 && y == 1)
					System.out.printf("%c",  '┌');
				else if (x == 10 && y == 1)
					System.out.printf("%c",  '┐');
				else if (x == 10 && y == 10)
					System.out.printf("%c",  '┘');
				else if (x == 1 && y == 10)
					System.out.printf("%c",  '└');
				else if (x == 1)
					System.out.printf("%c",  '├');
				else if (y == 1)
					System.out.printf("%c",  '┬');
				else if (x == 10)
					System.out.printf("%c",  '┤');
				else if (y == 10)
					System.out.printf("%c",  '┴');
				else
					System.out.printf("%c", '┼');
			System.out.println();
		}
	}
}
~~~
![image](https://user-images.githubusercontent.com/58898466/150713058-206904b0-eeab-4bf1-8d47-60dbe090bd02.png)
