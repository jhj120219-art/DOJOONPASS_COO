# 03_knowledge.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence에서 관리하는 지식(Knowledge)의 기준을 정의한다.

지식은 단순한 데이터나 문서가 아니라,
운영 과정에서 축적된 경험, 규칙, 절차 및 의사결정 정보를 의미한다.

Company Intelligence는 데이터를 저장하는 것이 아니라,
재사용 가능한 지식을 지속적으로 축적하는 것을 목표로 한다.

---

# 2. Objectives

Knowledge의 목표는 다음과 같다.

- 회사의 운영 지식을 축적한다.
- 지식을 검색 가능하게 관리한다.
- 동일한 문제를 반복 해결하지 않는다.
- AI가 활용할 수 있는 신뢰 가능한 지식을 제공한다.

---

# 3. Knowledge Sources

지식은 다음 정보로부터 생성된다.

- 승인된 Company History Record
- 업무 수행 결과
- 프로젝트 수행 과정
- 문서
- 회의 기록
- 의사결정
- 운영 규칙
- 문제 해결 사례

새로운 정보는 검토를 거쳐 지식으로 축적한다.

---

# 4. Knowledge Structure

모든 지식은 다음 정보를 가진다.

```
ID

Title

Category

Summary

Content

Source

Owner

Tags

Status

Created At

Updated At
```

필요에 따라 추가 속성을 정의할 수 있다.

---

# 5. Knowledge Classification

지식은 목적에 따라 분류한다.

| Category | Description |
|----------|-------------|
| Policy | 운영 정책 |
| Process | 업무 절차 |
| Decision | 의사결정 내용 |
| Reference | 참고 자료 |
| Best Practice | 검증된 운영 사례 |
| Lesson Learned | 경험 및 개선 사항 |

각 지식은 하나 이상의 분류를 가질 수 있다.

---

# 6. Knowledge Lifecycle

모든 지식은 동일한 생명주기를 따른다.

```
Create

↓

Review

↓

Publish

↓

Update

↓

Archive
```

검토되지 않은 정보는 공식 지식으로 사용하지 않는다.

History Record는 Review 단계에서 검토되고 Publish 단계에서 Knowledge로 승격된다.

---

# 7. Knowledge Principles

지식은 다음 원칙을 따른다.

- 검증 가능한 정보를 기록한다.
- 최신 상태를 유지한다.
- 중복 지식을 최소화한다.
- 출처를 명확히 관리한다.
- 지속적으로 개선한다.

---

# 8. Usage

Knowledge는 다음 영역에서 활용한다.

- 운영 기준 제공
- 업무 지원
- 검색
- RAG
- AI Context
- 의사결정 지원

---

# 9. Relationship to Other Documents

Knowledge는 다음 문서와 연결된다.

```
01_data_model.md

↓

02_entity_relationship.md

↓

03_knowledge.md

↓

04_search.md
```

지식은 데이터와 관계 정보를 기반으로 생성되며,
검색을 통해 활용된다.

---

# 10. Summary

Knowledge는 Company Intelligence의 핵심 자산이다.

회사의 경험과 운영 정보를 지속적으로 축적하고 관리하여,
사람과 AI가 동일한 지식을 기반으로 업무를 수행할 수 있도록 지원한다.