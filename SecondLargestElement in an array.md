package bhuvanasd;
import java.util.*;

public class SecondLargestElement {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		int []arr=new int[n];
		for(int i=0;i<n;i++) {
			arr[i]=sc.nextInt();
		}
		int lar=Integer.MIN_VALUE;
		int sec=Integer.MIN_VALUE;
		for(int i=0;i<n;i++) {
			if(arr[i]>lar) {
				sec=lar;
				lar=arr[i];
			}
			else if(arr[i]>sec && arr[i]!=lar) {
				arr[i]=sec;
			}
		}
		if(sec==Integer.MIN_VALUE) {
			System.out.println("There is no second largest element");
		}else {
			System.out.println("The second largest element is :"+sec);
		}
		sc.close();
	}
	

}
