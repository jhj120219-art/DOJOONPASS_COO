# 05_repository_registry.md

> Version: 1.0
> Status: Draft
> Owner: CEO
> Category: Foundation

---

# Repository Registry

Parties: dojoonpass, dojoonpass-content-os, DOJOONPASS_COO, DOJOONPASS_COMPANY_OPS

---

# 1. Purpose

본 문서는 4개 Repository(dojoonpass, dojoonpass-content-os, DOJOONPASS_COO, DOJOONPASS_COMPANY_OPS)의
역할, Owner, 입력, 출력, 참조 관계를 하나의 표로 통합한다.

본 문서는 각 Repository의 기존 내용을 이동하거나 복사하지 않는다.
위치, 소유, 참조 관계만 정리한다.

본 문서는 새로운 전략이나 기능을 정의하지 않는다.

---

# 2. Repository Registry Table

| Repository | 역할 | Owner | 입력 | 출력 | 참조 대상 | 참조 받는 대상 |
|---|---|---|---|---|---|---|
| dojoonpass | 제품 본체(콕찰/Kokchal) — 프론트엔드/백엔드/크롤러 + CEO 전략 문서 + CMO 문서 호스팅 | CEO(전략) / CTO(구현) | 법원경매 크롤링 데이터, Supabase Auth, 사용자 검색 요청 | `/api/v1/search`, 등기부 신청 API, 웹 애플리케이션, CEO/CMO 내부 문서 | 없음 | dojoonpass-content-os (비공식 런타임 호출) |
| dojoonpass-content-os | 콘텐츠 파이프라인 엔진(Engine A/B/C, Engine A v2) | CMO | dojoonpass Search API(런타임 호출), 외부 데이터소스, CEO/CTO 정책(복사본) | ResearchResult(schemaVersion 2.0.0), 채널별 콘텐츠, PublishResult | dojoonpass(문서 인용 + API 호출), 외부 Content OS Core(소재 미확인) | 확인된 참조 없음 |
| DOJOONPASS_COO | Company Operating System 메타 저장소 — Mission/Vision/Organization/Platform 설계/Standards | COO(Intelligence/Standards), CEO(Foundation), CTO(Platform/Engines, 문서상 태그) | 없음(정적 설계 문서) | Mission/Vision/Roadmap/역할정의/Repository Contract v1/본 Registry | DOJOONPASS_COMPANY_OPS(계약서 명시) | DOJOONPASS_COMPANY_OPS(참조 시 저장소명 표기 오류 존재, 별도 목록 관리) |
| DOJOONPASS_COMPANY_OPS | 실행 이벤트 수집 → Company History 자동화 파이프라인 | COO(end-to-end) | Desktop 1-4의 실행 이벤트(Reporter) | Event(schema_version 1.0), Notion Sync, Company History 아카이브 | DOJOONPASS_COO의 Repository Contract(참조 시 저장소명 표기 오류 존재), "Content OS"(project_id 예시로만 언급) | 확인된 참조 없음 |

---

# 3. Source

본 문서의 근거는 2026-08-04 COO Sprint Audit 및 Integration Sprint 결과이다.

새로운 사실은 추가하지 않았으며, 각 Repository의 기존 문서와 구조를 확인한 결과만 반영한다.

세부 근거(Source of Truth 항목별 문서 경로, Runtime Contract 세부 목록, Reference Error 목록)는
별도의 Audit/Integration Sprint 산출물을 따른다.

---

# 4. Maintenance

본 문서는 각 Repository의 구조 또는 참조 관계가 변경될 때 갱신한다.

갱신 시 근거가 되는 Repository 내 실제 문서 위치를 함께 기록한다.

본 문서 자체의 내용 변경은 `03_document_governance.md`의 Version/Status 관리 기준을 따른다.
