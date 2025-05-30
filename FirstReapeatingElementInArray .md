package bhuvanasd;

import java.util.HashMap;
import java.util.HashSet;
import java.util.Scanner;

public class FirstReapeatingElementInArray {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n= sc.nextInt();
		int arr[]=new int[n];
		for(int i=0;i<n;i++) {
			arr[i]=sc.nextInt();
		}
        HashSet<Integer> has=new HashSet<>();
        int first=-1;
        for(int i=0;i<n;i++) {
        	
        	if(has.contains(arr[i])) {
        		first=arr[i];
        	}else
        		has.add(arr[i]);
        }
        
	
	if(first!=-1) {
		System.out.print(first);
    	
	}else {
		System.out.print("it does not contains");
	}
	}}
