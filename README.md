import java.util.Arrays;

public class BubbleSort {
    public static void main(String[] args) {
        int[] notSortedArray = new int[10];
        boolean swapped = true;
        int temp = 0;

        for (int i = 0; i < 10; i++) {
            notSortedArray[i] = (int) (Math.random() * 100 + 1);
        }
        System.out.println("Not sorted array: " + Arrays.toString(notSortedArray));
        
        while (swapped) {
            swapped = false;
            for (int i = 0; i < 9; i++) {
                if (notSortedArray[i] > notSortedArray[i + 1]) {
                    temp = notSortedArray[i];
                    notSortedArray[i] = notSortedArray[i + 1];
                    notSortedArray[i + 1] = temp;
                    swapped = true;
                }
            }
        }
        System.out.println("Sorted array: " + Arrays.toString(notSortedArray));
    }
}
