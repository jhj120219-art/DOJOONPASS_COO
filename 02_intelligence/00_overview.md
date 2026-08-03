# 02_intelligence/00_overview.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence의 목적과 전체 구조를 정의한다.

Company Intelligence는 회사의 데이터를 단순히 저장하는 공간이 아니라,
운영 과정에서 생성되는 정보를 구조화하여 검색 가능하고 재사용 가능한 지식으로 관리하는 체계이다.

모든 데이터 모델, 검색, RAG, AI Context는 본 문서를 기준으로 설계한다.

---

# 2. Objectives

Company Intelligence의 목표는 다음과 같다.

- 회사 데이터를 표준화한다.
- 데이터 간 관계를 정의한다.
- 지식을 체계적으로 축적한다.
- 필요한 정보를 빠르게 검색한다.
- AI가 활용할 수 있는 Context를 제공한다.

---

# 3. Scope

Company Intelligence는 다음 영역으로 구성된다.

```
Data

↓

Relationship

↓

History

↓

Knowledge

↓

Search

↓

RAG

↓

Context
```

각 단계는 이전 단계를 기반으로 구축한다.

---

# 4. Core Components

Company Intelligence는 다음 구성 요소를 가진다.

## Data Model

회사의 데이터를 표준 구조로 정의한다.

---

## Entity Relationship

데이터 간 관계를 정의한다.

---

## History

Issue 중 장기적으로 의미 있는 결정과 학습만 선별하여 보존한다.

---

## Knowledge

운영 과정에서 생성되는 지식을 관리한다.

---

## Search

필요한 정보를 빠르게 검색할 수 있도록 지원한다.

---

## RAG

검색된 정보를 AI가 활용할 수 있는 형태로 제공한다.

---

## Context

업무 상황에 맞는 정보를 AI에게 전달한다.

---

# 5. Operating Principles

Company Intelligence는 다음 원칙을 따른다.

- 모든 데이터는 구조화한다.
- 데이터와 지식은 구분하여 관리한다.
- 동일한 정보는 하나의 원본만 가진다.
- 검색 가능한 형태로 관리한다.
- AI는 검증 가능한 정보만 활용한다.

---

# 6. Document Structure

Company Intelligence는 다음 문서로 구성된다.

```
02_intelligence/

00_overview.md
01_data_model.md
02_entity_relationship.md
03_knowledge.md
04_search.md
05_rag.md
06_context.md
07_principles.md
```

각 문서는 하나의 주제만 다룬다.

---

# 7. Relationship

Company Intelligence는 다른 도메인과 다음과 같이 연결된다.

```
Foundation
    │
    ▼
Organization
    │
    ▼
Company Intelligence
    │
    ├── Platform
    └── AI Engines
```

Company Intelligence는 Platform 위에서 구현되며,
AI Engine이 활용하는 지식의 기반이 된다.

---

# 8. Summary

Company Intelligence는 회사의 데이터를 지식으로 관리하는 체계이다.

모든 데이터는 구조화되고,
모든 지식은 검색 가능하며,
모든 AI는 Company Intelligence를 기반으로 업무를 지원한다.