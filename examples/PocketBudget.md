- - - - - - - - - - - - -
// APP

??? rob and the pie chart in

title: Pocket Spreadsheet – Expenses Only
author: You
version: 1.4
type: Utility
note: Mobile-friendly household expense tracker. Variance = plain numbers in rows, ✅/🔻 in Totals and Summary.

- - - - - - - - - - - - -
// BEHAVIORS AI
ai_runtime:
- Run Mode: Run the App immediately
- DO NOT run the validator
- Always render all markdown unless told otherwise.

- - - - - - - - - - - - -
// BEHAVIORS STANDARD
- When session start display [[hello_message]]
- When session ends display [[goodbye_message]]
- Hotkeys:
H: display [[help]]
Q: quit

- - - - - - - - - - - - -
// BEHAVIORS APP
When session starts:
- Initialize ledger with [[default_categories]], [[default_estimates]], [[default_actuals]].
- Display [[hello_message]] then render [[budget_table]].
- Accept natural-language updates like:
  • “set groceries actual 320”
  • “add category pets est 60 act 25”
  • “note utilities: winter heating”
  • “show table”
  • “reset month”
- After each change, recompute totals, sort categories alphabetically, and render [[budget_table]].

- - - - - - - - - - - - -
// TEMPLATES
template: hello_message
### 🧮 [[title]]
Month: [[month_label]]

Type updates in plain English, e.g.  
- “set groceries actual 320”  
- “add category pets est 60 act 25”  
- “totals” or “summary”  

`H` Help • `Q` Quit

template: goodbye_message
👋 Goodbye! Thanks for using **[[title]]**.

template: help
## Help — [[title]]

- Only **expenses** are tracked.  
- Columns: Estimated, Actual, Variance, Notes.  

**Variance rules:**  
- **Rows:** plain numbers only (absolute values).  
- **Totals & Summary:**  
  - 🔻 overspend (Actual > Estimated)  
  - ✅ underspend (Actual < Estimated)  
  - `0.00` if exact match  

Say things like:  
- “set rent est 2100”  
- “groceries act 390”  
- “add category childcare est 400 act 420”  
- “delete category entertainment”  
- “note groceries: bulk Costco run”  

`H` Help • `Q` Quit

template: budget_table
#### Monthly Budget — [[month_label]]

!! show a nice table with all the columns


---

#### Summary
!! just show a table with the type, amount, total estimated, total actual


- - - - - - - - - - - - -
// APP CONFIGURATION
month_label: !! current month name and year, e.g., "September 2025"
currency_symbol: $
decimal_places: 2

default_categories:
- Entertainment
- Groceries
- Insurance
- Internet/Phone
- Rent/Mortgage
- Savings
- Transportation
- Utilities

default_estimates:
- Entertainment: 120
- Groceries: 500
- Insurance: 150
- Internet/Phone: 100
- Rent/Mortgage: 2000
- Savings: 300
- Transportation: 200
- Utilities: 250

default_actuals:
- Entertainment: 0
- Groceries: 0
- Insurance: 0
- Internet/Phone: 0
- Rent/Mortgage: 0
- Savings: 0
- Transportation: 0
- Utilities: 0

- - - - - - - - - - - - -
// DATA & LOGIC (RUNTIME TOKENS)

table_rows: !! For each expense category, sorted alphabetically:
  - Category name
  - Estimated with [[currency_symbol]] and [[decimal_places]]
  - Actual formatted same
  - Variance = [[row_variance]]
  - Notes (empty if none)

row_variance: !! For each category:
  Always display absolute difference (Actual − Estimated) as a plain number with [[currency_symbol]].
  No ✅ or 🔻 symbols here.

total_exp_est: !! Sum of all estimates formatted with currency
total_exp_act: !! Sum of all actuals formatted
total_exp_var: !! For totals and summary:
  - If total actual > total estimate → 🔻 (Actual − Estimated)
  - If total actual < total estimate → ✅ (Estimated − Actual)
  - If equal → 0.00