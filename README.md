# Array


REVERSE 2D ARRAY

INPUT:
image={{1,1,0},
{1,0,2},
{0,0,0}}


output:
0 1 1 
2 0 1 
0 0 0


import java.util.*;
import java.lang.*;

public class YourClassNameHere {
    public static void main(String[] args) {
        
       int[][]image = {{1,1,0},{1,0,2},{0,0,0}};

       int n=image.length;        
       int[][] ans=new int[n][];
        for(int i=0;i<n;i++){
            int s=0;
            int e=n-1;
            
            while(s<e){
                int temp=image[i][s];
                image[i][s]=image[i][e];
                image[i][e]=temp;
                s++;
                e--;
            }
        }
        for(int row=0;row<n;row++){
            for(int col=0;col<image[row].length;col++){
                  System.out.print(image[row][col]+" ");
            }
            System.out.println();
        }
    
    }
}





INPUT:
image={{1,1,0},
{1,0,2},
{0,0,0}}

output:

0 0 0 
1 0 2 
1 1 0





import java.util.*;
import java.lang.*;

public class YourClassNameHere {
    public static void main(String[] args) {
        
       int[][]image = {{1,1,0},{1,0,2},{0,0,0}};

       int n=image.length;        
       int[][] ans=new int[n][];
        for(int i=0;i<n;i++){
            int s=0;
            int e=n-1;
            
            while(s<e){
             
                int temp=image[s][i];
                image[s][i]=image[e][i];
                image[e][i]=temp;
                s++;
                e--;
            }
        }
        for(int row=0;row<n;row++){
            for(int col=0;col<image[row].length;col++){
                  System.out.print(image[row][col]+" ");
            }
            System.out.println();
        }
    
    }
}
