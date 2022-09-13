import java.util.Scanner;

public class Converter {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println( "What is Bitcoin price today?");

        float inPutcourse = scanner.nextFloat();

        if (inPutcourse <0) {
            System.out.println("Invalid");
        } else
            System.out.println("How much $ do you have?");

        float inputDollars= scanner.nextFloat();

        if (inputDollars <0) {
            System.out.println("Invalid");
        } else
        System.out.println( "You can buy " + getBitcoin(inPutcourse, inputDollars) + " BTC");

    }
    public static float getBitcoin (float bitCoinCuorse, float dollar) {

        if (dollar < 0 || bitCoinCuorse <0 ) {
            System.out.println( "Invalid");
            return 0;
        } else {
            float bitCoin = dollar/bitCoinCuorse ;
            return bitCoin;
        }
    }
}
