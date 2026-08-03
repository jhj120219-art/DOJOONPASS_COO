# 02_entity_relationship.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Intelligence

---

# 1. Purpose

본 문서는 Company Intelligence를 구성하는 데이터 간의 관계(Entity Relationship)를 정의한다.

개별 데이터는 독립적으로 존재할 수 있지만,
실제 운영에서는 서로 연결되어 하나의 업무 흐름을 구성한다.

데이터 간 관계를 정의함으로써 검색, 추적, 분석 및 AI 활용의 기반을 제공한다.

---

# 2. Objectives

Entity Relationship의 목표는 다음과 같다.

- 데이터 간 연결 기준을 정의한다.
- 데이터의 흐름을 추적할 수 있도록 한다.
- 중복 데이터 생성을 방지한다.
- 검색과 AI 활용을 위한 관계 정보를 제공한다.

---

# 3. Relationship Principles

모든 데이터 관계는 다음 원칙을 따른다.

- 관계는 명확하게 정의한다.
- 동일한 관계를 중복 생성하지 않는다.
- 데이터는 참조(Reference)를 통해 연결한다.
- 관계는 양방향 추적이 가능해야 한다.

---

# 4. Core Entities

Company Intelligence는 다음 핵심 Entity를 관리한다.

- Organization
- Person
- Project
- Issue
- Document
- Asset
- Knowledge
- Event
- History

각 Entity는 독립적으로 존재하며,
필요에 따라 다른 Entity와 연결된다.

---

# 5. Relationship Types

Entity 간 관계는 다음 유형으로 구분한다.

| Type | Description |
|------|-------------|
| One-to-One | 하나의 데이터가 하나의 데이터와 연결 |
| One-to-Many | 하나의 데이터가 여러 데이터와 연결 |
| Many-to-Many | 여러 데이터가 서로 연결 |

관계 유형은 데이터의 특성에 따라 결정한다.

---

# 6. Relationship Structure

모든 관계는 다음 정보를 가진다.

```
Source Entity

↓

Relationship Type

↓

Target Entity
```

관계 자체도 관리 대상 데이터로 취급한다.

---

# 7. Relationship Rules

모든 관계는 다음 기준을 따른다.

- 연결 목적이 명확해야 한다.
- 순환 참조를 최소화한다.
- 불필요한 관계는 생성하지 않는다.
- 변경 시 관계의 무결성을 유지한다.

---

# 8. Usage

Entity Relationship은 다음 기능에서 활용된다.

- 데이터 탐색
- 지식 연결
- 검색 결과 확장
- RAG 데이터 구성
- AI Context 생성

---

# 9. Relationship to Other Documents

Entity Relationship은 다음 문서와 연결된다.

```
01_data_model.md

↓

02_entity_relationship.md

↓

03_knowledge.md
```

데이터 모델을 기반으로 관계를 정의하고,
관계를 기반으로 지식을 구성한다.

---

# 10. Summary

Entity Relationship은 Company Intelligence의 연결 구조를 정의한다.

모든 데이터는 독립적으로 관리되면서도,
명확한 관계를 통해 하나의 운영 지식 체계를 구성한다.