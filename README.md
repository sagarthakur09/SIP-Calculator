# SIP-Calculator
sip calculator
import java.util.Scanner;
import java.text.DecimalFormat;
public class sipcal {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        DecimalFormat df = new DecimalFormat("0.00");

        System.out.println("SIP Calculator");

        System.out.print("Monthly Investment (₹): ");
        double monthlyInvestment = scanner.nextDouble();

        System.out.print("Expected Annual Return Rate (%): ");
        double annualReturnRate = scanner.nextDouble();

        System.out.print("Investment Period (Years): ");
        int investmentPeriod = scanner.nextInt();

        // Calculate the total number of months
        int totalMonths = investmentPeriod * 12;

        // Calculate the monthly return rate
        double monthlyReturnRate = (annualReturnRate / 12) / 100;

        double futureValue = 0;

        // Use the future value of annuity formula for SIP calculation
        for (int i = 0; i < totalMonths; i++) {
            futureValue += monthlyInvestment * Math.pow(1 + monthlyReturnRate, i);
        }


        System.out.println("\nResults:");
        System.out.println("----------------------------------");
        System.out.println("Monthly Investment: ₹" + df.format(monthlyInvestment));
        System.out.println("Annual Return Rate: " + df.format(annualReturnRate) + "%");
        System.out.println("Investment Period: " + investmentPeriod + " years");
        System.out.println("----------------------------------");
        System.out.println("Total Investment: ₹" + df.format(monthlyInvestment * totalMonths)); // Added total investment
        System.out.println("Future Value: ₹" + df.format(futureValue));
        System.out.println("Wealth Gained: ₹" + df.format(futureValue - (monthlyInvestment * totalMonths) )); // Added wealth gained


        scanner.close();
    }
}

