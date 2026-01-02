# Filterable User List

## Problem Statement
Render a list of users and allow filtering via a text input.
As the user types, the list should update to show only matching users.

Filtering must be **case-insensitive** and must **not mutate** the original data set.

--- 

## Pattern
**Arrays / Strings**

---

## Sample Data

```ts
type User = {
    id: number;
    name: string;
}

const USERS: User[] = [
    {id: 1, name: "Alice Johnson" },
    {id: 2, name: "Bob Smith" },
    {id: 3, name: "Charlie Brown" },
    {id: 4, name: "Dana White" }
];
```

---
## Example:
- Input: `"bo"`
- Output: `Bob Smith`

## Frontend Concepts Tested
- Controlled inputs
- Array iteration and filtering
- Derived UI state
- String normalization

## Requirements
- Display a list of users
- Filter users by name based on input value
- Matching should be case insensitive
- Original List should remain unchanged

---

## Constraints & Assumptions
- User list is static for this excercise
- No server requests are required
- Performance optimization is optional

## Edge Cases
- Empty input (show all users)
- No Matching users
- Single users
- Input with loading/trailing whitespace

--- 

## Interview Talking Points
- Why filtered results should be derived rather than stored
- Time complexity of filtering (`O(n)`)
- How debouncing would be added in a real app
- How this scaled with large datasets

