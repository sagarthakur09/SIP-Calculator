# SIP Calculator (Java)

This is a simple Java program that calculates the final amount of a SIP (Systematic Investment Plan) investment.  A SIP is a popular investment strategy where a fixed amount of money is invested at regular intervals (usually monthly) over a long period.  This approach helps in rupee cost averaging and benefits from the power of compounding.

## How it Works

The calculator uses the following formula (simplified for monthly contributions):
FV = P * [((1 + r)^n - 1) / r] * (1 + r)

Where:

*   `FV` = Future Value (the final amount you'll have)
*   `P` = Periodic Investment (the amount you invest each month)
*   `r` = Periodic Interest Rate (annual rate divided by the number of periods per year, in this case, monthly)
*   `n` = Number of Periods (the total number of investment periods, in months)

The Java code calculates the future value using a loop to simulate the monthly investments and compounding.
