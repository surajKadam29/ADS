package stackkkk;
import java.util.Scanner;

class stack {
    int top = -1;
    int n = 10;
    int a[] = new int[n];
    Scanner sc = new Scanner(System.in);

    void push() {
        if (top == (n - 1)) {
            System.out.println("Overflow");
        } else {
            System.out.println("Enter Data");
            int i = sc.nextInt();
            top = top + 1;
            a[top] = i;
            System.out.println("Item inserted");
        }
    }

    void pop() {
        if (top == -1) {
            System.out.println("Underflow");
        } else {
            top = top - 1;
            System.out.println("Item deleted");
        }
    }

    void display() {
        if (top == -1) {
            System.out.println("Stack is empty.");
            return;
        }
        System.out.println("Items are: ");
        for (int j = top; j >= 0; j--) {
            System.out.println(a[j]);
        }
    }
}


public class stack_array {
    public static void main(String[] args) {
        int d;
        int l;

        Scanner sc = new Scanner(System.in);
        stack s = new stack();

        do {
            System.out.println("Press 1 to push");
            System.out.println("Press 2 to pop");
            System.out.println("Press 3 to display");
            System.out.println("Enter Your Choice");
            d = sc.nextInt();

            switch (d) {
                case 1:
                    s.push();
                    break;
                case 2:
                    s.pop();
                    break;
                case 3:
                    s.display();
                    break;
                default:
                    System.out.println("Invalid choice");
            }

            sc.nextLine();

            System.out.println("Enter 0 to go back to the main menu");
            System.out.println("Enter any other key to exit");
            l = sc.nextInt();

        } while (l == 0);

        System.out.println("Exit Success");
    }
}
