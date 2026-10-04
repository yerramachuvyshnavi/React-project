public class MatrixOperations {

    public static void main(String[] args) {

        // 1. Initialization of two 2x2 matrices
        int[][] matrixA = {
            {8, 6},
            {4, 2}
        };

        int[][] matrixB = {
            {4, 2},
            {2, 1}
        };

        int rows = matrixA.length;
        int cols = matrixA[0].length;

        // Arrays to store results
        int[][] sum = new int[rows][cols];
        int[][] sub = new int[rows][cols];
        int[][] mul = new int[rows][cols];
        double[][] div = new double[rows][cols];

        // 2. Addition, Subtraction and Division
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {

                // Addition
                sum[i][j] = matrixA[i][j] + matrixB[i][j];

                // Subtraction
                sub[i][j] = matrixA[i][j] - matrixB[i][j];

                // Element-wise Division
                div[i][j] = (double) matrixA[i][j] / matrixB[i][j];
            }
        }

        // 3. Matrix Multiplication
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {

                mul[i][j] = 0;

                for (int k = 0; k < cols; k++) {
                    mul[i][j] += matrixA[i][k] * matrixB[k][j];
                }
            }
        }

        // 4. Output Results

        System.out.println("=== Matrix A ===");
        printMatrix(matrixA);

        System.out.println("\n=== Matrix B ===");
        printMatrix(matrixB);

        System.out.println("\n=== Addition (A + B) ===");
        printMatrix(sum);

        System.out.println("\n=== Subtraction (A - B) ===");
        printMatrix(sub);

        System.out.println("\n=== Multiplication (A * B) ===");
        printMatrix(mul);

        System.out.println("\n=== Division (Element-wise A / B) ===");
        printDoubleMatrix(div);
    }

    // Method to print integer matrix
    public static void printMatrix(int[][] matrix) {

        for (int[] row : matrix) {
            for (int val : row) {
                System.out.print(val + "\t");
            }
            System.out.println();
        }
    }

    // Method to print double matrix
    public static void printDoubleMatrix(double[][] matrix) {

        for (double[] row : matrix) {
            for (double val : row) {
                System.out.printf("%.2f\t", val);
            }
            System.out.println();
        }
    }
}
