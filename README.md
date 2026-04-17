# 🚢 SQL Practice with Titanic Dataset 📊

> **SQLite와 Pandas를 활용한 SQL 기초 실습 프로젝트입니다.**
> 구글 코랩(Google Colab) 환경에서 타이타닉 승객 데이터를 데이터베이스화하고, 다양한 쿼리를 통해 데이터를 분석하는 연습을 진행했습니다.

---

## 🛠 Tech Stack
<div align=left>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white">
  <img src="https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white">
</div>

---

## 🚀 Key Features

### 1. SQL-Python Bridge 🌉
기존의 복잡한 연결 방식 대신, 파이썬의 `sqlite3`와 `pandas`를 결합하여 SQL 쿼리 결과를 즉시 **DataFrame**으로 확인할 수 있는 효율적인 환경을 구축했습니다.

```python
def sql(query):
    """SQL 쿼리를 실행하고 결과를 DataFrame으로 반환하는 마법의 함수"""
    result = pd.read_sql(query, conn)
    return result
```

### 2. Database Schema
- **passengers**: 타이타닉 승객 정보 (PassengerId, Survived, Pclass, Name, Sex, Age 등)
- **products**: 상품 관리 테이블 연습
- **employees**: 직원 정보 관리 및 DEFAULT 제약조건 연습

---

## 🔍 SQL Practice Highlights

실습에서 다룬 주요 SQL 문법들입니다:

### ✅ Data Exploration
```sql
-- 모든 테이블 목록 확인
SELECT name FROM sqlite_master WHERE type='table';

-- 상위 5개 데이터 조회
SELECT * FROM passengers LIMIT 5;
```

### ✅ Basic Queries
- **Filtering**: `WHERE Pclass = 1` (1등석 승객 필터링)
- **Aggregations**: `COUNT(*)` (총 승객 수 계산)
- **Aliasing**: `AS`를 활용한 컬럼명 한글화 (`Name AS 이름`)
- **Uniqueness**: `DISTINCT`를 이용한 중복 제거 (승선항 확인)

### ✅ DDL (Data Definition Language)
- `CREATE TABLE`을 활용한 테이블 구조 설계 및 데이터 타입(TEXT, INTEGER), 제약조건(DEFAULT) 활용 연습.

---

## 📈 실습을 통해 배운 점
- CSV 데이터를 관계형 데이터베이스(RDB) 테이블로 변환하는 워크플로우를 익혔습니다.
- Pandas의 `to_sql`과 `read_sql`을 활용한 효율적인 데이터 처리 방법을 학습했습니다.
- 실제 데이터셋을 대상으로 `WHERE`, `LIMIT`, `COUNT` 등 필수 SQL 구문을 응용해 보았습니다.

---

## 🏃‍♂️ How to Run
1. `sql.ipynb` 파일을 Jupyter Notebook 또는 VS Code에서 엽니다.
2. `titanic_train.csv` 데이터 경로를 설정합니다.
3. 셀을 순서대로 실행하여 `titanic.db`를 생성하고 쿼리 실습을 진행합니다.

---
**Author: 오정협**
