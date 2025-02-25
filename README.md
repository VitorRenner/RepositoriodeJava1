




public class POO1 {
    public static void main(String[] args) {
        int num1 = 10; // Example start number
        int num2 = 20; // Example end number

        countIntegersAndPrimes(num1, num2);
    }

    public static void countIntegersAndPrimes(int start, int end) {
        int integerCount = 0;
        int primeCount = 0;

        for (int i = start; i <= end; i++) {
            integerCount++;
            if (isPrime(i)) {
                primeCount++;
            }
        }

        System.out.println("Total integers: " + integerCount);
        System.out.println("Total prime numbers: " + primeCount);
    }

    public static boolean isPrime(int number) {
        if (number <= 1) return false;
        for (int i = 2; i <= Math.sqrt(number); i++) {
            if (number % i == 0) return false;
        }
        return true;
    }
}
