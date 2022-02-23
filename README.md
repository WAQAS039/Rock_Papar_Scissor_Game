# Rock_Papar_Scissor_Game
package JAVAFROMVIDEOS;

import java.util.Random;
import java.util.Scanner;

public class Rock_Papar_Scissor_Game {

	public static void main(String[] args) {
		Random random = new Random();
		Scanner scanner = new Scanner(System.in);
		String yesno; 
		// DO WHILE FOR YES/NO 
		do {
		// FOR LOOP FOR ROUNDS
		for(int round = 1; round < 3; round++) {
		//Code for Computer Move
		String  moves[] = {"r","p","s"};
		String computerMoves = moves[random.nextInt(moves.length)];
		//Code for Player Move
		String playerMove;
		System.out.print("ENTER YOUR MOVE :");
		playerMove = scanner.nextLine();
		// MOVE VALIDATION (MOVES SHOULD BE R,S,P)
		if(playerMove.equals("r") || playerMove.equals("p") || playerMove.equals("s"))
		{
			System.out.println("PLAYER MOVE IS :" + playerMove);
			System.out.println("COMPUTER MOVE IS :" +computerMoves);
		}
		else {
			System.out.println("Please ENter Valid MOve");
			// BREAK FOR LOOP
			break;
		}
		
		//Game Conditions
		// EQUAL CASE
		if(playerMove.equals(computerMoves))
			System.out.println("Tie");
		
		//Player Win Cases
		else if(playerMove.equals("s") && computerMoves.equals("p"))
			System.out.println("Win");
		
		else if(playerMove.equals("p") && computerMoves.equals("r"))
			System.out.println("Win");
		
		else if(playerMove.equals("r") && computerMoves.equals("s"))
			System.out.println("Win");
		
		//COMPUTER WIN CASES
		
		else if(playerMove.equals("r") && computerMoves.equals("p"))
			System.out.println("Lose");
		
		else if(playerMove.equals("p") && computerMoves.equals("s"))
			System.out.println("Lose");
		
		else if(playerMove.equals("s") && computerMoves.equals("r"))
			System.out.println("Lose");
		System.out.println("ROUND " + round + " COMPLETE");
		} // FOR LOOP END
		System.out.println("DO U WANT TO PLAY AGAIN Y/N");
		yesno = scanner.nextLine();
		} while (yesno.equals("Y")); //END OF DO WHILE
		System.out.println("THANK U GAME COMPLETE!");
		scanner.close(); 
		
	}
	

}
