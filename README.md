# interfacess

import java.util.Scanner;
interface calculator{
double add(double a,double b);
double subtract(double a,double b);
double multiply(double a,double b);
double divide(double a,double b);
}

class simplecalculator implements calculator{

    
    public double add(double a, double b) {
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
            System.out.println("error:division by zero is not allowed!");
            return Double.NaN;
        }
        return a/b;
    }
    
}
public class Interface {
        public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        calculator calc=new simplecalculator();
        System.out.println("WELCOME TO THE SIMPLE CALCULATOR!!");
        
        System.out.println("enter the first number:");
        double num1=sc.nextDouble();
        System.out.println("enter the second number:");
        double num2=sc.nextDouble();
        
        System.out.println("\n results:");
        System.out.println("addition:"+ calc.add(num1,num2));        
        System.out.println("subtraction:"+ calc.subtract(num1,num2));        
        System.out.println("multiplication:"+ calc.multiply(num1,num2));        
        System.out.println("division:"+ calc.divide(num1,num2));        
        
    }
    
}


Output:
WELCOME TO THE SIMPLE CALCULATOR!!
enter the first number:
6
enter the second number:
2

 results:
addition:8.0
subtraction:4.0
multiplication:12.0
division:3.0


