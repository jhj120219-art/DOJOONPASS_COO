# 01_data_model.md

> Version: 1.1
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence에서 사용하는 Data Model의 기본 구조와 관리 기준을 정의한다.

Data Model은 회사에서 발생하는 데이터를 일관된 형태로 축적하고,
검색, 분석, 지식화 및 향후 AI 활용이 가능하도록 만드는 기준이다.

Company Intelligence의 모든 데이터는 본 기준을 기반으로 관리한다.

---

# 2. Objectives

Data Model의 목표는 다음과 같다.

* 회사 데이터를 일관된 구조로 관리한다.
* 데이터의 출처를 추적할 수 있도록 한다.
* 데이터의 관리 책임을 명확하게 한다.
* 데이터가 언제 생성되고 변경되었는지 확인할 수 있도록 한다.
* 데이터 간 관계를 연결할 수 있도록 한다.
* 검색과 분석이 가능한 구조를 유지한다.
* 향후 AI가 신뢰할 수 있는 Context를 구성할 수 있도록 한다.

---

# 3. Core Principle

Company Intelligence에서 데이터는 단순한 값으로 저장하지 않는다.

가능한 경우 다음 질문에 답할 수 있어야 한다.

```text
What
무엇에 대한 데이터인가

↓

Source
어디에서 발생했는가

↓

Owner
누가 관리하는가

↓

Time
언제 발생하거나 변경되었는가

↓

Status
현재 유효한 정보인가

↓

Relationship
다른 데이터와 어떻게 연결되는가
```

모든 데이터에 모든 정보를 강제로 적용하지 않는다.

데이터의 중요도와 활용 목적에 따라 필요한 정보를 관리한다.

---

# 4. Core Data Structure

Company Intelligence의 주요 데이터는 다음 구조를 기본으로 한다.

```text
Data ID

Data Type

Content / Value

Source

Owner

Status

Created At

Updated At
```

필요한 경우 데이터 특성에 따라 추가 정보를 사용할 수 있다.

---

# 5. Data ID

관리 대상 데이터는 필요한 경우 고유한 식별자를 가진다.

Data ID는 동일하거나 유사한 데이터가 존재하더라도
각 데이터를 구분하고 추적할 수 있도록 한다.

Data ID는 다음 영역에서 활용할 수 있다.

* 데이터 조회
* 관계 연결
* 변경 추적
* 지식 연결
* AI Context 구성

구체적인 ID 생성 방식은 Platform 구현 단계에서 결정한다.

---

# 6. Data Type

Data Type은 데이터의 의미와 용도를 구분한다.

예를 들어 Company Intelligence에는 다음과 같은 데이터가 존재할 수 있다.

```text
Operation

Project

Issue

Decision

History

KPI

Customer

Market

Product

Document

Insight
```

Data Type은 회사 운영 과정에서 실제로 필요한 범위를 기준으로 정의한다.

현재 필요하지 않은 데이터 유형을 미리 과도하게 만들지 않는다.

---

# 7. Source

Source는 데이터가 어디에서 발생했는지를 나타낸다.

예를 들어 데이터의 Source는 다음과 같을 수 있다.

```text
System

Document

Customer

Project

Analytics

External Source

Human Input

AI Output
```

Source는 데이터의 신뢰성과 활용 가능성을 판단하기 위한 중요한 기준이다.

AI가 생성한 데이터와 실제 운영에서 발생한 데이터를 구분할 수 있어야 한다.

Source가 확인되지 않는 데이터를 중요한 사실이나 의사결정 근거로 사용할 경우 주의해야 한다.

---

# 8. Owner

중요한 데이터는 관리 책임을 가진다.

Owner는 데이터의 정확성, 최신성 및 관리 상태를 책임지는 역할이다.

Owner는 데이터를 직접 생성한 사람과 반드시 동일하지 않다.

예를 들어

```text
Marketing Data
→ CMO

Technology Data
→ CTO

Operations Data
→ COO
```

와 같이 해당 영역을 담당하는 역할이 Owner가 될 수 있다.

1인 기업 단계에서는 동일한 사람이 여러 Owner 역할을 수행할 수 있다.

---

# 9. Time

데이터는 시간 정보를 추적할 수 있어야 한다.

기본 시간 정보는 다음과 같다.

```text
Created At

Updated At
```

필요한 데이터는 실제 사건이나 측정 시점을 별도로 가질 수 있다.

시간 정보는 다음을 판단하는 데 사용한다.

* 데이터가 언제 생성되었는가
* 언제 마지막으로 변경되었는가
* 현재도 유효한 정보인가
* 과거와 현재 데이터를 어떻게 구분할 것인가

AI가 데이터를 활용할 때 오래된 정보를 현재 정보처럼 사용하는 것을 방지할 수 있어야 한다.

---

# 10. Status

필요한 데이터는 현재 상태를 가진다.

Status는 데이터의 성격에 따라 다르게 정의할 수 있다.

예를 들어

```text
Active

Inactive

Archived
```

또는 업무 데이터의 특성에 맞는 상태를 사용할 수 있다.

Status의 목적은 현재 사용해야 하는 데이터와
과거 기록을 구분하는 것이다.

세부 Status 값은 각 데이터 영역에서 필요한 경우 정의한다.

---

# 11. Relationships

회사 데이터는 독립적으로 존재하지 않는다.

데이터는 다른 데이터와 연결될 수 있어야 한다.

예를 들어

```text
Customer
↓
VOC
↓
Product Issue
↓
Decision
↓
Project
↓
Result
```

와 같은 관계를 구성할 수 있다.

Data Model은 이러한 연결이 가능하도록 설계한다.

구체적인 관계 구조는 `02_entity_relationship.md`에서 정의한다.

---

# 12. Facts and AI Output

실제 회사 데이터와 AI가 생성한 결과는 구분한다.

```text
Company Data
= 실제 운영, 시스템, 고객, 문서 등에서 발생한 데이터

AI Output
= AI가 분석, 요약, 추론 또는 생성한 결과
```

AI Output은 자동으로 회사의 공식 사실이 되지 않는다.

AI가 생성한 분석이나 추천은 원본 데이터와 구분하여 관리한다.

필요한 경우 사람이 검토한 후 공식 지식이나 의사결정에 반영한다.

---

# 13. Data Traceability

중요한 데이터는 가능한 범위에서 다음 흐름을 추적할 수 있어야 한다.

```text
Source

↓

Data

↓

Knowledge

↓

Context

↓

AI Analysis / Recommendation

↓

Decision
```

이를 통해 AI 또는 사람이 특정 분석이나 추천이
어떤 데이터에서 시작되었는지 확인할 수 있도록 한다.

모든 데이터에 복잡한 추적 시스템을 적용하는 것이 목적은 아니다.

중요한 회사 정보와 의사결정 근거를 추적 가능하게 만드는 것이 목적이다.

---

# 14. Data Quality

Company Intelligence의 데이터는 다음 기준을 우선한다.

* 정확성
* 최신성
* 일관성
* 출처 확인 가능성
* 중복 최소화
* 관계 추적 가능성

데이터가 많다는 이유만으로 좋은 Company Intelligence가 되는 것은 아니다.

신뢰할 수 있고 활용 가능한 데이터를 축적하는 것을 우선한다.

---

# 15. Single Source of Truth

동일한 사실은 가능한 하나의 원본을 기준으로 관리한다.

동일한 데이터를 여러 위치에서 각각 수정하지 않는다.

다른 시스템이나 문서에서 동일한 데이터가 필요한 경우
가능한 원본을 참조한다.

이를 통해 서로 다른 값이 동시에 존재하는 문제를 최소화한다.

---

# 16. AI Readiness

Data Model은 향후 AI가 회사 데이터를 활용할 수 있도록 설계한다.

AI는 데이터를 사용할 때 가능한 경우 다음 정보를 함께 판단할 수 있어야 한다.

```text
Data

+

Source

+

Time

+

Status

+

Relationship
```

이를 통해 AI가 단순히 데이터를 검색하는 것을 넘어,

* 어떤 정보가 현재 유효한지
* 어떤 정보가 신뢰 가능한지
* 어떤 데이터가 서로 관련되어 있는지
* 어떤 근거를 기반으로 분석했는지

판단할 수 있는 기반을 제공한다.

현재 단계에서는 AI 학습 시스템이나 복잡한 머신러닝 구조를 구현하지 않는다.

AI가 향후 활용하기 좋은 데이터 구조를 만드는 것까지만 본 문서의 범위로 한다.

---

# 17. Relationship to Other Documents

Data Model은 Company Intelligence의 데이터 기반을 정의한다.

```text
01_data_model.md

↓

02_entity_relationship.md

↓

03_knowledge.md

↓

04_search.md

↓

05_rag.md

↓

06_context.md
```

Data Model은 데이터의 기본 구조를 정의하고,

Entity Relationship은 데이터 간 연결을 정의하며,

Knowledge는 연결된 데이터를 재사용 가능한 지식으로 관리하고,

Search와 RAG는 필요한 지식을 검색하며,

Context는 해당 정보를 AI가 사용할 수 있는 형태로 구성한다.

---

# 18. Implementation Boundary

본 문서는 데이터의 논리적 관리 기준을 정의한다.

다음과 같은 실제 구현 방식은 Platform에서 결정한다.

* Database Schema
* Table Structure
* Storage
* Index
* API
* Permission
* Physical Data Type

Company Intelligence는 데이터가 어떤 의미와 관계를 가지는지 정의하고,
Platform은 이를 실제 시스템으로 구현한다.

---

# 19. Summary

Data Model은 Company Intelligence의 데이터 관리 기준이다.

회사 데이터는 단순히 저장하는 것이 아니라,

```text
출처

↓

책임

↓

시간

↓

상태

↓

관계
```

를 필요한 범위에서 추적할 수 있도록 관리한다.

이를 통해 회사의 데이터를 신뢰할 수 있는 지식으로 발전시키고,
향후 Company AI가 분석과 전략 추천에 활용할 수 있는 기반을 구축한다.
