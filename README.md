# gitL_IDEA
import java.util.*;

public class Test04 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] nums = new int[n];
        Map<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < n; i++) {
            int cur = scanner.nextInt();
            nums[i] = cur;
            map.put(cur, map.getOrDefault(cur, 0) + 1);
        }

        int maxOperations = 0;

        for (int i = 0; i < n; i++) {
            if (nums[i] == nums[(i + 1) % n]) {
                maxOperations++;
                i++;
            }
        }

        System.out.println(maxOperations);
    }
}
