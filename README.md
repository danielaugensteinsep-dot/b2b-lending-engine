# B2B Corporate Loan Engine

A Python-based financial system that evaluates corporate balance sheets, calculates post-transaction risk, and automates loan approval decisions using strict banking rules.

## Project Overview
This project simulates a backend risk-assessment engine for corporate lending. It ingests financial data (Equity, Existing Debt, Fixed Assets, and Requested Loan Amount), projects the company's financial health *after* the loan is applied and uses a tiered decision model to approve, deny, or route the application to a human underwriter.

## Key Features
* **Automated Risk Calculation:** Calculates current equity ratios and projects the new post-loan leverage to prevent over-indebtedness.
* **Dynamic Interest Pricing:** Automatically adjusts the final interest rate by applying a calculated risk penalty based on the company's financial health.
* **Tiered Decision Algorithm:**
  * **Auto-Approval:** Instantly clears micro-loans or companies with highly optimal balance sheets.
  * **Auto-Denial:** Blocks loans that push post transaction leverage above the strict maximum limit (3.0).
  * **Human-in-the-Loop:** Halts the system for borderline risk profiles, requiring a manual executive override (Yes/No).
* **Compliance Audit Trail:** Automatically logs every transaction, including the timestamp, company name, final decision, and system justification, into a secure database.

## Technologies Used
* **Python 3**
* **Standard Libraries:** `time`, `datetime` (No external dependencies required).

## How to Run the Code
1. Open the Python script or Google Colab notebook.
2. Run all cells in order to initialize the system parameters and functions.
3. Run the final execution cell to launch the interactive terminal.
4. Input the requested corporate financial data when prompted.
5. The system will output a detailed analysis report and log the final decision in the audit trail.
