# 03_document_governance.md

> Version: 1.1
> Status: Draft
> Owner: CEO
> Category: Foundation

---

# 1. Purpose

본 문서는 Company Operating System의 모든 문서를 관리하고 유지하기 위한 Document Governance 기준을 정의한다.

문서는 단순한 기록이 아니라 회사의 공식 지식이며,
회사의 운영, 설계, 의사결정 및 시스템 구축의 기준으로 사용한다.

본 문서는 문서의 세부 작성 규칙이 아니라,

* 소유권
* 상태
* 승인
* 변경
* 생명주기
* 유지관리

에 대한 최상위 관리 원칙을 정의한다.

세부 작성 및 관리 규칙은 `05_standards/`의 관련 문서를 따른다.

---

# 2. Objectives

Document Governance의 목표는 다음과 같다.

* 회사의 공식 문서를 명확하게 관리한다.
* 문서별 관리 책임을 명확하게 한다.
* 문서의 현재 상태를 확인할 수 있도록 한다.
* 변경 사항을 추적할 수 있도록 한다.
* 오래된 문서가 공식 기준으로 사용되는 것을 방지한다.
* 동일한 내용을 여러 문서에서 중복 관리하지 않는다.
* 문서와 실제 운영 및 시스템의 일관성을 유지한다.

---

# 3. Governance Principles

모든 문서는 다음 원칙을 따른다.

## Single Responsibility

하나의 문서는 하나의 주요 목적과 책임을 가진다.

서로 다른 도메인의 내용을 하나의 문서에서 불필요하게 혼합하지 않는다.

---

## Single Source of Truth

동일한 기준은 하나의 문서에서만 정의한다.

다른 문서에서 동일한 내용을 다시 정의하지 않고,
필요한 경우 원본 문서를 참조한다.

---

## Ownership

모든 문서는 명확한 Owner를 가진다.

Owner는 해당 문서의 정확성, 최신성 및 실제 운영과의 일치 여부를 관리한다.

---

## Traceability

중요한 변경은 추적 가능해야 한다.

문서의 현재 상태와 버전을 통해
어떤 기준이 현재 적용되고 있는지 확인할 수 있어야 한다.

---

## Operational Consistency

문서와 실제 운영 또는 시스템이 서로 다른 상태로 장기간 유지되어서는 안 된다.

운영이나 시스템이 변경되면 관련 문서를 함께 검토한다.

---

## AI Compatibility

문서는 사람뿐 아니라 AI가 회사의 공식 지식으로 활용할 수 있는 형태로 유지한다.

AI가 서로 충돌하는 여러 기준을 참조하지 않도록
원본 문서를 명확하게 유지한다.

---

# 4. Document Authority

Company Operating System의 문서는 회사 운영과 시스템 설계의 공식 기준으로 사용한다.

문서의 상태에 따라 권한을 구분한다.

| Status   | Authority               |
| -------- | ----------------------- |
| Draft    | 작성 중이며 공식 기준으로 사용하지 않음  |
| Review   | 검토 중이며 공식 기준으로 확정되지 않음  |
| Approved | 승인된 기준                  |
| Archived | 더 이상 현재 기준으로 사용하지 않는 문서 |

현재 적용되는 공식 기준은 Approved 상태의 문서를 우선한다.

---

# 5. Document Ownership

모든 문서는 하나의 Owner를 가진다.

기본 Ownership은 다음과 같다.

| Category     | Owner     |
| ------------ | --------- |
| Foundation   | CEO       |
| Organization | 해당 조직 책임자 |
| Intelligence | COO       |
| Platform     | CTO       |
| Engines      | CTO       |
| Standards    | COO       |

Owner는 문서를 직접 작성하는 사람을 의미하지 않는다.

Owner는 해당 문서가 회사의 실제 기준과 일치하도록 관리할 책임을 가진다.

1인 기업 단계에서는 한 사람이 여러 Owner 역할을 동시에 수행할 수 있다.

---

# 6. Document Lifecycle

모든 문서는 다음 생명주기를 따른다.

```text
Create

↓

Review

↓

Approve

↓

Use

↓

Update

↓

Archive
```

문서는 한 번 작성하고 종료되는 산출물이 아니다.

실제 회사 운영과 시스템 변화에 따라 지속적으로 관리한다.

---

# 7. Review & Approval

문서는 다음 상태를 기준으로 관리한다.

```text
Draft

↓

Review

↓

Approved
```

더 이상 현재 기준으로 사용하지 않는 문서는 다음 상태로 전환한다.

```text
Approved

↓

Archived
```

승인되지 않은 문서는 공식 운영 기준으로 간주하지 않는다.

1인 기업 단계에서는 동일한 사람이 작성자와 승인자 역할을 수행할 수 있다.

회사가 성장하면 역할에 따라 검토와 승인 책임을 분리할 수 있다.

---

# 8. Change Management

다음과 같은 변경이 발생하면 관련 문서를 검토한다.

* 조직 구조 변경
* 역할 또는 책임 변경
* 운영 프로세스 변경
* 데이터 구조 변경
* 시스템 구조 변경
* AI Engine 변경
* 회사 표준 변경

모든 작은 수정에 복잡한 승인 절차를 적용하지 않는다.

회사의 운영 기준이나 시스템 동작에 영향을 주는 변경을 우선적으로 관리한다.

---

# 9. Version Management

문서는 Version을 통해 주요 변경 상태를 관리한다.

기본 버전은 다음 형태를 사용한다.

```text
1.0
1.1
1.2
2.0
```

기준은 다음과 같다.

### Minor Version

기존 목적과 구조를 유지하면서 내용을 수정하거나 보완한 경우 사용한다.

예:

```text
1.0 → 1.1
```

### Major Version

문서의 목적, 책임 또는 핵심 구조가 크게 변경된 경우 사용한다.

예:

```text
1.2 → 2.0
```

단순한 오탈자 수정 등 의미에 영향을 주지 않는 변경까지 과도하게 버전 관리하지 않는다.

---

# 10. Archive

더 이상 현재 기준으로 사용하지 않는 문서는 삭제보다 Archive를 우선한다.

Archive된 문서는 과거의 운영 방식과 시스템 변화를 확인하기 위한 기록으로 유지할 수 있다.

Archived 문서는 현재 기준과 명확하게 구분되어야 한다.

AI 또는 사람이 현재 기준을 조회할 때 Archived 문서를 최신 기준으로 오인하지 않도록 한다.

---

# 11. Standards Relationship

Document Governance는 문서 관리의 상위 원칙을 정의한다.

세부 규칙은 `05_standards/`에서 관리한다.

```text
Document Governance
        ↓
05_standards/
        ↓
Naming
Documentation
Metadata
Folder
```

각 역할은 다음과 같이 구분한다.

| Document                           | Responsibility            |
| ---------------------------------- | ------------------------- |
| `03_document_governance.md`        | 문서의 소유권, 상태, 승인, 변경, 생명주기 |
| `05_standards/01_naming.md`        | 명명 규칙                     |
| `05_standards/02_documentation.md` | 문서 작성 기준                  |
| `05_standards/03_metadata.md`      | Metadata 기준               |
| `05_standards/04_folder.md`        | 폴더 구조 및 배치 기준             |

동일한 세부 규칙을 여러 문서에서 중복 정의하지 않는다.

---

# 12. AI Usage

AI가 Company Operating System의 문서를 사용할 경우 다음 원칙을 따른다.

* Approved 문서를 공식 기준으로 우선한다.
* Archived 문서를 현재 기준으로 사용하지 않는다.
* 동일한 정보가 존재할 경우 원본 문서를 우선한다.
* 문서에 존재하지 않는 회사 정책이나 사실을 임의로 생성하지 않는다.
* 서로 충돌하는 문서가 발견되면 임의로 판단하지 않고 충돌 사실을 식별한다.

Company Operating System의 문서는 향후 Company AI가 회사의 운영 기준을 이해하기 위한 공식 지식 기반으로 활용될 수 있다.

---

# 13. Governance Scope

Document Governance는 문서가 어떤 형식으로 작성되는지를 세세하게 규정하는 것이 목적이 아니다.

본 문서가 관리하는 것은 다음이다.

```text
누가 관리하는가

↓

현재 어떤 상태인가

↓

어떤 문서가 공식 기준인가

↓

언제 변경해야 하는가

↓

언제 더 이상 사용하지 않는가
```

세부 작성 방식은 Standards에서 관리한다.

---

# 14. Summary

Document Governance는 Company Operating System의 공식 문서를 관리하는 최상위 기준이다.

모든 문서는 명확한 Owner와 상태를 가지며,
변경과 생명주기를 추적할 수 있어야 한다.

세부 작성 규칙은 Standards에서 관리하고,
Document Governance는 문서의 권한과 관리 체계를 담당한다.

이를 통해 회사의 공식 지식이 중복되거나 충돌하지 않고,
사람과 AI가 동일한 기준을 사용할 수 있도록 한다.
