---
navigation:
  order: 30
---

# 3. 架構

同步由用戶端、同步 API、儲存區與通知這四個要素構成（[構成要素](components.md)）。變更自裝置傳至伺服器、再由伺服器傳至其他裝置的順序，列於[同步流程](sync-flow.md)。此順序的依據為[版本號](versioning.md)，而同一版本上重複更新時的處理方式，則定於[衝突解決](conflicts.md)。
