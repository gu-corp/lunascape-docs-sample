---
navigation:
  order: 20
---

# 3.2 সিঙ্ক্রোনাইজেশনের প্রবাহ

```mermaid
sequenceDiagram
  participant A as ডিভাইস A
  participant S as সিঙ্ক API
  participant B as ডিভাইস B
  A->>S: push(note, baseVersion=4)
  S->>S: সংস্করণ 5 নম্বর দেওয়া হয়
  S-->>A: 200 {version: 5}
  S-->>B: বিজ্ঞপ্তি(note)
  B->>S: pull(note, since=4)
  S-->>B: 200 {version: 5, body}
```

ডিভাইস A-এর পরিবর্তন সার্ভারে একটি নতুন সংস্করণ পায়, আর বিজ্ঞপ্তি পাওয়া ডিভাইস B সেটি নিয়ে আসে। বিজ্ঞপ্তি হলো নিয়ে আসার সংকেত মাত্র, এটি মূল লেখা বহন করে না।
