# Undo / Redo Text Input

## Problem Statement
Implement an input field with undo and redo functionality.

Users should be able to revert and reapply changes in the order they were made.

--- 

## Pattern
**Stack (LIFO)**

---

## Sample Data / Interaction History

```text
Initial State: ""
User types: "H"
User types: "He"
User types: "Hel
Undo -> "He"
Undo -> "H"
Redo -> "He"
```

---

Internally this can be modeled as:
- Undo stack: `["", "H", "He"]`
- Redo stack: `["Hel"]`

## Frontend Concepts Tested
- History Management
- Immutable state updates
- Controlled Inputs

--- 

## Edge Cases
- Undo with no history
- Redo with no future state
- Rapid consecutive changes

--- 

## Interview Talking Points
- Why stacks are a natural fit for undo/redo
- Managing two stacks vs a history pointer
- Real world examples (editors, form inputs)

