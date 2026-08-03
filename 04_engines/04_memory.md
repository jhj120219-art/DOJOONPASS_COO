# 04_memory.md

> Version: 1.1
> Status: Draft
> Owner: CTO
> Category: Engines

---

# 1. Purpose

본 문서는 Company Operating System의 AI Engine과 AI Agent에서 사용하는 Memory의 역할과 관리 기준을 정의한다.

Memory는 AI가 이전 작업과 상호작용의 맥락을 유지하여
연속성 있는 업무를 수행하도록 지원하는 정보 계층이다.

Memory는 Company Intelligence를 대체하지 않는다.

회사의 공식 데이터와 지식은 Company Intelligence에서 관리하고,
Memory는 AI 업무 수행에 필요한 연속성과 참고 정보를 제공한다.

---

# 2. Objectives

Memory의 목표는 다음과 같다.

* AI 업무의 연속성을 유지한다.
* 이전 작업의 필요한 맥락을 재사용한다.
* 반복적인 정보 전달을 줄인다.
* Agent가 이전 작업 상태를 참고할 수 있도록 한다.
* Company Intelligence와 AI Memory의 책임을 분리한다.
* 오래되거나 잘못된 Memory가 공식 사실로 사용되는 것을 방지한다.

---

# 3. Core Principle

Memory의 핵심 원칙은 다음과 같다.

```text
Company Intelligence
= 회사의 공식 데이터와 지식

Memory
= AI 업무 연속성을 위한 기억
```

따라서

```text
Memory ≠ Company Database

Memory ≠ Official Knowledge

Memory ≠ Source of Truth
```

이다.

회사의 공식 사실을 판단할 때는
Memory보다 Company Intelligence를 우선한다.

---

# 4. Memory Role

Memory는 AI가 이전 업무의 필요한 정보를 유지하는 데 사용한다.

예를 들어 다음과 같은 정보를 기억할 수 있다.

* 이전 작업 상태
* 이전 대화의 필요한 맥락
* 진행 중인 업무 정보
* 사용된 작업 조건
* 이전 AI Output
* 후속 작업에 필요한 참고 정보

Memory는 AI가 매번 모든 정보를 처음부터 다시 확인해야 하는 문제를 줄인다.

---

# 5. Memory Flow

기본적인 Memory 활용 흐름은 다음과 같다.

```text
Task

↓

Context

↓

AI Engine / Agent

↓

Output

↓

Relevant Memory

↓

Next Task
```

모든 AI Output을 Memory에 저장하지 않는다.

후속 업무에 필요한 정보만 유지한다.

---

# 6. Company Intelligence and Memory

Company Intelligence와 Memory는 다음과 같이 역할을 구분한다.

| Area          | Company Intelligence | Memory  |
| ------------- | -------------------- | ------- |
| 회사 공식 데이터     | 관리                   | 참조 가능   |
| 회사 공식 지식      | 관리                   | 참조 가능   |
| KPI           | 관리                   | 필요 시 참고 |
| Decision      | 관리                   | 필요 시 참고 |
| Customer Data | 관리                   | 필요 시 참고 |
| Market Data   | 관리                   | 필요 시 참고 |
| AI 작업 상태      | 필요 시 기록              | 관리      |
| 이전 AI Output  | 필요 시 기록              | 관리 가능   |
| 대화 맥락         | 관리 대상 아님             | 관리 가능   |
| 작업 연속성        | 지원                   | 관리      |

Company Intelligence는 회사의 Source of Truth이고,
Memory는 AI의 업무 연속성을 지원한다.

---

# 7. Context and Memory

Context와 Memory도 서로 다른 역할을 가진다.

```text
Company Intelligence

↓

Context

↓

AI Engine / Agent

↕

Memory
```

Context는 현재 업무에 필요한 공식 정보와 관련 정보를 제공한다.

Memory는 이전 업무에서 유지된 필요한 맥락을 제공한다.

AI는 현재 Task를 수행할 때
Context와 Memory를 함께 사용할 수 있다.

---

# 8. Context Priority

Company Intelligence에서 생성된 현재 Context와
Memory의 내용이 충돌할 경우 현재 Context를 우선한다.

기본 우선순위는 다음과 같다.

```text
Current Company Intelligence Context

↓

Approved Company Knowledge

↓

Relevant Memory

↓

AI Assumption
```

Memory에 저장된 과거 정보가
현재 회사 상태와 다를 수 있기 때문이다.

AI Assumption은 공식 사실로 사용하지 않는다.

---

# 9. Memory Types

Memory는 필요에 따라 다음과 같이 구분할 수 있다.

## Task Memory

현재 또는 연속된 작업을 수행하기 위해 필요한 정보이다.

예:

* 현재 작업 단계
* 완료된 작업
* 남은 작업
* 작업 조건

---

## Interaction Memory

이전 상호작용에서 후속 업무에 필요한 정보이다.

예:

* 이전 요청
* 이전 피드백
* 수정 방향
* 합의된 작업 조건

---

## Agent Memory

특정 Agent가 반복 업무를 수행하기 위해 필요한 업무 맥락이다.

예:

* 이전 실행 상태
* 이전 결과
* 반복적으로 사용되는 작업 정보

Memory Type은 실제 필요가 발생할 때 사용한다.

현재 필요하지 않은 Memory 구조를 미리 복잡하게 만들지 않는다.

---

# 10. Memory Creation

모든 정보가 자동으로 Memory가 되어서는 안 된다.

Memory로 유지할 정보는 다음 기준을 고려한다.

```text
Relevance

+

Future Use

+

Reliability
```

다음 작업에서 다시 사용할 가능성이 없거나
가치가 낮은 정보는 저장하지 않는 것을 우선한다.

---

# 11. Memory Source

Memory는 가능한 경우 어디에서 생성되었는지 구분할 수 있어야 한다.

예를 들어

```text
Human Input

AI Output

Task State

Company Intelligence Reference
```

등이 존재할 수 있다.

AI가 생성한 Memory와 사람이 제공한 정보를
필요한 경우 구분할 수 있어야 한다.

---

# 12. Memory and Facts

Memory에 존재한다는 이유만으로
해당 정보가 회사의 공식 사실이 되는 것은 아니다.

예를 들어 AI가 이전 작업에서

```text
A 전략이 가장 적합하다.
```

라고 분석했다고 하더라도,

이는

```text
AI Recommendation
```

이지

```text
Company Fact
```

가 아니다.

AI의 분석, 추론 및 추천은
확인된 회사 데이터와 구분한다.

---

# 13. Memory and Decisions

AI가 과거의 Decision을 기억해야 하는 경우
공식 Decision 기록을 우선 참조한다.

```text
Company Intelligence
Decision Record

↓

Context

↓

AI
```

Memory에 존재하는 과거 결정 내용이
공식 Decision Record를 대체하지 않는다.

중요한 의사결정은 Memory가 아니라
Company Intelligence에서 관리한다.

---

# 14. Memory Update

Memory는 새로운 정보에 따라 변경될 수 있다.

기존 Memory와 새로운 정보가 충돌하는 경우
최신 Company Intelligence와 현재 Context를 기준으로 판단한다.

오래된 Memory를 계속 유지하여
AI가 잘못된 정보를 반복적으로 사용하는 것을 방지한다.

---

# 15. Memory Expiration

모든 Memory를 영구적으로 유지할 필요는 없다.

다음과 같은 Memory는 필요성이 사라지면 제거하거나 더 이상 사용하지 않을 수 있다.

* 완료된 단기 작업 상태
* 오래된 임시 Context
* 더 이상 유효하지 않은 작업 조건
* 중복된 정보
* 현재 회사 상태와 충돌하는 과거 정보

Memory의 가치가 유지되는 기간은 정보의 목적에 따라 다를 수 있다.

---

# 16. Memory Promotion

Memory에서 장기적으로 회사에 가치가 있는 정보가 발견될 수 있다.

이 경우 해당 정보를 자동으로 Company Intelligence의 공식 지식으로 승격하지 않는다.

기본 흐름은 다음과 같다.

```text
Memory

↓

Potential Company Knowledge

↓

Review

↓

Approved

↓

Company Intelligence
```

예를 들어 반복적으로 확인된 고객 Insight나 중요한 운영 학습이 있다면
검토 후 Company Intelligence에 반영할 수 있다.

---

# 17. Memory and Strategy

AI가 전략을 분석하거나 추천할 때
Memory는 과거 작업 맥락을 제공할 수 있다.

그러나 전략 추천의 주요 근거는
현재 Company Intelligence와 Context여야 한다.

```text
Company Intelligence

+

Current Context

+

Relevant Memory

↓

Analysis

↓

Recommendation

↓

Human Decision
```

Memory는 전략 추천을 보조하지만,
과거 AI 판단을 그대로 반복하기 위한 수단으로 사용하지 않는다.

---

# 18. Memory and Permission

Memory도 Permission의 적용 대상이다.

AI Agent가 특정 Memory에 접근할 수 있다는 이유만으로
관련 Company Intelligence 데이터까지 자동으로 접근할 수 있는 것은 아니다.

반대로 Company Intelligence 접근 권한이 있다고 해서
모든 Agent Memory를 사용할 수 있는 것도 아니다.

접근 권한은 각 Resource의 목적에 따라 관리한다.

Permission 기준은 `03_platform/04_permission.md`를 따른다.

---

# 19. Memory and Agent Lifecycle

Agent가 생성되고 실행되고 종료되는 과정에서
Memory가 사용될 수 있다.

```text
Agent Start

↓

Load Relevant Memory

↓

Receive Context

↓

Execute Task

↓

Generate Output

↓

Update Relevant Memory

↓

Agent End
```

Agent가 종료된다고 모든 Memory를 반드시 삭제하거나
모든 Memory를 영구 보존하는 방식으로 고정하지 않는다.

업무 목적에 따라 필요한 Memory만 유지한다.

Agent Lifecycle 기준은 `02_agent_lifecycle.md`를 따른다.

---

# 20. Memory Quality

Memory는 다음 기준을 고려하여 관리한다.

* 현재 업무와 관련성이 있는가
* 출처를 구분할 수 있는가
* 현재도 유효한가
* 공식 사실과 AI Output이 구분되는가
* 중복되지 않는가
* 후속 업무에 실제 가치가 있는가

Memory의 양보다 품질과 활용 가능성을 우선한다.

---

# 21. Memory Safety

Memory에는 불필요한 민감 정보나
Agent 업무와 관련 없는 데이터를 저장하지 않는다.

AI가 Memory를 통해 Permission을 우회하거나
원래 접근할 수 없는 정보를 간접적으로 획득하지 않도록 한다.

Memory는 편의를 위한 정보 저장소이지
접근 통제를 우회하는 저장소가 아니다.

---

# 22. Implementation Boundary

본 문서는 Memory의 논리적 역할과 관리 기준을 정의한다.

다음 구현 방식은 실제 Engine 개발 단계에서 결정한다.

* Memory Database
* Vector Memory
* Conversation Memory
* Memory Retrieval
* Memory Ranking
* Memory Summarization
* Memory Retention Period
* Memory Storage Format

현재 단계에서는 특정 Memory Framework나 AI 기술에 종속되지 않는다.

---

# 23. Relationship to Other Documents

Memory는 Company Intelligence와 AI Engine 사이에서
AI 업무의 연속성을 지원한다.

```text
Company Intelligence

↓

Context

↓

AI Engine / Agent

↕

Memory
```

관련 역할은 다음과 같다.

```text
Company Intelligence
→ 공식 데이터와 지식

Context
→ 현재 업무에 필요한 정보

Prompt
→ AI 업무 수행 기준

Memory
→ 이전 업무의 필요한 맥락

AI Engine / Agent
→ 실제 업무 수행
```

Memory는 이 구조에서 Company Intelligence를 대체하지 않는다.

---

# 24. Summary

Memory는 AI가 이전 업무의 필요한 맥락을 유지하여
연속성 있게 작업할 수 있도록 지원하는 정보 계층이다.

핵심 구조는 다음과 같다.

```text
Company Intelligence
= 회사가 아는 것

Context
= 지금 AI가 알아야 하는 것

Memory
= AI가 이전 작업에서 기억해야 하는 것
```

회사의 공식 데이터와 지식은 Company Intelligence에서 관리한다.

Memory는 이를 보조하며,
현재 Context와 충돌할 경우 공식 회사 정보를 우선한다.

이를 통해 향후 AI Agent가 장기간 업무를 수행하더라도
회사의 공식 지식과 AI의 기억이 혼재되지 않는 구조를 유지한다.
