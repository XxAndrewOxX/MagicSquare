# MagicSquare
import java.util.*;


import java.util.*;

public class MagicSquare {
public static final int SIZE = 3;
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner console = new Scanner(System.in);
		int[][] magicSquare = new int[SIZE][SIZE];
		for(int i =0; i<3; i++)
			for(int j =0; j<3; j++){
		System.out.print("what is the row "+i+" column "+j+" value for the table? ");
		magicSquare[i][j]= console.nextInt();
				if(i!=0||j!=0){
					for(int row = 0; row<i+1;row++)
						for(int col =0; col<j+1;col++){
							if(magicSquare[i][j]==magicSquare[row][col]){
						System.out.print("repeat");
						magicSquare[i][j]= console.nextInt();
						row++;						
					
							}
						}
					
					
				}
						}
						
					
		System.out.println(magicSquare[0][0]+" "+magicSquare[0][1] +" "+magicSquare[0][2]);
		System.out.println(magicSquare[1][0]+" "+magicSquare[1][1]+" "+magicSquare[1][2]);
		System.out.println(magicSquare[2][0]+" "+magicSquare[2][1]+" "+magicSquare[2][2]);
	System.out.println(isMagic(magicSquare));	
		
		
	}
	public static boolean isMagic( int[][] magicSquare){
		for(int i =0; i<3; i++)
			for(int j = 0; j<3; j++){
				if(magicSquare[i][0]+magicSquare[i][1]+magicSquare[i][2]!= 15)
					return false;
				if(magicSquare[0][i]+magicSquare[1][i]+magicSquare[2][i]!=15)
					return false;
				if(magicSquare[0][0]+magicSquare[1][1]+magicSquare[2][2]!=15)
					return false;
				if(magicSquare[0][2]+magicSquare[1][1]+magicSquare[2][0]!=15)
					return false;
			}
		return true;
		
	}
	

}
