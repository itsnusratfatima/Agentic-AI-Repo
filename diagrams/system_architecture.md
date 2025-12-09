# System Architecture – Auto-Categorization Agent

```
                ┌────────────────────────┐
                │     Transaction Feed    │
                └───────────┬────────────┘
                            │
                            ▼
                 ┌──────────────────┐
                 │  Preprocessing    │
                 └─────┬────────────┘
                       │
                       ▼
           ┌────────────────────────────┐
           │  LLM Classification Agent  │
           └───────┬───────────┬───────┘
                   │           │
                   ▼           ▼
       ┌────────────────┐   ┌───────────────┐
       │ Rules Engine    │   │ Feedback Loop │
       └───────┬────────┘   └──────┬────────┘
               │                  │
               ▼                  ▼
      ┌────────────────────┐   ┌────────────────┐
      │ Final Category      │   │ Model Retrain  │
      └────────────────────┘   └────────────────┘
```

Key points:
- Classification + rules = hybrid accuracy
- Feedback loop learns from corrections
