package bhuvanasd;
import java.util.Scanner;

import java.util.*;
public class RotateTheArrayToTheRightBy_K_Steps {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n= sc.nextInt();
		int arr[]=new int[n];
		for(int i=0;i<n;i++) {
			arr[i]=sc.nextInt();
		}
		//to rotate the array
		// 1)get the k value
		int k=sc.nextInt();
		k=k%n;//it gives the rotate times and it also manage the k>n also
		rotate(arr,0,n-1);
		rotate(arr,0,k-1);
		rotate(arr,k,n-1);
		for(int num:arr) {
		System.out.print(num+" ");
		}
		
	}
	private static void rotate(int[] arr, int first, int last) {
		while(first<last) {
		int temp=arr[first];
		arr[first]=arr[last];
		arr[last]=temp;
		first++;
		last--;
		}
		
	}
	
	}
