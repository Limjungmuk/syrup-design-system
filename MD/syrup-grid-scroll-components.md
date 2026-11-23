# Syrup Design System — Grid Scroll 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Grid Scroll` 페이지 → [Grid Scroll 섹션 `8958:77373`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8958-77373) |
| 섹션 구성 | `Grid Scroll` 1440×2720 → `Guidelines` 960×1016 → `Usage` 1360×464 (가로 일렬) · 별도 `Section 1` 2588×6604 |
| 컴포넌트 수 | **7개** (Component Set 3 · Component 4) |
| 기준일 | 2026-11-23 (Review 본문 최대 4줄·초과 말줄임 확인) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **아이콘과 텍스트로 구성된 아이템을 가로로 스크롤하며 탐색하는 리스트 컴포넌트에요.**
> 한정된 화면에서 여러 개의 메뉴나 서비스를 효율적으로 보여줄 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Grid Scroll / Scroll Item / Icon/Shopping` | `8958:79249` |
| `Grid Scroll / Scroll Item / Review` | `10577:4138` |
| `Grid Scroll / Scroll Item / Live` | `9298:17785` |
| `Grid Scroll / Icon / Image` | `8958:77489` |

2026-11-11 중복 이름을 Item·Icon·Image 역할로 구분했어요. 상위 묶음 이름과 원본 연결은 유지해요.
- `Grid Scroll / Icon / Image`: 이번에 공개 이름으로 정리한 개별 에셋 `8958:77489` / 기존 상위 묶음 `8958:77378`.

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Master Component 3종](#1-master-component-3종)
3. [Child Item — Scroll Item](#2-child-item--scroll-item)
4. [Icon](#3-icon)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

섹션 2,720 · 노드 201개로 중간 규모입니다. [Grid List](syrup-grid-list-components.md)와 이름이 비슷하지만 **용도가 다릅니다.**

| | Grid List | **Grid Scroll** |
| --- | --- | --- |
| 배치 | 격자 (줄바꿈) | **가로 1줄 스크롤** |
| 폭 | 328~360 (화면 안) | **598~664 (화면 밖으로 넘침)** |
| 성격 | 메뉴 전체 보기 | 넘겨 보며 탐색 |

마스터 컴포넌트의 폭이 **598~664로 화면 폭(360)을 넘습니다.** 가로 스크롤 영역을 Figma에서 펼쳐 표현한 것입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Icon` · `Live` · `Winner` |
| y 1228 → 1368 | Child Item → Scroll Item | Scroll Item 3종 |
| y 2078 | Icon | 쇼핑 아이콘 17종 |

### 전체 목록

| # | 이름 | 타입 | Variant / Props | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Grid Scroll / Icon` | Set | `Variant` **1종**뿐 | 664 × 116 | 1 |
| 2 | `Grid Scroll / Live` | Component | — | 604 × 116 | **0** |
| 3 | `Grid Scroll / Winner` | Component | — | 598 × 110 | **0** |
| 4 | `Grid Scroll / Scroll Item / Icon/Shopping` | Component | — | 56 × 98 | 18 |
| 5 | `Grid Scroll / Scroll Item / Review` | Component | — | 142 × 110 | 8 |
| 6 | `Grid Scroll / Scroll Item / Live` | Set | `State` 4종 | 282 × 116 | 2 |
| 7 | `Grid Scroll / Icon / Image` | Set | `Variant` **17종** | 56 × 56 | 20 |

---

## 1. Master Component 3종

### Grid Scroll / Icon

**Node** `8958:77378` · Component Set · **1 variant**

| Property | Type | Options |
| --- | --- | --- |
| `Variant` | VARIANT | `Shopping` |

**variant가 하나뿐인 컴포넌트셋**입니다 → [점검 2](#2-variant가-하나뿐인-컴포넌트셋)

| 항목 | 값 |
| --- | --- |
| 크기 | 664 × 116 |
| 방향 | 가로 |
| Padding | 0 |
| Gap | `Spacing/500` (20) |
| 배경 | 없음 |

쇼핑 아이콘 9개를 가로로 나열한 행입니다. 실제 화면에서는 오른쪽으로 스크롤됩니다.

### Grid Scroll / Live

**Node** `9298:17926` · Component · variant 없음

| 항목 | 값 |
| --- | --- |
| 크기 | 604 × 116 |
| 방향 | 가로 |
| Padding | `0 / Spacing/400(16) / 0 / Spacing/400(16)` |
| Gap | `Spacing/200` (8) |

라이브 방송 시간대 카드 2장을 나열합니다. `.primitive / … / Live`를 담는 묶음입니다.

### Grid Scroll / Winner

**Node** `10577:4166` · Component · variant 없음

| 항목 | 값 |
| --- | --- |
| 크기 | 598 × 110 |
| 방향 | 가로 |
| Padding | 0 |
| Gap | `Spacing/250` (10) |
| Radius | `Corner radius/300` (12) |

당첨자 축하 메시지 카드를 나열합니다. `.primitive / … / Review`를 담습니다.

> `Live`와 `Winner`는 **인스턴스가 0건**입니다 → [점검 5](#5-live--winner-마스터-사용-0건)

---

## 2. Child Item — Scroll Item

### Grid Scroll / Scroll Item / Icon/Shopping

**Node** `8958:79249` · Component · 56 × 98

| 항목 | 값 |
| --- | --- |
| 방향 | 세로 |
| Padding | 0 |
| Gap | `Spacing/150` (6) |
| 구성 | 아이콘 56 × 56 + 라벨 + 금액 |

**이 페이지에서 가장 많이 쓰입니다**(18건 — `Card` 9 · `Grid Scroll` 9).

레이어 이름이 **`Icon/Shopping`** 으로 슬래시 앞뒤 공백이 없습니다 → [점검 3](#3-이름-규칙-불일치--iconshopping)

### Grid Scroll / Scroll Item / Review

**Node** `10577:4138` · Component · 142 × 110

| 항목 | 값 |
| --- | --- |
| 방향 | 세로 |
| Padding | `Spacing/300` (12) 사방 |
| Gap | `Spacing/100` (4) |
| 배경 | **`Color/Third_Pastel_Blue`** |
| Radius | `Corner radius/200` (8) |

축하 메시지를 담는 작은 카드입니다. 인스턴스 8건(`Grid Scroll` 4 · **`Ticker` 4**)으로, **다른 페이지에서도 쓰이는 유일한 Scroll Item**입니다.

Review 본문 `10577:4119`는 최대 4줄까지 표시하고 초과하면 끝에 말줄임표를 표시해요. 현재 원본은 `maxLines=4`, `textTruncation=ENDING`, `textAutoResize=HEIGHT`, 본문 폭 118·13px·행간 16이며 4줄 높이는 64예요. 글자 수로 임의 절단하거나 카드 높이를 늘려 전체 후기를 펼치지 않아요. 닉네임·당첨 날짜에는 이 4줄 제한을 일괄 적용하지 않아요. 동일 Review 인스턴스를 사용하는 Grid Scroll과 Ticker에서도 이 기준을 유지해요.

### Grid Scroll / Scroll Item / Live

**Node** `9298:17785` · Component Set · **4 variants** · 282 × 116

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `State` | VARIANT | `Available` | `Available` · `Completed` · `Upcoming` · `Ended` |

(2026-10-12 `Property 1` → `State` 정리 완료 → [점검 4](#4--property-1--state-2026-10-12-완료))

#### 공통 레이아웃

| 항목 | 값 |
| --- | --- |
| Padding | `600/400/400/400` (24/16/16/16) |
| Gap | `Spacing/400` (16) |
| 배경 | `Color/Gray_White` |
| Radius | `Corner radius/400` (16) |
| 효과 | `DROP_SHADOW` |
| 테두리 | `Color/Primary_Orange` 1px — **`Available`만 표시** |

#### 상태별 차이

| Variant | 테두리 | 시간 텍스트 | 버튼 배경 | 버튼 라벨 | 의미 |
| --- | --- | --- | --- | --- | --- |
| `Available` | **표시** | `Opacity_Black_100` (75%) | `Color/Primary_Orange` | `Color/Gray_White` "3금 받기" | 참여 가능 |
| `Completed` | 숨김 | `Opacity_Black_100` (75%) | `Color/Gray_900` | `Color/Gray_600` "참여 완료" | 참여함 |
| `Upcoming` | 숨김 | **`Opacity_Black_200`** (50%) | `Color/Gray_900` | `Color/Gray_600` "Coming Soon" | 시작 전 |
| `Ended` | 숨김 | **`Opacity_Black_200`** (50%) | `Color/Gray_900` | `Color/Gray_600` "참여 종료" | 종료 |

시간 텍스트는 `t1300_15_medium` + `t800_17_bold` 조합이고, 버튼 라벨은 `t1000_15_bold`입니다.

**세 단계로 흐려집니다** — 참여 가능(오렌지 테두리 + 진한 글자) → 참여 완료(테두리 없음 + 진한 글자) → 예정·종료(테두리 없음 + 흐린 글자).

> 네 variant 모두 **오렌지 테두리를 갖고 있고 `Available`만 페인트를 표시**합니다. 테두리를 지우지 않고 켜고 끄는 방식이라, 스펙만 읽으면 전부 오렌지 테두리로 보입니다.

---

## 3. Icon

### Grid Scroll / Icon / Image

**Node** `8958:77489` · Component Set · **17 variants** · 56 × 56

제휴 쇼핑몰 로고입니다.

| Variant |
| --- |
| 금받는쇼핑 · 핫딜쇼핑 · 쇼핑적립 · 지마켓 · 오늘의집 · **네이버플러스스토어_오픈전** · 네이버플러스스토어 · 옥션 · SSG · 이마트몰 · 지그재그 · 아이허브 · 11번가 · 쿠팡 · 컬리 · 엘지전자 · 알리익스프레스 |

인스턴스 20건(`Card` 10 · `Grid Scroll` 10)입니다.

> `네이버플러스트어_오픈전` 오타는 2026-10-12에 수정했습니다 → [점검 1](#1--variant-이름-오타-수정-2026-10-12-완료)

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 마스터 폭 | 598~664 (화면 밖으로 넘치는 스크롤 영역) |
| 마스터 높이 | 110~116 |
| 아이콘 | 56 × 56 |
| 아이콘–라벨 간격 | `Spacing/150` (6) |
| 아이템 간격 | `Spacing/500`(20) · `Spacing/250`(10) · `Spacing/200`(8) |
| 카드 Radius | `Corner radius/400`(16) · `Corner radius/300`(12) · `Corner radius/200`(8) |
| 선택 강조 | `Color/Primary_Orange` 1px 테두리 |
| 비활성 | `Color/Gray_900` 배경 + `Color/Gray_600` 글자 |

### 텍스트 스타일

| 스타일 | 용도 |
| --- | --- |
| `t1360_13_medium` | 아이콘 라벨 |
| `t800_17_bold` | 시간 (강조) |
| `t1300_15_medium` | 시간 (보조) |
| `t1000_15_bold` | 버튼 라벨 |
| `b500_13_regular` | 축하 메시지 |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11540:1871`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11540-1871) · 1360 × 464 |
| 구성 | 3패턴 · 화면 360 · 슬롯 높이 142~148 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다 (2026-11-06).

**패턴이 마스터 3종과 일대일로 맞습니다.** `Grid Scroll`은 **아이템 하나가 아니라 가로로 나열한 행 전체**가 컴포넌트라, 무엇을 나열하느냐가 곧 어느 마스터를 쓰느냐입니다.

| | 패턴 | 설명 | 마스터 | 행 너비 · 간격 |
| --- | --- | --- | --- | --- |
| **A** | 쇼핑 메뉴 탐색 | 쇼핑몰이나 서비스로 이동할 때 Icon 유형을 사용해요. 아이콘 아래에 이름과 적립 혜택을 표시하고 가로로 탐색해요. | `Grid Scroll / Icon` (`Variant=Shopping`) | 664 · 간격 **20** · 9개 |
| **B** | 시간대별 참여 | 정해진 시간에 참여하는 콘텐츠에는 Live 유형을 사용해요. 시간과 참여 상태를 보여주고, 상태에 맞는 버튼을 사용해요. | `Grid Scroll / Live` | 604 · 간격 **8** · 2개 |
| **C** | 당첨 후기 탐색 | 여러 당첨 후기를 나란히 보여줄 때 Winner 유형을 사용해요. 자동으로 흐르는 후기는 Ticker에서 별도로 구성해요. | `Grid Scroll / Winner` | 598 · 간격 **10** · 4개 |

**세 컷 모두 360 화면 밖으로 넘칩니다.** 행 너비가 598~664인데 화면이 360이라 오른쪽이 잘립니다. **가로 스크롤**이 되는 상태를 Figma에서 그대로 보여 준 것입니다.

| 컷 | 행 너비 | 화면에 보이는 것 |
| --- | --- | --- |
| A | 664 | 아이템 4.5개 |
| B | 604 | 아이템 1.2개 |
| C | 598 | 아이템 2.5개 |

**아이템 크기와 간격이 유형마다 다릅니다.** Icon은 56 폭에 간격 20, Live는 282 폭에 간격 8, Winner는 142 폭에 간격 10입니다. 담는 내용의 밀도가 달라서이고, [Guidelines 1](#1-콘텐츠에-맞는-유형을-사용해요)이 「각 컴포넌트의 기본 구성을 유지해요」라고 못 박는 이유입니다.

**B만 회색 배경 위에 있습니다.** Live 아이템이 흰 카드라 흰 화면에서는 경계가 보이지 않아, 화면 배경을 `Color/Gray_950`으로 두었습니다. A · C는 아이템 자체가 색을 가져 흰 배경에서도 읽힙니다.

**C의 설명이 경계를 그어 줍니다.** 「자동으로 흐르는 후기는 Ticker에서 별도로 구성해요」 — 같은 후기 카드라도 **가로로 넘겨 보면 Grid Scroll, 저절로 흐르면 Ticker**입니다. 제품 실측이 정확히 그렇습니다.

### 제품 실측 (2026-11-06)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체를 전수 조사했습니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 마스터 세트 | **`Grid Scroll / Icon`** | **10** (전부 `쇼핑 적립`) |
| | `Grid Scroll / Live` | **0** |
| | `Grid Scroll / Winner` | **0** |
| 세트 배치 | 중첩 · 직접 | 5 · 5 |
| 개별 아이템 | `Scroll Item / Review` | **16** (전부 `⇥ 금한돈 타이머`) |
| | `Grid Scroll Item / Live` | **6** (전부 `⇥ 모이는 라방`) |

**마스터 세트는 `Icon`만 쓰입니다.** `Live` · `Winner`는 세트를 거치지 않고 **안쪽 아이템을 직접 깔아** 씁니다 → [점검 5](#5-live--winner-마스터-사용-0건)

**`Review` 16건이 전부 `Ticker / Marquee / Card` 안에 있습니다.** Usage C의 설명 그대로 — 당첨 후기를 **흐르게** 쓰는 화면이라 Grid Scroll이 아니라 Ticker를 썼습니다. 후기 카드는 같고 **움직이는 방식만 다릅니다.**

**제품의 Live 아이템 6건은 옛 이름·옛 프로퍼티를 씁니다.** `Grid Scroll Item / Live` + `Property 1`(Available 2 · Upcoming 2 · Completed 1 · Ended 1)이고, 2026-10-12에 `Scroll Item / Live` + `State`로 정리한 것이 아직 반영되지 않았습니다 → [점검 9](#9-usage-b와-guidelines-1이-원격-사본을-가리킵니다)

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11540:1870`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11540-1870)** (960 × 1016) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**두 규칙 모두 「두 경우 비교」입니다 — Do / Don't가 없습니다.** Grid Scroll에서 갈리는 것은 맞고 틀림이 아니라 **어느 유형·어느 상태를 고르느냐**이기 때문입니다. 네 라벨 모두 `#222222`입니다.

| 형식 | 규칙 | 슬롯 라벨 |
| --- | --- | --- |
| 두 경우 비교 | **1** | 「Icon · 메뉴 이동」 · 「Live · 시간대별 참여」 |
| | **2** | 「Available · Completed」 · 「Upcoming · Ended」 |

### 1. 콘텐츠에 맞는 유형을 사용해요

이동할 메뉴는 Icon, 시간대별 참여는 Live, 당첨 후기는 Winner를 사용해요.
화면 폭을 넘는 항목은 가로로 탐색하고, 아이템 크기와 간격은 각 컴포넌트의 기본 구성을 유지해요.

| 라벨 | 마스터 | 아이템 | 간격 | 담는 것 |
| --- | --- | --- | --- | --- |
| **Icon · 메뉴 이동** | `Grid Scroll / Icon` | 56 × 98 · 9개 | **20** | 아이콘 + 이름 + 적립 혜택 |
| **Live · 시간대별 참여** | `Grid Scroll / Live` | 282 × 116 · 2개 | **8** | 시간 + 상태 버튼 |

**아이템 폭이 다섯 배 차이 납니다** (56 ↔ 282). 메뉴는 아이콘 하나로 알아보지만, 시간대별 참여는 시간·버튼·상태를 한 카드에 담아야 하기 때문입니다.

**설명은 세 유형을 말하는데 컷은 둘입니다.** 나머지 `Winner`는 [Usage C](#usage)가 맡고 있어 문서 전체로는 빠진 내용이 없습니다.

### 2. 참여 상태에 맞춰 Live를 사용해요

참여 가능은 Available, 참여 완료는 Completed, 시작 전은 Upcoming, 종료 후는 Ended를 사용해요.
시간과 참여 여부에 맞는 상태를 선택하고, 참여할 수 없는 상태를 참여 가능한 버튼으로 표시하지 않아요.

| 라벨 | `State` | 버튼 | 라벨 문구 |
| --- | --- | --- | --- |
| **Available · Completed** | `Available` | `Variant=Fill` · 활성 | 「3금 받기」 |
| | `Completed` | `Variant=Weak` · **비활성** | 「참여 완료」 |
| **Upcoming · Ended** | `Upcoming` | `Variant=Weak` · 비활성 | 「Coming Soon」 |
| | `Ended` | `Variant=Weak` · 비활성 · **아이콘 없음** | 「참여 종료」 |

**네 상태를 두 컷에 나눠 담았습니다.** 왼쪽은 **지금 참여하는 시간대**(가능 ↔ 완료), 오른쪽은 **지금이 아닌 시간대**(시작 전 ↔ 종료)입니다.

**누를 수 있는 것은 `Available` 하나뿐입니다.** 나머지 셋은 전부 `Disabled=True`입니다. 설명의 「참여할 수 없는 상태를 참여 가능한 버튼으로 표시하지 않아요」가 그 뜻입니다.

**`Ended`만 금 아이콘이 없습니다.** 끝난 시간대에는 받을 금이 없으니 아이콘도 빠집니다 — 나머지 셋은 `Icon=true`로 금 아이콘을 답니다.

---

## 점검 필요 사항

### 1. ✅ Variant 이름 오타 수정 (2026-10-12 완료)

`Grid Scroll / Icon / Image`의 variant 중 하나에 **글자 누락**이 있었습니다.

| Node | 변경 전 | 변경 후 |
| --- | --- | --- |
| `8958:77643` | `Variant=네이버플러스**트어**_오픈전` | `Variant=네이버플러스**스토어**_오픈전` |

바로 옆 variant가 `네이버플러스스토어`로 정상 표기되어 있어 **같은 브랜드인데 이름이 어긋난 상태**였고, 코드에서 문자열로 variant를 지정하면 매칭에 실패했습니다.

| 항목 | 결과 |
| --- | --- |
| 이 variant를 쓰는 인스턴스 | **0건** (영향 없음) |
| `Variant` 옵션 | `네이버플러스스토어_오픈전` · `네이버플러스스토어` — 표기 일치 |

> 이 컴포넌트셋은 2026-10-01에 **variant 이름의 제어문자(U+001D)를 제거**한 곳이기도 합니다. 당시에는 보이지 않는 문자만 처리했고 오타는 남아 있었습니다.

### 2. Variant가 하나뿐인 컴포넌트셋

`Grid Scroll / Icon` `8958:77378`은 **Component Set인데 variant가 `Shopping` 하나**뿐입니다.

| 항목 | 값 |
| --- | --- |
| 타입 | COMPONENT_SET |
| variant | **1개** (`Variant=Shopping`) |

variant가 하나면 컴포넌트셋으로 둘 이유가 없습니다. 선택지는 둘입니다.

| 방향 | 내용 |
| --- | --- |
| **확장 예정이라면** | 유지. `Live` · `Winner`를 같은 셋에 variant로 합치면 축이 생깁니다 |
| **아니라면** | 일반 Component로 전환해 프로퍼티 패널의 빈 드롭다운 제거 |

같은 페이지의 `Live` · `Winner`가 **단일 Component**로 되어 있어, 셋으로 묶을지 각각 둘지 기준이 어긋난 상태입니다.

### 3. 이름 규칙 불일치 — `Icon/Shopping`

`.primitive / Grid Scroll / Scroll Item / **Icon/Shopping**` — 마지막 구분자만 **슬래시 앞뒤 공백이 없습니다.**

| 컴포넌트 | 이름 |
| --- | --- |
| `Grid Scroll / Scroll Item / Review` | ✅ |
| `Grid Scroll / Scroll Item / Live` | ✅ |
| `Grid Scroll / Scroll Item / Icon/Shopping` | ⚠️ |

Figma는 ` / `를 폴더 구분으로 쓰므로, 에셋 패널에서 `Icon/Shopping`이 **한 덩어리 이름**으로 취급됩니다.

Grid List에서 `56 /Pocket`을 정리한 것과 **같은 유형**입니다. `Scroll Item / Icon / Shopping` 또는 `Scroll Item / Shopping`으로 맞추면 됩니다.

### 4. ✅ `Property 1` → `State` (2026-10-12 완료)

`Grid Scroll / Scroll Item / Live` `9298:17785`의 프로퍼티명이 Figma 기본값이었습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 프로퍼티명 | `Property 1` | **`State`** |
| variant 이름 | `Property 1=Available` 외 3종 | **`State=Available` · `State=Completed` · `State=Upcoming` · `State=Ended`** |
| 인스턴스 | 2건 (`Grid Scroll`) | 자동 반영, 끊긴 참조 0건 |

값 4개가 모두 **참여 상태**를 가리키므로 `State`가 적합합니다. `Button / News`를 `State`로 정리한 선례와 같은 성격입니다.

**`Grid Scroll` 페이지의 `Property 1`은 0건**이 되었습니다. 파일 전체로는 57개 컴포넌트셋에 남아 있습니다.

### 5. `Live` · `Winner` 마스터 사용 0건

**2026-11-06에 문서 쪽은 해소되었습니다.** [Usage B · C](#usage)와 [Guidelines 1 · 2](#guidelines)가 두 마스터를 컷으로 쓰고 있어, 디자인 시스템 파일 안에서는 더 이상 0건이 아닙니다.

**제품 파일에서는 여전히 0건입니다.**

| 마스터 | 디자인 시스템 | 제품 (Syrup_App) |
| --- | --- | --- |
| `Grid Scroll / Icon` | 2 (Usage A · Guidelines 1) | **10** (전부 `쇼핑 적립`) |
| `Grid Scroll / Live` | 2 (Usage B · Guidelines 1) | **0** |
| `Grid Scroll / Winner` | 1 (Usage C) | **0** |

다만 **안쪽 아이템은 제품에서 쓰이고 있습니다.**

| 아이템 | 제품 사용 | 어디에서 |
| --- | --- | --- |
| `Scroll Item / Review` | **16** | 전부 `Ticker / Marquee / Card` 안 (`⇥ 금한돈 타이머`) |
| `Grid Scroll Item / Live` | **6** | `⇥ 모이는 라방` — 세트 없이 개별 배치 |

**`Review` 16건이 전부 Ticker 안에 있다는 것이 중요합니다.** 같은 후기 카드를 **가로로 넘겨 보면 Grid Scroll, 저절로 흐르면 Ticker**입니다. [Usage C](#usage)의 설명이 그 경계를 이미 적어 두었습니다 — `Grid Scroll / Winner` 마스터가 제품에서 안 쓰이는 것은 **쓸모가 없어서가 아니라 그 화면이 Ticker를 골랐기 때문**입니다.

마스터를 유지할지는 **「넘겨 보는 후기」 화면을 만들 계획이 있는지**에 달려 있습니다. 계획이 없다면 Winner는 Ticker 쪽으로 넘기고, Live는 세트 없이 아이템만 쓰는 현재 방식을 인정하는 정리도 가능합니다.

### 6. 스타일 미적용 텍스트 16건

보드 표기 6건을 제외한 수치입니다.

| 크기 · 굵기 | 건수 | 위치 |
| --- | --- | --- |
| **11 Medium** | 10 | `Grid Scroll / Icon` · `Scroll Item / Icon/Shopping` (금액 라벨) |
| **13 Regular** | 5 | `Grid Scroll / Winner` · `Scroll Item / Review` (축하 메시지) |
| `10 Bold` | 1 | — |

**`11 Medium` 10건은 토큰화하지 않기로 한 범주**(13px이 하한)입니다. Card의 `11 Medium` 12건과 같은 성격입니다.

**`13 Regular` 5건은 다릅니다.** 13px은 시스템 관리 대상이고 `b500_13_regular`가 존재합니다.

| | 현재 | `b500_13_regular` |
| --- | --- | --- |
| 폰트 · 크기 | Pretendard Regular 13 | 동일 |
| line-height | **16** | **18** |
| letter-spacing | 0 | 0 |

**라인하이트만 2 다릅니다.** 스타일을 적용하면 텍스트 블록 높이가 늘어나므로 무손실은 아닙니다. 현재 본문은 최대 4줄·끝 말줄임이므로 `Review` 카드(142 × 110) 높이에 영향을 줄 수 있어, 적용 전 확인이 필요합니다.

### 7. Pretendard SemiBold 4건

| 폰트 | 건수 |
| --- | --- |
| Pretendard Medium | 26 |
| Pretendard Regular | 16 |
| Pretendard Bold | 14 |
| **Pretendard SemiBold** | **4** |

전부 Pretendard로 통일되어 있으나 SemiBold는 Syrup 타입 스케일에 없는 굵기입니다. **4건 모두 보드 섹션 헤더**(`Master Component` · `Child Item` 등 40/32 SemiBold)로, 제품 UI가 아닙니다.

### 8. 토큰 상태 — 양호

| 항목 | 결과 |
| --- | --- |
| 미바인딩 fill | **1건** — `#1F80FF` (아이콘 제외 기준) |
| 미바인딩 stroke | `#9747FF` 3건 — Figma 컴포넌트셋 기본 점선 |
| 미바인딩 radius · gap | **0건** |
| 미바인딩 padding | `100` 6 · `546` 2 — 문서 보드 전용 |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs` 7 — 문서 레이아웃 전용 |
| 제어문자 · U+2028 | **0건** |

**간격·라운드가 전부 토큰에 바인딩**되어 있습니다. 지금까지 문서화한 페이지 중 간격 미바인딩이 0건인 것은 Chip·Checkbox에 이어 세 번째입니다.

`#1F80FF` 1건은 Card 페이지에서도 지적한 색으로, `Color/Secondary_Blue`(#3496F4)와 역할이 겹칩니다.

**새로 만든 Usage · Guidelines 두 섹션은 이렇습니다 (2026-11-06).**

| 항목 | 결과 |
| --- | --- |
| 미바인딩 fill | **6건** — `#1F80FF` · `#00C01E` · `#00A1FF` 각 2 (쇼핑몰 브랜드 로고, 토큰화 대상 아님) |
| 스타일 없는 TEXT | **22건** — `11 Medium` 18 · `13 Regular` 4 |
| 레이어 이름 | 5개 모두 제목과 일치 |

스타일 없는 텍스트는 전부 **컴포넌트 안에서 딸려 온 것**이고 위 6번과 같은 건입니다. 제가 만든 `스크롤 영역` 프레임 3개의 흰 배경은 `Color/Gray_White`에 바인딩했습니다.

### 9. Usage B와 Guidelines 1이 원격 사본을 가리킵니다

두 컷의 `Grid Scroll / Live` 인스턴스가 **로컬 마스터가 아니라 원격 사본**을 가리킵니다.

| | 로컬 (정상) | Usage B · Guidelines 1이 쓰는 것 |
| --- | --- | --- |
| 마스터 | `Grid Scroll / Live` **`9298:17926`** | `Grid Scroll / Live` **`11532:83858`** · **`remote: true`** |
| 안쪽 아이템 | `.primitive / Grid Scroll / **Scroll Item** / Live` | `.primitive / Grid Scroll / **Grid Scroll Item** / Live` |
| 프로퍼티 | **`State`** (Available · Completed · Upcoming · Ended) | **`Property 1`** (같은 네 값) |

**2026-10-12에 정리한 이름이 이 두 컷에는 적용되지 않습니다.** [점검 4](#4--property-1--state-2026-10-12-완료)에서 「페이지 내 `Property 1` 0건」을 확인했는데, 그 뒤 들어온 원격 사본이 옛 이름을 다시 들여왔습니다.

**출처는 `Section 1`로 보입니다.** 제품 화면(`GT01` · `EP05` · `SP01`)을 이 파일로 가져오면서, 그 안의 `Grid Scroll / Live`가 **제품 파일의 컴포넌트를 가리키는 원격 참조**로 들어왔습니다. 노드 ID도 `Section 1`과 같은 `11532:` 대역입니다.

| 섹션의 Grid Scroll 인스턴스 | 로컬 | 원격 |
| --- | --- | --- |
| Usage A · C · Guidelines 1(Icon) · Guidelines 2(4건) | **7** | — |
| **Usage B · Guidelines 1(Live)** | — | **2** |

**지금은 보이는 결과가 같지만**, 로컬 마스터를 고쳐도 이 두 컷은 따라오지 않습니다. 로컬 `Grid Scroll / Live`(`9298:17926`) 인스턴스로 바꿔 끼우면 해소됩니다 — 양쪽 모두 604 × 116에 `Available` + `Upcoming` 구성이라 교체해도 컷이 달라지지 않습니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-12)

| 항목 | 내용 |
| --- | --- |
| Variant 오타 수정 ([1](#1--variant-이름-오타-수정-2026-10-12-완료)) | `네이버플러스트어_오픈전` → `네이버플러스스토어_오픈전` |
| `Property 1` → `State` ([4](#4--property-1--state-2026-10-12-완료)) | **페이지 내 `Property 1` 0건** |

둘 다 **이름만 변경**이며 크기·렌더링 변화가 없습니다. 작업 후 컴포넌트셋 178개 · 인스턴스 1,828개를 전수 검증해 오류·끊긴 참조 **0건**을 확인했습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | Usage B · Guidelines 1의 원격 사본을 로컬로 교체 ([9](#9-usage-b와-guidelines-1이-원격-사본을-가리킵니다)) | 인스턴스 교체 | 낮음 |
| 2 | `Icon/Shopping` 이름 공백 ([3](#3-이름-규칙-불일치--iconshopping)) | 이름만 변경 | 낮음 |
| 3 | `Live` · `Winner` 마스터 유지 여부 ([5](#5-live--winner-마스터-사용-0건)) | 서비스 확인 필요 | 중간 |
| 4 | `13 Regular` 5건 스타일 적용 ([6](#6-스타일-미적용-텍스트-16건)) | 높이 변화 확인 필요 | 중간 |
| 5 | variant 1개짜리 컴포넌트셋 ([2](#2-variant가-하나뿐인-컴포넌트셋)) | 구조 판단 | 중간 |
| 6 | `#1F80FF` 토큰화 여부 ([8](#8-토큰-상태--양호)) | 판단 필요 | 중간 |


## 2026-11-23 Review 본문 변경

사용자가 수정한 원본의 본문 최대 4줄과 초과 말줄임을 확인해 반영했어요. 해당 Review가 포함된 가이드라인·예제 이미지를 최신 Figma 원본으로 웹에 반영해요. 상단 Icon 스크롤 시연은 유지해요.
