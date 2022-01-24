~~~
package homework;

public class ArraySearch {

	public static void main(String[] args) {
		int[] nums = {5,2,7,4,6,1,3};
		int index = -1;
		
		for(int i=0; i<nums.length; i++) {
			if(nums[i] == 1) {
				index = i;
				break;
			}
		}
		System.out.println(index);
	}

}
~~~
![image](https://user-images.githubusercontent.com/58898466/150738086-d58c0083-350a-419c-9fe7-8eaa7bf20506.png)
