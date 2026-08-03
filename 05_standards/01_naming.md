# 01_naming.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Standards

---

# 1. Purpose

본 문서는 Company Operating System에서 사용하는 명명(Naming) 기준을 정의한다.

일관된 명명 규칙은 문서, 데이터, 코드 및 시스템을 쉽게 이해하고 관리할 수 있도록 지원한다.

모든 구성 요소는 본 문서의 명명 규칙을 따른다.

---

# 2. Objectives

Naming의 목표는 다음과 같다.

- 일관된 이름을 사용한다.
- 의미를 명확하게 표현한다.
- 중복과 혼동을 방지한다.
- 검색과 관리가 쉽도록 한다.

---

# 3. General Principles

모든 이름은 다음 원칙을 따른다.

- 의미를 명확하게 표현한다.
- 약어 사용을 최소화한다.
- 동일한 대상에는 동일한 이름을 사용한다.
- 하나의 이름은 하나의 의미만 가진다.
- 프로젝트 전체에서 일관성을 유지한다.

---

# 4. Language Rules

명명은 다음 기준을 따른다.

| Target | Standard |
|---------|----------|
| Folder | English |
| File | English |
| Code | English |
| API | English |
| Database | English |
| Document Contents | Korean |

식별자는 영어를 사용하며,
문서 내용은 한국어를 기본으로 작성한다.

---

# 5. File Naming

파일명은 다음 규칙을 따른다.

```
00_overview.md

01_naming.md

02_folder.md
```

규칙

- 두 자리 번호를 사용한다.
- snake_case를 사용한다.
- 소문자를 사용한다.
- 확장자는 `.md`를 사용한다.

---

# 6. Identifier Naming

시스템에서 사용하는 식별자는 다음 기준을 따른다.

| Target | Convention |
|---------|------------|
| Database Table | snake_case |
| Database Column | snake_case |
| API Endpoint | kebab-case |
| JSON Field | camelCase |
| Class | PascalCase |
| Function | camelCase |
| Constant | UPPER_SNAKE_CASE |

각 대상은 하나의 명명 규칙만 사용한다.

---

# 7. Reserved Words

예약어나 의미가 불명확한 이름은 사용하지 않는다.

예시

- data
- temp
- test
- new
- value

의미를 명확히 표현하는 이름을 사용한다.

---

# 8. Change Management

기존 명명 규칙을 변경할 경우 다음 사항을 검토한다.

- 영향 범위
- 호환성
- 문서 반영
- 관련 시스템 수정

명명 변경은 프로젝트 전체의 일관성을 유지해야 한다.

---

# 9. Summary

명명 규칙은 Company Operating System의 공통 언어이다.

모든 문서, 데이터 및 시스템은 일관된 Naming 기준을 적용하여
가독성, 유지보수성 및 검색 효율성을 확보한다.