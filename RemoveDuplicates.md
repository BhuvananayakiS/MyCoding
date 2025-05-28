package bhuvanasd;

import java.util.HashSet;
import java.util.Scanner;

public class RemoveDuplicates {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		int arr[]=new int[n];
		for(int i=0;i<n;i++) {
			arr[i]=sc.nextInt();
		}
		HashSet<Integer> hs=new HashSet<>();
		for(int i=0;i<n;i++) {
		hs.add(arr[i]);
		}
		for(int num:hs){
			System.out.print(num);
		}
		

	}

}
