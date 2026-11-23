# Syrup Design System — Dim 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Dim` 페이지 → [Dim 섹션 `10301:4056`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=10301-4056) |
| 섹션 구성 | `Dim` 1440×918 → `Guidelines` 960×1632 → `Usage` 960×856 (가로 일렬) |
| 컴포넌트 수 | **1개** (Component) |
| 기준일 | 2026-11-06 (Usage · Guidelines 신설 / 스펙 정리: 2026-10-12) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **화면 위에 반투명 레이어를 표시하여 현재 콘텐츠를 강조하는 컴포넌트에요.**
> Dialog, Bottom Sheet 등 사용자의 시선을 집중시키거나 배경과 콘텐츠를 구분할 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Dim — Master Component](#1-dim--master-component)
3. [Opacity Black 스케일](#2-opacity-black-스케일)
4. [설계 규칙 요약](#설계-규칙-요약)
5. [Usage](#usage)
6. [Guidelines](#guidelines)
7. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

**지금까지 문서화한 페이지 중 가장 작습니다.** 섹션 높이 918, 노드 15개, 컴포넌트 1개입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 제목 + 설명 |
| y 434 | Master Component | `Dim` 1종 |

`Child Item` · `Icon` 섹션이 없습니다. Variant도 없는 **단일 컴포넌트 하나**뿐입니다.

| # | 이름 | 타입 | Variant / Props | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Dim` | Component | **없음** | 80 × 80 |

---

## 1. Dim — Master Component

**Node** `10285:3541` · Component · variant 없음

### 스펙

| 항목 | 값 |
| --- | --- |
| 크기 | **80 × 80** (고정) |
| 배경 | **`Color/Opacity_Black_100`** = `#000000` **75%** |
| 라운드 | 0 |
| 리사이징 | 가로·세로 모두 FIXED |
| 제약 | `horizontal: MIN` · `vertical: MIN` |
| 레이아웃 | VERTICAL 오토레이아웃 (자식 없음) |
| 자식 | **없음** |
| 효과 | 없음 |
| 블렌드 모드 | `PASS_THROUGH` |
| Description | **없음** |

**프로퍼티가 하나도 없는 빈 사각형**입니다. 색 하나만 담고 있습니다.

흰 배경 위에 올리면 `#404040`으로 보입니다.

### 실제 구현에서의 사용

Figma 컴포넌트는 80 × 80 고정이지만, 실제로는 **화면 전체를 덮는 오버레이**로 쓰입니다. 구현 시에는 크기를 화면에 맞춰 늘려야 합니다.

```css
/* 전체 화면 딤 */
position: fixed;
inset: 0;
background: rgba(0, 0, 0, 0.75);   /* Color/Opacity_Black_100 */
```

---

## 2. Opacity Black 스케일

Dim이 쓰는 `Opacity_Black_100`은 6단계 스케일의 **가장 진한 값**입니다.

| 토큰 | 투명도 | 흰 배경 위 | 주요 사용처 |
| --- | --- | --- | --- |
| **`Color/Opacity_Black_100`** | **75%** | `#404040` | **Dim** · Grid Scroll `Live` 배지 · Banner 이미지 |
| `Color/Opacity_Black_200` | 50% | `#808080` | Badge 비활성 배경 · Label `Tag` · Product List 만료 딤 |
| `Color/Opacity_Black_300` | 25% | `#BFBFBF` | AD · Indicator 배경 |
| `Color/Opacity_Black_400` | 12% | `#E0E0E0` | — |
| `Color/Opacity_Black_450` | 8% | `#EBEBEB` | Button `State layer` (누름 효과) |
| `Color/Opacity_Black_500` | 4% | `#F5F5F5` | — |

번호가 **작을수록 진합니다.** Gray Scale과 같은 방향입니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 색 | `#000000` |
| 투명도 | **75%** (`Color/Opacity_Black_100`) |
| 라운드 | 0 |
| 효과 | 없음 (블러 없음) |
| 적용 범위 | 화면 전체 (구현 시 확장) |

**블러나 그림자 없이 단색 반투명만** 씁니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11530:303`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11530-303) · 960 × 856 |
| 구성 | 2패턴 · 화면 360 × 540 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다 (2026-11-06).

**Dim은 혼자서는 아무것도 보여 주지 못합니다.** 색 하나짜리 반투명 사각형이라, **무엇을 덮고 무엇을 띄우는지**가 함께 있어야 패턴이 읽힙니다. 그래서 두 컷 모두 **뒤 화면 · 딤 · 그 위의 팝업** 세 층을 한꺼번에 세웠습니다.

| 층 | 내용 |
| --- | --- |
| 1. `배경 콘텐츠` | 헤더(150 × 24) + 콘텐츠 블록 4개(320 × 80) — `Color/Gray_950` |
| 2. **`Dim`** | 360 × 540 · `Color/Opacity_Black_100` (검정 75%) |
| 3. 팝업 | `Dialog` 또는 `Bottom Sheet` |

| | 패턴 | 설명 | 그 위에 뜨는 것 | 자리 |
| --- | --- | --- | --- | --- |
| **A** | Dialog | 화면 전체에 Dim을 깔고, 그 위에 Dialog를 가로·세로 중앙에 배치해요. | `Dialog` 288 × 182 | 좌우 **36** · **중앙** |
| **B** | Bottom Sheet | 화면 전체에 Dim을 깔고, 그 위에 Bottom Sheet를 하단에 배치해요. | `Bottom Sheet` 340 × 326 | 좌우 **10** · 하단 **32** |

**두 패턴의 차이는 딤이 아니라 그 위에 오는 것의 자리입니다.** `Dim`은 두 컷에서 360 × 540으로 똑같고, [Dialog는 중앙](syrup-dialog-components.md#1-화면-중앙에-dialog를-배치하고-dim을-함께-사용해요)·[Bottom Sheet는 하단에 띄워](syrup-bottom-sheet-components.md#1-화면-아래에서-띄워-배치해요) 놓입니다. 두 페이지의 규칙 1이 각각 그 자리를 정합니다.

**배경 콘텐츠가 딤 아래로 비쳐 보입니다.** 헤더와 콘텐츠 블록이 어둡게 깔리면서 **뒤에 화면이 있다는 것**이 드러납니다 — 딤이 하는 일이 바로 이것입니다.

### 제품 실측 (2026-11-06)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체에서 딤 레이어를 전수 조사했습니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| **`Dim` 컴포넌트 인스턴스** | 제품 | **115** |
| | 아이데이션 | 1 |
| 인스턴스 크기 | **360 × 780** (화면 전체) | **111** |
| | 360 × 700 · 360 × 725 | 4 |
| **직접 그린 딤 레이어** | 제품 | **79** |
| | 아이데이션 | 51 |

**컴포넌트 인스턴스 115건이 전부 화면 크기로 리사이즈되어 있습니다.** 마스터는 80 × 80인데 실제 쓰임은 360 × 780입니다 → [점검 4](#4-80--80-고정이-오버레이-성격과-맞지-않음)

**직접 그린 딤 79건은 농도가 네 가지로 갈립니다.**

| 값 | 건수 | `Dim`과 같은가 |
| --- | --- | --- |
| `#000000` 75% (바인딩) | **31** | ✅ 같음 — 컴포넌트로 바꿀 수 있음 |
| fill 종류가 단색이 아님 (이미지·그라디언트) | 23 | — 딤이 아닌 레이어 |
| `#666666` + 레이어 투명도 **5%** | 16 | ❌ 전혀 다른 농도 |
| `#000000` **70%** (미바인딩) | 6 | ❌ 토큰 밖 값 |
| `#000000` **50%** (바인딩) | 3 | ❌ `Opacity_Black_200` |

이름이 `dim`으로 시작하는 레이어 기준입니다 → [점검 7](#7-제품에-직접-그린-딤이-79건-있습니다)

**페이지별로는 `지금` 23 · `⇥ 출석체크` 20 · `모으기 🟢` 15 순입니다.** 직접 그린 딤은 `⇥ 금 받는 식단 기록` 16 · `⇥ 월금명세서` 15 · `팝업` 12 · `⇥ 게임하고 모으기` 12에 몰려 있습니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11530:302`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11530-302)** (960 × 1632) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**두 규칙 모두 Do / Don't입니다.** 딤에서 갈리는 것은 선택이 아니라 **덮느냐 못 덮느냐**라서, 두 경우 비교로 둘 항목이 없습니다.

| 형식 | 규칙 | 슬롯 라벨 | 라벨 색 |
| --- | --- | --- | --- |
| Do / Don't | 1 · 2 | `Do` · `Don’t` | `#222222` · **`#FF3E00`** |

### 1. 화면 전체를 덮도록 사용해요

Dim은 뒤 화면 전체를 덮도록 배치해요. 헤더나 하단 영역이 일부 남지 않도록 해요.

| | `Dim` 크기 · 자리 | 결과 |
| --- | --- | --- |
| **Do** | **360 × 540** @(0, 0) | 화면이 끝까지 덮임 |
| **Don't** | **360 × 390** @(0, **75**) | 위아래로 **75씩** 덮이지 않고 남음 |

두 컷 모두 같은 Dialog가 같은 자리에 있고, **다른 것은 딤의 높이와 y 좌표**입니다.

**덮다 만 딤은 팝업보다 눈에 띕니다.** 위아래 흰 띠가 가로로 길게 남아, 사용자의 시선이 팝업이 아니라 그 경계선으로 갑니다. 딤의 목적이 정확히 반대로 작동하는 상태입니다.

**구현에서는 `inset: 0`입니다.** Figma 컴포넌트는 80 × 80 고정이라 인스턴스를 놓아도 자동으로 늘어나지 않습니다. 매번 화면 크기로 늘려야 하고, 그것을 빠뜨린 것이 이 Don't입니다 → [점검 4](#4-80--80-고정이-오버레이-성격과-맞지-않음)

### 2. 팝업 아래에 한 번만 배치해요

화면 → Dim → Dialog 또는 Bottom Sheet 순서로 배치해요. Dim이 중복되어 배경이 지나치게 어두워지지 않도록 해요.

| | `Dim` 개수 | 실제 농도 | 결과 |
| --- | --- | --- | --- |
| **Do** | **1개** | 75% | 뒤 화면이 비쳐 보임 |
| **Don't** | **2개** (겹침) | **약 94%** | 뒤 화면이 거의 보이지 않음 |

두 컷 모두 같은 배경 콘텐츠와 같은 Dialog이고, **다른 것은 `Dim` 레이어 하나가 더 있는지**입니다.

**반투명은 겹치면 곱해집니다.** 75%를 두 번 겹치면 남는 빛이 0.25 × 0.25 = **6%** 뿐이라, 헤더와 콘텐츠 블록이 사라집니다. 뒤에 화면이 있다는 신호가 없어지면 **팝업이 아니라 별도 화면처럼** 보입니다.

**레이어 순서도 함께 정합니다.** 화면 → Dim → 팝업이고, 팝업이 딤 위에 와야 합니다. 순서가 뒤집히면 팝업까지 어두워집니다.

---

## 점검 필요 사항

### 1. ✅ 사용처 0건 → 디자인 시스템 44건 · 제품 115건 (2026-11-06)

2026-10-12에는 「`Dim` 컴포넌트의 인스턴스가 파일 어디에도 없다」고 적었습니다. **상황이 달라졌습니다.**

| 조사 범위 | 2026-10-12 | 2026-11-06 |
| --- | --- | --- |
| 디자인 시스템 파일 | **0건** | **44건** |
| 제품 파일 (Syrup_App) | — | **115건** |

디자인 시스템 44건의 내역입니다.

| 페이지 | 건수 | 쓰임 |
| --- | --- | --- |
| `Bottom Sheet` | **19** | Usage 8컷 · Guidelines 11컷 |
| `Dialog` | **18** | Usage 11컷 · Guidelines 7컷 |
| `Dim` | **7** | 이 페이지의 Usage 2 · Guidelines 5 |

**설명문과 파일 내용이 이제 일치합니다.** 「Dialog, Bottom Sheet 등에 사용」이 세 페이지의 컷으로 실제로 증명됩니다. 제품에서도 115건이 쓰이고 있어, **쓰이지 않는 컴포넌트가 아닙니다.**

남은 것은 **쓰는 방식**입니다 — 크기 제약([4번](#4-80--80-고정이-오버레이-성격과-맞지-않음))과 직접 그린 딤([7번](#7-제품에-직접-그린-딤이-79건-있습니다))입니다.

### 2. `Product List`에 같은 이름의 별도 딤 레이어 — **투명도가 다름**

`Dim` 컴포넌트를 쓰지 않고 **직접 만든 딤 레이어**가 한 곳 있습니다.

| 항목 | `Dim` 컴포넌트 | `Product List / Coupon` ▸ `Property 1=Expired` |
| --- | --- | --- |
| Node | `10285:3541` | `10575:3884` |
| 타입 | COMPONENT | **FRAME** (인스턴스 아님) |
| 레이어명 | `Dim` | **`Dim`** (동일) |
| 크기 | 80 × 80 | 80 × 80 (동일) |
| 투명도 | **`Opacity_Black_100` 75%** | **`Opacity_Black_200` 50%** |

이름·크기·역할이 같은데 **투명도만 다릅니다.** 쿠폰 만료 상태에서 썸네일을 덮고 "사용완료"를 올리는 용도입니다.

| 판단 | 내용 |
| --- | --- |
| **의도된 차이라면** | 전체 화면 딤(75%)과 **요소 단위 딤**(50%)은 목적이 달라 값이 다를 수 있습니다. 그렇다면 Dim 컴포넌트에 variant를 추가하거나, 요소 딤을 별도 토큰·컴포넌트로 명명하는 편이 낫습니다 |
| **실수라면** | `Opacity_Black_100`으로 맞추고 `Dim` 컴포넌트 인스턴스로 교체 |

어느 쪽이든 **같은 이름의 레이어가 다른 값을 갖는 상태는 혼동을 줍니다.**

### 3. `.primitive / Color / Opacity`와 크기·역할이 겹침

`❖Components` 페이지에 **색상 견본 컴포넌트**가 있고, `Dim`과 크기가 같습니다.

| 컴포넌트 | 크기 | 내용 |
| --- | --- | --- |
| `Dim` | **80 × 80** | `Opacity_Black_100` 단색 |
| `.primitive / Color / Opacity` `10301:4085` | **80 × 80** × 6종 | `Black_100` ~ `Black_500` 견본 |

`.primitive / Color / Opacity` ▸ `Property 1=Black_100`과 **`Dim`은 크기·색·구조가 완전히 동일**합니다. 즉 현재의 `Dim`은 기능 컴포넌트라기보다 **색상 견본 하나를 복제해 둔 것**에 가깝습니다.

딤이 실제로 쓰이려면 다음 중 하나가 필요합니다.

- **전체 화면 크기로 정의** (예: 360 × 640)하고 리사이징을 FILL로 두어 오버레이임을 분명히 하기
- 또는 컴포넌트를 없애고 **토큰(`Color/Opacity_Black_100`) 사용 규칙만 문서화**하기

### 4. 80 × 80 고정이 오버레이 성격과 맞지 않음

| 항목 | 현재 |
| --- | --- |
| 크기 | 80 × 80 **FIXED** |
| 제약 | `MIN` / `MIN` (좌상단 고정) |
| 리사이징 | 가로·세로 FIXED |

딤은 **부모를 가득 채워야** 하는 레이어인데, 현재 설정은 좌상단에 80 × 80으로 고정됩니다. 인스턴스를 배치해도 자동으로 늘어나지 않습니다.

제약을 `SCALE` 또는 `STRETCH`(상하좌우)로 바꾸면 부모 크기를 따라가게 됩니다.

**제품 실측이 이 문제를 그대로 보여 줍니다 (2026-11-06).**

| 인스턴스 크기 | 건수 |
| --- | --- |
| **360 × 780** (화면 전체) | **111** |
| 360 × 700 · 360 × 725 | 4 |
| 80 × 80 (마스터 크기 그대로) | **0** |

**115건 전부 손으로 늘린 것입니다.** 마스터 크기를 그대로 쓴 인스턴스는 한 건도 없습니다. 매번 늘려야 하니 빠뜨리기도 쉽고, 실제로 [Guidelines 1](#1-화면-전체를-덮도록-사용해요)의 Don't가 그 상태입니다.

마스터를 **360 × 780으로 키우고 제약을 `STRETCH`로** 두면 놓는 즉시 화면을 덮습니다. 80 × 80을 유지할 이유는 `.primitive / Color / Opacity` 견본과 크기를 맞추는 것뿐인데, 그 역할은 [3번](#3-primitive--color--opacity와-크기역할이-겹침)에서 이미 분리 대상으로 보고 있습니다.

### 5. 빈 오토레이아웃

자식이 없는데 `layoutMode = VERTICAL`이 설정되어 있습니다. 동작에 영향은 없지만 불필요한 설정입니다.

### 6. 토큰 상태 — 매우 양호

| 항목 | 결과 |
| --- | --- |
| 미바인딩 fill | **0건** |
| 미바인딩 stroke · radius · padding · gap | **0건** |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs` 2 — 문서 레이아웃 전용 |
| 제어문자 | **0건** |
| 스타일 미적용 텍스트 | 3건 — **전부 보드 표기**(제목 72 Bold · 설명 16 Regular · 섹션 헤더 40 SemiBold) |

**컴포넌트 자체에는 지적할 토큰 문제가 전혀 없습니다.** 노드 15개 규모라 당연한 결과이기도 합니다.

**새로 만든 Usage · Guidelines 두 섹션도 같습니다** — 화면 프레임 6개 전부 토큰 바인딩, 스타일 없는 텍스트 **0건**, 미바인딩 fill **0건**입니다.

### 7. 제품에 직접 그린 딤이 79건 있습니다

제품 파일에서 이름이 `dim`으로 시작하는 레이어를 전수 조사한 결과입니다.

| 값 | 건수 | `Dim`과 같은가 | 조치 |
| --- | --- | --- | --- |
| `#000000` 75% (토큰 바인딩) | **31** | ✅ 같음 | **인스턴스로 교체 가능** |
| 단색이 아닌 fill (이미지·그라디언트) | 23 | — | 딤이 아닌 레이어 |
| `#666666` + 레이어 투명도 **5%** | 16 | ❌ | 다른 용도로 보임 — 확인 필요 |
| `#000000` **70%** (미바인딩) | 6 | ❌ | 토큰 밖 값 — 75%로 맞출지 판단 |
| `#000000` **50%** (`Opacity_Black_200`) | 3 | ❌ | 요소 단위 딤 — [2번](#2-product-list에-같은-이름의-별도-딤-레이어--투명도가-다름)과 같은 계열 |

**값이 같은 31건은 바로 교체할 수 있습니다.** 보이는 결과가 똑같으니 무손실이고, 교체하면 **딤 농도가 바뀔 때 함께 따라옵니다.**

**`#000000` 70% 6건이 가장 급합니다.** 토큰에 없는 값이라 어느 쪽으로도 관리되지 않습니다.

이 건은 [Dialog 점검 6](syrup-dialog-components.md#6-딤을-직접-그린-사각형으로-쓴-곳이-21건입니다)·[Bottom Sheet 점검 10](syrup-bottom-sheet-components.md#10-딤을-직접-그린-사각형으로-쓴-곳이-있습니다)과 **같은 문제를 딤 쪽에서 본 것**입니다. 페이지별로는 `⇥ 금 받는 식단 기록` 16 · `⇥ 월금명세서` 15 · `팝업` 12 · `⇥ 게임하고 모으기` 12에 몰려 있습니다.

### 8. Guidelines 1의 Don't에 배경 콘텐츠가 없습니다

[Guidelines 1](#1-화면-전체를-덮도록-사용해요)의 Do에는 `배경 콘텐츠` 안에 헤더와 콘텐츠 블록 4개가 들어 있는데, **Don't 쪽은 그 프레임이 비어 있습니다.**

| | `배경 콘텐츠` | 덮이지 않은 띠에 보이는 것 |
| --- | --- | --- |
| **Do** | 헤더 + 콘텐츠 4개 | — (전부 덮임) |
| **Don't** | **비어 있음** | 흰 여백 |

규칙의 설명은 「헤더나 하단 영역이 **일부 남지 않도록**」인데, 남은 띠에 **정작 헤더가 없습니다.** 지금도 흰 띠로 차이가 보여 규칙은 읽히지만, Do와 같은 배경을 넣으면 **덮다 만 헤더가 그대로 드러나** 설명과 정확히 맞아떨어집니다.

Usage A · B와 Guidelines 2는 양쪽 모두 배경 콘텐츠를 갖고 있어, **이 한 컷만 비어 있습니다.**

---

## 정리 우선순위

2026-11-06에 Usage · Guidelines가 생기고 제품 실측이 더해지면서 순서가 바뀌었습니다.

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | 마스터를 화면 크기로 키우고 제약을 `STRETCH`로 ([4](#4-80--80-고정이-오버레이-성격과-맞지-않음)) | 구조 변경 | 낮음 |
| 2 | 값이 같은 직접 그린 딤 31건을 인스턴스로 교체 ([7](#7-제품에-직접-그린-딤이-79건-있습니다)) | 치환 | 낮음 |
| 3 | 토큰 밖 값 `#000000` 70% 6건 정리 ([7](#7-제품에-직접-그린-딤이-79건-있습니다)) | 판단 필요 | 낮음 |
| 4 | `Product List`의 딤 투명도 차이 확인 ([2](#2-product-list에-같은-이름의-별도-딤-레이어--투명도가-다름)) | 판단 필요 | 낮음 |
| 5 | Guidelines 1 Don't에 배경 콘텐츠 넣기 ([8](#8-guidelines-1의-dont에-배경-콘텐츠가-없습니다)) | 컷 보완 | 낮음 |
| 6 | `.primitive / Color / Opacity`와 역할 정리 ([3](#3-primitive--color--opacity와-크기역할이-겹침)) | 구조 판단 | 중간 |
| 7 | 빈 오토레이아웃 해제 ([5](#5-빈-오토레이아웃)) | 정리 | 낮음 |

**「컴포넌트로 관리할 것인가, 토큰 규칙으로 관리할 것인가」는 답이 났습니다.** 2026-10-12에는 아무도 쓰지 않아 둘 다 아닌 상태였지만, 지금은 디자인 시스템 44건 · 제품 115건이 **컴포넌트를 쓰고 있습니다.**

그래서 남은 일은 **컴포넌트를 쓰기 좋게 만드는 것**입니다 — 놓으면 화면을 덮도록 크기와 제약을 고치고(1순위), 아직 손으로 그린 딤을 끌어오는 것(2·3순위)입니다.
