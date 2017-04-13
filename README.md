# Exercise-13
Hi-Low game
/*
* Jonathan Saldivar 
* ITSE 1302-011 
* Exercise 13 
* Demostrates a guessing game of High and low.
*/

import java.util.*;

public class HiLow {

public static void main (String [] strArgs) {

  Random objRandom = new Random();
  int intlimit = 1000000001;//The highest # the random generator can select -1
  int intNumber = objRandom.nextInt(intlimit);
  Scanner objScanner = new Scanner(System.in);
  int intPlayer = 0;

    do {
        System.out.print("Guess a # between 0 and 1000000000: ");
        intPlayer = objScanner.nextInt();

        if(intPlayer < intNumber) {
            System.out.println("Too Low.");//Tells the player to try again but with a higher #
        }else if(intPlayer > intNumber) {
            System.out.println("Too High");//Tells the player to try again but with a lower #
        }

    } while(intPlayer != intNumber);//Makes sure that it doesnt show this println unless the player has chosen the correct #
    System.out.println("Congratulations! The number was " + intNumber);//Congratulates the player and displays the correct #

  }
}
