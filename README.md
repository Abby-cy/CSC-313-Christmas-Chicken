1.WRITE A JAVA PROGRAM TO PRINT OUT THE FLAG OF NIGERIA  using a single loop first, then a nested loop 
Answer
Single Loop
Import  java.util.Scanner
public class NigeriaFlagSingleLoop {
    public static void main(String[] args) {
        int width = 15;
        int height = 9; 

        for (int i = 0; i < height; i++) {
            for (int j = 0; j < width; j++) {
                if (j < width / 3 || j >= 2 * width / 3) {
                    System.out.print("*");
                } else {
                    System.out.print("=");
                }
            }
            System.out.println();
        }
    }
}



Nested Loop
public class NigeriaFlagNestedLoop {
    public static void main(String[] args) {
        int width = 15;
        int height = 9; 

        for (int i = 0; i < height; i++) {
            for (int j = 0; j < width; j++) {
                if (j < width / 3 || j >= 2 * width / 3) {
                    System.out.print("*");
                } else {
                    System.out.print("=");
                }
            }
            System.out.println();
        }
    }
}






2.  Consider an array that has the data shown below. Write a java program to do the following: The mean. mean = sum of all element/number of element. Print out the median. median = element at the middle The standard deviation = √∑▒(x_i−μ)^2/N  	where N is size of population, μ is the population mean 	 x_i is each value from the population. the array is;     
2    5	5	9	4	7	0	9	6	11	12 
Answer
import java.util.Arrays;

public class ArrayStatistics {
    public static void main(String[] args) {
        int[] array = {2, 5, 5, 9, 4, 7, 0, 9, 6, 11, 12};
        
        double mean = calculateMean(array);
        System.out.println("Mean: " + mean);


        double median = calculateMedian(array);
        System.out.println("Median: " + median);


        double standardDeviation = calculateStandardDeviation(array, mean);
        System.out.println("Standard Deviation: " + standardDeviation);
    }

    public static double calculateMean(int[] array) {
        double sum = 0;
        for (int num : array) {
            sum += num;
        }
        return sum / array.length;
    }

       public static double calculateMedian(int[] array) {
        Arrays.sort(array); 
        int n = array.length;
        if (n % 2 == 0) {
                     return (array[n / 2 - 1] + array[n / 2]) / 2.0;
        } else {
                       return array[n / 2];
        }
    }

     public static double calculateStandardDeviation(int[] array, double mean) {
        double sumSquaredDifferences = 0;
        for (int num : array) {
            sumSquaredDifferences += Math.pow(num - mean, 2);
        }
        return Math.sqrt(sumSquaredDifferences / array.length);
    }
}
3. Declare an array of length 10.
Write a program using a loop to assign elements to the array by accepting input from the user. Make sure to state the index that the user’s input will be to the user before accepting the input.
Using a for each loop, print out the input entered by the user.

Answer
import java.util.Scanner;

public class ArrayInputExample {
    public static void main(String[] args) {
        int[] array = new int[10]; 
        Scanner scanner = new Scanner(System.in);

        
        for (int i = 0; i < array.length; i++) {
            System.out.print("Enter the value for index " + i + ": ");
            array[i] = scanner.nextInt();
        }
        System.out.println("\nYou entered:");
        for (int value : array) {
            System.out.println(value);
        }
      scanner.close(); 
    }
}

4. Declare a 2D array of size 10 by 10.
Write a program using a loop to assign elements to the array by accepting input from the user. Make sure to state the index that the user’s input will be to the user before accepting the input.
Using a for each loop, print out the input entered by the user.

Answer
import java.util.Scanner;

public class TwoDArrayInput {
    public static void main(String[] args) {
        int[][] array = new int[10][10]; 
        Scanner scanner = new Scanner(System.in);

        
        for (int i = 0; i < array.length; i++) { 
            for (int j = 0; j < array[i].length; j++) { 
                System.out.print("Enter the value for index [" + i + "][" + j + "]: ");
                array[i][j] = scanner.nextInt();
            }
        }

        
        System.out.println("\nYou entered:");
        for (int[] row : array) { 
            for (int value : row) { 
                System.out.print(value + " ");
            }
            System.out.println();
        }

        scanner.close();
    }
}

