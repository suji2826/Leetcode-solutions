class Solution {
    private void helper(int[]guard,int[][]matrix){
        int m=matrix.length;
        int n=matrix[0].length;
        int x=guard[0];
        int y=guard[1];
        for(int i=x-1;i>=0;i--){
            if(matrix[i][y]==1||matrix[i][y]==2)break;
            if(matrix[i][y]==0)matrix[i][y]=3;
        }
        for(int i=x+1;i<m;i++){
            if(matrix[i][y]==1||matrix[i][y]==2)break;
            if(matrix[i][y]==0)matrix[i][y]=3;
        }
        for(int j=y-1;j>=0;j--){
            if(matrix[x][j]==1||matrix[x][j]==2)break;
            if(matrix[x][j]==0)matrix[x][j]=3;
        }
        for(int j=y+1;j<n;j++){
            if(matrix[x][j]==1||matrix[x][j]==2)break;
            if(matrix[x][j]==0)matrix[x][j]=3;
        }
    }
    public int countUnguarded(int m, int n, int[][] guards, int[][] walls) {
        int [][] matrix=new int[m][n];
        for(int []guard : guards){
            int x=guard[0];
            int y=guard[1];
            matrix[x][y]=1;
        }
        for(int []wall : walls){
            int x=wall[0];
            int y=wall[1];
            matrix[x][y]=2;
        }
        for(int []guard : guards){
            helper(guard,matrix);
        }

        int count=0;
        for (int i=0;i<m;i++) {
            for (int j=0;j<n;j++) {
                if (matrix[i][j]==0)count++;
            }
        }
        return count;
    }
}
