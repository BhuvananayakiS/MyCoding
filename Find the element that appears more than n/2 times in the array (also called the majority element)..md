import java.util.*;

public class MajorityElement {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();  // Input size
        int[] arr = new int[n];

        // Input elements
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        HashMap<Integer, Integer> freq = new HashMap<>();

        for (int i = 0; i < n; i++) {
            int key = arr[i];
            freq.put(key, freq.getOrDefault(key, 0) + 1);
        }

        for (int key : freq.keySet()) {
            if (freq.get(key) > n / 2) {
                System.out.println("Majority element is: " + key);
                return;
            }
        }

        System.out.println("No majority element");
    }
}
