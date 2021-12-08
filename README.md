# Exercise3
//Problem 1. Write a Java program to sum values of an array. //
package programs;

public class Exercise1
{

	public static void main(String[] args) {
		int my_array[] = {1,2,3,4,5,6,7,8,9,10};
		int sum = 0;
		
		for (int i : my_array)
			sum += i;
		System.out.println("The sum is " + sum);
	}

}
Output : The sum is 55

//Problem 2.Write  a Java program to print the following grid.//
package programs;
public class Exercise2
{
	public static void main(String[] args) {
		int [][]a = new int[10][10];
		for(int i =0; i < 10; i++)
		{
			for(int j = 0; j < 10; j++)
			{
				System.out.printf("%2d", a[i][j]);
			}
			System.out.println();
		}
	}
}
Output  : 
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 0 0 0 0 0 0 0 0 0 0
 
 //Problem 3.Write a Java program to calculate the average value of array element .//
package programs;
public class Exercise3
{
public static void main(String[] args) 
{
 int[] numbers = new int[] {20,30,25,35,-16,60,-100};
    int sum = 0;
    for(int i=0; i < numbers.length ;i++)
    	sum = sum + numbers[i];
    double average = sum /numbers.length;
    System.out.println("Average value of the array elements is : " + average );
	}
	}

Output  : Average value of the array elements is : 7.0

//Problem 4.Write a Java program to insert an element (specific position) into an array .//

package programs;
import java.util.Arrays;
public class Exercise4 {
	public static void main(String[]args) {
		int[] my_array = {25, 14, 56, 15, 36, 56, 77, 18, 29, 49};
		int Index_position = 2;
		int newValue  = 5;
		System.out.println("Original  Array :"+Arrays.toString(my_array));
		
		for(int i=my_array.length-1; i > Index_position; i-- ) {
			my_array[i] = my_array[i-1];
		}
		my_array[Index_position] = newValue;
		System.out.println("New Array: "+Arrays.toString(my_array));
	}
}

Output :
Original  Array :[25, 14, 56, 15, 36, 56, 77, 18, 29, 49]
New Array: [25, 14, 5, 56, 15, 36, 56, 77, 18, 29]

//Problem 5.Write a Java program to test if an array contains a specific  value .//

package programs;
import java.util.Arrays;
public class Exercise5 {

	public static void main(String[] args) {
		int[] my_array = {25, 14, 56, 15, 36, 56, 77, 18, 29, 49};
		System.out.println("Original Array :"+Arrays.toString(my_array));
		int removeIndex = 1;
		
		for(int i = removeIndex; i < my_array.length-1; i++) {
			my_array[i] = my_array[i + 1];
		}
      System.out.println("After removing the second element: "+Arrays.toString(my_array));
	}

}

Output : 
Original Array :[25, 14, 56, 15, 36, 56, 77, 18, 29, 49]
After removing the second element: [25, 56, 15, 36, 56, 77, 18, 29, 49, 49]

//Problem 6.Write a Java program to copy an array by iterating the array .//

package programs;
import java.util.Arrays;
public class Exercise6 {

	public static void main(String[] args) {
		int[] my_array = {25, 14, 56, 36, 56, 77, 18, 29, 49};
		int[] new_array = new int[10];
		System.out.println("Source Array : "+Arrays.toString(my_array));
		for(int i=0; i < my_array.length; i++) {
			new_array[i] = my_array[i];
		}
		System.out.println("New Array :"+Arrays.toString(new_array));
	}
}

Output :
Source Array : [25, 14, 56, 36, 56, 77, 18, 29, 49]
New Array :[25, 14, 56, 36, 56, 77, 18, 29, 49, 0]

//Problem 7.Write a Java program to reverse an array of integer values .//

package programs;
import java.util.Arrays;
public class Exercise7 {

	public static void main(String[] args) {
		int[] my_array1 = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
		System.out.println("Original array : "+Arrays.toString(my_array1));
          for(int i = 0; i < my_array1.length / 2; i++)
          {
        	  int temp = my_array1[i];
        	  my_array1[i] = my_array1[my_array1.length - i - 1];
        	  my_array1[my_array1.length - i - 1] = temp;
          }
          System.out.println("Reverse array  : "+Arrays.toString(my_array1));
	}
}
Output :

Original array : [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Reverse array  : [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]

//Problem 8.Write a Java program to find the second largest element in an array .//

package programs;
import java.util.Arrays;
public class Exercise8 {
public static void main(String[] args) {
	int[] my_array = { 100, 90, 88, 79, 69, 50, 48, 38, 26, 10};
	System.out.println("Original numeric array : "+Arrays.toString(my_array));
	Arrays.sort(my_array);
	int index = my_array.length-1;
	while(my_array[index]==my_array[my_array.length-1]) {
		index--;
	}
	System.out.println("Second largest value : " + my_array[index]);
	}
}

Output :
Original numeric array : [100, 90, 88, 79, 69, 50, 48, 38, 26, 10]
Second largest value : 90

//Problem 9.Write a Java program to convert an array to Array List.//

package programs;
import java.util.ArrayList;
import java.util.Arrays;
public class Exercise9 {
public static void main(String[] args)
{
		String[] my_array = new String[] {"Python","JAVA","PHP","Perl","C#","C++"};
		ArrayList<String> list = new ArrayList<String>(Arrays.asList(my_array));
		System.out.println(list);
	}
	}
Output : [Python, JAVA, PHP, Perl, C#, C++]
  
  //Problem 10.Write a Java program to cyclically rotate a given array clockwise by one.//

package programs;
import java.util.Arrays;
public class Exercise10 
{
 static int arra[] = new int[] {10, 20, 30, 40, 50, 60};
 static void rotate_array()
 {
	 int a = arra[arra.length-1], i;
	 for (i = arra.length-1; i > 0; i--)
		 arra[i] = arra[i-1];
	 arra[0] = a;
 }
	public static void main(String[] args) 
	{
		System.out.println("Original arraay: ");
		System.out.println(Arrays.toString(arra));

		rotate_array();
		
		System.out.println("Rotated arraay: ");
		System.out.println(Arrays.toString(arra));
	}
}

Output : 
Original arraay: 
[10, 20, 30, 40, 50, 60]
Rotated arraay: 
[60, 10, 20, 30, 40, 50]
  
