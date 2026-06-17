# 資料字典（Data Dictionary）

本文件說明健康管理系統各資料表之欄位定義、資料型態與用途。

---

# USER（使用者資料表）

| 欄位名稱       | 資料型態         | 鍵值 | 說明    |
| ---------- | ------------ | -- | ----- |
| user_id    | INT          | PK | 使用者編號 |
| name       | VARCHAR(50)  | -  | 使用者姓名 |
| email      | VARCHAR(100) | -  | 電子郵件  |
| password   | VARCHAR(100) | -  | 使用者密碼 |
| gender     | VARCHAR(10)  | -  | 性別    |
| birth_date | DATE         | -  | 出生日期  |

---

# HEALTH_RECORD（健康紀錄資料表）

| 欄位名稱        | 資料型態  | 鍵值 | 說明     |
| ----------- | ----- | -- | ------ |
| record_id   | INT   | PK | 健康紀錄編號 |
| user_id     | INT   | FK | 使用者編號  |
| height      | FLOAT | -  | 身高（公分） |
| weight      | FLOAT | -  | 體重（公斤） |
| bmi         | FLOAT | -  | BMI 指數 |
| record_date | DATE  | -  | 紀錄日期   |

---

# EXERCISE_RECORD（運動紀錄資料表）

| 欄位名稱          | 資料型態        | 鍵值 | 說明       |
| ------------- | ----------- | -- | -------- |
| exercise_id   | INT         | PK | 運動紀錄編號   |
| user_id       | INT         | FK | 使用者編號    |
| exercise_type | VARCHAR(50) | -  | 運動類型     |
| duration      | INT         | -  | 運動時間（分鐘） |
| calories      | FLOAT       | -  | 消耗熱量     |
| record_date   | DATE        | -  | 紀錄日期     |

---

# HEALTH_GOAL（健康目標資料表）

| 欄位名稱                 | 資料型態  | 鍵值 | 說明     |
| -------------------- | ----- | -- | ------ |
| goal_id              | INT   | PK | 健康目標編號 |
| user_id              | INT   | FK | 使用者編號  |
| target_weight        | FLOAT | -  | 目標體重   |
| weekly_exercise_days | INT   | -  | 每週運動天數 |
| start_date           | DATE  | -  | 目標開始日期 |
| end_date             | DATE  | -  | 目標結束日期 |

---

# 資料表關聯說明

* 一位使用者（USER）可擁有多筆健康紀錄（HEALTH_RECORD）。
* 一位使用者（USER）可擁有多筆運動紀錄（EXERCISE_RECORD）。
* 一位使用者（USER）可設定多個健康目標（HEALTH_GOAL）。

---

# 主鍵與外鍵說明

## 主鍵（Primary Key）

* USER.user_id
* HEALTH_RECORD.record_id
* EXERCISE_RECORD.exercise_id
* HEALTH_GOAL.goal_id

## 外鍵（Foreign Key）

* HEALTH_RECORD.user_id → USER.user_id
* EXERCISE_RECORD.user_id → USER.user_id
* HEALTH_GOAL.user_id → USER.user_id
