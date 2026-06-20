Loan Ledger — EMI Calculator

A clean, browser-based EMI calculator that shows the full repayment picture — not just one number.

Live Demo: https://emi-calculator-hazel-ten.vercel.app
GitHub: https://github.com/shivayaaa12/-emi-calculator

Built for the Digital Heroes developer trial task.


Why I Built This

Most EMI calculators I've used — including the ones on bank websites — only show you the monthly payment. They don't show how much of that payment goes toward interest versus your actual loan, and almost none of them let you see what happens if you pay a little extra each month. Those are the two questions I actually want answered before taking a loan, so I built a calculator that answers both, in one clean page, for free.

Features

Core calculation


Enter loan amount, annual interest rate, and tenure (in years)
Monthly EMI is calculated instantly using the standard reducing-balance formula
Updates live as you type — no "Calculate" button needed


Visual breakdown


A donut chart shows the split between total principal and total interest paid over the life of the loan
Color-coded consistently across the whole page (gold = principal, rust = interest) so it's easy to read at a glance


Repayment ledger


A full month-by-month amortization table — shows the EMI, principal, interest, and remaining balance for every single month
Scrollable, so long tenures (e.g. 20-year loans) don't overwhelm the page


Extra payment mode


Add an optional extra amount paid every month
The tool recalculates the entire schedule and tells you exactly how much interest you save and how many months early the loan finishes


Theming


Three switchable color themes — Dark, Light, and Blue
All chart colors, text, and table colors adapt automatically


Design Decisions

I designed this around a "bank passbook" feel rather than a generic calculator look — a serif font for the big EMI number (makes it feel like a stamped, official figure), a monospace font for every number in the table (mimics a printed ledger), and a consistent gold/rust color pairing throughout so principal and interest are always visually distinguishable, not just labeled in text.

How It Works

The monthly EMI is calculated with the standard formula:

EMI = P × r × (1 + r)^n / ((1 + r)^n − 1)

where P is the loan principal, r is the monthly interest rate (annual rate ÷ 12 ÷ 100), and n is the tenure in months.

The repayment ledger is built by simulating the loan month by month:


Calculate interest owed on the current balance
Subtract the principal portion of the EMI (and any extra payment) from the balance
Repeat until the balance reaches zero


When an extra payment is added, it's applied directly to the principal each month, which is what allows the loan to close early and reduces total interest paid — the tool calculates both the "normal" and "with extra payment" schedules to show the difference.

Tech Stack

Plain HTML, CSS, and JavaScript — no frameworks, no build step, no backend, no dependencies. Everything runs entirely client-side in the browser. I chose this deliberately: the tool needed to be free to host, fast to load, and simple enough that the logic stays easy to follow in one file.

Project Structure

.
├── index.html   → everything: markup, styles, and calculation logic
└── README.md    → this file

A single file was a deliberate choice for a tool this size — it keeps the project easy to read top to bottom and trivial to deploy on any static host.

Running It Locally

No setup or installation needed.


Clone or download this repo
Open index.html directly in any browser


Possible Future Improvements


Compare two loan offers side by side
Export the repayment ledger as a PDF or CSV
Support for floating vs. fixed interest rate scenarios


Built For

This project was built as part of the Digital Heroes developer trial task — a free, no-cost challenge to design, build, and deploy a genuinely useful tool.
