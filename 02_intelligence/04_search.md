# 04_search.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence의 검색(Search) 기준을 정의한다.

검색은 회사에 축적된 데이터와 지식을 필요한 시점에 빠르게 찾기 위한 기능이며,
Company Intelligence를 활용하는 모든 사용자의 기본 진입점이다.

---

# 2. Objectives

Search의 목표는 다음과 같다.

- 필요한 정보를 빠르게 찾는다.
- 데이터와 지식을 통합하여 검색한다.
- 검색 결과의 정확성을 높인다.
- AI가 활용할 수 있는 검색 결과를 제공한다.

---

# 3. Search Scope

검색 대상은 다음과 같다.

- 데이터
- 문서
- 프로젝트
- 업무
- 지식
- 정책
- 의사결정
- 운영 기록

모든 검색 대상은 Company Intelligence에 등록된 정보만을 기준으로 한다.

---

# 4. Search Process

검색은 다음 순서로 수행한다.

```
Search Query

↓

Search

↓

Ranking

↓

Result

↓

Reference
```

검색 결과는 관련성이 높은 순으로 제공한다.

---

# 5. Search Principles

검색은 다음 원칙을 따른다.

- 정확성을 우선한다.
- 최신 정보를 우선한다.
- 중복 결과를 최소화한다.
- 출처를 함께 제공한다.
- 검색 결과는 추적 가능해야 한다.

---

# 6. Search Results

검색 결과는 다음 정보를 포함한다.

```
Title

Summary

Category

Source

Owner

Last Updated

Reference
```

필요에 따라 상세 정보를 조회할 수 있다.

---

# 7. Search Types

검색은 목적에 따라 다음 유형으로 구분한다.

| Type | Description |
|------|-------------|
| Keyword Search | 키워드 기반 검색 |
| Entity Search | 특정 Entity 검색 |
| Knowledge Search | 지식 검색 |
| Document Search | 문서 검색 |
| Related Search | 연관 정보 검색 |

필요에 따라 검색 유형을 추가할 수 있다.

---

# 8. Usage

Search는 다음 영역에서 활용한다.

- 정보 조회
- 업무 수행
- 지식 탐색
- RAG
- AI Context 생성

모든 AI 검색은 Search를 기반으로 수행한다.

---

# 9. Relationship to Other Documents

Search는 다음 문서와 연결된다.

```
03_knowledge.md

↓

04_search.md

↓

05_rag.md
```

검색은 Company Intelligence의 지식을 조회하며,
검색 결과는 RAG의 입력으로 활용된다.

---

# 10. Summary

Search는 Company Intelligence의 정보를 활용하기 위한 기본 기능이다.

사용자와 AI는 동일한 검색 체계를 기반으로 필요한 정보를 조회하며,
모든 검색 결과는 신뢰 가능한 출처와 함께 제공한다.