package pkginterface;
import java.util.Scanner;
interface Calculator{
    double add(double a,double b);
    double subtract(double a,double b);
    double multiply(double a,double b);
    double divide(double a,double b);
}
class SimpleCalculator implements Calculator{
    public double add(double a,double b){
        return a+b;
    }
    public double subtract(double a,double b){
        return a-b;
    }
    

    
    public double multiply(double a, double b) {
        return a*b; 
    }

    
    public double divide(double a, double b) {
        if(b==0){
            System.out.println("Error: division by zero is not allowed1");
            return Double.NaN;
        }
        return a/b; //To change body of generated methods, choose Tools | Templates.
    }
}

public class Interface {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Calculator calculator=new SimpleCalculator();
        System.out.println("Welcome to the Simple Calculator1");
        System.out.println("Enter the first number:");
        double num1 = scanner.nextDouble();
        System.out.println("Enter the second number:");
        double num2 = scanner.nextDouble();
        System.out.println("\nResults:");
        System.out.println("Addition:"+ calculator.add(num1, num2));
        System.out.println("Subtraction:" + calculator.subtract(num1, num2));
        System.out.println("Multiplication:" + calculator.multiply(num1, num2));
        System.out.println("Division:"+ calculator.divide(num1, num2));
        scanner.close();
    }
    
}

OUTPUT:
Welcome to the Simple Calculator1
Enter the first number:
5
Enter the second number:
2

Results:
Addition:7.0
Subtraction:3.0
Multiplication:10.0
Division:2.5
