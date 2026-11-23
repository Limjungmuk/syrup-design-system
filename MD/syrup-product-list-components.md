# Syrup Design System — Product List 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Product List` 페이지 → [Product List 섹션 `9354:34720`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9354-34720) |
| 섹션 크기 | 1440 × 1661 |
| 컴포넌트 수 | **2개** (전부 Component Set) |
| 기준일 | 2026-11-09 (가이드라인·Usage 갱신) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **상품 정보를 리스트 형태로 구성해 보여주는 컴포넌트예요.**
> 상품 이미지, 가격, 혜택, 설명 등 필요한 정보를 세로로 나열하여 상품 목록을 구성할 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Product List / Product](#1-product-list--product)
3. [Product List / Coupon](#2-product-list--coupon)
4. [가이드라인](#가이드라인)
5. [Usage — 사용 예제](#usage--사용-예제)
6. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

마스터는 `Product List / Product`와 `Product List / Coupon` 2종이에요. 별도 섹션에 가이드라인 4개와 예제 A~G를 구성했어요. 노드·인스턴스의 기존 집계는 2026-10-12 기준이며, 새 사용 화면과 예제는 포함하지 않아요.

[Product Grid](syrup-product-grid-components.md)와 짝을 이룹니다.

| | Product Grid | **Product List** |
| --- | --- | --- |
| 배치 | 가로 **WRAP 격자** | **세로 1열 나열** |
| 아이템 | 이미지 위 · 텍스트 아래 | **이미지 좌 · 텍스트 우** |
| primitive | 5종 | **없음** (자체 구성) |

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Product List / Product` | Set | `Type` 4종 + `Image` | 332~360 × 60~118 | **0** |
| 2 | `Product List / Coupon` | Set | `State` 2종 + `Date` · `Dday` | 328 × 128 | **0** |

---

## 1. Product List / Product

**Node** `9354:34762` · Component Set · **4 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Action` | `Action` · `Media` · `Product` · `Content` |
| `Image` | BOOLEAN | `true` | — |

### Variant별 스펙

| Type | 크기 | Padding | Gap | 테두리 | 대표 텍스트 |
| --- | --- | --- | --- | --- | --- |
| `Action` | 360 × 86 | **0** | `Spacing/500` (20) | 없음 | `c100_12_regular` |
| `Media` | **332** × 60 | **0** | `Spacing/400` (16) | 없음 | `b400_14_regular` |
| `Product` | 360 × 118 | `400/600/400/600` | **14** ⚠️ | **`Color/Gray_900` 하단 1px** | `t900_16_bold` |
| `Content` | 360 × 105 | `300/500/300/500` | `Spacing/400` (16) | 없음 | `t1300_15_medium` |

**네 variant의 스펙이 거의 공유되지 않습니다.** 크기 · 패딩 · 간격 · 테두리가 모두 다릅니다.

| 구성 | Type |
| --- | --- |
| `Image` + `Content` + `Button` | `Action` |
| `Image` + `Text` | `Media` · `Product` · `Content` |

`Action`만 [Button](syrup-button-components.md) 인스턴스를 포함합니다.

> `Product`의 간격 `14`는 토큰 스케일 밖이고, 테두리도 이 variant에만 있습니다 → [점검 3](#3-variant-간-규칙-공유가-거의-없음)

---

## 2. Product List / Coupon

**Node** `10575:3860` · Component Set · **2 variants** · 328 × 128

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `State` | VARIANT | `Default` | `Default` · `Expired` |
| `Date` | BOOLEAN | **`false`** | — |
| `Dday` | BOOLEAN | `true` | — |

(2026-10-12 `Property 1` → `State`, `D-day` → `Dday` 정리 → [점검 2](#2--property-1--state--d-day--dday-2026-10-12-완료))

### 공통 레이아웃

| 항목 | 값 |
| --- | --- |
| 크기 | 328 × 128 |
| Padding | `Spacing/600` (24) 사방 |
| Gap | `Spacing/500` (20) |
| 배경 | `Color/Gray_White` |
| 테두리 | `Color/Gray_850` 1px 사방 |
| 라운드 | `Corner radius/400` (16) |

### 구조

```
Image [80×80]
└ Product Grid / Icon / Stamp 인스턴스
  (Expired에는 Dim 레이어 추가)
Text [180×50]
├ Date [106×20]  ✗숨김
│ ├ D-day [33×20]  Third_Pastel_Coral
│ └ text «2026.08.14»  b500_13_regular · Gray_400
├ Partner «메가커피»  b100_17_regular · Gray_100
└ Text «(ICE) 아메리카…»  t800_17_bold · Gray_100
```

이미지는 [Product Grid](syrup-product-grid-components.md)의 **브랜드 로고 아이콘**을 가져다 씁니다.

### Default ↔ Expired

| 항목 | `Default` | `Expired` |
| --- | --- | --- |
| 추가 레이어 | — | **`Dim`** 80 × 80 |
| Dim 색 | — | `Color/Opacity_Black_200` (검정 **50%**) |
| Dim 위 텍스트 | — | "사용완료" `t1000_15_bold` · `Color/Gray_White` |

이미지 위에 요소용 Dim과 상태 문구를 표시해요. `Expired`는 기간 만료뿐 아니라 사용 완료·사용 불가 쿠폰에도 사용하는 구성이에요. 실제 사유는 “사용완료”·“기간만료”·“사용불가” 문구로 구분하고, 사용할 수 없는 쿠폰은 `Dday=False`로 표시해요. 카드 전체를 전체 화면용 Dim으로 덮지 않아요.

> 이 `Dim` 레이어는 [Dim 컴포넌트](syrup-dim-components.md)의 인스턴스가 아니라 **직접 만든 프레임**이고, 투명도도 75%가 아닌 **50%** 입니다 → [점검 4](#4-dim이-컴포넌트가-아닌-직접-제작)

### `Date` 프레임이 기본 숨김

마스터의 `Date` 기본값은 `false`예요. 사용 기한을 안내할 때는 `Date=True`로 켜고, 남은 일수를 함께 안내할 때 `Dday=True`로 사용해요. `Date=False`이면 내부 D-day도 보이지 않아요.

안에는 `D-day` 배지(`Third_Pastel_Coral`)와 만료일 텍스트가 들어 있습니다.

---

## 가이드라인

### 1. 상품 정보와 동작에 맞는 유형을 사용해요

브랜드·상품명·가격을 보여줄 때는 Product를 사용해요. 받기처럼 행 안에서 실행할 동작이 있으면 Action을 사용하고, 버튼 문구로 동작을 분명하게 안내해요.

[Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1302)

### 2. 콘텐츠의 설명 수준에 맞춰 구성해요

이미지와 짧은 제목으로 보여줄 때는 Media, 제목과 부가 설명을 함께 보여줄 때는 Content를 사용해요.

[Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1359)

### 3. 쿠폰 날짜는 필요한 경우에 표시해요

상품 구성만 안내할 때는 Date=False, 사용 기한을 알려줄 때는 Date=True로 사용해요. 남은 일수도 함께 안내할 때는 Dday=True로 표시해요. D-day는 Date 영역이 켜져 있을 때 함께 보여요.

| 용도 | `Date` | `Dday` |
| --- | --- | --- |
| 상품 구성만 안내 | `False` | Date 영역이 숨겨져 D-day도 보이지 않아요 |
| 날짜만 안내 | `True` | `False` |
| 날짜와 남은 일수 안내 | `True` | `True` |

[Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1404)

### 4. 사용할 수 없는 쿠폰은 상태를 구분해요

사용할 수 있는 쿠폰은 Default, 사용 완료·기간 만료·사용 불가 쿠폰은 Expired 구성을 사용해요. 이미지 위에 실제 상태를 문구로 표시하고, 사용할 수 없는 쿠폰의 D-day는 숨겨요.

| 실제 상태 | `State` | 이미지 위 문구 | `Dday` |
| --- | --- | --- | --- |
| 사용 가능 | `Default` | 상태 덮개 없음 | 안내 목적에 맞게 설정 |
| 사용 완료 | `Expired` | 사용완료 | `False` |
| 기간 만료 | `Expired` | 기간만료 | `False` |
| 사용 불가 | `Expired` | 사용불가 | `False` |

세 가지 사유는 별도 Variant가 아니라 현재 `Expired` 구성의 문구로 구분해요.

[Figma 가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1458)

---

## Usage — 사용 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1301)에 사용 목적별 예제 7개를 구성했어요.

| 예제 | 구성 | 설명 | 항목 사이 간격 |
| --- | --- | --- | --- |
| [A. 받기 버튼이 있는 상품](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1542) | `Product / Type=Action` | 상품 정보와 받기 버튼을 한 행에 구성해요. Action을 사용해 상품을 확인하면서 바로 동작할 수 있도록 해요. | 16 |
| [B. 미디어 목록](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1585) | `Product / Type=Media` | 이미지와 짧은 제목을 함께 보여주는 Media 구성이에요. 같은 목록의 이미지와 텍스트 시작 위치를 맞춰요. | 12 |
| [C. 가격 중심 상품 목록](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1612) | `Product / Type=Product` | 브랜드·상품명·가격을 보여주는 Product 구성이에요. 각 행의 하단 구분선으로 상품을 구분해요. | 추가 간격 없이 배치(0) |
| [D. 설명이 있는 콘텐츠](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1651) | `Product / Type=Content` | 제목과 부가 설명이 함께 필요한 경우 Content를 사용해요. 콘텐츠를 이해하는 데 필요한 정보를 간결하게 표시해요. | 추가 간격 없이 배치(0) |
| [E. 기한이 있는 쿠폰](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1682) | `Coupon / State=Default`, `Date=True` | Date=True로 사용 기한을 표시해요. 남은 일수도 안내할 때는 Dday=True로 함께 표시해요. | 12 |
| [F. 상품 안내용 쿠폰](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1723) | `Coupon / State=Default`, `Date=False` | 쿠폰의 상품 구성만 안내할 때는 Date=False로 사용해요. 날짜와 D-day 영역을 숨기고 이미지·제휴처·상품명을 보여줘요. | 여러 개 배치할 때 12 |
| [G. 사용할 수 없는 쿠폰](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11641-1749) | `Coupon / State=Expired`, `Dday=False` | Expired 구성을 사용하고, 이미지 위 문구로 사용 완료·기간 만료·사용 불가를 구분해요. Dday=False로 남은 일수는 숨겨요. | 12 |

간격은 각 예제의 항목과 항목 사이 값이에요. 컴포넌트 내부 이미지–텍스트 간격이나 내부 패딩과 혼동하지 않아요. 예제의 상품명·가격·날짜·D-day 값은 소재이며 실제 사용 시 데이터에 맞춰 표시해요.

## 예제 레이아웃과 AI 사용 기준

- 컴포넌트만 배치하는 경우 불필요한 `화면` 프레임 없이 슬롯에 인스턴스를 직접 넣어요. 여러 컴포넌트의 항목 간격도 슬롯의 오토레이아웃으로 구성할 수 있어요.
- 슬롯에는 불필요한 패딩을 추가하지 않고 좌측·상단 정렬로 배치해요. 보조 프레임이 필요해도 추가 좌우 여백으로 들여쓰기가 생기지 않도록 해요. 컴포넌트 자체의 패딩은 유지해요.
- Product의 `Image` 옵션이 있으면 문서 예제는 `Image=False`로 간결하게 표현해요. 이는 예제의 표현 기준이며, 실제 제품 화면에서 이미지 사용을 금지하는 규칙은 아니에요. 이미지 영역 자체가 없어지는 것으로 추정하지 말고 컴포넌트가 제공하는 표시 방식을 따라요.
- Coupon에는 Product의 `Image` 옵션을 임의로 적용하지 않아요. 쿠폰 이미지와 상태 덮개는 상태를 설명하는 데 활용해요.
- `Type`은 상품·콘텐츠의 정보 구성, `State`는 쿠폰의 사용 상태를 고르는 속성이에요. `Expired`를 만료 사유 하나로 제한하거나 사용 완료·사용 불가 Variant를 새로 만들지 않아요.
- `Date`와 `Dday`는 별도 BOOLEAN이에요. `Dday=True`만으로 숨겨진 Date 영역이 켜진다고 가정하지 않아요.
- 각 예제의 항목 간격을 사용하고, 컴포넌트 내부의 간격·패딩을 같은 값으로 덮어쓰지 않아요. Product·Content의 항목 간격 0도 내부 여백을 없애라는 뜻이 아니에요.
- 부모에 맞게 인스턴스 폭을 구성하고, 마스터의 샘플 폭·높이를 전체 화면의 고정 규격으로 해석하지 않아요. 원본 인스턴스 연결을 유지해요.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 폭 | **360** (전체 폭) · 332(`Media`) · 328(`Coupon`) |
| 높이 | 60 ~ 128 |
| 이미지 | 80 × 80 (`Coupon`) |
| 배치 | **가로 — 이미지 좌 · 텍스트 우** |
| 패딩 | `Spacing/600`(24) · `Spacing/500`(20) · `Spacing/400`(16) · `Spacing/300`(12) |
| 내부 간격 | `Spacing/500`(20) · `Spacing/400`(16), Product의 기존 값 14 |
| 예제 항목 간격 | Action 16 · Media 12 · Product/Content 0 · Coupon 12 |
| 카드 테두리 | `Color/Gray_850` 1px (`Coupon`) |
| 구분선 | `Color/Gray_900` 하단 1px (`Product`) |
| 라운드 | `Corner radius/400` (16) |

### 텍스트 스타일

| 스타일 | 용도 |
| --- | --- |
| `t800_17_bold` | 상품명 |
| `b100_17_regular` | 제휴처 |
| `t900_16_bold` | 브랜드명 |
| `t1300_15_medium` | 콘텐츠 제목 |
| `b400_14_regular` | 본문 |
| `b500_13_regular` | 날짜 |
| `c100_12_regular` | 캡션 |

---

## 점검 필요 사항

> 아래는 2026-10-12의 점검 기록이에요. 이번 갱신은 가이드라인·Usage와 사용 기준 문서화이며, 파일 전체의 인스턴스·토큰·스타일 건수는 재집계하지 않았어요. 과거 통계·검토 제안을 현재 사용 규칙과 구분해요.

### 1. ✅ 외부 토큰 `typeset_xs_bold` 10건 해제 (2026-10-12 완료)

**2026-10-08에 `typeset_xs_bold` 텍스트 스타일 연결을 해제**했으나([syrup-design-tokens.md](syrup-design-tokens.md) 참조), **그 스타일이 끌고 오던 외부 변수 바인딩은 그대로 남아 있었습니다.**

#### 위치

| Node | Variant | 경로 | 내용 |
| --- | --- | --- | --- |
| `10575:3869` | `State=Default` | `Text` › `Date` › **`D-day`** › `item` | "D-19" |
| `10575:3879` | `State=Expired` | `Text` › `Date` › **`D-day`** › `item` | "D-19" |

각 노드가 **5개 외부 변수**를 참조했습니다.

| 속성 | 참조 변수 |
| --- | --- |
| `fontSize` | `typeset_xs_bold/size` |
| `fontFamily` | `typeset_xs_bold/font` |
| `fontWeight` | `typeset_xs_bold/weight` |
| `lineHeight` | `typeset_xs_bold/lineheight` |
| `letterSpacing` | `typeset_xs_bold/letterspacing` |

> **이 텍스트는 현재 화면에 나오지 않습니다.** `Date` 프레임이 `visible: false`이고 `Date` BOOLEAN 기본값이 `false`라, 날짜·D-day 영역은 꺼진 상태입니다.

#### 무엇이 잘못되었나

당시 작업에서 **텍스트 스타일 링크만 끊고** 폰트·크기·라인하이트·자간 값이 유지됨을 확인했습니다. 하지만 그 값들이 **여전히 외부 라이브러리 변수를 참조**하고 있다는 점은 확인하지 않았습니다.

| 당시 확인한 것 | 확인하지 않은 것 |
| --- | --- |
| `textStyleId` 해제 ✅ | `boundVariables.fontSize` 등 **외부 변수 참조** ❌ |
| 폰트·크기·LH·LS 값 유지 ✅ | |

**"원격 텍스트 스타일 0건"은 맞지만 외부 변수 의존은 남아 있던 상태**였습니다.

#### 처리 결과

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 외부 변수 바인딩 | **10건** | **0건** |
| 폰트 · 크기 · LH · LS | Pretendard Bold 11 / 16 / 0 | **동일** |
| 텍스트 크기 | 25 × 16 | **동일** |
| Variant 크기 | 328 × 128 | **동일** |

값이 완전한 리터럴이 되었고 **렌더링 변화는 없습니다.** 11px은 토큰화하지 않기로 한 범주라 로컬 토큰으로 옮길 대상도 아닙니다.

**`Product List` 페이지의 외부 토큰은 `Spec docs` 3건**(문서 레이아웃 전용)만 남았습니다.

#### ⚠️ 같은 패턴이 다른 페이지에 18건

"텍스트 스타일은 없는데 외부 타이포 변수는 걸려 있는" 노드를 파일 전체에서 찾은 결과입니다.

| 페이지 | 외부 변수 출처 | 건수 | 내용 |
| --- | --- | --- | --- |
| **`Ticker`** | `fontSize` 계열 | **15** | "금한돈 당첨" · "조*주님" · 당첨 후기 |
| `Bottom Info` | `fontSize` 계열 | 2 | "중요 부분은 Bold처리…" |
| `List Header` | `fontFamilies` | 1 | "AD" 배지 |

**이 18건은 원래 파일에 있던 것**으로, 이번 작업과 무관합니다. 각 페이지를 문서화할 때 값 확인 후 함께 정리하는 편이 좋습니다.

> **교훈** — 텍스트 스타일을 해제할 때는 `textStyleId`뿐 아니라 **`boundVariables`의 타이포 변수(`fontSize` · `fontFamily` · `fontWeight` · `lineHeight` · `letterSpacing`)까지 확인**해야 합니다. 스타일을 떼어도 변수 참조는 남습니다.

### 2. ✅ `Property 1` → `State` · `D-day` → `Dday` (2026-10-12 완료)

`Product List / Coupon` `10575:3860`의 프로퍼티 두 개를 정리했습니다.

| 항목 | 변경 전 | 변경 후 | 이유 |
| --- | --- | --- | --- |
| VARIANT | **`Property 1`** | **`State`** | 값이 쿠폰 사용 상태(`Default` · `Expired`) |
| BOOLEAN | **`D-day`** | **`Dday`** | 하이픈 제거 |

#### `D-day` 하이픈 문제

파일 전체에서 **하이픈을 쓰는 프로퍼티명은 이 하나**였습니다. 코드에서 속성명으로 쓸 때 `D-day`는 **식별자로 바로 쓸 수 없어** 따옴표가 필요했습니다.

```js
props["D-day"]   // 따옴표 필요
props.Dday       // 바로 사용 가능
```

**`Product List` 페이지의 `Property 1`은 0건**이 되었습니다. 파일 전체로는 **43개** 컴포넌트셋에 남아 있습니다(44 → 43).

### 3. Variant 간 규칙 공유가 거의 없음

`Product List / Product`의 네 variant가 **공통 규칙을 거의 공유하지 않습니다.**

| Type | 크기 | Padding | Gap | 테두리 |
| --- | --- | --- | --- | --- |
| `Action` | 360 × 86 | 0 | 20 | 없음 |
| `Media` | **332** × 60 | 0 | 16 | 없음 |
| `Product` | 360 × 118 | 16/24 | **14** | **하단 1px** |
| `Content` | 360 × 105 | 12/20 | 16 | 없음 |

- **폭이 `Media`만 332**입니다. 나머지는 360입니다.
- **테두리가 `Product`에만** 있습니다.
- **간격 `14`** 는 Spacing 스케일(2 · 4 · 6 · 8 · 10 · 12 · 16 …)에 없는 값입니다.
- 패딩도 variant마다 다릅니다.

같은 컴포넌트셋 안에서 **네 가지 다른 리스트 행**을 담고 있는 셈입니다. [Card](syrup-card-components.md) · [List Row](syrup-list-row-components.md)에서 본 카탈로그형 구조와 비슷하지만, 그쪽은 **별도 컴포넌트로 분리**되어 있습니다.

| 방향 | 내용 |
| --- | --- |
| **현행 유지** | `Type` 하나로 고르는 편의 |
| 분리 | `Product List / Action` · `/ Media` 등으로 나눠 각자 규칙을 가짐 |

최소한 **간격 `14`와 `Media`의 폭 332**는 의도인지 확인이 필요합니다.

### 4. `Dim`이 컴포넌트가 아닌 직접 제작

`Product List / Coupon` ▸ `Expired`의 썸네일 덮개입니다.

| 항목 | `Dim` 컴포넌트 | 이 레이어 |
| --- | --- | --- |
| 타입 | COMPONENT | **FRAME** (인스턴스 아님) |
| 레이어명 | `Dim` | **`Dim`** (동일) |
| 크기 | 80 × 80 | 80 × 80 (동일) |
| 투명도 | `Opacity_Black_100` **75%** | **`Opacity_Black_200` 50%** |

[Dim 문서](syrup-dim-components.md) 점검 2에서 지적한 바로 그 건입니다. **이름·크기·역할이 같은데 투명도만 다릅니다.**

전체 화면 딤(75%)과 **요소 단위 딤**(50%)은 목적이 달라 값이 다를 수 있습니다. 의도라면 `Dim` 컴포넌트에 variant를 추가하거나 요소용 딤을 따로 명명하는 편이 낫습니다.

### 5. 마스터 2종 사용 0건 — 과거 집계

| 컴포넌트 | 인스턴스 |
| --- | --- |
| `Product List / Product` | **0** |
| `Product List / Coupon` | **0** |

> 이 수치는 2026-10-12의 기존 집계예요. 현재 Section 1과 Usage에 두 마스터의 사용 사례가 추가되어, 현재 사용 여부를 뜻하지 않아요. 다른 파일·디태치·코드 사용은 포함하지 않아요.

리스트 행은 반복 배치되는 요소라 보드에 대표 1개만 그려 두는 경우가 많습니다. [List Row](syrup-list-row-components.md)(15종 전부 0건)와 같은 양상입니다.

### 6. 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| [Product Grid](syrup-product-grid-components.md) | `Product Grid / Icon / Stamp` | **2** |
| [Button](syrup-button-components.md) | `Button` | 1 |
| `❖System Components` | `Title Bar` · `Section Header` | 2 (보드 표기) |

**외부 라이브러리 인스턴스는 0건**입니다.

> `Icon / Stamp`는 2026-10-12에 `Property 1` → `Type`으로 정리했습니다. 이 페이지 인스턴스도 자동 반영되었습니다.

### 7. 미바인딩 값

| 값 | 건수 | 성격 |
| --- | --- | --- |
| fill `#A8A8A8` | 1 | 회색, Gray 스케일 밖 |
| radius `2` | 1 | 작은 값 |
| gap `14` | 1 | `Product` variant — 스케일 밖 |
| padding `100` | 2 | 문서 보드 |

**미바인딩이 전체 4건뿐**으로 매우 적습니다. 컴포넌트 기준으로는 3건입니다.

### 8. 토큰 상태 — 양호

| 항목 | 결과 |
| --- | --- |
| **원격 텍스트 스타일** | **0건** |
| **제어문자 · U+2028** | **0건** |
| 미바인딩 (컴포넌트) | **3건** |
| 스타일 미적용 텍스트 | **2건** — `11 Bold` ("D-19") |
| **외부 토큰** | **`Spec docs` 3건**만 — `typeset_xs_bold` 10건은 2026-10-12 해제 ([1](#1--외부-토큰-typeset_xs_bold-10건-해제-2026-10-12-완료)) |
| 폰트 | 전부 Pretendard |

스타일 미적용 2건은 **11px**이라 토큰화하지 않기로 한 범주입니다.

**이 페이지는 매우 깨끗합니다.** 남은 외부 토큰은 문서 레이아웃 전용 `Spec docs` 3건뿐입니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-12)

| 항목 | 내용 |
| --- | --- |
| `typeset_xs_bold` 외부 변수 **10건** 해제 ([1](#1--외부-토큰-typeset_xs_bold-10건-해제-2026-10-12-완료)) | 값 유지 · 페이지 외부 토큰은 `Spec docs`만 잔존 |
| `Property 1` → `State` ([2](#2--property-1--state--d-day--dday-2026-10-12-완료)) | 페이지 내 `Property 1` **0건** |
| `D-day` → `Dday` ([2](#2--property-1--state--d-day--dday-2026-10-12-완료)) | 파일 내 유일한 하이픈 프로퍼티명 해소 |

전부 **크기·렌더링 변화가 없습니다.** 작업 후 컴포넌트셋 178개 · 인스턴스 1,828개를 전수 검증해 오류·끊긴 참조 **0건**을 확인했습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | gap `14` · `Media` 폭 332 확인 ([3](#3-variant-간-규칙-공유가-거의-없음)) | 값 확인 | 낮음 |
| 2 | `Dim` 처리 방식 ([4](#4-dim이-컴포넌트가-아닌-직접-제작)) | **Dim 페이지와 함께 판단** | 중간 |

### 이 페이지 밖으로 이어지는 과제

| 항목 | 내용 |
| --- | --- |
| 스타일 없이 외부 타이포 변수가 걸린 노드 **18건** | `Ticker` 15 · `Bottom Info` 2 · `List Header` 1 — 해당 페이지 문서화 시 함께 정리 |
