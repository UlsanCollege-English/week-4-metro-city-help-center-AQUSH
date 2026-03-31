## Complexity

### `ActionStack.pop`
- Time: O(1)
- Why: Removing the last element from a Python list is constant time because it does not require shifting elements.

---

### `RequestQueue.dequeue`
- Time: O(1)
- Why: `collections.deque.popleft()` removes the first element in constant time without shifting the rest.

---

### `is_note_balanced`
- Time: O(n)
- Why: We iterate through the string once, and each character is processed in constant time using a stack.

---

### `process_request_line`
- Time: O(n)
- Why: Each citizen is added (enqueue) and removed (dequeue) exactly once, so total operations are proportional to n.

---

## Edge-case checklist
- [x] empty action stack  
- [x] empty request queue  
- [x] empty string for `is_note_balanced`  
- [x] note with no brackets  
- [x] empty citizen list  

---

## Assistance & sources
- AI used? (Y)
- What it helped with: Understanding stack and queue implementation, debugging, and explaining time complexity.
- Other sources: Python documentation (collections.deque)