# nanobot-skill-finance

Nanobot AI skill for expense tracking, budget management, and financial insights.

## Features
- Track expenses and income with categories
- Monthly budget summaries
- Spending breakdown by category
- Balance calculations for any time period
- Multi-currency support (default: TRY)

## Installation

1. Open your Nanobot AI Dashboard
2. Go to **Settings → Skills → Marketplace**
3. Search for "finance"
4. Click **Install**

Or install via API:
```bash
curl -X POST /api/v1/skills/marketplace/install \
  -H "Content-Type: application/json" \
  -d '{"repo": "kombalarasoftware-cmd/nanobot-skill-finance"}'
```

## Tools
| Tool | Description |
|------|-------------|
| `add_expense` | Record a new expense |
| `add_income` | Record income received |
| `get_balance` | Get current balance |
| `list_transactions` | List recent transactions |
| `budget_summary` | Monthly budget overview |
| `spending_by_category` | Spending breakdown |

## License
MIT
