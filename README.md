# Salary
import java.util.Scanner;

public class Salary {
   public static void main(String[] args) {
      // Declare variables
      double hours, salary, hourlyrate, extrahours;  
      int sentinel = -1;  // Terminating value for input
      Scanner in = new Scanner(System.in);

	  System.out.print("Enter hours worked (-1 to end): ");
	  hours = in.nextDouble();

	while (hours != sentinel) {
   // Read the rest of inputs
   System.out.print("Enter hourly rate of the employee: ");
   hourlyrate = in.nextDouble();

   if (hours < 40) {
   	salary = hours*hourlyrate;
   } else {
   	salary = hourlyrate*40 + (hours - 40)*(hourlyrate*1.5);
   }
   
   System.out.printf("Salary is: $" + String.format("%.2f", salary));
   // Read the next input.
   // Repeat the loop if input is not the terminating value.
   // Take note that you have to repeat these statements
   System.out.print("\n\nEnter hours worked (-1 to end): ");
   hours = in.nextDouble();
	}
	
	System.out.printf("bye");
      in.close();
   }
}
