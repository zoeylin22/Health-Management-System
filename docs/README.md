# 系統分析文件

本資料夾收錄健康管理系統之需求分析、功能規格、非功能規格及資料庫設計相關文件。

---

# 文件導覽

## 需求分析文件

### [需求分析文件（Requirement Analysis）](RequirementAnalysis.md)
說明系統開發背景、問題定義、專案目標、利害關係人及系統範圍。

---

### [功能需求規格書（Functional Requirements）](FunctionalRequirements.md)
說明系統應具備之功能需求，包括：
* 會員註冊
* 會員登入
* 健康紀錄管理
* BMI 計算
* 運動紀錄管理
* 健康目標管理
* 健康分析

---

### [非功能需求規格書（Non-Functional Requirements）](NonFunctionalRequirements.md)
說明系統品質需求，包括：
* 系統效能
* 系統安全性
* 系統可靠性
* 系統可維護性
* 系統擴充性

---

## 資料庫設計文件

### [資料字典（Data Dictionary）](DataDictionary.md)
說明資料表設計、欄位定義、資料型態、主鍵與外鍵關聯。
包含資料表：
* USER
* HEALTH_RECORD
* EXERCISE_RECORD
* HEALTH_GOAL

---

# 文件架構

```text
docs/
├── RequirementAnalysis.md
├── FunctionalRequirements.md
├── NonFunctionalRequirements.md
└── DataDictionary.md
```
