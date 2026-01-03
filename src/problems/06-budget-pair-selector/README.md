# Budget Pair Selector (Two Sum)

## Problem Statement
Build a UI that helps a user find **two expenses** that add up to a given **target budget**.

The user entres a budget value. The app should determine whether **any two distinct expenses** sum to that budget. If a match exists, highlight the matching expenses, and display the pair. If not, show a "No matching pair" message.

You may not use the same expense twice.

---

## Sample Data
```ts
type Expense = {
    id: number;
    label: string;
    amount: number;
}

const EXPENSES: Expense[] = [
    { id: 1, label: "Groceries", amount: 25 },
    { id: 2, label: "Gas", amount: 40 },
    { id: 3, label: "Coffee", amount: 5 },
    { id: 4, label: "Lunch", amount: 15 },
    { id: 5, label: "Snacks", amount: 10 },
]
```

---

## Examples
- Target `30` -> Groceries (25) + Coffee (5) ✅
- Target `50` -> Groceries (40) + Coffee (10) ✅
- Target `99` -> No match ❌

---

## Frontend Concepts Tested
- Controlled Input (Budget Field)
- Derived UI state (match is computed, not stored redundantly)
- Conditional rendering (match vs no match)
- Clean state modeling and edge case handling

---

## Requirements
- Render an input for target budget
- Render a list of expenses
- Find a pair of expenses that sums to a target
- Highlight the matching items
- Display a clean empty/no-match state

---

## Constraints and Assumptions
- Expense list is static for this excercise
- Return the first matching pair
- Performance optimization is optional

---

## Edge Cases
- Empty budget input
- Non-numeric input
- Duplicate amounts (e.g two expenses of $10)
- Multiple valid pairs (choose first match)

---

## Interview Talking Points
- Why this maps to *Two Sum*
- Brute Force O(n<sup>2</sup>) vs hash map O(n)
- why derived state is preferred over storing "match" in multiple places
- How this scales with large lists and frequent typing (memoization/debouncing)
