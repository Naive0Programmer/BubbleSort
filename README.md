# Bubble Sort (Java Programming)

Bubble Sort is the simplest sorting algorithm that works by swapping the adjacent elements if they are in wrong order. 

However, it performs poorly and used primarily as educational tool. Has the worst case and average complexity of $O(n^2)$

For more information ([geeksforgeeks](https://www.geeksforgeeks.org/bubble-sort/))

```java
import java.util.Arrays;

public class QuickSort {
    public static int array[] = { 20, 25, 30, 199, 22, 14, 88, 60, 45, 37, 21, 6, 73, 7, 20, 25, 30, 11, 23, 14, 104,
            60, 45, 38, 21, 77, 3, 3, 29, 27, 32, 18, 22, 14, 66, 60, 45, 33, 21, 6, 3, 8 };

    public static int[] bubbleSort(int[] array) {
        int counter = array.length-1;
        for(int i = 0;i < array.length-1;i++) {
            if(array[i]>array[i+1]) {
                int holder = array[i+1];
                array[i+1] = array[i];
                array[i] = holder;
            }
            if(counter!=0&&i==array.length-2) {
                counter--;
                i=-1;
            }
        }
        return array;
    }

    public static void main(String args[]) {
        System.out.println("Original:     " + Arrays.toString(array));
        float start = System.currentTimeMillis();
        int myNewArray[] = QuickSort.bubbleSort(array);
        System.out.println("Sorted:        " + Arrays.toString(myNewArray));
        float done = System.currentTimeMillis() - start;
        System.out.println("Time: " + done);
    }
}

```

