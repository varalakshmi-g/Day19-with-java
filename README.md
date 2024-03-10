# Day19-with-java

Hello everyone, It's Day19 of my coding journey with java.I am proudly saying that I am growing everyday and I'm taking a step forward to learn coding. Hoping to continue this journey by enjoying it.

Today's challenge is to reverse a string.

Here is the code....

 import java.util.Scanner;

public class StringReverse {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string to reverse: ");
        String input = scanner.nextLine();
        scanner.close();
        
        String reversed = reverseString(input);
        System.out.println("Original string: " + input);
        System.out.println("Reversed string: " + reversed);
    }

    public static String reverseString(String str) {
        char[] charArray = str.toCharArray();
        int left = 0;
        int right = charArray.length - 1;
        
        while (left < right) {
            char temp = charArray[left];
            charArray[left] = charArray[right];
            charArray[right] = temp;
            left++;
            right--;
        }
        return new String(charArray);
    }
}

output: 
Enter a string to reverse: "varalakshmi"
Original string: "varalakshmi"
Reversed string:  "imhskalarav"
