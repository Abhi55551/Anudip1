# Anudip1
package Aemo;
import java.util.ArrayList;
import java.util.Scanner;

public class StudentGrades {
	 public static void main(String[] args) {
	        Scanner scanner = new Scanner(System.in);
	        ArrayList<Double> grades = new ArrayList<>();
	        String input;
	        
	        System.out.println("Enter student grades (type 'done' to finish):");
	        
	        while (true) {
	            System.out.print("Enter grade: ");
	            input = scanner.nextLine();
	            
	            if (input.equalsIgnoreCase("done")) {
	                break;
	            }
	            
	            try {
	                double grade = Double.parseDouble(input);
	                
	                if (grade < 0 || grade > 100) {
	                    System.out.println("Please enter a valid grade between 0 and 100.");
	                } else {
	                    grades.add(grade);
	                }
	            } catch (NumberFormatException e) {
	                System.out.println("Invalid input. Please enter a numeric grade.");
	            }
	        }
	        
	        if (grades.size() > 0) {
	            double total = 0;
	            for (double grade : grades) {
	                total += grade;
	            }
	            double average = total / grades.size();
	            System.out.println("The average grade is: " + average);
	        } else {
	            System.out.println("No grades entered.");
	        }
	        
	        scanner.close();
	    }
	}




