# FinWise AI – Requirements

## A. User Profile

### Information to collect
- Monthly Income
- Monthly Expenses
- Savings
- Goals
- Loans/EMI

### Compulsory fields
- Name
- Monthly income
- Current savings
- Monthly budget (optional)
- Existing loan/EMI details (optional)

## B. Expense Entry

### Information to save
- Description — what was purchased?
- Date
- Amount
- Category
- Payment method (optional) — cash, UPI, card, etc.

### Initial expense categories
- Food
- Transport
- Other

## C. Monthly Dashboard

### Important numbers to display
- Total balance
- Total Income
- Total Expense
- Savings
- Earning Bar graph
- Expenses by category wagon wheel
- Recent Transactions
- Goals battery percentage graph

## D. Goal Calculator

### Information required
- Goal amount
- Savings Amount

### If the user has no money left after expenses and EMI
- Tell the user to reduce expenses and shows the negative savings
- The user first have to reduce the loss to start savings

## E. Expense Tracking Rules

### Monthly expense estimate
- Used as an initial estimate during profile setup.

### Actual transactions
- Used to calculate the user's real spending.

### How to prevent double counting
- Keep the estimate separate from actual transactions.
- Once transactions are added, calculate actual spending from those transactions only.
- Never add the estimate to the transaction total.

## F. Database Design

### Collections
- users: stores user account information
- transactions: stores individual transactions
- goals: stores each user's financial goals
- loans: stores loan and EMI information

### Rules
- Each user has a unique user ID.
- Each transaction belongs to one user.
- Each transaction is stored as a separate document.
- Goals and loans are linked to the user ID.

## G. EMI Handling

- Ask whether EMI is already included in monthly expenses.
- If included, do not subtract it again.
- If separate, subtract EMI from available balance.
- Allow users to update their EMI information.
