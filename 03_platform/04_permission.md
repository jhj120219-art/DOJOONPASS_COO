# 04_permission.md

> Version: 1.1
> Status: Draft
> Owner: CTO
> Category: Platform

---

# 1. Purpose

본 문서는 Company Operating System에서 사용하는 Permission의 기준을 정의한다.

Permission은 사용자, 시스템 및 AI Agent가
허용된 데이터와 기능에만 접근할 수 있도록 관리하는 접근 제어 체계이다.

모든 접근은 본 문서의 권한 원칙을 따른다.

---

# 2. Objectives

Permission의 목표는 다음과 같다.

* 권한 없는 접근을 차단한다.
* 필요한 범위의 권한만 부여한다.
* 사람과 AI의 접근을 동일한 기준으로 관리한다.
* Company Intelligence의 데이터를 보호한다.
* 중요한 접근과 권한 변경을 추적할 수 있도록 한다.
* 회사가 성장해도 동일한 접근 원칙을 유지할 수 있도록 한다.

---

# 3. Permission Subjects

Permission은 다음 접근 주체에 적용한다.

```text
Human

System

AI Agent
```

사람뿐 아니라 시스템과 AI Agent도 독립적인 접근 주체로 관리할 수 있어야 한다.

AI라는 이유로 회사 데이터 전체에 자동 접근할 수 있는 권한을 부여하지 않는다.

---

# 4. Permission Resources

Permission은 다음 Resource에 적용할 수 있다.

```text
Database

Storage

API

Company Intelligence

System Function

AI Function
```

각 Resource는 필요한 접근 권한을 가진다.

모든 Resource에 동일한 권한 구조를 강제로 적용하지 않는다.

Resource의 중요도와 사용 목적에 따라 필요한 권한을 설정한다.

---

# 5. Permission Structure

기본 권한 구조는 다음과 같다.

```text
Subject

↓

Role

↓

Permission

↓

Resource
```

Subject는 역할과 권한을 통해 Resource에 접근한다.

현재 1인 기업 단계에서는 구조를 단순하게 운영할 수 있다.

회사가 성장하거나 AI Agent가 증가해도
기본 권한 원칙은 동일하게 유지한다.

---

# 6. Permission Types

기본 Permission Type은 다음과 같다.

| Type    | Description       |
| ------- | ----------------- |
| Read    | 조회                |
| Create  | 생성                |
| Update  | 수정                |
| Delete  | 삭제                |
| Execute | 기능 또는 작업 실행       |
| Manage  | 권한 또는 Resource 관리 |

필요한 Resource에 필요한 Permission만 부여한다.

---

# 7. Least Privilege

모든 권한은 최소 권한 원칙을 따른다.

```text
필요한 주체에게

↓

필요한 Resource만

↓

필요한 권한만
```

업무 수행에 필요하지 않은 접근 권한은 부여하지 않는다.

관리 편의를 이유로 과도한 권한을 기본값으로 사용하지 않는다.

---

# 8. Default Access

기본 접근 정책은 허용이 아니라 제한을 우선한다.

권한이 명확하지 않은 Resource에 대해
자동으로 접근을 허용하지 않는다.

새로운 사용자, 시스템 또는 AI Agent가 추가되면
필요한 접근 범위를 확인한 후 권한을 부여한다.

---

# 9. Human Permission

사람의 권한은 역할과 책임을 기준으로 관리한다.

예를 들어

```text
CEO

COO

CTO

CMO
```

등의 역할에 따라 필요한 Resource 접근 범위가 달라질 수 있다.

1인 기업 단계에서는 한 사람이 여러 역할을 수행할 수 있으므로
실제 운영에서는 동일한 사용자가 여러 권한을 가질 수 있다.

역할 구분은 향후 조직 확장을 위해 유지한다.

---

# 10. AI Agent Permission

AI Agent도 독립적인 접근 주체로 취급한다.

각 Agent는 자신의 업무 수행에 필요한 Resource만 사용할 수 있어야 한다.

기본 구조는 다음과 같다.

```text
AI Agent

↓

Assigned Task

↓

Required Permission

↓

Allowed Resource
```

AI Agent는 권한이 없는 데이터나 기능에 접근해서는 안 된다.

AI Agent가 다른 Agent보다 더 많은 권한을 필요로 하는 경우에도
업무 목적에 필요한 범위만 허용한다.

---

# 11. Company Intelligence Access

Company Intelligence에는 회사의 중요한 운영 데이터와 지식이 축적된다.

따라서 Company Intelligence 전체에 대한 무제한 접근을 기본값으로 사용하지 않는다.

접근은 다음 기준을 고려한다.

```text
Role

Task

Data Scope

Permission
```

예를 들어 특정 업무를 수행하는 AI Agent는
해당 업무에 필요한 Company Intelligence 데이터만 사용할 수 있어야 한다.

Company Intelligence가 향후 Company AI의 Data Hub로 발전하더라도
Permission 원칙은 동일하게 유지한다.

---

# 12. Read and Write Separation

데이터를 읽는 권한과 변경하는 권한은 구분한다.

```text
Read
≠
Update
≠
Delete
```

정보를 분석하기 위해 데이터 조회가 필요한 AI Agent에게
자동으로 수정 또는 삭제 권한까지 부여하지 않는다.

특히 회사의 공식 데이터와 지식을 변경하는 권한은
조회 권한보다 엄격하게 관리한다.

---

# 13. AI Output and Official Data

AI가 데이터를 읽을 수 있다는 이유만으로
Company Intelligence의 공식 데이터를 자유롭게 변경할 수 있는 것은 아니다.

기본 원칙은 다음과 같다.

```text
Company Intelligence

↓

AI Read

↓

Analysis / Recommendation

↓

Human Review

↓

Approved Change
```

AI Output은 자동으로 회사의 공식 사실이나 지식이 되지 않는다.

공식 데이터 변경이 필요한 경우
해당 업무의 권한과 승인 기준을 따른다.

---

# 14. Permission Change

권한은 필요에 따라 추가, 변경 또는 제거할 수 있다.

권한 변경 시 다음 사항을 확인한다.

* 접근 주체
* 변경되는 권한
* 대상 Resource
* 변경 목적

불필요한 권한은 유지하지 않는다.

역할이나 업무가 변경되면 관련 권한도 함께 검토한다.

---

# 15. Audit

중요한 접근과 권한 변경은 추적 가능해야 한다.

필요한 Audit 정보는 다음과 같다.

```text
Subject

Action

Resource

Result

Timestamp
```

특히 다음 활동은 필요한 경우 기록한다.

* 권한 변경
* 중요 데이터 접근
* 중요 데이터 수정
* 중요 데이터 삭제
* AI Agent의 주요 실행

모든 단순 조회를 과도하게 기록하는 것이 목적은 아니다.

보안과 운영 추적에 필요한 활동을 우선한다.

---

# 16. Permission and API

API를 통한 Resource 접근도 Permission을 따른다.

```text
Request

↓

Authentication

↓

Permission Check

↓

Resource Access

↓

Response
```

인증되었다는 이유만으로 모든 Resource에 접근할 수 있는 것은 아니다.

API는 요청 주체가 해당 작업을 수행할 권한이 있는지 확인해야 한다.

API의 세부 기준은 `03_api.md`에서 정의한다.

---

# 17. Permission and AI Engines

AI Engine과 Agent는 Platform의 Permission을 우회하지 않는다.

```text
AI Engine / Agent

↓

Permission

↓

API / Resource

↓

Company Intelligence
```

AI가 사용하는 데이터와 기능도
일반 시스템과 동일한 접근 제어 원칙을 따른다.

AI Engine의 세부 구조는 `04_engines/`에서 정의한다.

---

# 18. Permission Principles

모든 Permission은 다음 원칙을 따른다.

* 최소 권한을 적용한다.
* 기본 접근은 제한한다.
* 사람과 AI 모두 권한 관리 대상이다.
* Read와 Write 권한을 구분한다.
* 중요한 데이터 변경 권한은 제한한다.
* 권한 변경은 추적 가능해야 한다.
* AI Agent는 Permission을 우회하지 않는다.
* 회사 성장에 따라 권한을 확장하되 기본 원칙은 유지한다.

---

# 19. Implementation Boundary

본 문서는 Permission의 논리적 기준을 정의한다.

다음과 같은 구체적인 구현 방식은 실제 Platform 개발 단계에서 결정한다.

* Authentication Provider
* RBAC 구현 방식
* Token
* Session
* Database Policy
* API Middleware
* Row Level Security

현재 단계에서는 특정 인증 또는 권한 기술에 종속되지 않는다.

---

# 20. Relationship to Other Documents

Permission은 Platform의 접근 제어를 담당한다.

```text
01_database.md
      ↓
02_storage.md
      ↓
03_api.md
      ↓
04_permission.md
      ↓
05_event.md
```

Database와 Storage는 Resource를 관리하고,

API는 Resource에 접근하는 인터페이스를 제공하며,

Permission은 접근 가능 여부를 판단하고,

Event는 필요한 주요 활동과 변경 사항을 기록하고 전달한다.

AI Engine과 Agent 역시 동일한 Permission 기준을 따른다.

---

# 21. Summary

Permission은 Company Operating System의 접근 제어 기준이다.

접근 주체는

```text
Human

System

AI Agent
```

모두 포함한다.

모든 접근은

```text
누가

↓

어떤 업무를 위해

↓

어떤 Resource에

↓

어떤 권한으로 접근하는가
```

를 기준으로 관리한다.

특히 Company Intelligence와 AI Agent가 확장되더라도
최소 권한과 추적 가능성을 유지하여 회사의 데이터와 시스템을 보호한다.
