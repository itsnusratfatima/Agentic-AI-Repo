# Prompt Library – Auto-Categorization Agent

## Base Classification Prompt

```
Given a transaction description, amount, vendor, and history,
categorize into one of the chart-of-accounts categories.

Return:
{
  "category": "...",
  "confidence": 0-100
}
```

---

## Chain of Thought

```
Think step-by-step:
- detect vendor
- detect purpose
- look at similar past entries
- choose top category
```

---

## Correction Learning

```
If user changes a category:
- store feedback
- update model weights
- re-evaluate future similar patterns
```

