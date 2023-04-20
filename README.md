# Halloween-party
Alex is attending a Halloween party with his girlfriend, Silvia. At the party, Silvia spots the corner of an infinite chocolate bar (two dimensional, infinitely long in width and length).

If the chocolate can be served only as 1 x 1 sized pieces and Alex can cut the chocolate bar exactly  times, what is the maximum number of chocolate pieces Alex can cut and give Silvia?

Input Format
The first line contains an integer , the number of test cases.  lines follow.
Each line contains an integer .

Output Format
 lines; each line should contain an integer that denotes the maximum number of pieces that can be obtained for each test case.

Constraints



Note: Chocolate must be served in 1 x 1 sized pieces. Alex can't relocate any of the pieces, nor can he place any piece on top of another.

Sample Input #00

4
5
6
7
8
Sample Output #00

6
9
12
16
import java.util.*;

public class Solution {

    private static Scanner in;

    public static void main(String[] args) {
        in = new Scanner(System.in);

        int numberTestCases = in.nextInt();

        start(numberTestCases);

    }

    private static void start(int numberTestCases) {
        in.nextLine();
        StringBuilder result = new StringBuilder();
        for(int i = 0; i < numberTestCases; i++){
            result.append(maxNumberChocolatePieces((long)in.nextInt()));
            result.append("\n");
          //  in.nextLine();
        }
        System.out.print(result);
    }

    protected static long maxNumberChocolatePieces(long i) {
        long pieces = (i/2) * (i-i/2);

        return pieces;
    }
}
