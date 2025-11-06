[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/rwJlsS2t)
# HW03 — Word Puzzle: Group Anagrams (Dict Keys)

**Story intro (new theme):**  
You help a **word puzzle club**. They want to group words that are **anagrams** (same letters, different order). Build fast grouping using a **dictionary**.

**Today’s topic focus:** using `dict` effectively with hashable keys.

---

## Technical description
- **Goal:** Implement `group_anagrams(words)` that returns a **dict** mapping a **signature key** to a list of words in **input order**.
- **Signature:** Use `''.join(sorted(word.lower()))` as the key.
- **Inputs:** `words` is a list of strings. Words may have mixed case; treat case-insensitively.
- **Output:** dict where each key is the signature, and each value is the list of original words that match it, **in the order they appear**.
- **Constraints:** Keep it simple. Only letters `a–z` are relevant; ignore other characters (strip them). No external libs.
- **Expected complexity:** For `n` words of avg length `k`, about **O(n · k log k)** (sorting each word).

---

## ESL scaffold — The 8 Steps
**Brief prompts (hw03): Steps 1–3 only**
1. **Read & Understand:** Group words that share the same letters.  
2. **Re-phrase:** Use a dict: key = sorted lowercase letters; value = list of original words.  
3. **Identify I/O/vars:** Input: list of words; Output: dict; Vars: `key`, `bucket`.

**Students handle Steps 4–8.**

---

## Hints
- Build a small helper to clean a word: keep letters only, make lowercase.
- Use `d.get(key, [])` to append into a list.
- Keep original word (not cleaned) in the result to show exact input.

---

## How to run tests locally
```python -m pytest -q```


---

## FAQ
**Q1. Return type?** A dict: signature → list of original words.  
**Q2. Order?** Preserve input order inside each list.  
**Q3. Complexity?** ~O(n · k log k).  
**Q4. Non-letters?** Ignore them when building the signature.  
**Q5. Empty input?** Return `{}`.  
**Q6. Mutate inputs?** Do not change the input list.  
**Q7. Grading?** Pytest autograder; pass all tests.