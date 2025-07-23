# wallet_credit_score
# Wallet Credit Scoring using DeFi Transactions

This project predicts credit scores (between 0 to 1000) for wallets based on their historical activity on the Aave V2 protocol. The model is developed using Python and processes JSON transaction data.

 Features Extracted
- Total `deposit`, `borrow`, `repay`, `redeemUnderlying`, `liquidationCall` amounts
- Total number of transactions per wallet

 Scoring Logic
The score is computed using weighted sums:
- Positive weight to `deposit` and `repay`
- Negative weight to `borrow` and `liquidationCall`
- Bonus for higher `repay` to transaction ratio

 Risk Classification
- 750–1000: Safe
- 500–749: Moderate
- 0–499: Risky

 Files
- `wallet_credit_score.ipynb`: Full working Jupyter notebook
- `wallet_scores.json`: JSON file with wallet scores
- `wallet_scores_classified.csv`: Wallets with scores and risk category
- `analysis.md`: Visual and behavioral analysis

 How to Run
1. Place your `user-wallet-transactions.json.zip` in the working directory.
2. Open and run the notebook: `wallet_credit_score.ipynb`
3. Outputs will be saved as `.json` and `.csv`, and a histogram will be displayed.

 Visualization
- Histogram of score distribution is included for easy understanding.

