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
    A1[任務1: 研擬任務<br>開始: 2024-11-01<br>結束: 2024-11-01<br>時長: 1天] --> A2[任務2: 任務分配<br>開始: 2024-11-02<br>結束: 2024-11-05<br>時長: 4天]
    A1 --> A3[任務3: 取得硬體<br>開始: 2024-11-02<br>結束: 2024-11-18<br>時長: 17天]
    A2 --> A4[任務4: 程式開發<br>開始: 2024-11-06<br>結束: 2025-01-15<br>時長: 70天]
    A3 --> A5[任務5: 安裝硬體<br>開始: 2024-11-19<br>結束: 2024-11-28<br>時長: 10天]
    A4 --> A6[任務6: 程式測試<br>開始: 2025-01-16<br>結束: 2025-02-14<br>時長: 30天]
    A5 --> A7[任務7: 撰寫使用手冊<br>開始: 2024-11-29<br>結束: 2024-12-23<br>時長: 25天]
    A5 --> A8[任務8: 轉換檔案<br>開始: 2024-11-29<br>結束: 2024-12-18<br>時長: 20天]
    A6 --> A9[任務9: 系統測試<br>開始: 2025-01-16<br>結束: 2025-02-09<br>時長: 25天]
    A7 --> A10[任務10: 使用者訓練<br>開始: 2024-12-24<br>結束: 2025-01-12<br>時長: 20天]
    A8 --> A10
    A9 --> A11[任務11: 使用者測試<br>開始: 2025-02-10<br>結束: 2025-03-06<br>時長: 25天]
    A10 --> A11
```

## 任務甘特圖
> 將任務表轉換成時間甘特圖
``` mermaid
gantt
    title 任務甘特圖
    dateFormat  YYYY-MM-DD
    section 任務
    研擬任務          :         des1, 2024-11-01, 1d
    任務分配          :         des2, 2024-11-02, 4d
    取得硬體          :         des3, 2024-11-02, 17d
    程式開發          :         des4, 2024-11-06, 70d
    安裝硬體          :         des5, 2024-11-19, 10d
    程式測試          :         des6, 2025-01-15, 30d
    撰寫使用手冊      :         des7, 2024-11-29, 25d
    轉換檔案          :         des8, 2024-11-29, 20d
    系統測試          :         des9, 2025-01-15, 25d
    使用者訓練        :         des10, 2024-12-23, 20d
    使用者測試        :         des11, 2025-02-09, 25d
```

## PERT/CPM 圖 
> 有將關鍵任務透過橘色標記起來
```mermaid
graph TD
    A1[任務1: 研擬任務<br>開始: 2024-11-01<br>結束: 2024-11-01<br>時長: 1天] --> A2[任務2: 任務分配<br>開始: 2024-11-02<br>結束: 2024-11-05<br>時長: 4天]
    A1 --> A3[任務3: 取得硬體<br>開始: 2024-11-02<br>結束: 2024-11-18<br>時長: 17天]
    A2 --> A4[任務4: 程式開發<br>開始: 2024-11-06<br>結束: 2025-01-15<br>時長: 70天]
    A3 --> A5[任務5: 安裝硬體<br>開始: 2024-11-19<br>結束: 2024-11-28<br>時長: 10天]
    A4 --> A6[任務6: 程式測試<br>開始: 2025-01-16<br>結束: 2025-02-14<br>時長: 30天]
    A5 --> A7[任務7: 撰寫使用手冊<br>開始: 2024-11-29<br>結束: 2024-12-23<br>時長: 25天]
    A5 --> A8[任務8: 轉換檔案<br>開始: 2024-11-29<br>結束: 2024-12-18<br>時長: 20天]
    A6 --> A9[任務9: 系統測試<br>開始: 2025-01-16<br>結束: 2025-02-09<br>時長: 25天]
    A7 --> A10[任務10: 使用者訓練<br>開始: 2024-12-24<br>結束: 2025-01-12<br>時長: 20天]
    A8 --> A10
    A9 --> A11[任務11: 使用者測試<br>開始: 2025-02-10<br>結束: 2025-03-06<br>時長: 25天]
    A10 --> A11
    
    %% 標記關鍵任務
    style A1 fill:#f96
    style A2 fill:#f96
    style A4 fill:#f96
    style A6 fill:#f96
    style A9 fill:#f96
    style A11 fill:#f96

```
