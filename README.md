# Week 4: Metro City Help Center

## Summary
This assignment builds a small support system for Metro City Help Center using stacks and queues. I implemented an `ActionStack` for LIFO-based action tracking, a `RequestQueue` for FIFO-based citizen serving, a bracket validator for help notes, and a function that processes a citizen waiting line in arrival order. The hardest part was making sure the bracket checker correctly matched opening and closing bracket types rather than just counting them.

---

## Complexity

| Function | Time Complexity | Why |
|---|---|---|
| `ActionStack.pop` | O(1) | Python list `.pop()` from the end is constant time |
| `RequestQueue.dequeue` | O(1) | `deque.popleft()` is constant time, unlike removing from the front of a list |
| `is_note_balanced` | O(n) | Each character in the note is visited exactly once |
| `process_request_line` | O(n) | Each citizen is enqueued and dequeued exactly once |

---

## Edge-case checklist

- **Empty action stack:** `pop()` and `peek()` call `is_empty()` first and return `None` instead of raising an error.
- **Empty request queue:** `dequeue()` and `peek()` call `is_empty()` first and return `None` safely.
- **Empty string for `is_note_balanced`:** The loop does not execute and the stack remains empty, so the function correctly returns `True`.
- **Note with no brackets:** All non-bracket characters are skipped entirely, so the function returns `True`.
- **Empty citizen list:** The enqueue loop does not execute and the function returns `[]` as expected.

---

## Assistance & Sources

- Python Documentation (docs.python.org):
  - Help received: Referenced `collections.deque` methods and time complexity of list operations for stack and queue implementation.

- Class lecture notes:
  - Help received: Reviewed LIFO vs FIFO behavior and bracket-matching stack patterns.