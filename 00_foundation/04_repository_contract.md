# 04_repository_contract.md

> Version: 1.0
> Status: Draft
> Owner: CEO
> Category: Foundation

---

# COO ↔ COMPANY_OPS Repository Contract v1

Parties: DOJOONPASS_COO, DOJOONPASS_COMPANY_OPS

---

# 1. Source of Truth

- COO: Company / Organization / Intelligence 설계 / Platform·Engine·Standards 원칙
- COMPANY_OPS: 자신의 Project 스펙(docs/), Event/History 실데이터, Runtime State
- Knowledge: SoT 미확정 (설계=COO, 데이터=미구현)

---

# 2. Ownership

- COO 문서: COO 자체 Document Governance를 따른다.
- COMPANY_OPS 문서/코드: COMPANY_OPS README §2를 따른다.
- 교차 인용 정확성: 인용하는 쪽이 책임진다.

---

# 3. Dependency

- COMPANY_OPS → COO: 개념/표준 의존 (문서 참조)
- COO → COMPANY_OPS: 실증 근거 의존 (문서 참조)
- 코드 레벨 의존: 없음 (양방향)

---

# 4. Allowed Direction

- 문서 간 링크/인용(양방향)

---

# 5. Forbidden Direction

- 파일 복사·병합 금지
- 코드의 상대 저장소 직접 참조(import/read) 금지
- 상대 저장소 문서의 일방적 수정 금지
- COO의 COMPANY_OPS 구현 세부사항 규범적 인용 금지(예시 각주만 허용)

---

# 6. Synchronization Rule

- 자동 동기화 없음, 독립적 clone/pull/push 유지
- 계층 변경 시 상대측 인용부 수동 재검토

---

# 7. Versioning Rule

- COO: 기존 Version/Status 필드 유지
- COMPANY_OPS: 버전 필드 도입 권장(별도 Phase)
- 저장소 간 커밋 고정 없음, Contract 자체만 버전 관리(v1, v2...)

---

# 8. Change Management Rule

- COO Company/Organization 변경 = Breaking → COMPANY_OPS README §2 재검토
- COO Intelligence Entity 추가 = Non-breaking / 삭제·의미변경 = Breaking
- COMPANY_OPS Event Schema 변경 = COO 실증 근거 갱신 플래그
- 본 Contract 변경 = 관계자 명시적 재승인 필요
