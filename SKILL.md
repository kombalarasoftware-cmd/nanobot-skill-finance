# Finance

## Metadata
- **name**: finance
- **version**: 1.0.0
- **author**: kombalarasoftware
- **category**: finance
- **description**: Expense tracking, budget management, and financial insights

## Prompt Extension
You have access to a personal finance tracking system. You can record expenses and income, check balances, and provide spending insights.

When the user mentions spending money, buying something, or receiving payment, offer to record it.
When asked about finances, provide a clear summary with totals.
Always use the user's preferred currency (default: TRY).
Categorize transactions automatically when possible.

## Tools

### add_expense
Record a new expense.

**Parameters:**
- `amount` (number, required): Expense amount (positive number)
- `category` (string, required): Category (food, transport, shopping, bills, health, entertainment, other)
- `description` (string, optional): What the expense was for
- `date` (string, optional): Date in ISO 8601. Defaults to today
- `currency` (string, optional): Currency code (default: TRY)

**Returns:** Transaction object with id, amount, category, date

### add_income
Record income received.

**Parameters:**
- `amount` (number, required): Income amount (positive number)
- `source` (string, required): Income source (salary, freelance, investment, gift, other)
- `description` (string, optional): Description
- `date` (string, optional): Date in ISO 8601. Defaults to today
- `currency` (string, optional): Currency code (default: TRY)

**Returns:** Transaction object

### get_balance
Get current balance (income minus expenses).

**Parameters:**
- `period` (string, optional): Time period - "today", "week", "month", "year", "all" (default: month)
- `currency` (string, optional): Currency code

**Returns:** Object with total_income, total_expenses, net_balance

### list_transactions
List recent transactions.

**Parameters:**
- `limit` (integer, optional): Max results (default: 20)
- `type` (string, optional): Filter by "expense" or "income"
- `category` (string, optional): Filter by category
- `start_date` (string, optional): Start of date range
- `end_date` (string, optional): End of date range

**Returns:** Array of transactions

### budget_summary
Get a monthly budget summary.

**Parameters:**
- `month` (string, optional): Month in YYYY-MM format. Defaults to current month

**Returns:** Object with income, expenses by category, savings rate

### spending_by_category
Get spending breakdown by category.

**Parameters:**
- `period` (string, optional): Time period - "week", "month", "year" (default: month)

**Returns:** Array of objects with category, total, percentage, transaction_count
