## 實體關係圖（ERD）

```mermaid
erDiagram
    %% 實體定義
    Users {
        int user_id PK "使用者ID"
        string email "信箱(帳號)"
        string password_hash "加密密碼"
        enum role "角色 (Member/Admin)"
        datetime created_at "註冊時間"
    }

    MenuItem {
        int item_id PK "菜單項目ID"
        string name "飲料名稱"
        decimal price "價格 (NT$)"
        boolean is_active "是否在架上販售"
    }

    Orders {
        int order_id PK "訂單編號"
        int user_id FK "顧客ID"
        datetime order_time "訂單時間"
        decimal total_amount "訂單總金額"
        enum status "訂單狀態 (待處理/製作中/已完成/已取消)"
    }

    OrderDetail {
        int detail_id PK "細項ID"
        int order_id FK "訂單ID"
        int item_id FK "菜單項目ID"
        int quantity "購買數量"
    }
    
    %% 修正後的 Customization 實體定義 (將 PK 和 FK 放在單獨的行，避免解析錯誤)
    Customization {
        int detail_id PK "對應的OrderDetail ID"
        int detail_id_fk FK "OrderDetail 外鍵"
        string size "尺寸 (大杯/小杯)"
        string sugar_level "甜度 (全糖/無糖)"
        string ice_level "冰量 (正常/去冰)"
        text notes "備註/客製化需求"
    }

    %% 關係定義
    Users ||--o{ Orders : "下訂單"
    
    Orders ||--|{ OrderDetail : "包含細項"
    MenuItem ||--o{ OrderDetail : "被包含於"
    
    OrderDetail ||--|| Customization : "客製化細節"
