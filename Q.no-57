class Solution {
    public int[][] insert(int[][] intervals, int[] newInterval) {
        int start = -1, end = -1;
        for (int i = 0; i < intervals.length; i++) {
            int opening = intervals[i][0];
            int closing = intervals[i][1];
            if (closing >= newInterval[0] && start == -1) {
                start = i; 
            }
            if (opening > newInterval[1]) {
                end = i;  
                break;
            }
        }
        if (start == -1) {
            start = intervals.length;
        }
        if (end == -1) {
            end = intervals.length;
        }
        int mergedSize = intervals.length - (end - start) + 1;
        int[][] ans = new int[mergedSize][2];
        int index = 0;
        for (int i = 0; i < start; i++) {
            ans[index++] = intervals[i];
        }
        int newStart = newInterval[0];
        int newEnd = newInterval[1];
        for (int i = start; i < end; i++) {
            newStart = Math.min(newStart, intervals[i][0]);
            newEnd = Math.max(newEnd, intervals[i][1]);
        }
        ans[index++] = new int[]{newStart, newEnd};
        for (int i = end; i < intervals.length; i++) {
            ans[index++] = intervals[i];
        }
        return ans;
    }
}
