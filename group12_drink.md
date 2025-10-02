### 工作結構分解表
![工作結構分解表](工作結構分解表.png)
### PERT/CPM 圖
![PERT圖](小組關鍵流程圖.png)
##### 關鍵路徑：1 → 2 → 3 → 5 → 6 → 7 → 9 → 10 → 11
### 甘特圖
``` mermaid
gantt
    title 學餐菇蒂飲料訂購
     dateFormat  YYYY-MM-DD
    section 分析與設計
    需求分析與規劃     :done, task1, 2025-10-01, 2d
    設計系統架構       :done, after task1, 4d

    section 系統開發
    資料庫設計         :done, after task2, 5d
    前端UI/UX設計與優化 :after task2, 12d
    會員註冊登入       :after task3, 6d
    開發飲料清單功能   :after task3, 8d
    開發客製化選項功能 :after task_5, 10d
    開發購物車與訂單確認功能 :after task_6, 7d
    
    section 測試與文件
    系統整合測試       :after task4, after task7, after task8, 10d
    使用者測試         :after task9, 5d
    文件統整           :after task10, 2d
```
