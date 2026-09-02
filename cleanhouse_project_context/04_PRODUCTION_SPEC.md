# 04_PRODUCTION_SPEC.md
# 클린하우스 입주청소 — 최종 제작설계서

상태: FINAL PRODUCTION SPEC
현재 단계: Codex 전체 구현 가능
Page Architecture: MULTI PAGE
Selected Design: B / Editorial Trust
Secondary Influence: C / Result First의 Before / After 결과 강조 방식
Primary Conversion: 견적 요청

이 문서는 `01_FACTS.md`, `02_FINAL_PLAN.md`, `03_DESIGN_DIRECTION.md`를 실제 구현 가능한 수준으로 고정한 최종 제작 기준서다.
Codex는 이 문서를 구현의 직접 기준으로 사용한다.
사업 사실이 충돌할 경우 항상 `01_FACTS.md`가 우선한다.

---

## 1. 제작 목표

클린하우스 사이트는 긴 원페이지를 읽게 만드는 구조가 아니라, 방문자가 자신의 질문에 맞는 페이지를 1~2개 확인한 뒤 견적 요청으로 이동하는 멀티페이지 전환형 사이트로 제작한다.

방문자가 빠르게 해결해야 할 핵심 질문:
- 얼마인가?
- 추가비가 생기는가?
- 어디까지 청소하는가?
- 실제로 잘하는가?
- 작업 후 문제가 생기면 어떻게 되는가?
- 원하는 지역과 일정에 가능한가?

최종 사용자 판단:
“가격과 범위를 이해했고, 결과와 보완 방식도 확인했으니 견적을 받아봐도 되겠다.”

---

## 2. 최종 사이트 구조

경로:
- `/` Home
- `/service` Service
- `/price` Price
- `/cases` Cases / Reviews
- `/guide` Guide / FAQ
- `/estimate` Estimate

공통 네비게이션:
- 서비스
- 가격
- 사례·후기
- 이용안내
- 견적 요청

Primary CTA:
- 견적 요청

Secondary Action:
- 전화 상담
- 카카오톡 상담

전화번호와 카카오톡 URL이 실제로 제공되기 전에는 임의 값을 만들지 않는다.

---

## 3. 최종 디자인 원칙

### 3.1 Visual Direction

기본 방향은 B / Editorial Trust다.

핵심 특징:
- 대형 한국어 타이포그래피
- 비대칭 편집형 레이아웃
- 이미지와 텍스트의 긴장감 있는 배치
- 가격과 실적 숫자를 강한 시각적 앵커로 사용
- 밝은 구간과 다크 구간의 명도 대비
- 카드 반복보다 페이지 목적에 맞는 레이아웃 변화
- 일반 청소업체 전단지나 저가형 템플릿 느낌 금지

C / Result First의 영향은 Cases / Reviews 및 Before / After에만 강하게 적용한다.

### 3.2 금지 패턴

- 모든 섹션을 동일한 카드 Grid로 구성
- Hero를 단순한 텍스트 50% + 사진 50% 분할로 처리
- 가격을 작은 카드 여러 개로 쪼개기
- `1,200+`를 통계 카드 안에 축소
- Before / After를 작은 썸네일 갤러리로만 처리
- 과도한 그라디언트
- 과도한 glassmorphism
- SaaS 대시보드 같은 UI
- 청소 아이콘 반복
- 과도한 라운드 카드

---

## 4. 디자인 토큰

### 4.1 Color

기본 토큰:
- `--color-canvas: #F3F1EB`
- `--color-surface: #FAF9F6`
- `--color-paper: #ECEAE4`
- `--color-ink: #20221D`
- `--color-text: #2A2D27`
- `--color-muted: #74786F`
- `--color-line: #C9CBC4`
- `--color-accent: #1F7043`
- `--color-accent-hover: #185A35`
- `--color-dark: #20221D`
- `--color-dark-muted: #B9BDB5`
- `--color-light-on-dark: #F5F4EF`

원칙:
- 기본 페이지는 warm neutral / paper 계열
- 딥 그린은 CTA와 핵심 상태 강조용
- 다크 배경은 Trust / Cases 등 핵심 Proof 장면에 제한
- 전체 사이트를 다크 테마처럼 보이게 만들지 않는다.

### 4.2 Typography

Font Stack:
- Primary Korean: `Pretendard`, `Noto Sans KR`, system sans-serif
- Editorial Accent: 필요 시 serif를 숫자 또는 짧은 영문 display에 제한적으로 사용
- 영문 utility label: clean sans 또는 mono 계열 사용 가능

Desktop Scale:
- Display XL: 72–88px / 0.96–1.03 line-height
- H1: 64–80px / 0.98–1.08
- H2: 46–60px / 1.04–1.12
- H3: 28–36px / 1.15–1.25
- Lead: 20–24px / 1.45–1.6
- Body: 16–18px / 1.65–1.8
- Small: 13–14px / 1.5–1.65
- Utility / Eyebrow: 11–13px / letter-spacing 0.06–0.12em

Mobile Scale:
- H1: 42–52px
- H2: 32–40px
- H3: 24–30px
- Body: 15–17px

한국어 본문은 장식성보다 가독성을 우선한다.

### 4.3 Layout

Content Width:
- Global max width: 1240px
- Editorial wide section: 최대 1360px 허용
- Reading text width: 680–760px

Grid:
- Desktop: 12 columns
- Tablet: 8 columns
- Mobile: 4 columns

Horizontal Padding:
- Desktop: 40–56px
- Tablet: 28–36px
- Mobile: 18–22px

Section Spacing:
- Desktop major: 120–160px
- Desktop compact: 80–100px
- Tablet: 88–120px
- Mobile: 64–88px

Spacing은 8px rhythm을 기본으로 한다.

---

## 5. 공통 Header

Desktop:
- 높이 약 88–96px
- 좌측 로고/브랜드
- 중앙 또는 우측 주요 메뉴
- 우측 Primary CTA `견적 요청`
- 전화/카카오톡은 필요 시 utility 영역 또는 하위 위계로 배치

Header 스타일:
- Hero와 자연스럽게 연결되는 light surface
- 스크롤 시 sticky 허용
- sticky 전환 시 약한 배경 불투명도 또는 solid surface 사용
- 과한 blur 효과 금지

Mobile:
- 로고
- 메뉴 버튼
- 메뉴 오픈 시 전체 화면 또는 큰 drawer
- 주요 메뉴와 견적 요청을 명확히 노출
- 필요 시 하단 fixed Primary CTA 사용 가능

---

## 6. 공통 Footer

구성:
- 브랜드명
- 주요 페이지 링크
- 전화 / 카카오톡 실제 연결값이 제공되면 노출
- 사업자 관련 정보는 실제 자료 제공 시만 추가
- 개인정보처리방침은 실제 문서 확보 후 연결

임의 사업자번호, 주소, 대표자명 생성 금지.

---

# 7. Home `/`

## 7.1 역할

전체 정보를 압축해서 반복하는 페이지가 아니라, 방문자가 빠르게 판단하고 적절한 상세 페이지로 이동하는 전환 허브다.

## 7.2 Hero

Layout:
- B / Editorial Trust 비대칭 Hero
- 텍스트와 이미지가 서로 겹치거나 교차하는 편집형 구성
- 단순 50:50 분할 금지
- 이미지가 화면의 50% 이상을 차지할 수 있으나 텍스트 위계를 침범하지 않음

H1:
- `새집의 시작을 더 깨끗하고 편안하게`

Supporting Copy:
- 입주·이사 전 공간을 꼼꼼하게 청소하고, 평수별 기본 가격과 추가비 조건을 먼저 안내한다는 의미 전달

Primary CTA:
- `청소 견적 요청하기`

Secondary navigation text:
- 가격 보기
- 서비스 범위 보기

Hero Image:
- 깨끗하게 정돈된 실제 주거공간 결과 이미지
- 실제 이미지 미제공 시 DESIGN MOCK ASSET 표시

## 7.3 대표 가격

목적:
- 가격 투명성을 빠르게 인지

구성:
- `180,000원`을 대표 숫자로 크게 표현
- `20평 이하` 명확히 연결
- 나머지 구간은 간결한 리스트
- `전체 가격 보기 → /price`

작은 가격 카드 반복 금지.

## 7.4 추가비 사전 안내

핵심 메시지:
- `추가 비용이 필요한 경우 작업 전에 안내합니다.`

표현:
- 짧고 강한 한 문장
- 작은 주의 박스보다 editorial callout 형태

## 7.5 서비스 요약

입주청소 / 이사청소의 차이를 2개의 거대한 카드로 단순화하지 않는다.

권장:
- 큰 공간 이미지와 짧은 텍스트를 교차 배치
- 상세 범위는 `/service`로 연결

## 7.6 Trust Scene

다크 배경 사용.

핵심:
- `1,200+`
- `누적 입주·이사청소 진행`

구성:
- 숫자는 화면의 주 시각 요소
- 작업 또는 결과 이미지와 결합 가능
- 숫자를 작은 stat card로 만들지 않는다.

## 7.7 Representative Before / After

C / Result First의 영향을 반영.

구성:
- 큰 이미지 2장 또는 겹침 비교
- 결과가 설명보다 먼저 보이게 함
- 실제 자료 미제공 시 DESIGN MOCK ASSET
- `/cases`로 연결

## 7.8 검수·보완 요약

핵심:
- 작업 완료 후 고객 검수
- 미흡 시 사진 접수 후 보완 방문 여부 및 일정 협의

없는 정책을 추가하지 않는다.

## 7.9 후기 요약

실제 후기 확보 전에는 Mock 표시.

권장:
- 메시지 화면을 연상시키는 typography-led layout
- 별점 카드 3개 반복 금지

## 7.10 Final CTA

Copy Direction:
- `입주 날짜가 정해졌다면, 지금 필요한 건 견적 확인입니다.`

CTA:
- `평수와 날짜 보내고 견적 받기`

---

# 8. Service `/service`

## 8.1 핵심 질문
- 어디까지 청소해주는가?

## 8.2 Hero

- 대형 공간 이미지
- 짧은 제목
- 입주청소 / 이사청소 정의
- 정보 카드보다 이미지 우선

## 8.3 서비스 구분

입주청소:
- 입주 전 빈집 전체 청소

이사청소:
- 이사 전후 생활오염과 묵은 때 중심 청소

## 8.4 기본 범위

FACT:
- 주방
- 욕실
- 창틀
- 바닥
- 수납장

표현:
- 공간마다 사진 + 텍스트 조합
- 동일한 5개 아이콘 카드 금지
- 이미지 크기와 텍스트 위치를 섹션마다 약간 달리해 실제 공간을 이동하는 리듬 생성

## 8.5 옵션

- 냉장고 내부 30,000원
- 세탁기 내부 30,000원
- 오븐 내부 20,000원
- 전자레인지 내부 20,000원

가격 상세는 `/price` 연결.

## 8.6 작업 방식

- 전문 장비
- 친환경 세제
- 공간별 체계적 청소
- 고객 검수 및 미흡 부분 보완

특정 브랜드·인증·성분을 만들지 않는다.

## 8.7 CTA

- `우리 집 청소 범위와 비용 확인하기`
- `/estimate` 연결

---

# 9. Price `/price`

## 9.1 핵심 질문
- 얼마인가?
- 추가 비용은 언제 발생하는가?

## 9.2 Hero / Lead Price

대표 숫자:
- `180,000원`
- `20평 이하`

큰 typography로 표현.

## 9.3 기본 가격표

- 20평 이하: 180,000원
- 21~30평: 230,000원
- 31~40평: 280,000원
- 41~50평: 330,000원
- 51평 이상: 상담 후 안내

UI:
- 한눈에 비교 가능한 horizontal list / clean table
- 모바일은 vertical rows
- 과도한 카드화 금지

## 9.4 옵션 가격

- 냉장고 내부: 30,000원
- 세탁기 내부: 30,000원
- 오븐 내부: 20,000원
- 전자레인지 내부: 20,000원

## 9.5 추가 비용 조건

- 베란다·창틀 오염이 심한 경우
- 반려동물 털이 많은 경우
- 심한 생활오염이 있는 경우
- 폐기물 처리가 필요한 경우

핵심 강조:
- 작업 전에 사진 확인 또는 상담을 통해 먼저 안내

## 9.6 CTA

- `우리 집 예상 견적 확인하기`

---

# 10. Cases / Reviews `/cases`

## 10.1 핵심 질문
- 실제로 잘하는가?

## 10.2 Visual Priority

이 페이지가 사이트에서 가장 이미지 중심이어야 한다.

## 10.3 Featured Before / After

- near full-width 허용
- Before와 After의 사이즈를 완전히 동일하게 고정할 필요 없음
- overlap / offset / stagger 허용
- 이미지 위 최소한의 label만 사용
- 결과 이미지가 먼저 인지되게 함

## 10.4 Case Gallery

실제 사례 확보 시:
- 대표 사례는 크게
- 나머지는 보조적인 irregular grid 가능
- Pinterest식 과밀 갤러리 금지

## 10.5 Trust Proof

- `1,200+`
- 실제 작업 이미지 또는 케이스 구간과 결합
- 숫자가 작은 카드 안에 들어가지 않음

## 10.6 Reviews

실제 카카오톡/문자 후기를 기반으로 구성.

시각 방향:
- 메시지 또는 인용문의 감각
- 고객 식별정보 비식별 처리
- 별점 SaaS 카드 반복 금지

실제 자료 미제공 시 Mock임을 명시.

## 10.7 CTA

- `우리 집도 견적 받아보기`

---

# 11. Guide / FAQ `/guide`

## 11.1 핵심 질문
- 어떻게 진행되는가?
- 문제가 생기면 어떻게 되는가?

## 11.2 Process

FACT 순서:
1. 상담 및 예약
2. 현장 정보 확인
3. 견적 안내
4. 방문 청소
5. 고객 검수
6. 미흡 부분 보완

UI:
- connected timeline
- scroll progression 또는 선으로 이어진 flow
- 동일 카드 6개 반복 금지

## 11.3 검수 및 보완

FACT:
- 작업 완료 후 고객 검수
- 미흡 확인 시 사진 접수
- 보완 방문 여부와 일정 협의

금지:
- 무료 보완 기간 생성
- 보완 횟수 생성
- 보완 보장 조건 생성

## 11.4 지역

- 서울·경기 중심
- 지역별 방문 가능 여부 상담 확인

## 11.5 예약 변경

- 최소 2일 전 요청

## 11.6 FAQ

질문:
- 기본 청소 비용은 얼마인가요?
- 추가 비용이 발생할 수 있나요?
- 옵션 청소도 가능한가요?
- 작업 후 직접 확인할 수 있나요?
- 청소가 미흡하면 어떻게 하나요?
- 서울·경기 어디든 가능한가요?
- 예약 변경은 언제까지 가능한가요?

동작:
- accordion
- 키보드 접근 가능
- 열린 항목은 시각적으로 명확히 구분
- 한 번에 여러 개 열림 여부는 구현 편의에 따라 선택 가능

---

# 12. Estimate `/estimate`

## 12.1 역할

전환 전용 페이지.
장식보다 견적 요청 완료가 우선이다.

## 12.2 Hero

짧은 제목:
- `평수와 날짜를 알려주시면 먼저 확인해드립니다.`

긴 브랜드 설명 금지.

## 12.3 Form

실제 endpoint 미제공 상태이므로 구현 시 placeholder 상태를 명확히 둔다.

권장 필드 구조:
- 평수 또는 평형 구간
- 입주청소 / 이사청소
- 희망 날짜
- 지역
- 옵션 여부
- 추가 전달사항

주의:
연락처 등 실제 운영에 필수인 필드는 최종 연결 단계에서 고객 운영 방식에 맞게 확정한다.
현재 FACT에 없는 개인정보 수집 범위나 동의 문구를 임의 확정하지 않는다.

Form States:
- default
- focus
- validation error
- submitting
- success
- failure

endpoint가 없으면 실제 전송 성공처럼 가장하지 않는다.

## 12.4 보조 정보

- 추가비 필요 시 사전 안내
- 서울·경기 중심
- 일정은 상담 후 확인

---

## 13. 이미지 규칙

### Hero
- 결과 공간 위주
- 너무 광고 스톡 같은 웃는 작업자 정면 사진 지양

### Service
- 공간별 청소 범위를 이해시키는 이미지

### Cases
- 실제 Before / After 중심

### Reviews
- 실제 후기 캡처 또는 비식별화된 재구성

### Mock
실제 자료가 없을 때 디자인 검증용 이미지 사용 가능.
반드시 `DESIGN MOCK ASSET` 또는 동등한 내부 식별 방식으로 구분한다.
공개 전 실제 자료로 교체한다.

---

## 14. Motion

Motion Intensity:
- 3 / 10

허용:
- 짧은 text reveal
- image reveal
- 8–20px 수준의 subtle vertical movement
- 숫자 강조 transition
- Before / After drag 또는 hover interaction
- process line progression

권장 duration:
- 240–650ms

금지:
- scroll hijacking
- 긴 intro animation
- 반복되는 강한 parallax
- 필수 정보가 애니메이션 완료 후에만 보이는 구조

`prefers-reduced-motion: reduce`에서는 필수 모션 제거.

---

## 15. 반응형 규칙

프로토타입 A/B/C 검토 단계에서는 desktop만 확인했지만, 최종 제작물은 responsive로 구현한다.

Desktop:
- Editorial asymmetry를 가장 강하게 표현

Tablet:
- 비대칭 구조 유지하되 겹침 정도 감소
- 2-column → 1-column 또는 8-grid 재배치

Mobile:
- 읽기 순서 우선
- 겹침 최소화
- 큰 이미지와 큰 숫자 위계는 유지
- 가격표는 vertical rows
- Before / After는 stacked 또는 swipe/drag interaction
- header는 compact
- 견적 CTA 접근성이 떨어질 경우 하단 fixed CTA 허용

모바일에서 데스크톱 화면을 단순 축소하지 않는다.

---

## 16. Interaction States

Button:
- default
- hover
- focus-visible
- active
- disabled

Link:
- underline 또는 명확한 hover/focus affordance

Form:
- error message는 입력 필드와 직접 연결
- 색상만으로 오류를 표시하지 않음

Before / After interaction을 구현할 경우:
- drag 없이도 두 이미지를 각각 확인 가능해야 함
- 터치 대응
- 키보드 사용자를 위해 대체 방식 제공

---

## 17. Accessibility

최소 기준:
- semantic heading hierarchy
- nav / main / footer landmark
- 이미지 alt 제공
- 장식 이미지는 empty alt
- keyboard navigation 가능
- focus-visible 명확
- CTA 텍스트 대비 확보
- 본문 최소 15–16px 수준 유지
- interactive target 약 44px 이상 권장
- accordion ARIA 상태 제공
- form label 명시
- prefers-reduced-motion 대응

---

## 18. 구현 컴포넌트 권장 구조

공통:
- `SiteHeader`
- `SiteFooter`
- `PrimaryCTA`
- `PageIntro`
- `EditorialSectionHeader`

Home:
- `HomeHero`
- `LeadPrice`
- `SurchargeStatement`
- `ServicePreview`
- `TrustScene`
- `FeaturedBeforeAfter`
- `PolicyPreview`
- `ReviewPreview`
- `FinalCTA`

Service:
- `ServiceHero`
- `ServiceTypeIntro`
- `SpaceStory`
- `OptionList`
- `MethodStatement`

Price:
- `PriceHero`
- `BasePriceTable`
- `OptionPriceList`
- `SurchargeConditions`

Cases:
- `CasesHero`
- `FeaturedCase`
- `CaseGallery`
- `ProofNumber`
- `ReviewStream`

Guide:
- `ProcessTimeline`
- `InspectionPolicy`
- `ServiceArea`
- `BookingPolicy`
- `FAQAccordion`

Estimate:
- `EstimateIntro`
- `EstimateForm`
- `EstimateSupportInfo`

컴포넌트화는 재사용을 위한 것이며, 모든 페이지를 동일한 카드 스타일로 강제하는 용도로 사용하지 않는다.

---

## 19. FACT / MOCK / PLACEHOLDER 상태

### CONFIRMED FACT
변경 금지:
- 입주청소
- 이사청소
- 청소 범위
- 가격
- 옵션 가격
- 추가비 조건
- 작업 과정
- 서울·경기 중심
- 검수·보완 정책
- 예약 변경 최소 2일 전
- 전문 장비
- 친환경 세제
- 1,200건+

### DESIGN MOCK ASSET
임시 사용 가능:
- Hero 사진
- 서비스 사진
- Before / After
- 후기 시안
- 샘플 고객명

### CONNECTION PLACEHOLDER
아직 미제공:
- 전화번호
- 카카오톡 URL
- 폼 endpoint
- 개인정보처리방침
- 개인정보 수집 동의

연결값을 임의 생성하지 않는다.

---

## 20. 공개 전 필수 교체 / 확인

- 실제 Hero 사진
- 실제 서비스 사진
- 실제 Before / After
- 실제 후기 원본 및 비식별 처리
- 전화번호
- 카카오톡 URL
- 문의폼 endpoint
- 개인정보처리방침
- 개인정보 수집 동의
- 실제 공개 가능한 1,200건+ 근거 확인
- 실제 가격표 최종 확인
- 서비스 지역 최종 확인
- 정책 문구 최종 확인

---

## 21. QA Acceptance Criteria

### 구조
- 6개 경로가 모두 정상 동작
- 공통 Header / Footer 정상
- 모든 주요 페이지에서 Estimate로 이동 가능

### 디자인
- B / Editorial Trust가 전체 기준으로 유지됨
- Hero만이 아니라 Price / Trust / Cases / Guide까지 페이지별 레이아웃 개성이 있음
- 동일 카드 UI 반복에 의존하지 않음
- Cases의 Before / After가 충분히 강한 Proof 장면으로 보임
- `180,000원`, `1,200+`가 시각적 앵커로 작동

### 정보
- FACT가 `01_FACTS.md`와 일치
- 미확정 정책을 생성하지 않음
- 옵션/가격/추가비 조건 누락 없음

### Conversion
- Primary CTA가 명확함
- 한 화면에서 동일 위계 Primary CTA가 과도하게 경쟁하지 않음
- Home에서 상세 페이지와 Estimate로 이동 경로가 명확함

### Responsive
- Desktop / Tablet / Mobile에서 레이아웃 깨짐 없음
- 모바일에서 typography와 이미지 위계 유지
- 가로 스크롤 없음

### Accessibility
- keyboard navigation 가능
- focus-visible 존재
- contrast 문제 없음
- accordion / form 접근성 처리
- reduced motion 지원

### Asset Safety
- Mock asset이 실제 사례처럼 보이지 않음
- 실제 연결정보가 없는 상태에서 가짜 전화번호/URL/성공 전송을 만들지 않음

---

## 22. Codex 구현 우선순위

문서 우선순위:
1. `01_FACTS.md`
2. `02_FINAL_PLAN.md`
3. `03_DESIGN_DIRECTION.md`
4. `04_PRODUCTION_SPEC.md`

충돌 시:
- 사업 사실은 `01_FACTS.md`
- 페이지 목적과 전환 전략은 `02_FINAL_PLAN.md`
- 비주얼 기준은 `03_DESIGN_DIRECTION.md`
- 구체 구현 규칙은 `04_PRODUCTION_SPEC.md`

임의로 사실이나 정책을 만들어 충돌을 해결하지 않는다.

---

## 23. 최종 판정

기획: 확정
Page Architecture: MULTI PAGE 확정
디자인 방향: B / Editorial Trust 확정
Before / After 보완 방향: C / Result First 일부 반영 확정
Creative Build Brief: 확정
최종 제작설계서: 확정

현재 상태에서는 Codex가 전체 멀티페이지 구현에 착수할 수 있다.

단, 실제 공개는 `20. 공개 전 필수 교체 / 확인` 항목이 완료된 이후에만 가능하다.
