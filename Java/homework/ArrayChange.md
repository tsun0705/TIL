~~~
package homework;

public class ArraySearch {

	public static void main(String[] args) {
		int[] nums = {5,2,7,4,6,1,3};
		int temp;
		
		for(int i=0; i<nums.length; i++)
			System.out.printf("%d ", nums[i]);
		
		System.out.println();

		
		temp = nums[1];
		nums[1] = nums[3];
		nums[3] = temp;
		
		for(int i=0; i<nums.length; i++)
			System.out.printf("%d ", nums[i]);
	}

}
~~~
![image](https://user-images.githubusercontent.com/58898466/150739023-2336e1e7-6623-4afe-b5a1-bf98f85b0c2b.png)
