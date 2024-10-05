# 個人作業2: 請在個人的github 新增hw2.md
## 任務表
| 任務 | 說明 | 需時（天數） | 前置任務 |
| -------- | -------- | -------- | -------- |
| 1 | 研擬任務  | 1 | - |
| 2 | 任務分配  | 4 | 1 |
| 3 | 取得硬體  | 17 | 1 |
| 4 | 程式開發  | 70 | 2 |
| 5 | 安裝硬體  | 10 | 3 |
| 6 | 程式測試  | 30 | 4 |
| 7 | 撰寫使用手冊  | 25 | 5 |
| 8 | 轉換檔案  | 20 | 5 |
| 9 | 系統測試  | 25 | 6 |
| 10 | 使用者訓練  | 20 | 7, 8 |
| 11 | 使用者測試  | 25 | 9, 10 |


## 任務 PERT/CPM 圖
> 將 任務表 轉換成 PERT/CPM 圖
``` mermaid
graph TD
    A1[研擬任務] --> A2[任務分配]
    A1 --> A3[取得硬體]
    A2 --> A4[程式開發]
    A3 --> A5[安裝硬體]
    A4 --> A6[程式測試]
    A5 --> A7[撰寫使用手冊]
    A5 --> A8[轉換檔案]
    A6 --> A9[系統測試]
    A7 --> A10[使用者訓練]
    A8 --> A10
    A9 --> A11[使用者測試]
    A10 --> A11
```

## 任務甘特圖
> 將任務表轉換成時間甘特圖
``` mermaid
gantt
    title 專案計劃
    dateFormat  YYYY-MM-DD
    section 任務
    研擬任務          :done,    des1, 2024-10-05, 1d
    任務分配          :active,  des2, after des1, 4d
    取得硬體          :         des3, after des1, 17d
    程式開發          :         des4, after des2, 70d
    安裝硬體          :         des5, after des3, 10d
    程式測試          :         des6, after des4, 30d
    撰寫使用手冊      :         des7, after des5, 25d
    轉換檔案          :         des8, after des5, 20d
    系統測試          :         des9, after des6, 25d
    使用者訓練        :         des10, after des7, 20d
    使用者測試        :         des11, after des9, 25d
```

## PERT/CPM 圖 
> 有將關鍵任務透過橘色標記起來
```mermaid
graph TD
    A1[研擬任務] --> A2[任務分配]
    A1 --> A3[取得硬體]
    A2 --> A4[程式開發]
    A3 --> A5[安裝硬體]
    A4 --> A6[程式測試]
    A5 --> A7[撰寫使用手冊]
    A5 --> A8[轉換檔案]
    A6 --> A9[系統測試]
    A7 --> A10[使用者訓練]
    A8 --> A10
    A9 --> A11[使用者測試]
    A10 --> A11
    
    %% 標記關鍵任務
    style A1 fill:#f96
    style A2 fill:#f96
    style A4 fill:#f96
    style A6 fill:#f96
    style A9 fill:#f96
    style A11 fill:#f96

```
