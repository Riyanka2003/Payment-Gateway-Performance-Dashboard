# Payment-Gateway-Performance-Dashboard
This project showcases a **real-time performance dashboard** for major payment gateways like **Razorpay**, **PayU**, and **Stripe**, using simulated metrics such as latency, uptime, and transaction success rates.

## 🚀 Tools Used
- **Power BI**
- **Microsoft Excel / Power Query**
- **DAX (Data Analysis Expressions)**

## 📊 Key Features
- Visualized **Uptime**, **Latency**, and **Success Rates** across multiple gateways.
- Simulated real-time performance data for 7 days (hourly).
- Custom DAX KPIs:
  - Total Transactions
  - Success Rate (%)
  - Average Latency (ms)
  - Average Uptime (%)

## 📂 File Structure

📁 Payment-Gateway-Dashboard/
├── PaymentGatewayPerformance.xlsx # Raw data (hourly simulation)
├── PaymentGatewayDashboard.pbix # Power BI Dashboard file (create manually)
├── PaymentGatewayPerformance.csv # Alternate CSV version
└── README.md # Project details

mathematica
Copy
Edit

## 🛠 How to Use
1. Open `PaymentGatewayPerformance.xlsx` or `.csv` in Power BI.
2. Import the data and name the table `PaymentData`.
3. Create DAX measures (see below).
4. Add visuals like cards, charts, and slicers.
5. Explore gateway performance insights!

## 📐 DAX Measures

```DAX
Total Transactions = SUM(PaymentData[Transactions])

Total Success Transactions = SUM(PaymentData[Success Transactions])

Success Rate (%) = 
DIVIDE([Total Success Transactions], [Total Transactions], 0)

Avg Latency (ms) = 
AVERAGE(PaymentData[Latency (ms)])

Avg Uptime (%) = 
AVERAGE(PaymentData[Uptime (%)])
