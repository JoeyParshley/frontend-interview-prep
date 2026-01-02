# Pagingated Data Table

## Problem Statement
Render a list of items in pages of fixed size.
Proved controls to navigate between pages.

Only the items for the current page should be visible.

--- 

## Pattern
**Two Pointers / Boundary Mangement**

---

## Sample Data

```ts
const ITEMS = [
    "Item 1", "Item 2", "Item 3", "Item 4", "Item 5",
    "Item 6", "Item 7", "Item 8", "Item 9", "Item 10",
    "Item 11", "Item 12"
]

const PAGE_SIZE = 5;
```

---
## Example: 
- Page 1 -> `Item 1` - `Item 5`
- Page 2 -> `Item 6` - `Item 10`
- Page 3 -> `Item 11` - `Item 12`

---

## Frontend Concepts Tested
- Pagination Logic
- Boundary Checks
- Derived UI state
- Off-by-one awareness

## Requirements
- Display a list of users
- Filter users by name based on input value
- Matching should be case insensitive
- Original List should remain unchanged

---

## Edge Cases
- First page (no previous)
- Last page (no next)
- Total items < page size

--- 

## Interview Talking Points
- Calculating state and end indices
- Preventing off-by-one errors
- Pagination vs infinite scroll

