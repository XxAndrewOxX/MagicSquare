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
		
		
		int[] arr = new int[magicSquare.length * magicSquare.length];
		  for(int k = 0; k < magicSquare.length; k ++)
		  {
		    for(int s = 0; s < magicSquare.length; s ++)
		    {
		      arr[(k * magicSquare.length) + s] = magicSquare[k][s];
		    }
		  }
		  
		  for(int w =0; w <(i*3+j); w++)
			  if(arr[w]==magicSquare[i][j]){
				  System.out.println("repeat");
				  magicSquare[i][j]= console.nextInt();
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
