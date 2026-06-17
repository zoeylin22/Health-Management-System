# Login Flow

```mermaid
flowchart TD

A[開始] --> B[輸入帳號密碼]
B --> C[驗證帳號密碼]

C --> D{驗證成功?}

D -->|是| E[進入系統首頁]
D -->|否| F[顯示錯誤訊息]

F --> B

E --> G[結束]
```
