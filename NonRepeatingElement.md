import java.util.*;
import java.util.HashMap;
import java.util.Scanner;

public class Main
{
	public static void main(String[] args) {
		  Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        HashMap<Integer,Integer> has=new HashMap<>();
      
        for(int i=0;i<n;i++){
              int key=arr[i];
            if(has.containsKey(key)){
                has.put(key,has.get(key)+1);
            }else{
                has.put(key,1);
            }
        }
        for(int i=0;i<n;i++){
            if(has.get(arr[i])==1){
                System.out.print("The non repeated element is "+arr[i]);
                return;
            }
	}
                System.out.print("no non repeating element");
            
	}
}
