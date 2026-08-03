# 02_roadmap.md

> Version: 1.1
> Status: Draft
> Owner: CEO
> Category: Foundation

---

# 1. Purpose

본 문서는 Company Operating System 구축을 위한 전체 개발 로드맵을 정의한다.

로드맵은 단순한 기능 개발 계획이 아니라,
회사의 운영체계를 단계적으로 구축하기 위한 기준이다.

모든 프로젝트와 개발 일정은 본 문서를 기준으로 계획한다.

---

# 2. Vision

Company Operating System은 다음 단계를 거쳐 발전한다.

```text
Standardized Company

↓

Data-driven Company

↓

Knowledge-driven Company

↓

AI-assisted Company

↓

Autonomous Company
```

각 단계는 이전 단계에서 구축된 운영체계와 데이터를 기반으로 발전한다.

현재 필요한 기반을 먼저 구축하고,
미래 기능을 현재 단계에서 과도하게 구현하지 않는다.

---

# 3. Development Principles

로드맵은 다음 원칙을 따른다.

* 운영을 먼저 설계한다.
* 프로세스를 표준화한 후 자동화한다.
* 데이터를 회사의 자산으로 축적한다.
* 축적된 데이터를 지식으로 연결한다.
* AI는 회사의 데이터와 지식을 기반으로 동작한다.
* AI는 의사결정을 지원하며 최종 결정은 사람이 수행한다.
* 각 단계는 실제 운영을 통해 검증한다.
* 현재 필요한 기능을 우선하고 불필요한 선행 개발을 하지 않는다.

---

# 4. Phase 1 : Foundation & Organization

## Goal

Company Operating System의 운영 기반을 정의한다.

회사의 운영 철학, 조직, 역할, 책임, 의사결정 및 공통 기준을 문서화한다.

### Deliverables

* Company Foundation
* Operating Principles
* Organization Architecture
* Role & Responsibility
* Decision Principles
* Documentation Governance
* Company Standards

### Success Criteria

* 회사 운영 원칙 정의 완료
* 조직 역할과 책임 정의 완료
* 의사결정 기준 정의 완료
* 문서 체계 구축 완료
* 공통 운영 표준 정의 완료

---

# 5. Phase 2 : Company Intelligence

## Goal

회사의 운영 과정에서 발생하는 데이터를 축적하고,
검색 및 재사용 가능한 회사 지식으로 관리한다.

Company Intelligence는 회사의 모든 운영 데이터를 축적·연결·활용하는 핵심 영역이며,
향후 Company AI가 활용하는 Data Hub 역할을 한다.

### Deliverables

* Company Intelligence Architecture
* Data Model
* Entity Relationship
* Knowledge Structure
* Search
* RAG
* AI Context

### Success Criteria

* 회사 데이터 구조 표준화
* 데이터의 출처와 관계 추적 가능
* 회사 지식 검색 가능
* 필요한 정보를 Context로 구성 가능
* AI가 회사 지식을 근거로 활용할 수 있는 기반 확보

---

# 6. Phase 3 : Platform

## Goal

Company Operating System을 실제 시스템으로 구현하기 위한 기술 기반을 구축한다.

### Deliverables

* Database
* Storage
* API
* Permission
* Event

### Success Criteria

* 회사 데이터 저장 가능
* 표준 API를 통한 데이터 접근 가능
* 사용자와 시스템의 접근 권한 관리 가능
* 주요 시스템 활동 추적 가능
* Company Intelligence를 실제 시스템에서 운영할 수 있는 기반 확보

---

# 7. Phase 4 : AI Engines

## Goal

회사 데이터와 지식을 활용하여 각 조직의 업무를 지원하는 AI Engine을 구축한다.

AI Engine은 독립적으로 회사를 운영하는 시스템이 아니라,
사람의 업무와 의사결정을 지원하는 시스템으로 설계한다.

### Deliverables

* Engine Architecture
* Agent Lifecycle
* Prompt Standard
* Memory
* Shared AI Functions

### Success Criteria

* AI가 Company Intelligence를 활용할 수 있음
* 업무별 AI 지원 가능
* 근거 기반 분석 및 추천 가능
* AI 실행 과정 추적 가능
* 사람이 최종 결과를 검토하고 결정할 수 있음

---

# 8. Phase 5 : Automation

## Goal

검증된 반복 업무를 자동화하여 운영 효율을 높인다.

자동화는 이미 정의되고 검증된 프로세스를 대상으로 한다.

### Deliverables

* Workflow Automation
* Reporting Automation
* Notification Automation
* KPI Monitoring
* Repetitive Task Automation

### Success Criteria

* 반복 업무 감소
* 업무 처리 시간 단축
* 운영 데이터 자동 축적
* 자동화 결과 추적 가능
* 사람이 필요한 예외 상황에 집중할 수 있음

---

# 9. Phase 6 : Advanced AI Operations

## Goal

충분한 운영 데이터와 검증된 AI 활용 경험이 축적된 이후,
예측과 고도화된 의사결정 지원 기능을 단계적으로 검토한다.

### Possible Capabilities

* Predictive Analytics
* Advanced Decision Support
* Business Simulation
* Company Digital Twin
* Autonomous Optimization

본 Phase의 기능은 현재 개발 범위에 포함하지 않는다.

실제 데이터 규모, 회사 성장 단계 및 사업적 필요성이 확인된 이후 별도로 결정한다.

---

# 10. Current Scope

현재 우선 개발 범위는 다음과 같다.

```text
Phase 1
Foundation & Organization

↓

Phase 2
Company Intelligence

↓

Phase 3
Platform
```

AI Engines는 위 기반이 실제로 사용할 수 있는 상태가 된 이후 개발한다.

Automation과 Advanced AI Operations는 현재 개발하지 않는다.

현재 제외 범위는 다음과 같다.

* Autonomous AI
* Company Digital Twin
* Autonomous Decision Making
* Full Business Simulation
* Autonomous Optimization

필요성이 검증되기 전에는 선행 개발하지 않는다.

---

# 11. Development Sequence

전체 개발 순서는 다음을 기본으로 한다.

```text
Foundation

↓

Organization

↓

Company Intelligence

↓

Platform

↓

AI Engines

↓

Automation

↓

Advanced AI Operations
```

단순히 문서 작성 완료를 다음 단계 진입 조건으로 사용하지 않는다.

각 단계에서 정의된 구조가 실제 다음 단계에서 사용할 수 있는 수준인지 검증한 후 진행한다.

---

# 12. Milestones

| Phase                     | Status      | Priority |
| ------------------------- | ----------- | -------- |
| Foundation & Organization | In Progress | High     |
| Company Intelligence      | Planned     | High     |
| Platform                  | Planned     | High     |
| AI Engines                | Planned     | Medium   |
| Automation                | Future      | Low      |
| Advanced AI Operations    | Future      | Low      |

Status는 실제 개발 진행 상황에 따라 갱신한다.

---

# 13. Risks

주요 리스크는 다음과 같다.

* 실제 운영보다 문서 설계가 앞서는 문제
* 필요하지 않은 기능의 선행 개발
* 데이터 구조의 일관성 부족
* 데이터 출처 및 변경 이력 관리 부족
* 문서와 실제 시스템의 불일치
* AI가 근거 없는 정보를 생성하는 문제
* AI에 과도한 의사결정 권한을 부여하는 문제
* 기술 부채 누적

모든 리스크는 실제 발생 가능성과 영향도를 기준으로 관리한다.

---

# 14. Success Metrics

Company Operating System 구축 성공 여부는 기능 개수가 아니라 실제 운영 가능성을 기준으로 평가한다.

주요 기준은 다음과 같다.

* 조직과 책임이 명확하게 정의되어 있는가
* 운영 기준이 실제 업무에 적용되고 있는가
* 회사 데이터가 일관된 구조로 축적되는가
* 데이터의 출처와 변경 사항을 추적할 수 있는가
* 필요한 회사 지식을 검색하고 재사용할 수 있는가
* AI가 회사 데이터를 근거로 활용할 수 있는가
* 반복 업무가 검증된 프로세스를 기반으로 자동화되는가
* 문서와 실제 시스템이 일치하는가

---

# 15. Summary

Company Operating System은 AI 기능을 먼저 만드는 프로젝트가 아니다.

```text
운영체계

↓

데이터

↓

지식

↓

플랫폼

↓

AI 지원

↓

자동화
```

순서로 회사를 단계적으로 구축하는 프로젝트이다.

현재 필요한 기반을 먼저 완성하고,
실제 데이터와 운영 경험이 필요한 기능은 그 시점에 개발한다.

모든 개발은 본 로드맵을 기준으로 우선순위를 결정한다.
