package bhuvanasd;

import java.util.HashMap;
import java.util.Scanner;

public class RepeatedWElement {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		int n= sc.nextInt();
		int arr[]=new int[n];
		for(int i=0;i<n;i++) {
			arr[i]=sc.nextInt();
		}
		HashMap<Integer,Integer> has=new HashMap<>();
		for( int i=0;i<n;i++) {
			int key=arr[i];
			if(has.containsKey(key)) {
				has.put(key,has.get(key)+1);
			}else {
				has.put(key,1);
			}
			
			}
		
	for(int num:has.keySet()) {
		System.out.println(num+"->"+has.get(num)+"times");
	}
}}
