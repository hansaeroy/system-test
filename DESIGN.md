# Cleanhouse Design Exploration Contract

상태: DESIGN PROTOTYPE ONLY

이 문서는 최종 제작설계서가 아니라, `Home`의 대표 4구간을 A/B/C로 비교하기 위한 시각 검증 계약이다. 사업 사실과 멀티페이지 전략은 `cleanhouse_project_context/01_FACTS.md`, `02_FINAL_PLAN.md`을 따른다.

## 고정 입력

- Page Architecture: MULTI PAGE
- Primary Conversion: 견적 요청
- Hero: `새집의 시작을 더 깨끗하고 편안하게`
- Primary CTA: `청소 견적 요청하기`
- 가격: 20평 이하 180,000원 / 21~30평 230,000원 / 31~40평 280,000원 / 41~50평 330,000원 / 51평 이상 상담
- 신뢰: `누적 1,200건+ 입주·이사청소 진행`
- 추가 비용: 필요한 경우 작업 전에 안내
- 대표 구간: Hero / 가격 요약 / 1,200건+ 신뢰 / Before & After

## 공통 토큰

- type: `Pretendard`, `Noto Sans KR`, system sans fallback
- content max: 1240px
- base spacing: 8px rhythm
- primary action: deep green `#1f7043`
- body ink: `#17211c`
- no gradients used as the primary visual device; image treatment and layout carry the distinction
- mock imagery uses Unsplash image URLs and is visibly labelled `DESIGN MOCK ASSET`

## Directions

### A / Clean Premium

White canvas, deep green accent, generous 120px section rhythm. Hero is a 42/58 split with a large home image. Price is a dedicated horizontal table. Trust is a centered numeric monument with surrounding whitespace. Before/After is one wide two-image case spread.

### B / Editorial Trust

Ink-and-paper palette, high-contrast display scale, asymmetrically overlaid Hero, numbered editorial labels, and a giant `1,200+` paired with a work image. Price uses a featured `180,000원` typographic lead plus a separate index list. Before/After uses offset vertical images rather than a split.

### C / Result First

Dark charcoal shell, luminous green signal, image-led composition. Hero is a full-bleed completed-space image with text layered over it. Price is a floating light panel over a second image. Trust is a work image and numeric proof in one composition. Before/After is a near full-width overlapping comparison and the dominant scene.

## Structural separation rule

Each direction has its own section markup and layout selectors: `a-*`, `b-*`, and `c-*`. Only navigation, typography tokens, color tokens, and the primary CTA are shared. Pricing, trust, and Before/After are not shared components.

## Prototype limits

- This prototype does not implement Service / Price / Cases / Guide / Estimate pages.
- Phone, KakaoTalk, form endpoint, real photography, reviews, and policy links are not invented.
- Desktop comparison is the acceptance target for this stage; mobile adaptation is intentionally out of scope for this prototype.
- Motion is limited to short reveal/hover transitions and must not be necessary to understand content.
