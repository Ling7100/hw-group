### 第12組 組員任務
| 組員   | 角色 | 任務                                                                 | 預估時間 |
|--------|------|--------------------------------------------------------------------------|----------|
| 陳貞伶 | 組長 | GitHub管理、模型設計、時程規劃 | 4-6 週   | 
| 蔡若筠 | 組員 | 分析與報告，視覺設計 | 3-5 週   | 
| 林郁芊 | 組員 | 分析與報告，表單設計 | 3-5 週   |
### 工作結構分解表
![工作結構分解表](工作結構分解表.png)
### PERT/CPM 圖
![PERT圖](小組關鍵流程圖.png)
##### 關鍵路徑：1 → 2 → 3 → 5 → 6 → 7 → 9 → 10 → 11
### 甘特圖
``` mermaid
gantt
    title 學餐菇蒂飲料訂購專案甘特圖
    dateFormat  YYYY-MM-DD
    axisFormat  %m/%d

    section 分析與設計
    需求分析與規劃           :done, task1, 2025-10-01, 2025-10-02
    資料蒐集與彙整           :done, task2, after task1, 4d
    資料視覺設計             :done, task3, after task2, 3d
    開發使用者流程與人力排程 :done, task4, after task2, 5d
    開發線框圖與互動設計     :active, task5, after task3, 10d
    開發視覺設計稿           :active, task6, after task5, 10d

    section UIUX與前端
    開發 UIUX 設計規範       :active, task7, after task6, 5d
    前端開發                 :active, task8, after task6, 15d

    section 測試與驗收
    系統整合測試             :active, task9, after task7, 10d
    使用者測試               :active, task10, after task9, 5d
    文件編寫與驗收           :active, task11, after task10, 5d
```
