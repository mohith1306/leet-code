class Solution {
    public int[][] floodFill(int[][] image, int sr, int sc, int color) {
        int m = image.length, n = image[0].length;
        int originalColor = image[sr][sc];
        if (originalColor == color) return image;
        Queue<int[]> queue = new LinkedList<>();
        queue.offer(new int[]{sr, sc});
        image[sr][sc] = color; 
        while (!queue.isEmpty()) {
            int[] coordinates = queue.poll();
            int row = coordinates[0], col = coordinates[1];
            if (row > 0 && image[row - 1][col] == originalColor) {
                queue.offer(new int[]{row - 1, col});
                image[row - 1][col] = color;
            }
            if (row < m - 1 && image[row + 1][col] == originalColor) {
                queue.offer(new int[]{row + 1, col});
                image[row + 1][col] = color;
            }
            if (col > 0 && image[row][col - 1] == originalColor) {
                queue.offer(new int[]{row, col - 1});
                image[row][col - 1] = color;
            }
            if (col < n - 1 && image[row][col + 1] == originalColor) {
                queue.offer(new int[]{row, col + 1});
                image[row][col + 1] = color;
            }
        }
        return image;
    }
}
