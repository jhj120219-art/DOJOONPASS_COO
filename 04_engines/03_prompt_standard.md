# 03_prompt_standard.md

> Version: 1.1
> Status: Draft
> Owner: CTO
> Category: Engines

---

# 1. Purpose

본 문서는 Company Operating System의 AI Engine과 AI Agent에서 사용하는 Prompt의 공통 기준을 정의한다.

Prompt Standard는 AI가 Company Intelligence의 데이터와 Context를 일관된 방식으로 활용하고,
근거 기반의 분석과 결과를 생성하도록 하는 기준이다.

모든 AI Engine과 Agent의 Prompt는 본 원칙을 따른다.

---

# 2. Objectives

Prompt Standard의 목표는 다음과 같다.

* AI 출력의 일관성을 유지한다.
* Company Intelligence의 Context를 정확하게 활용한다.
* 근거 없는 사실 생성을 최소화한다.
* 사실과 분석을 구분한다.
* 불확실성을 명확하게 표현한다.
* 결과의 근거를 추적할 수 있도록 한다.
* 사람이 검토하고 판단하기 쉬운 결과를 생성한다.
* Engine과 Agent 간 공통 Prompt 기준을 유지한다.

---

# 3. Core Principles

모든 Prompt는 다음 원칙을 따른다.

```text
Context Based

Evidence Based

No Fabrication

Clear Reasoning

Uncertainty Aware

Structured Output

Human Decision
```

AI는 제공된 Context를 우선적으로 사용하며,
정보가 부족한 경우 임의의 사실을 생성하지 않는다.

---

# 4. Standard Prompt Structure

Prompt는 필요한 경우 다음 구조를 기본으로 사용한다.

```text
Role

↓

Task

↓

Context

↓

Constraints

↓

Output
```

각 영역은 다음 역할을 가진다.

| Component   | Purpose          |
| ----------- | ---------------- |
| Role        | AI의 역할과 책임 정의    |
| Task        | 수행해야 하는 업무 정의    |
| Context     | 업무에 필요한 회사 정보 제공 |
| Constraints | 금지 사항과 판단 기준 정의  |
| Output      | 결과 형식 정의         |

모든 Prompt가 동일한 길이나 형식을 가져야 하는 것은 아니다.

업무 목적에 따라 필요한 요소만 사용한다.

---

# 5. Role

Role은 AI가 어떤 책임과 관점에서 업무를 수행하는지 정의한다.

예를 들어

```text
COO Assistant

CTO Assistant

CMO Assistant

Analysis Agent
```

등과 같이 업무 목적에 따라 역할을 설정할 수 있다.

Role은 AI에게 실제 조직 권한을 부여하는 것이 아니다.

AI의 역할은 분석과 업무 지원 범위를 정의하기 위한 Context이다.

---

# 6. Task

Task는 AI가 수행해야 하는 업무를 명확하게 정의한다.

Task는 가능한 한 하나의 주요 목적을 가진다.

예를 들어

```text
Analyze

Summarize

Compare

Evaluate

Recommend
```

처럼 결과의 목적을 명확하게 한다.

불필요하게 여러 목적을 하나의 Prompt에 혼합하지 않는다.

---

# 7. Context

AI는 현재 Task에 필요한 Context를 기반으로 작업한다.

```text
Company Intelligence

↓

Context

↓

Prompt

↓

AI
```

Context에는 필요한 경우 다음 정보가 포함될 수 있다.

* Company Data
* Knowledge
* KPI
* Decision
* Project
* Customer Insight
* Market Insight
* Source
* Time
* Status

Context의 구성 기준은 `02_intelligence/06_context.md`를 따른다.

---

# 8. Evidence Based

AI의 중요한 분석과 추천은 가능한 경우 제공된 근거를 기반으로 한다.

기본 흐름은 다음과 같다.

```text
Evidence

↓

Observation

↓

Analysis

↓

Recommendation
```

AI는 분석 결과와 그 근거를 구분할 수 있어야 한다.

특히 전략, 투자, 제품, 운영 등 중요한 추천에서는
어떤 정보가 판단에 사용되었는지 확인할 수 있도록 한다.

---

# 9. No Fabrication

AI는 Context에 존재하지 않는 회사 사실을 임의로 생성하지 않는다.

특히 다음 정보를 추측으로 만들어서는 안 된다.

* KPI
* 매출
* 비용
* 고객 데이터
* 프로젝트 결과
* 의사결정
* 시장 조사 결과
* 회사 정책
* 확인되지 않은 사건

필요한 정보가 존재하지 않는 경우
정보가 없다는 사실을 명확하게 표현한다.

---

# 10. Fact and Analysis

Prompt는 가능한 경우 사실과 AI의 해석을 구분하도록 설계한다.

기본 구분은 다음과 같다.

```text
Fact

↓

Observation

↓

Analysis

↓

Recommendation
```

### Fact

Company Intelligence 또는 신뢰할 수 있는 Context에서 확인된 정보이다.

### Observation

Fact에서 직접 확인할 수 있는 현상이다.

### Analysis

Fact와 Observation을 기반으로 AI가 해석한 결과이다.

### Recommendation

Analysis를 기반으로 제안하는 행동이다.

Recommendation은 Fact가 아니다.

---

# 11. Uncertainty

AI는 모든 상황에서 확정적인 답을 만들어낼 필요가 없다.

정보 상태를 필요한 경우 다음과 같이 구분한다.

```text
Known

Uncertain

Unknown
```

근거가 충분하지 않은 경우
확정적인 표현보다 불확실성을 명확하게 표시한다.

추가 정보가 필요한 경우
어떤 정보가 부족한지 식별할 수 있어야 한다.

---

# 12. Constraints

Prompt에는 업무 수행 과정에서 지켜야 할 제한 조건을 필요한 범위에서 명시한다.

예를 들어

```text
제공된 Context를 우선한다.

없는 회사 데이터를 만들지 않는다.

과거 데이터를 현재 데이터로 해석하지 않는다.

AI Output을 확인된 사실로 표현하지 않는다.

근거가 부족하면 불확실성을 표시한다.
```

등의 조건을 사용할 수 있다.

모든 Prompt에 불필요하게 긴 제한 조건을 반복하지 않는다.

공통 기준은 본 문서를 따르고,
개별 Prompt에는 해당 업무에 필요한 추가 조건만 정의한다.

---

# 13. Structured Output

AI 결과는 사람이 검토하고 시스템이 재사용하기 쉬운 구조를 우선한다.

분석 또는 전략 추천 업무에서는 필요한 경우 다음 구조를 사용할 수 있다.

```text
Summary

Evidence

Analysis

Recommendation

Risk

Uncertainty

Next Action
```

모든 Prompt에 동일한 Output 구조를 강제하지 않는다.

업무 목적에 맞는 최소한의 구조를 사용한다.

---

# 14. Recommendation

AI가 Recommendation을 생성하는 경우
단순한 의견보다 근거 기반의 선택지를 제공하는 것을 우선한다.

기본 구조는 다음과 같다.

```text
Current Situation

↓

Evidence

↓

Options

↓

Recommendation

↓

Expected Impact

↓

Risk
```

AI는 가능한 경우 하나의 답만 제시하기보다
의사결정자가 비교할 수 있는 선택지를 제공할 수 있다.

단순하거나 명확한 문제에 불필요한 선택지를 만들 필요는 없다.

---

# 15. Decision Support

AI Engine과 Agent의 목적은 사람의 의사결정을 지원하는 것이다.

```text
Company Data

↓

AI Analysis

↓

Recommendation

↓

Human Decision
```

AI의 Recommendation은 최종 의사결정이 아니다.

회사의 중요한 전략, 투자, 조직, 제품 및 운영 결정은
권한을 가진 사람이 최종 판단한다.

---

# 16. Prompt and Permission

Prompt는 Permission을 우회하는 수단이 될 수 없다.

AI Engine 또는 Agent는
허용된 Context와 Resource만 사용할 수 있다.

```text
Permission

↓

Allowed Context

↓

Prompt

↓

AI
```

Prompt에 특정 정보를 요청했다고 해서
해당 Agent에게 자동으로 접근 권한이 생기지 않는다.

Permission 기준은 `03_platform/04_permission.md`를 따른다.

---

# 17. Prompt and Memory

Prompt에서 Memory를 사용할 경우
Memory와 Company Intelligence를 구분한다.

Company Intelligence는 회사의 공식 데이터와 지식을 관리한다.

Memory는 AI의 업무 연속성을 지원한다.

AI가 회사의 공식 사실을 판단할 때는
Memory보다 현재 Company Intelligence Context를 우선한다.

Memory 기준은 `04_memory.md`를 따른다.

---

# 18. Prompt Reuse

반복적으로 사용하는 Prompt는 가능한 재사용 가능한 구조로 관리한다.

동일한 목적의 Prompt를 여러 위치에서 각각 관리하지 않는다.

Prompt 변경 시 해당 Prompt를 사용하는 Engine 또는 Agent에 미치는 영향을 확인한다.

단순한 일회성 업무까지 모두 표준 Prompt로 만들 필요는 없다.

---

# 19. Prompt Version

운영에 중요한 Prompt는 변경을 추적할 수 있어야 한다.

특히 다음과 같은 변경은 관리 대상이 될 수 있다.

* Role 변경
* Task 변경
* Context 구조 변경
* Constraint 변경
* Output 구조 변경
* 판단 기준 변경

단순한 문구 수정까지 과도하게 버전 관리하지 않는다.

실제 AI 결과에 영향을 주는 변경을 우선 관리한다.

---

# 20. Evaluation

중요한 Prompt는 실제 결과를 기준으로 평가한다.

평가 시 다음 항목을 확인할 수 있다.

* Task 수행 여부
* Context 활용 여부
* 근거 정확성
* Fabrication 여부
* 논리적 일관성
* Output 구조 준수
* 실제 업무 활용 가능성

Prompt의 품질은 문장 자체가 아니라
실제 AI 결과를 기준으로 판단한다.

---

# 21. Improvement

Prompt는 실제 운영 결과를 기반으로 개선한다.

기본 개선 흐름은 다음과 같다.

```text
Prompt

↓

AI Output

↓

Review

↓

Issue

↓

Improvement

↓

Updated Prompt
```

문제가 발생할 때마다 Prompt를 무조건 길게 만드는 방식은 피한다.

문제의 원인이

```text
Prompt

Context

Data

Model

Workflow
```

중 어디에 있는지 먼저 구분한다.

---

# 22. Implementation Boundary

본 문서는 Prompt의 공통 설계 기준을 정의한다.

다음과 같은 구체적인 구현 방식은 각 Engine 또는 실제 개발 단계에서 결정한다.

* Prompt 저장 방식
* Prompt Template Engine
* Model별 Prompt 최적화
* Token 관리
* Prompt Cache
* Prompt 실행 코드
* 자동 평가 시스템

현재 단계에서는 특정 LLM이나 Prompt Framework에 종속되지 않는다.

---

# 23. Relationship to Other Documents

Prompt Standard는 Company Intelligence와 AI Engine을 연결하는 실행 기준이다.

```text
Company Intelligence

↓

Context

↓

Permission

↓

Prompt

↓

AI Engine / Agent

↓

Analysis / Recommendation

↓

Human Decision
```

Context는 AI에게 필요한 정보를 제공하고,

Permission은 사용할 수 있는 정보와 기능을 제한하며,

Prompt는 AI가 해당 정보를 어떻게 활용할지 정의하고,

Engine과 Agent는 실제 업무를 수행한다.

---

# 24. Summary

Prompt Standard는 Company Operating System에서 AI가 회사 데이터를 안전하고 일관되게 활용하기 위한 공통 기준이다.

AI는

```text
Context

↓

Evidence

↓

Analysis

↓

Recommendation
```

순서로 정보를 활용하는 것을 기본으로 한다.

없는 사실을 생성하지 않고,
사실과 분석을 구분하며,
불확실성을 명확하게 표현한다.

이를 통해 Company AI가 단순한 정보 정리를 넘어
회사의 실제 데이터를 기반으로 분석하고 전략을 추천할 수 있도록 하되,
최종 의사결정은 사람이 수행한다.
