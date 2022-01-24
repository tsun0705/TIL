~~~
package homework;

public class ArraySum {

	public static void main(String[] args) {
		int[] nums1 = {1,2,3};
		int[] nums2 = {4,5,6};
		int[] nums = new int[6];
		

			for(int i=0; i<3; i++) {
				nums[i] = nums1[i];
				nums[i+3] = nums2[i];
			}
			
		for (int i=0; i<6; i++)
			System.out.println(nums[i]);
	}
}
~~~
![image](https://user-images.githubusercontent.com/58898466/150716633-bdbdabed-78c3-4770-94cb-eefe9a799237.png)
