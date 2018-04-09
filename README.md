# Magic8Ball-Java

import java.util.Scanner;
import java.util.Random;

public class Magic8Ball {

		public static void askAnother(int r) {

		    System.out.print("Hello! would You like to ask a Yes or No Question ...... What is your question? ");
		    Scanner input = new Scanner(System.in);
		    String question = input.nextLine();

		    String yes_or_no;
		    String next_question;
		    randomAnswer(r);

		    boolean playAgain = true;

		    while(playAgain) {
		        System.out.println("Would you like to ask another question? Y to ask, N to quit.");

		        yes_or_no = input.nextLine();

		        if (yes_or_no.equalsIgnoreCase("Y")) {
		            System.out.println("What is your next question?");
		            next_question = input.nextLine();
		            randomAnswer(r);

		        }//end if

		        else if (yes_or_no.equalsIgnoreCase("N")) {
		        playAgain = false;
		        System.out.println("Thanks for playing. Goodbye.");
		        System.exit(0);
		    }
		        else {
		            System.out.println("Invalid Input. Please enter Y or N.");
		            continue;
		        }//end else
		    }//end while
		}

		public static int randomAnswer(int random1) {

		    random1 = (int)(Math.random() * 20);

		switch(random1) {
		    case 0: System.out.println("It is certain"); break;
		    case 1: System.out.println("It is decidedly so"); break;
		    case 2: System.out.println("Without a doubt"); break;
		    case 3: System.out.println("Yes definitely"); break;
		    case 4: System.out.println("You may rely on it"); break;
		    case 5: System.out.println("As I see it, yes"); break;
		    case 6: System.out.println("Most likely"); break;
		    case 7: System.out.println("Outlook good"); break;
		    case 8: System.out.println("Yes"); break;
		    case 9: System.out.println("Signs point to yes"); break;
		    case 10: System.out.println("Reply hazy try again"); break;
		    case 11: System.out.println("Ask again later"); break;
		    case 12: System.out.println("Better not tell you now"); break;
		    case 13: System.out.println("Cannot predict now"); break;
		    case 14: System.out.println("Concentrate and ask again"); break;
		    case 15: System.out.println("Don't count on it"); break;
		    case 16: System.out.println("My reply is no"); break;
		    case 17: System.out.println("My sources say no"); break;
		    case 18: System.out.println("Outlook not so good"); break;
		    case 19: System.out.println("Very doubtful"); break;

		}//end switch
		return random1;
		}//end 
	
		
		
		public static void main(String[] args) {
			
			
			 int random = 0;
			    boolean playAgain = true;

			   while (playAgain) {
			       askAnother(random);
			    }//end while
			}//end main

	}



