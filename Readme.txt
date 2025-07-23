
This project analyzes DeFi wallet behavior on the Aave V2 protocol and assigns a credit score (0 to 1000) to each wallet using historical transaction data.
Features Used:
- 'deposit`, `borrow`, `repay`, `redeemunderlying`, `liquidationcall` amounts
- Transaction count
- Ratio of repayments

Files(outputs are saved in):
- 'user-wallet-transactions.json.zip': dataset
- 'wallet_credit_score.py': Scoring logic
- 'wallet_scores.json': Output scores
- 'wallet_scores_classified.csv': Scores + risk category
- Histogram plot of scores

Steps to Run (in Jupyter):
1. Upload the '.zip' file and '.py' script.
2. Import and run each function block from the script.
3. Visualize and export results using 'save_results()' and 'plot_histogram()'.

Credit Score Scale
- 750–1000: Safe
- 500–749: Moderate
- 0–499: Risky
----------------------------------------------------------------------------------------------------------------------------------------------------------------

This project assigns credit scores (0–1000) to wallets based on their DeFi transaction behavior from Aave V2.

What it does:
Reads JSON transaction data

Extracts features like deposits, borrows, repayments, liquidations

Assigns a score per wallet (higher = safer)

Input:
user-wallet-transactions.json.zip (contains raw wallet actions)

Output:
wallet_scores.json – scores for each wallet

wallet_scores_classified.csv – score + risk label (Safe / Moderate / Risky)

How to run:
Place the zip file in your working folder

Run the Jupyter notebook or wallet_credit_score.py

See output files + histogram

