---
navigation:
  order: 10
---

# 4.1 एंडपॉइंट

| मेथड | पथ | उद्देश्य | आवश्यकता |
|---|---|---|---|
| POST | `/notes/push` | नोट का परिवर्तन भेजें | REQ-001, REQ-002 |
| GET | `/notes/pull?since=<version>` | दिए गए संस्करण के बाद के परिवर्तन प्राप्त करें | REQ-001 |
| DELETE | `/notes/{id}` | नोट हटाएँ (ट्रैश में) | REQ-005 |
| POST | `/notes/{id}/restore` | ट्रैश से वापस लाएँ | REQ-005 |
