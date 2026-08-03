# 05_coding.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Standards

---

# 1. Purpose

본 문서는 Company Operating System에서 사용하는 코딩(Coding) 표준을 정의한다.

코딩 표준은 코드의 일관성, 가독성 및 유지보수성을 확보하기 위한 공통 기준이며,
모든 프로젝트에서 동일하게 적용한다.

---

# 2. Objectives

Coding의 목표는 다음과 같다.

- 일관된 코드 스타일을 유지한다.
- 가독성을 향상한다.
- 유지보수 비용을 줄인다.
- 협업 효율성을 높인다.
- 코드 품질을 지속적으로 유지한다.

---

# 3. Coding Principles

모든 코드는 다음 원칙을 따른다.

- 읽기 쉬운 코드를 작성한다.
- 단순한 구조를 우선한다.
- 중복을 최소화한다.
- 명확한 책임을 가진 구조를 유지한다.
- 표준을 일관되게 적용한다.

---

# 4. Naming Rules

코드의 명명 규칙은 `01_naming.md`를 따른다.

기본 규칙은 다음과 같다.

| Target | Convention |
|---------|------------|
| Class | PascalCase |
| Function | camelCase |
| Variable | camelCase |
| Constant | UPPER_SNAKE_CASE |
| File | snake_case 또는 프로젝트 표준 |
| Folder | snake_case |

---

# 5. Code Structure

코드는 다음 원칙을 따른다.

- 하나의 파일은 하나의 주요 역할을 가진다.
- 하나의 함수는 하나의 기능만 수행한다.
- 함수와 클래스는 적절한 크기를 유지한다.
- 공통 기능은 재사용 가능한 형태로 분리한다.
- 의존성을 최소화한다.

---

# 6. Error Handling

오류 처리는 다음 기준을 따른다.

- 예외 상황을 명확하게 처리한다.
- 오류 메시지는 이해하기 쉽게 작성한다.
- 필요한 경우 로그를 남긴다.
- 오류를 숨기지 않는다.
- 복구 가능한 오류와 치명적인 오류를 구분한다.

---

# 7. Code Review

코드 검토 시 다음 항목을 확인한다.

- 표준 준수 여부
- 가독성
- 중복 코드
- 불필요한 복잡성
- 유지보수성
- 성능에 영향을 주는 구조

---

# 8. Documentation

구현과 문서는 함께 관리한다.

다음 사항이 변경되면 관련 문서를 함께 수정한다.

- API
- 데이터 구조
- 비즈니스 로직
- 시스템 구조
- 운영 정책

문서와 실제 구현은 항상 일치해야 한다.

---

# 9. Relationship to Other Documents

Coding은 Standards의 마지막 문서이며,
다음 기준을 기반으로 구현을 수행한다.

```
01_naming.md

↓

02_folder.md

↓

03_metadata.md

↓

04_documentation.md

↓

05_coding.md
```

Coding은 앞선 모든 Standards를 실제 구현에 적용하는 기준이다.

---

# 10. Summary

Coding은 Company Operating System의 구현 표준이다.

모든 개발은 동일한 코딩 기준을 적용하여
가독성, 일관성 및 유지보수성을 확보하며,
문서와 구현이 항상 동일한 기준을 유지하는 것을 원칙으로 한다.