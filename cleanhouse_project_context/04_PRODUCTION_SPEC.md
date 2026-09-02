# 04_PRODUCTION_SPEC.md
# 클린하우스 입주청소 — 제작설계서 상태

상태: ON HOLD — VISUAL DESIGN RESET
현재 단계: Visual Exploration 진행 전
Page Architecture: MULTI PAGE
Primary Conversion: 견적 요청

## 1. 상태 변경 이유

이 파일은 이전에 `FINAL PRODUCTION SPEC`으로 확정되어 있었으나, 실제 화면 디자인을 충분히 확정하기 전에 디자인 방향과 구현 규칙을 먼저 고정한 문제가 확인되었다.

따라서 기존 B / Editorial Trust 기반 최종 제작설계서는 현재 구현 기준으로 사용하지 않는다.
GitHub 이력에는 남아 있으나, 새 디자인 탐색이 끝나기 전에는 Codex 전체 구현 기준으로 참조하지 않는다.

## 2. 현재 우선순위

현재 프로젝트 우선순위는 다음과 같다.

1. `01_FACTS.md`
2. `02_FINAL_PLAN.md`
3. `03_DESIGN_DIRECTION.md` — 현재는 Visual Exploration Brief
4. 실제 Visual Exploration 결과
5. Visual QA / 선택 결과
6. 선택 화면에서 추출한 Design System
7. 새 `04_PRODUCTION_SPEC.md`
8. Codex 전체 구현

## 3. 현재 구현 금지

Visual Exploration과 디자인 선택이 끝나기 전에는 다음을 완료 처리하지 않는다.

- 전체 멀티페이지 최종 구현
- 기존 B 프로토타입 기준 확장
- 기존 색상 토큰을 최종값으로 사용
- 기존 타이포 스케일을 최종값으로 사용
- 기존 레이아웃 규칙을 최종값으로 사용
- 기존 Production Spec을 그대로 복원하여 구현

## 4. 현재 허용 작업

- Hero 시각 시안
- Price 시각 시안
- Trust / `1,200+` 시각 시안
- Before / After 시각 시안
- 각 시안의 이미지·타이포·구성·여백 실험
- 디자인 QA 및 실제 화면 선택

## 5. 다음 확정 조건

다음 네 가지 실제 화면이 선택되어야 Production Spec 작성으로 넘어간다.

- Hero
- Price
- Trust / Proof
- Before / After

선택 후 실제 화면에서 다음을 추출한다.

- Color System
- Typography System
- Grid / Layout logic
- Spacing rhythm
- Image ratios / crop rules
- Numeric treatment
- Section rhythm
- Motion language
- CTA treatment
- Reusable vs page-specific composition rules

그 결과를 바탕으로 이 파일을 다시 `FINAL PRODUCTION SPEC`으로 작성한다.

## 6. 기존 문서 처리

`01_FACTS.md`와 `02_FINAL_PLAN.md`는 유지한다.

`03_DESIGN_DIRECTION.md`는 기존의 디자인 선택 문서가 아니라 현재 Visual Exploration Brief로 사용한다.

과거 B / Editorial Trust 시안과 A/B/C 프로토타입은 실험 기록일 뿐이며 새 디자인 생성의 Source of Truth가 아니다.

## 7. 현재 다음 액션

`03_DESIGN_DIRECTION.md`를 기준으로 코드 구현이 아닌 실제 Visual Exploration을 시작한다.

먼저 Hero / Price / Trust / Before & After 대표 4구간의 시안을 만들고 실제 화면으로 검토한다.
