# 06_context.md

> Version: 1.1
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence에서 AI가 업무를 수행할 때 사용하는 Context의 구성 및 관리 기준을 정의한다.

Context는 Company Intelligence에 축적된 데이터와 지식 중
현재 업무에 필요한 정보를 선택하여 AI가 활용할 수 있는 형태로 제공하는 정보 집합이다.

Context의 목적은 많은 정보를 AI에게 전달하는 것이 아니라,
현재 업무에 필요한 신뢰할 수 있는 정보를 정확하게 제공하는 것이다.

---

# 2. Objectives

Context의 목표는 다음과 같다.

* AI가 현재 업무에 필요한 정보를 사용할 수 있도록 한다.
* 관련 없는 정보의 사용을 최소화한다.
* 데이터의 출처와 시점을 함께 전달한다.
* 현재 정보와 과거 정보를 구분한다.
* 사실과 AI의 분석을 구분한다.
* AI가 근거 기반으로 분석하고 추천할 수 있도록 한다.
* 동일한 회사 데이터를 여러 AI Engine에서 일관되게 활용할 수 있도록 한다.

---

# 3. Context Principle

Context는 단순한 데이터 묶음이 아니다.

AI가 정보를 올바르게 해석할 수 있도록
필요한 의미와 관계를 함께 제공해야 한다.

기본 구조는 다음과 같다.

```text
Task

↓

Relevant Data

↓

Relevant Knowledge

↓

Source & Time

↓

Relationships

↓

Context

↓

AI
```

Context는 현재 Task를 기준으로 구성한다.

---

# 4. Context Components

Context는 업무 목적에 따라 다음 정보를 포함할 수 있다.

```text
Task

Company Data

Knowledge

Decision

KPI

Project

Customer Insight

Market Insight

Product Information

Source

Time

Status
```

모든 Context에 모든 정보를 포함하지 않는다.

현재 업무에 필요한 정보만 선택하여 제공한다.

---

# 5. Task Context

Context는 항상 현재 수행할 업무를 기준으로 구성한다.

예를 들어 AI가 수행하는 업무가

```text
분석

요약

비교

추천

전략 검토
```

중 무엇인지에 따라 필요한 Context가 달라질 수 있다.

Context는 Task와 직접 관련된 정보를 우선한다.

---

# 6. Source Context

중요한 정보는 가능한 경우 Source와 함께 제공한다.

```text
Information

+

Source
```

Source는 해당 정보가 어디에서 발생했는지를 나타낸다.

예를 들어

```text
Company System

Document

Customer

Analytics

External Source

Human Input

AI Output
```

등이 존재할 수 있다.

AI는 Source를 통해 정보의 성격과 신뢰성을 판단할 수 있어야 한다.

---

# 7. Time Context

Context는 필요한 경우 정보의 시간적 의미를 함께 제공한다.

예를 들어

```text
현재 KPI

과거 KPI

현재 고객 의견

과거 고객 의견

현재 시장 정보

과거 시장 정보
```

를 구분할 수 있어야 한다.

중요한 정보는 가능한 경우 다음과 같은 시간 정보를 함께 가진다.

```text
Created At

Updated At

Observed At
```

AI는 오래된 정보를 현재 사실처럼 사용해서는 안 된다.

---

# 8. Status Context

Context에 포함되는 정보가 현재 유효한지 판단할 수 있어야 한다.

예를 들어

```text
Active

Inactive

Archived
```

등의 상태를 활용할 수 있다.

Archived 정보는 과거 분석이나 변화 추적에는 사용할 수 있지만,
현재 회사 상태를 나타내는 정보로 자동 해석해서는 안 된다.

---

# 9. Fact and Interpretation

Context에서는 사실과 해석을 가능한 명확하게 구분한다.

```text
Fact
= 실제 데이터 또는 확인된 정보

Interpretation
= 데이터를 기반으로 한 분석 또는 해석

Recommendation
= 분석을 기반으로 제안된 행동
```

예를 들어

```text
매출 10% 감소
= Fact

신규 고객 감소가 주요 원인으로 보임
= Interpretation

신규 고객 확보 전략을 강화할 필요가 있음
= Recommendation
```

AI가 생성한 Interpretation과 Recommendation은
자동으로 회사의 공식 사실이 되지 않는다.

---

# 10. Decision Context

과거의 중요한 의사결정은 필요한 경우 Context에 포함할 수 있다.

Decision Context는 다음 정보를 포함할 수 있다.

```text
Decision

Reason

Evidence

Result

Time
```

이를 통해 AI가 과거에 어떤 판단을 했는지뿐 아니라,
왜 그런 결정을 했고 결과가 어땠는지 참고할 수 있도록 한다.

과거의 Decision은 현재 상황에 자동 적용하지 않는다.

현재 Context와 비교하여 활용한다.

---

# 11. KPI Context

전략 및 운영 관련 업무에서는 필요한 KPI를 Context에 포함할 수 있다.

KPI는 가능한 경우 단순한 현재 값뿐 아니라
비교 가능한 정보를 함께 제공한다.

```text
Current

Previous

Target
```

이를 통해 AI가 단순한 숫자가 아니라
변화와 목표를 함께 판단할 수 있도록 한다.

---

# 12. Customer and Market Context

고객 및 시장 정보는 필요한 업무에서 Context로 사용할 수 있다.

Customer Context는 다음과 같은 정보를 포함할 수 있다.

```text
VOC

Customer Behavior

Customer Feedback

Customer Insight
```

Market Context는 다음과 같은 정보를 포함할 수 있다.

```text
Market Data

Competitor Information

Trend

External Research
```

외부 시장 정보는 가능한 경우 Source와 시점을 함께 관리한다.

---

# 13. Context Selection

Company Intelligence의 모든 정보를 AI에게 전달하지 않는다.

Context는 현재 업무와 관련성이 높은 정보를 우선 선택한다.

기본 원칙은 다음과 같다.

```text
Relevance

+

Reliability

+

Recency

+

Authority
```

정보량보다 관련성과 신뢰도를 우선한다.

불필요한 Context는 AI의 판단 품질을 낮출 수 있다.

---

# 14. Context and RAG

RAG는 Company Intelligence에서 관련 정보를 검색하는 방법 중 하나이다.

```text
Company Intelligence

↓

Search / RAG

↓

Relevant Information

↓

Context

↓

AI Engine
```

RAG가 검색한 결과 전체가 자동으로 Context가 되는 것은 아니다.

검색 결과 중 현재 업무에 필요한 정보를 선택하여 Context를 구성한다.

RAG의 세부 기준은 `05_rag.md`에서 관리한다.

---

# 15. Context and Memory

Context와 Memory는 서로 다른 역할을 가진다.

```text
Context
= 현재 업무 수행에 필요한 정보

Memory
= AI가 이전 작업이나 상호작용에서 유지하는 정보
```

Company Intelligence는 회사의 공식 데이터와 지식을 관리한다.

Memory는 Company Intelligence를 대체하지 않는다.

AI가 회사의 공식 사실을 판단할 때는
Memory보다 Company Intelligence의 현재 정보를 우선한다.

Memory의 세부 기준은 `04_engines/04_memory.md`에서 정의한다.

---

# 16. Context and AI Engines

AI Engine은 Company Intelligence 전체에 직접 의존하지 않는다.

필요한 정보를 Context 형태로 전달받아 업무를 수행한다.

```text
Company Intelligence

↓

Context

↓

AI Engine

↓

Analysis / Recommendation / Output
```

이를 통해 각 AI Engine이 동일한 회사 데이터와 지식을
일관된 기준으로 활용할 수 있도록 한다.

---

# 17. Evidence Based Context

분석이나 추천에 사용되는 중요한 Context는
가능한 경우 근거를 추적할 수 있어야 한다.

```text
Source

↓

Data

↓

Knowledge

↓

Context

↓

AI Analysis

↓

Recommendation
```

AI가 중요한 추천을 생성할 경우,
어떤 정보가 판단 근거로 사용되었는지 확인할 수 있는 구조를 유지한다.

---

# 18. Uncertainty

Context가 부족하거나 신뢰하기 어려운 경우
AI가 이를 사실처럼 보완해서는 안 된다.

다음 상황을 구분할 수 있어야 한다.

```text
Known

Unknown

Uncertain
```

필요한 정보가 없는 경우 AI는 추측보다
정보 부족 상태를 명확하게 표현하는 것을 우선한다.

---

# 19. Context Quality

좋은 Context는 많은 정보를 포함하는 Context가 아니다.

다음 기준을 충족하는 Context를 우선한다.

* 현재 Task와 관련성이 높다.
* 출처를 확인할 수 있다.
* 시간적 의미를 판단할 수 있다.
* 현재 유효한 정보인지 구분할 수 있다.
* 사실과 해석을 구분할 수 있다.
* 필요한 관계 정보를 포함한다.
* 불필요한 중복이 적다.

Context 품질은 AI 결과 품질에 직접적인 영향을 준다.

---

# 20. Implementation Boundary

본 문서는 Context의 논리적 구성 기준을 정의한다.

다음 구현 방식은 Intelligence 또는 Platform의 관련 문서에서 결정한다.

* 검색 방식
* Vector Database
* Embedding
* Context Window 관리
* Token 최적화
* Ranking Algorithm
* Database Query
* API 구현

현재 단계에서는 특정 AI 기술이나 저장 기술에 종속되지 않는다.

---

# 21. Relationship to Other Documents

Context는 Company Intelligence의 마지막 활용 단계이다.

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

↓

AI Engines
```

Data Model은 데이터를 정의하고,

Entity Relationship은 데이터 간 관계를 정의하며,

Knowledge는 데이터를 재사용 가능한 지식으로 관리하고,

Search와 RAG는 필요한 정보를 찾으며,

Context는 해당 정보를 현재 AI 업무에 사용할 수 있는 형태로 구성한다.

---

# 22. Summary

Context는 Company Intelligence와 AI Engine을 연결하는 정보 계층이다.

Company Intelligence 전체를 AI에게 전달하는 것이 아니라,

```text
현재 업무

↓

관련 정보 선택

↓

출처·시점·상태 확인

↓

Context 구성

↓

AI 분석 및 추천
```

순서로 필요한 정보를 제공한다.

이를 통해 향후 Company AI가 회사 데이터를 단순히 검색하는 수준을 넘어,
신뢰할 수 있는 근거를 바탕으로 분석하고 전략을 추천할 수 있도록 한다.

최종 의사결정은 사람이 수행한다.
