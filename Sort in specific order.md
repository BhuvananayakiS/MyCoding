import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		int arr[]=new int [n];
		for(int i=0;i<n;i++){
		    arr[i]=sc.nextInt();
		    
		}
		List<Integer> odd=new ArrayList<>();
		List<Integer>even=new ArrayList<>();
		for(int num:arr){
		    if(num%2!=0){
		    odd.add(num);
		}
		    else{
		        even.add(num);
		    }
		}
		odd.sort(Collections.reverseOrder());
		Collections.sort(even);
		int i=0;
		for(int od:odd){
		    arr[i++]=od;
		}
			for(int eve:even){
		    arr[i++]=eve;
		}
		System.out.println(Arrays.toString(arr));
	    
	}
}
