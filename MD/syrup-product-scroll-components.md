# Syrup Design System — Product Scroll 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Product Scroll` 페이지 → [Product Scroll 섹션 `9354:27924`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9354-27924) |
| 섹션 크기 | 1440 × 1803 |
| 컴포넌트 수 | **2개** (전부 Component Set) |
| 기준일 | 2026-11-09 (가이드라인·Usage 갱신) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **상품 정보를 가로 스크롤 레이아웃으로 구성해 보여주는 컴포넌트예요.**
> 상품 이미지, 가격, 혜택, 상태 등 필요한 정보를 좌우로 탐색할 수 있도록 상품 목록을 구성할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Product Scroll / Scroll Item` | `8964:9838` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Product Scroll — Master Component](#1-product-scroll--master-component)
3. [Child Item — Scroll Item](#2-child-item--scroll-item)
4. [가이드라인](#가이드라인)
5. [Usage — 사용 예제](#usage--사용-예제)
6. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

마스터 1종과 primitive 1종으로 구성돼요. 별도 섹션에 가이드라인 2개와 Usage 2개를 정리했어요. 기존 노드·인스턴스 집계는 2026-10-12 기준이며, 새 사용 화면과 예제는 포함하지 않아요.

### Product 3형제

[Product Grid](syrup-product-grid-components.md) · [Product List](syrup-product-list-components.md)와 함께 콘텐츠를 배치하는 방식과 정보 구성에 맞춰 선택해요.

| | Product Grid | Product List | **Product Scroll** |
| --- | --- | --- | --- |
| 배치 | 가로 **WRAP 격자** | **세로 1열** | **가로 1줄 스크롤** |
| 폭 | 312~360 (화면 안) | 328~360 (화면 안) | **648~728 (화면 밖으로 넘침)** |
| 아이템 | 이미지 위 · 텍스트 아래 | 이미지 좌 · 텍스트 우 | **이미지 위 · 텍스트 아래** |

마스터 폭이 화면(360)을 넘는 것은 [Grid Scroll](syrup-grid-scroll-components.md)과 같은 방식으로, **가로 스크롤 영역을 Figma에서 펼쳐 표현**한 것입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Product Scroll` 2종 |
| y 1186 | Child Item | `Product Scroll / Scroll Item` 2종 |
| 별도 섹션 | [Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1094) | 유형 선택·가로 스크롤 배치 2개 |
| 별도 섹션 | [Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1095) | 심리테스트·출석 제휴 상품 예제 2개 |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Product Scroll` | Set | `Variant` 2종 | 648~728 × 144 / 192 | **0** |
| 2 | `Product Scroll / Scroll Item` | Set | `Variant` 2종 + `Gold` · `Image` | 84~120 × 144 / 173 | 13 |

---

## 1. Product Scroll — Master Component

**Node** `8964:9728` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Personality Test` | `Personality Test` · `Check-in` |

| Variant | 크기 | Gap | 담는 아이템 |
| --- | --- | --- | --- |
| `Personality Test` | **728** × 144 | `Spacing/200` (8) | **8개** |
| `Check-in` | **648** × 192 | `Spacing/300` (12) | **5개** |

공통 — Padding 0, 배경 없음, 가로 오토레이아웃

위 폭과 아이템 수는 마스터에 펼쳐 놓은 샘플 구성이에요. 화면에 보이는 스크롤 영역의 폭이나 실제 항목 수를 고정하는 값이 아니에요. 사용 영역의 폭을 제한하고, 안쪽 콘텐츠는 한 줄로 유지해요.

**두 variant 모두 primitive 인스턴스만 나열한 래퍼**입니다. 실제 모양은 안쪽이 결정합니다.

자식 레이어 이름은 **`Scroll Item`** 입니다. (2026-10-12 `Grid Scroll Item` → `Scroll Item` 13건 정리 → [점검 2](#2--자식-레이어명-정리-2026-10-12-완료))

---

## 2. Child Item — Scroll Item

**Node** `8964:9838` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Personality Test` | `Personality Test` · `Check-in` |
| `Gold` | BOOLEAN | `true` | — |
| `Image` | BOOLEAN | **`false`** | — |

### Variant=Personality Test

| 항목 | 값 |
| --- | --- |
| 크기 | **84 × 144** |
| Padding · Gap | 0 / `Spacing/250` (10) |
| 배경 | 없음 |

| 레이어 | 크기 | 스펙 |
| --- | --- | --- |
| `Image` | 84 × 116 | `Color/Gray_950` · `Corner radius/150` (6) |
| `Text` | 84 × 18 | 좌우 패딩 `Spacing/100`(4) · `b500_13_regular` · `Color/Gray_100` |

### Variant=Check-in

| 항목 | 값 |
| --- | --- |
| 크기 | **120 × 173** |
| Padding · Gap | 0 / `Spacing/300` (12) |
| 배경 | **`Color/Gray_White`** |

| 레이어 | 크기 | 스펙 |
| --- | --- | --- |
| `Image` | 120 × 120 | `Color/Gray_950` · `Corner radius/250` (10) |
| `Text` | 120 × 41 | 좌우 패딩 `Spacing/50`(2) · 내부 간격 `Spacing/50`(2) |
| └ `Text` | 116 × 19 | `t1300_15_medium` · **`Color/Gray_500`** |
| └ `Price` | 116 × 20 | `t900_16_bold` · **`Color/Gray_200`** |

`Check-in`은 상품명과 가격 영역을 함께 사용하고, 이미지는 정사각(120 × 120)이에요. 위 120 × 173은 한 줄 상품명 기준의 primitive 크기이며, 두 줄 상품명을 사용하는 마스터 사례는 높이가 192예요. 이미지 영역·가격 줄을 유지하면서 실제 문구에 맞게 높이를 구성해요.

### 두 variant의 차이

| 항목 | Personality Test | Check-in |
| --- | --- | --- |
| 이미지 비율 | 84 × **116** (세로형) | 120 × **120** (정사각) |
| 이미지 라운드 | `r150` (6) | **`r250`** (10) |
| 텍스트 구성 | 짧은 제목 | 상품명 + 가격 (상품명 줄 수에 따라 높이 변경) |
| 텍스트 색 | `Color/Gray_100` | **`Color/Gray_500`** |
| 텍스트 스타일 | `b500_13_regular` | **`t1300_15_medium`** |
| 배경 | 없음 | **`Color/Gray_White`** |
| 좌우 패딩 | `Spacing/100` (4) | **`Spacing/50`** (2) |

**거의 모든 값이 다릅니다.** 같은 컴포넌트셋 안에 성격이 다른 두 카드가 들어 있는 구조입니다.

> `Image` BOOLEAN의 기본값이 `false`라, 두 variant 모두 **이미지가 꺼진 상태**(`Color/Gray_950` 플레이스홀더)로 출고됩니다.

---

## 가이드라인

### 1. 콘텐츠에 맞는 유형을 사용해요

심리테스트처럼 이미지와 짧은 제목을 보여줄 때는 Personality Test를 사용해요. 출석 화면의 제휴 상품처럼 상품명과 가격을 함께 보여줄 때는 Check-in을 사용해요.

| 용도 | `Variant` | 아이템 폭 | 이미지 영역 | 표시 정보 |
| --- | --- | --- | --- | --- |
| 심리테스트 콘텐츠 | `Personality Test` | 84 | 84 × 116 세로형 | 짧은 제목 |
| 출석 화면의 제휴 상품 | `Check-in` | 120 | 120 × 120 정사각 | 상품명·가격 |

[Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1096)

### 2. 항목을 한 줄로 배치해 가로로 탐색해요

스크롤 영역 안에 항목을 한 줄로 배치하고, 영역을 넘는 부분은 가로로 탐색하도록 구성해요. 전체 항목을 넣기 위해 아이템 폭을 줄이거나 여러 줄로 바꾸지 않아요.

- 안쪽 Product Scroll은 한 줄을 유지하고, 바깥 스크롤 영역은 화면에서 사용할 수 있는 폭으로 구성해요.
- 넘치는 부분은 영역 밖으로 보이지 않게 처리하고 가로로 탐색할 수 있게 해요. 실제 예제의 스크롤 영역은 `clipsContent=true`, `overflowDirection=HORIZONTAL`로 구성돼 있어요.
- Personality Test는 항목 간격 8, Check-in은 항목 간격 12로 배치해요. 슬롯 패딩을 더해 간격이나 시작 위치를 바꾸지 않아요.

[Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1138)

---

## Usage — 사용 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1095)에 실제 사용 목적별 예제 2개를 구성했어요.

| 예제 | 사용 구성 | 설명 | 항목 간격 |
| --- | --- | --- | --- |
| [A. 심리테스트 목록](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1245) | `Product Scroll / Variant=Personality Test` | 심리테스트 콘텐츠를 한 줄로 보여줄 때 Personality Test를 사용해요. 세로형 썸네일 아래에 짧은 제목을 표시하고, 항목 사이는 8 간격으로 배치해요. | 8 |
| [B. 출석 화면의 제휴 상품](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11653-1304) | `Product Scroll / Variant=Check-in` | 출석 화면에서 제휴 상품을 보여줄 때 Check-in을 사용해요. 정사각 썸네일 아래에 상품명과 가격을 표시하고, 항목 사이는 12 간격으로 배치해요. | 12 |

현재 가이드라인 2의 스크롤 영역은 폭 328, Usage A·B는 폭 360이에요. 예제의 표시 폭이며 모든 사용처를 같은 폭으로 고정하라는 뜻은 아니에요. 아이템 폭과 유형별 간격을 유지하면서 부모 영역에 맞춰 바깥 표시 폭을 정해요.

상품명·테스트 제목·가격과 항목 수는 예제 소재예요. 실제 콘텐츠에 맞게 사용하고, 마스터의 반복 상품이나 가격을 실제 데이터로 해석하지 않아요.

## 예제 레이아웃과 AI 사용 기준

- 단독 아이템을 비교하는 가이드라인 1은 슬롯에 컴포넌트를 직접 배치해요. 불필요한 `화면` 레이어를 만들지 않아요.
- 가로 탐색을 설명하는 가이드라인 2와 Usage에는 폭 제한과 클리핑을 위한 `스크롤 영역` 프레임을 사용해요. 이 프레임은 스크롤을 표현하는 데 필요한 구조이므로 유지해요.
- 슬롯과 스크롤 영역은 불필요한 패딩 없이 좌측·상단 정렬로 구성해요. 컴포넌트 자체의 텍스트 패딩은 유지해요.
- 문서 예제의 Scroll Item은 `Image=False`로 간결하게 표현해요. 이미지 영역은 유지되고 내부 썸네일만 꺼져요. 실제 서비스 화면에서 이미지 사용을 금지하는 규칙은 아니에요.
- `Variant`는 콘텐츠의 정보 구성에 맞춰 선택해요. Check-in을 선택했다고 출석 완료 상태나 리워드 지급 완료 상태로 해석하지 않아요.
- `Gold` 속성이 있다는 이유만으로 리워드 표시나 동작을 임의로 추가하지 않아요. 현재 가이드라인과 예제는 Gold의 사용 규칙을 정의하지 않아요.
- 항목 간격(8·12)과 아이템 내부 이미지–텍스트 간격(10·12)을 구분해요. 전체 항목을 화면에 맞추려고 아이템을 축소하거나 줄바꿈하지 않아요.
- 기존 Product Scroll·Scroll Item 인스턴스를 활용하고 연결을 유지해요. 마스터의 전체 콘텐츠 폭과 바깥 스크롤 영역의 표시 폭을 구분해요.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 마스터 콘텐츠 폭 | 648 · 728 (전체 항목을 펼친 샘플 폭) |
| 스크롤 표시 영역 | 부모 영역에 맞는 폭 · 가이드라인 2는 328, Usage는 360 |
| 아이템 폭 | 84 (`Personality Test`) · 120 (`Check-in`) |
| 아이템 간격 | `Spacing/200`(8) · `Spacing/300`(12) |
| 이미지–텍스트 간격 | `Spacing/250`(10) · `Spacing/300`(12) |
| 이미지 배경 | `Color/Gray_950` (플레이스홀더) |
| 이미지 라운드 | `Corner radius/150`(6) · `Corner radius/250`(10) |
| 텍스트 | `b500_13_regular` · `t1300_15_medium` · `t900_16_bold` |

---

## 점검 필요 사항

> 아래는 2026-10-12의 점검 기록이에요. 이번 갱신은 가이드라인·Usage와 사용 기준 문서화이며, 파일 전체의 토큰·스타일·인스턴스 건수는 재집계하지 않았어요. 과거 통계와 검토 제안을 최신 사용 규칙과 구분해요.

### 1. 토큰 상태 — 완벽에 가까움

| 항목 | 결과 |
| --- | --- |
| **미바인딩 fill · radius · gap** | **전부 0건** |
| **스타일 미적용 텍스트** | **0건** (보드 표기 4건 제외) |
| **원격 텍스트 스타일** | **0건** |
| **외부 타이포 변수 잔재** | **0건** |
| 미바인딩 stroke | `#9747FF` 2건 — Figma 컴포넌트셋 기본 점선 |
| 미바인딩 padding | `100` 4 · `546` 2 — 전부 문서 보드 |
| 외부 토큰 | `Spec docs` 5 — 문서 레이아웃 전용 |
| 제어문자 · U+2028 | **0건** |
| 폰트 | 전부 Pretendard |

**컴포넌트 영역에 지적할 토큰 문제가 하나도 없습니다.**

[Product List](syrup-product-list-components.md)에서 발견한 "스타일 없이 외부 타이포 변수가 걸린" 패턴도 **0건**입니다.

> `Check-in` variant의 패딩만 `0!`(리터럴)인데, 값이 0이라 토큰 바인딩 대상이 아닙니다.

### 2. ✅ 자식 레이어명 정리 (2026-10-12 완료)

`Product Scroll` 마스터의 자식 인스턴스 **13개 전부** 이름이 `Grid Scroll Item`이었습니다.

| Variant | 자식 수 | 변경 전 | 변경 후 |
| --- | --- | --- | --- |
| `Personality Test` | 8 | **`Grid Scroll Item`** | **`Scroll Item`** |
| `Check-in` | 5 | **`Grid Scroll Item`** | **`Scroll Item`** |

실제로 참조하는 컴포넌트는 `.primitive / **Product Scroll** / Scroll Item`이었고, **[Grid Scroll](syrup-grid-scroll-components.md) 페이지에서 복제해 만든 흔적**이었습니다. 동작에는 문제가 없었지만 레이어 목록만 보면 Grid Scroll 컴포넌트를 쓰는 것으로 오해할 수 있었습니다.

| 항목 | 결과 |
| --- | --- |
| 변경 건수 | **13건** |
| Variant 크기 | 728 × 144 · 648 × 192 — **변화 없음** |
| 페이지 내 `Grid Scroll` 잔여 | **0건** |

> [Product Grid](syrup-product-grid-components.md)에서 마스터 이름이 `Grid List /`로 시작하던 것과 같은 유형(다른 페이지 이름 잔재)이며, 둘 다 2026-10-12에 정리했습니다.

### 3. 두 variant가 거의 모든 값을 달리함

`Product Scroll / Scroll Item`의 두 variant는 **공유하는 스펙이 거의 없습니다.**

| 항목 | Personality Test | Check-in |
| --- | --- | --- |
| 크기 | 84 × 144 | **120 × 173** |
| 이미지 | 84 × 116 · `r150` | **120 × 120 · `r250`** |
| 텍스트 줄 | 1 | **2** |
| 텍스트 색 | `Gray_100` | **`Gray_500`** |
| 배경 | 없음 | **`Gray_White`** |
| 좌우 패딩 | `Spacing/100` | **`Spacing/50`** |
| Gap | `Spacing/250` | **`Spacing/300`** |

[Product List](syrup-product-list-components.md)의 `Type` 4종에서도 같은 지적을 했습니다. **하나의 `Variant` 축에 성격이 다른 카드를 담는 패턴**이 Product 계열 전반에 있습니다.

특히 **텍스트 색이 `Gray_100`(#222222)과 `Gray_500`(#999999)으로 크게 다른 점**은 확인이 필요합니다. 같은 역할(상품명)인데 한쪽은 진하고 한쪽은 흐립니다.

| 방향 | 내용 |
| --- | --- |
| **현행 유지** | `Variant` 하나로 고르는 편의 |
| 분리 | 각자 규칙을 가진 별도 컴포넌트로 |

### 4. 마스터 사용 0건 — 과거 집계

| 컴포넌트 | 인스턴스 |
| --- | --- |
| **`Product Scroll`** | **0** |
| `.primitive / … / Scroll Item` | 13 (전부 마스터 내부) |

> 이 수치는 2026-10-12의 기존 집계예요. 현재 Section 1과 Usage에 사용 사례가 추가되어, 현재 사용 여부를 뜻하지 않아요. 다른 파일·디태치·코드 사용은 포함하지 않아요.

가로 스크롤 영역은 화면 폭을 넘는 요소라 다른 컴포넌트 안에 배치하기 어렵습니다. [Grid Scroll](syrup-grid-scroll-components.md)(마스터 3종 중 2종 0건)과 같은 양상입니다.

### 5. 외부 의존 없음

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| `❖System Components` | `Title Bar` · `Section Header` | 3 (보드 표기) |

**제품 컴포넌트가 다른 페이지나 외부 라이브러리에 전혀 의존하지 않습니다.**

[Keypad](syrup-keypad-components.md) · [List Header](syrup-list-header-components.md)처럼 조립형인 페이지들과 대조적이며, 자체 완결성이 높습니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-12)

| 항목 | 내용 |
| --- | --- |
| `Grid Scroll Item` → `Scroll Item` ([2](#2--자식-레이어명-정리-2026-10-12-완료)) | **13건** · 크기·렌더링 변화 없음 |

작업 후 컴포넌트셋 178개 · 인스턴스 1,828개를 전수 검증해 오류·끊긴 참조 **0건**을 확인했습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | 텍스트 색 `Gray_100` ↔ `Gray_500` 확인 ([3](#3-두-variant가-거의-모든-값을-달리함)) | 디자인 판단 | 낮음 |
| 2 | 두 variant 분리 여부 ([3](#3-두-variant가-거의-모든-값을-달리함)) | 구조 판단 | 중간 |

**토큰 문제가 없어 남은 과제는 디자인·구조 판단뿐**입니다. [Dim](syrup-dim-components.md) · [Loader](syrup-loader-components.md) · [Keypad](syrup-keypad-components.md)와 함께 가장 깨끗한 페이지입니다.
