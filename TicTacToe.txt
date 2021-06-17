package Testing;

import java.util.Scanner;

public class tictactoe {
	public static void main(String[] args) {
		char[] pos= {' ',' ',' ',' ',' ',' ',' ',' ',' '};
		Scanner scanner = new Scanner(System.in);
		int n;
		int currentTurn = 1;
		char turn ='X';
		System.out.println("\t~~  Welcome to Tic Tac Toe  ~~\n\t Here is the sample 3X3 Tic Tac Toe board with position.\n");
		System.out.println("\t 1 | 2 | 3 \n\t---+---+---\n\t 4 | 5 | 6 \n \t---+---+---\n\t 7 | 8 | 9 \n");
		while(true) {
			do {
		System.out.print("\tEnter a position : ");
		n = scanner.nextInt();
		}while(pos[n-1] == 'X' || pos[n-1] == 'O');
		pos[n-1] = turn;
		
		System.out.println("\n\t "+pos[0]+" | "+pos[1]+ " | "+pos[2]+" ");
		System.out.println("\t---+---+---");
		System.out.println("\t "+pos[3]+" | "+pos[4]+ " | "+pos[5]+" ");
		System.out.println("\t---+---+---");
		System.out.println("\t "+pos[6]+" | "+pos[7]+ " | "+pos[8]+" ");
		
		if(pos[6] == turn && pos[7] == turn&& pos[8]==turn 
		|| pos[3] == turn && pos[4] == turn&& pos[5]==turn
		||pos[0] == turn && pos[1] == turn&& pos[2]==turn
		||pos[0] == turn && pos[3] == turn&& pos[6]==turn
		||pos[1] == turn && pos[4] == turn&& pos[7]==turn
		||pos[0] == turn && pos[4] == turn&& pos[8]==turn
		||pos[6] == turn && pos[4] == turn&& pos[2]==turn) {
			System.out.println("\tCONGRATULATIONS!!  " +turn + " is the Winner");
			break;
			
		}
		if(turn=='X') {
			turn='O';
			
		}
		else {
			turn = 'X';
		}
		if(currentTurn>9) {
			System.out.println("\tTIE\n \tWould you like to break tie? Play Again!");
			break;
		}
		}
	}

}
