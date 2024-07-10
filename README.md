# intresection-of-two-arrays
class Solution {
    public int[] intersection(int[] nums1, int[] nums2) {
        // Use HashSet to store unique elements of nums1
        Set<Integer> set1 = new HashSet<>();
        for (int num : nums1) {
            set1.add(num);
        }

        // Use HashSet to store the intersection
        Set<Integer> intersection = new HashSet<>();
        for (int num : nums2) {
            if (set1.contains(num)) {
                intersection.add(num);
            }
        }

        // Convert the result set to an array
        int[] result = new int[intersection.size()];
        int index = 0;
        for (int num : intersection) {
            result[index++] = num;
        }

        return result; 
    }
}
