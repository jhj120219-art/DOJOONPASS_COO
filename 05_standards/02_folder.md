# 02_folder.md

> Version: 1.0
> Status: Draft
> Owner: COO
> Category: Standards

---

# 1. Purpose

본 문서는 Company Operating System에서 사용하는 폴더(Folder) 구조와 관리 기준을 정의한다.

일관된 폴더 구조는 문서와 소스코드의 위치를 명확하게 하며,
유지보수성과 검색 효율성을 높이기 위한 기준이 된다.

---

# 2. Objectives

Folder의 목표는 다음과 같다.

- 일관된 디렉터리 구조를 유지한다.
- 문서와 자산의 위치를 명확하게 한다.
- 중복 저장을 방지한다.
- 유지보수와 확장을 용이하게 한다.

---

# 3. Folder Principles

모든 폴더는 다음 원칙을 따른다.

- 하나의 폴더는 하나의 목적만 가진다.
- 동일한 종류의 파일은 동일한 폴더에서 관리한다.
- 폴더 간 역할이 중복되지 않아야 한다.
- 불필요한 계층 구조를 만들지 않는다.
- 동일한 구조를 프로젝트 전체에 적용한다.

---

# 4. Folder Structure

최상위 폴더는 도메인 단위로 구성한다.

```
00_foundation/

01_organization/

02_intelligence/

03_platform/

04_engines/

05_standards/
```

각 폴더는 하나의 도메인만 담당한다.

---

# 5. Naming Rules

폴더명은 다음 규칙을 따른다.

- 두 자리 번호를 사용한다.
- 소문자를 사용한다.
- snake_case를 사용한다.
- 의미를 명확하게 표현한다.

예시

```
00_foundation

02_intelligence

05_standards
```

---

# 6. File Placement

파일은 가장 적절한 도메인 폴더에 저장한다.

동일한 파일을 여러 위치에 저장하지 않는다.

공통 내용은 하나의 문서에서만 관리하며,
다른 문서에서는 참조를 원칙으로 한다.

---

# 7. Folder Management

폴더를 생성하거나 변경할 경우 다음 기준을 따른다.

- 목적이 명확해야 한다.
- 기존 구조와 중복되지 않아야 한다.
- 관련 문서를 함께 정리한다.
- 변경 내용을 문서화한다.

---

# 8. Relationship to Other Documents

Folder는 다음 문서와 연결된다.

```
01_naming.md

↓

02_folder.md

↓

03_metadata.md
```

Naming은 이름을 정의하고,
Folder는 위치를 정의하며,
Metadata는 파일의 관리 정보를 정의한다.

---

# 9. Summary

Folder는 Company Operating System의 정보 구조를 구성하는 기준이다.

모든 문서와 자산은 정의된 폴더 구조를 따르며,
일관성, 검색성 및 유지보수성을 유지하는 것을 기본 원칙으로 한다.