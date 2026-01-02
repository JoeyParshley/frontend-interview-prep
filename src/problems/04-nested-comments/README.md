# Nested Comment Viewer

## Problem Statement
Render a list of comments where each comment may contain nested replies.

Replies should be displayed recursivly, preserving hierarchy.

--- 

## Pattern
**Trees / Recursion**

---

## Sample Data

```ts
type Comment = {
    id: number;
    text: string;
    replies?: Comment[];
};

const comments: Comment[] = [
  {
    id: 1,
    text: "This is the first comment",
    replies: [
      {
        id: 2,
        text: "Reply to first comment",
        replies: [
          {
            id: 3,
            text: "Nested reply"
          }
        ]
      }
    ]
  },
  {
    id: 4,
    text: "Second top-level comment"
  }
];
```

## Frontend Concepts Tested
- Recursive rendering
- Tree traversal
- Base case handling

---

## Edge Cases
- No comments
- Deeply nested replies
- Single node tree

--- 

## Interview Talking Points
- Why recursion fits tree structures
- Identifying base cases
- Mapping this to DOM and component trees

