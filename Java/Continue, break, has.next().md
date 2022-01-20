~~~
package ex13.control.continue_break;

import java.util.Scanner;

public class Program {
	public static void main(String[] args) {
		int n = 0;
		Scanner scan = new Scanner(System.in);
		System.out.println("값을 Space로 구분해서 5개 이상 입력하세요.");
		
		/* 34 5 6 234 345 54 45 Enter
		   Space로 구분하여 한 개씩 저장 */
		while(scan.hasNext()) { // 다음 값이 있을 경우 반복
			n = scan.nextInt();
			
			if(n < 10) continue;
			
			if(n > 300) break;
			
			System.out.println(n);
		}
	}
}
~~~
