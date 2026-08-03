# 05_rag.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence에서 사용하는 RAG(Retrieval-Augmented Generation)의 운영 기준을 정의한다.

RAG는 AI가 자체 지식만으로 답변하지 않고,
Company Intelligence에서 검색한 정보를 근거로 응답하도록 지원하는 구조이다.

모든 AI는 RAG를 통해 회사의 최신 정보와 지식을 활용한다.

---

# 2. Objectives

RAG의 목표는 다음과 같다.

- AI 응답의 정확성을 높인다.
- 최신 회사 정보를 활용한다.
- 답변의 근거를 제공한다.
- Hallucination을 최소화한다.
- Company Intelligence를 효과적으로 활용한다.

---

# 3. RAG Process

RAG는 다음 순서로 수행한다.

```
User Request

↓

Search

↓

Retrieve

↓

Context Construction

↓

AI Response

↓

Reference
```

검색된 정보만을 기반으로 AI가 응답을 생성한다.

---

# 4. Retrieval Scope

RAG는 다음 정보를 검색 대상으로 사용한다.

- Data
- Knowledge
- Documents
- Policies
- Processes
- Decisions
- Project Information

외부 정보는 필요에 따라 별도로 활용할 수 있으며,
Company Intelligence와 구분하여 관리한다.

---

# 5. Context Construction

검색된 정보는 AI가 이해할 수 있는 Context로 구성한다.

Context는 다음 요소를 포함할 수 있다.

- 관련 데이터
- 관련 지식
- 관련 문서
- 관련 업무
- 관련 의사결정
- 관련 규칙

Context는 요청 목적에 맞게 필요한 정보만 포함한다.

---

# 6. Response Principles

RAG 기반 응답은 다음 원칙을 따른다.

- 검색 결과를 기반으로 답변한다.
- 확인되지 않은 내용을 생성하지 않는다.
- 근거를 함께 제공한다.
- 최신 정보를 우선 활용한다.
- 부족한 정보는 추측하지 않는다.

---

# 7. Reference Management

모든 RAG 응답은 참조 정보를 관리한다.

참조 정보는 다음 항목을 포함한다.

```
Source

Document

Knowledge

Last Updated
```

사용자는 답변의 근거를 확인할 수 있어야 한다.

---

# 8. Usage

RAG는 다음 영역에서 활용한다.

- AI Assistant
- 업무 지원
- 문서 검색
- 지식 검색
- 의사결정 지원

Company Intelligence를 사용하는 모든 AI는 동일한 RAG 기준을 따른다.

---

# 9. Relationship to Other Documents

RAG는 다음 문서와 연결된다.

```
04_search.md

↓

05_rag.md

↓

06_context.md
```

Search는 필요한 정보를 조회하고,
RAG는 조회된 정보를 AI가 활용할 수 있도록 구성하며,
Context는 AI에게 전달되는 최종 정보 구조를 정의한다.

---

# 10. Summary

RAG는 Company Intelligence와 AI를 연결하는 핵심 구조이다.

모든 AI는 Company Intelligence에서 검색한 정보를 기반으로 응답하며,
정확성, 최신성, 근거 제공을 기본 원칙으로 한다.