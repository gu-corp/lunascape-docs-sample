---
navigation:
  order: 20
---

# 2.2 Non-functional requirements

| ID | Requirement | Target |
|---|---|---|
| NFR-001 | Sync API response time | Under 300 ms at the 95th percentile |
| NFR-002 | Availability | 99.9% per month |
| NFR-003 | Protection of traffic | TLS 1.3; note bodies encrypted at rest on the server |
| NFR-004 | Notes per user | Performance requirements hold up to 100,000 notes |
