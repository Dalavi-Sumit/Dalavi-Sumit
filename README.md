import java.util.Scanner;

public class Prime{
    
    public static boolean isPrime(int number) {
        if (number <= 1) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(number); i++) {
            if (number % i == 0) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the first number: ");
        int start = scanner.nextInt();
        
        System.out.print("Enter the second number: ");
        int end = scanner.nextInt();
        
        if (start > end) {
            System.out.println("The first number must be less than or equal to the second number.");
            return;
        }

        System.out.println("Prime numbers between " + start + " and " + end + ":");
        
        for (int i = start; i <= end; i++) {
            if (isPrime(i)) {
                System.out.print(i + " ");
            }
        }
        
        scanner.close();
    }
}
