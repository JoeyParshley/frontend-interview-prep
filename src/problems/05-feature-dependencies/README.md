# Feature Dependency Toggle

## Problem Statement
Implement feature toggles where some features depend on others.

A feature should only be enabled if all of its dependencies are enabled.

--- 

## Pattern
**Graphs / DFS**

---

## Sample Data

```ts
const featureDependencies: Record<string, string[]> = {
    auth: [],
    analytics: ["auth"],
    billing: ["auth"],
    reports: ["analytics"],
};
```
---

## Example:
- Enabling `reports` requires:
    - `analytics`
    - `auth`
- Disabling `auth` shoudl disable:
    - `analytics`
    - `billing`
    - `reports`
---
## Frontend Concepts Tested
- Dependency modeling
- Rechability checks
- Defensive state updates

## Edge Cases
- Features with no dependencies
- Shared dependecies
- Disabling a root dependency

--- 

## Interview Talking Points
- Modeling dependencies as a graph
- DFS vs BFS for validation
- Feature flags in feal world systems

