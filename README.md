Loan Ledger — EMI Calculator

A clean, browser-based EMI calculator that shows the full repayment picture — not just one number.

Live Demo: https://emi-calculator-hazel-ten.vercel.app
GitHub: https://github.com/shivayaaa12/-emi-calculator

Built for the Digital Heroes developer trial task.

Why I Built This

Most EMI calculators I've used only show the monthly payment. They never show how much of that payment is interest vs. principal, or how much paying extra each month would actually save. This tool fixes that.

Features


Instant EMI calculation from loan amount, interest rate, and tenure
Principal vs. interest breakdown shown as a donut chart
Full month-by-month repayment ledger (amortization table)
"Extra payment" mode — shows exact interest and time saved by paying more
Three color themes: Dark, Light, Blue
Fully responsive, works on mobile


Tech Stack

Plain HTML, CSS, and JavaScript — no frameworks, no build step, no backend. Everything runs client-side in the browser.

How It Works

EMI is calculated using the standard reducing-balance formula:

EMI = P × r × (1 + r)^n / ((1 + r)^n − 1)

where P is the loan amount, r is the monthly interest rate, and n is the tenure in months. The repayment ledger recalculates this month by month, reducing the balance each time — and applying any extra payment directly to the principal.

Running It Locally

No setup needed — it's a single static file.


Clone or download this repo
Open index.html directly in any browser


Built For

This project was built as part of the Digital Heroes developer trial task — a free, no-cost challenge to design, build, and deploy a genuinely useful tool.
