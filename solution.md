Una posible solución es llevar un array de visitados con las posiciones que ya fueron visitadas por el robot.


```
import java.io.*;
        import java.util.*;
        import java.text.*;
        import java.math.*;
        import java.util.regex.*;

        public class Solution {
            public static void main(String args[] ) throws Exception {
                Scanner in= new Scanner(System.in);
                String commands= in.nextLine();
                int initialPosition=in.nextInt();
                int totalMovements=1;
                int []visited= new int[commands.length()+1];
                visited[0]= initialPosition;
                boolean repeated=false;
                int currentPosition=1;
                for(int i=0;i<commands.length();i++){
                        if(commands.charAt(i)=='D'){
                            initialPosition++;
                        }else{
                            initialPosition--;
                        }
                        //Me fijo si está visitado
                        for(int j=0;j<visited.length && !repeated;j++){
                            if(visited[j]==initialPosition){
                                repeated=true;
                            }
                        }
                    //Si no está visitado, se suma uno al total de movimientos
                    if(!repeated){
                        totalMovements++;
                        visited[currentPosition++]=initialPosition;
                    }
                    repeated=false;
                    
                }
                System.out.println(totalMovements);
            }
        }
```
