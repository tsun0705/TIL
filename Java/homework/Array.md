## 배열 값 이동
~~~
package homework;

public class Array {

	public static void main(String[] args) {
		int[] nums = {1,2,3,4,5,6,7};
		int[] temp = new int[10];
		
		for(int i=0; i<7; i++)
			System.out.printf("%d ", nums[i]);
		
		for(int i=0; i<7; i++) {
			temp[i] = nums[i];
		}
		
		nums = temp;
		nums[7] = 8;
		
		for(int i=0; i<8; i++)
			System.out.printf("%d ", nums[i]);
	}
}
~~~
![image](https://user-images.githubusercontent.com/58898466/150715825-a396ca97-1efd-4ebd-8a69-0f2f247adf23.png)
