# Movie-Ticket-Booking
import java.util.*;
import java.io.*;
import java.time.*;
public class Main{
	public static void main(String args[]) {
		    Scanner input = new Scanner(System.in);

		    int[] SeatNo = new int[35];
		    int Seats;
		    int YesOrNo = 1;
		    String CustomerName;
		    String email;
		    String movie;
		    int time;
		    int date;

		    while (YesOrNo == 1) {
		      System.out.print("Welcome to BEZAWADA MOVIES!\nMay I know your good name?\n");
		      CustomerName = input.nextLine();
		      System.out.println("Please Enter your e-mail id :");
		      email = input.nextLine();
 
		      System.out.printf("Welcome %s! Please have a look at the Movies playing.\n\n", CustomerName);
		      for (int i = 1; i <= 34; i++) {
			        System.out.printf("*");
			      }
		      System.out.println("\nSyeera\nWhistle\nWar\nKhaidi");
		      movie=input.nextLine();
		      System.out.println("Enter the date :");
		      date=input.nextInt();
		      System.out.println("Available show times are 1.10:00 AM \n2.1:40 PM \n3.3:45 PM \n4.7:50 PM");
		      time=input.nextInt();
		      {
		      if (time==1)
		      {
		    	  System.out.println("You have selected 10:00 AM show");
		      }
		      else if(time==2)
		      {
		    	  System.out.println("You have selected 1:40 PM show");
		      }
		      else if(time==3)
		      {
		    	  System.out.println("You have selected 3:45 PM show");
		      }
		      else if(time==4)
		      {
		    	  System.out.println("You have selected 7:50 PM show");
		      }
		      else
		      {
		    	  System.out.println("Invalid time");
		      }
		    }
		      for (int i = 1; i <= 34; i++) {
		        System.out.print("*");
		      }
		      System.out.println();

		      System.out.println("Plese select your seat");

		      for (int j = 1; j <= 34; j++) {
		        System.out.print("*");
		      }
		      System.out.println();
		      {

		      for (int SeatCounter = 1; SeatCounter < 34; SeatCounter++) {
		        System.out.printf(SeatCounter + "\t");

		        if (SeatCounter == 4) {
		          System.out.println();
		        } else if (SeatCounter == 9) {
		          System.out.println();
		        } else if (SeatCounter == 14) {
		          System.out.println();
		        } else if (SeatCounter == 19) {
		          System.out.println();
		        } else if (SeatCounter == 24) {
		          System.out.println();
		        } else if (SeatCounter == 29) {
		          System.out.println();
		        }else if (SeatCounter == 34) {
			          System.out.println();
		      }
		      }
		      }
		      for (int k = 1; k <= 34; k++) {
		        System.out.print("*");
		      }
		      System.out.println();

		      System.out.print("Please select the seat");
		      Seats = input.nextInt();

		      while (Seats < 0 || Seats >34) {
		        System.out.println("Only 0 - 34 seats are allowed to book. Please try again: ");
		        Seats = input.nextInt();
		      }

		      for (int SeatCounter = 0; SeatCounter < SeatNo.length; SeatCounter++) {
		        if (SeatCounter == Seats) {
		        	Date timenow = new Date();
		        	System.out.println("\tBEZAWADA CINEMAS\t");
		        	System.out.println("" + timenow.toString());
		        	System.out.println("Customer Name : " +CustomerName);
		        	System.out.println("E-MAIL ID : " +email);
		        	System.out.println("DATE :" +date);
		          System.out.println("Seat " + Seats + " is selected.");
		          System.out.println("Total amount to be paid is RS:120");
		          System.out.println("Pay and collect  your tickets at Box office");
		          
		          System.out.println(
		              "Thanks for booking!\n\nWould you like to make next booking? (Type 1 = Yes; Type 2 = No)");
		          YesOrNo = input.nextInt();

		          if (YesOrNo == 2) {
		            System.out.println("Thank you for choosing BEZAWADA CINEMAS.");
		          }
		        }
		      }

		      while (YesOrNo != 1 && YesOrNo != 2) {
		        System.out.println("Invalid input.");
		        System.out.println("Type 1 = Continue booking; Type 2 = Exit the program");
		        YesOrNo = input.nextInt();

		        if (YesOrNo == 2) {
		          System.out.println("Thank you for using this program.");
		        }
		      }
		    }
	}
}
