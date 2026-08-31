# 04_PRODUCTION_SPEC.md
# 클린하우스 입주청소 — 제작설계서

상태: NOT FINAL
주의: 디자인 방향 선택 전 최종 구현 금지.

## 현재 단계
온보딩
→ 추가 확인
→ 최종기획
→ 디자인 모드 판정
→ 디자인 시안 비교
→ 디자인 방향 선택
→ 이 파일 최종 확정
→ Codex 구현
→ QA

현재는 디자인 시안 비교 단계다.

## 이 파일의 역할
최종 선택된 디자인 방향을 실제 구현 가능한 단일 기준서로 변환한다.

최종본에는 반드시 아래 내용이 포함되어야 한다.

### 1. 구현 범위
- 원페이지 여부
- 페이지/라우트 구조
- 앵커 ID
- Header / Footer
- 모바일 고정 CTA

### 2. 디자인 시스템
- 색상 토큰
- 타이포 스케일
- spacing
- radius
- border/shadow
- container width
- grid
- responsive breakpoint

### 3. 섹션별 상세 규칙
각 섹션마다:
- 목적
- 핵심 메시지
- 콘텐츠
- 시각 구조
- 이미지 사용 방식
- Primary CTA 여부 및 문구
- Secondary Action 처리
- 모바일 변화
- 상태 / placeholder / mock 교체 기준

### 4. CTA 규칙
- 한 화면/주요 섹션에 Primary CTA 최대 1개
- 동일 위계의 CTA 병렬 배치 금지
- 전화/카카오톡은 Secondary Action으로 처리
- 모바일에서도 우선 행동 하나가 명확해야 함

### 5. 이미지 규칙
- Hero
- 서비스 범위
- Before / After
- 후기/증거
- 테스트용 DESIGN MOCK ASSET 교체 기준

### 6. 모션 규칙
최종 디자인 방향에 따라:
- scroll reveal
- layer movement
- parallax 허용 범위
- hover interaction
- reduced-motion 대응
- 모바일에서 축소할 효과

### 7. 접근성
- 텍스트 대비
- keyboard focus
- button/link semantics
- accordion 접근성
- form label / error
- reduced motion

### 8. 폼 및 연결
실제 값 미제공 시 placeholder 사용:
- 전화번호
- 카카오톡 URL
- 문의폼 endpoint
- 개인정보 처리방침
- 개인정보 수집 동의

임의 값 생성 금지.

### 9. 공개 전 교체·검증
- 가격
- 실적
- 후기
- 작업사진
- Before / After
- 친환경 세제 표현
- 서비스 지역
- 연락처
- 법적 고지

## 현재 구현 제한
디자인 방향이 선택되기 전에는:
- 전체 프로덕션 홈페이지 구현 금지
- 최종 컴포넌트 구조 고정 금지
- 세부 애니메이션 구현값 확정 금지
- 최종 breakpoint 수치 확정 금지

시안 비교를 위한 임시 정적 화면 또는 mock은 가능하다.

## 다음 업데이트 조건
`03_DESIGN_DIRECTION.md`가 DESIGN SELECTED 상태가 되면,
01_FACTS.md + 02_FINAL_PLAN.md + 03_DESIGN_DIRECTION.md를 기준으로 이 파일을 FINAL PRODUCTION SPEC으로 업데이트한다.
