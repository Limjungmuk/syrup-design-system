# Syrup Design System — Badge 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Badge` 페이지 → [Badge 섹션 `8469:24881`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8469-24881) |
| 섹션 구성 | `Badge` 1440×1508 → `Guidelines` 960×1908 → `Usage` 2160×914.5 (가로 일렬) |
| 기준일 | 2026-11-03 (Usage·Guidelines 전면 개편 / 컷을 컴포넌트 인스턴스로 교체 / 스펙 정리: 2026-10-08) / 2026-11-11 variant별 배경·오버라이드 처리 보완 |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **콘텐츠의 상태나 속성을 강조해 보여주는 컴포넌트예요.**
> 보상, LIVE, NEW, 예정, 완료 등 상태를 표시할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Badge / Icon` | `8469:25130` |

## 목차

1. [2026-10-08 변경 요약](#2026-10-08-변경-요약)
2. [구성 한눈에 보기](#구성-한눈에-보기)
3. [Badge — Master Component](#1-badge--master-component)
4. [Child Item — Badge / Icon](#2-child-item--badge--icon)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [점검 필요 사항](#점검-필요-사항)

---

## 2026-10-08 변경 요약

### 1. `Shape`에 pill 형태 신설 + 이름 정리

`Shape` 축이 2 → **3옵션**이 되고, variant는 11 → **12개**가 되었습니다. 신설 직후에는 이름과 모양이 뒤바뀌어 있었으나 **같은 날 교환해 정리**했습니다.

| Shape | Radius | 모양 | 개수 |
| --- | --- | --- | --- |
| **`Pill`** | `Corner radius/circle` (S) · `Corner radius/500` (M) | **알약형** | 4 |
| **`Rounded`** | `Corner radius/100` (4) | 라운드 사각형 | 4 |
| `Flag` | 우하단만 `Corner radius/150` (6) | 깃발 꼬리 | 4 |

**세 Shape가 4종씩 균등**해졌습니다. 기존 `Pill` 4종(S)이 `Rounded`로 이름이 바뀌었고, 신설된 알약형이 `Pill`을 가져갔습니다.

### 2. `Size=S` 높이 22 → **20**

S 계열 variant의 높이가 모두 2px 줄었습니다. **폭은 아이콘 축소(아래 4번)로 기존 값으로 돌아왔습니다.**

| Variant | 전 | 후 |
| --- | --- | --- |
| S · Gold · Rounded / Flag | 43 × **22** | 43 × **20** |
| S · Stamp · Rounded / Flag | 50 × **22** | 50 × **20** |
| S · Gold · Disabled | 96 × **22** | 96 × **20** |
| S · Stamp · Disabled | 83 × **22** | 83 × **20** |
| **S · Gold · Pill** 🆕 | — | **45 × 20** |

### 3. `Size=S` 패딩·간격 변경

| 항목 | 전 | 후 |
| --- | --- | --- |
| 상하 패딩 | `Spacing/50` (2) | **1** |
| Gold 좌우 패딩 | `Spacing/100` (4) | **5** |
| Stamp 좌 / 우 패딩 | 2 / `Spacing/100` (4) | `Spacing/50` (2) / **5** |
| Gold 간격 | `Spacing/50` (2) | **1** |
| **`Pill` 좌우 패딩** 🆕 | — | **6** |

### 4. 아이콘 15 × 15로 통일 (원본 포함)

`Size=S`의 아이콘이 **원본 컴포넌트까지 15 × 15**가 되었습니다.

| 대상 | 전 | 후 |
| --- | --- | --- |
| `Badge / Icon` ▸ `Size=S, Image=Gold` | 16 × 16 | **15 × 15** |
| `Badge / Icon` ▸ `Size=S, Image=Stamp` | 16 × 16 | **15 × 15** |
| `Badge / Icon` ▸ `Size=M, Image=Gold` | 20 × 20 | 변화 없음 |
| Badge 내 S 아이콘 인스턴스 | 16 → 15 축소 지정 | **원본과 동일** |

**원본이 15가 되어 인스턴스 쪽 축소 지정이 더 이상 필요 없습니다.** 파일 전체 27곳의 사용처를 조사한 결과 **전부 원본 크기와 일치**합니다.

| 아이콘 | 사용처 | 크기 |
| --- | --- | --- |
| `Size=M, Image=Gold` | 16곳 | 20 × 20 |
| `Size=S, Image=Gold` | 8곳 | 15 × 15 |
| `Size=S, Image=Stamp` | 3곳 | 15 × 15 |

16으로 쓰는 곳이 남아 있지 않아 **다른 페이지 영향은 없습니다.**

### 5. `Size=S` + `Check=True` 신설

체크 상태가 M에만 있었는데 **S에도 추가**되어 variant가 12 → **13개**가 되었습니다.

| 신규 variant | 크기 | 구성 |
| --- | --- | --- |
| `Check=True, Size=S, Icon=Gold, Shape=Pill` | **20 × 20** | `Checkbox` ▸ `Variant=Circle, Size=L, Checked=True` 인스턴스 1개 |

M의 체크(30 × 30)와 같은 구조이며, 배경은 `Color/Primary_Orange`입니다.

라운드는 신설 당시 `66.67` 리터럴이었으나 같은 날 **`Corner radius/circle`로 바인딩**했습니다 → [점검 10](#10--s-check의-라운드-토큰-바인딩-2026-10-08-완료)

### 6. Stamp 비활성 아이콘 소스 통일

`S · Stamp · Rounded · Disabled` 1종만 구 에셋 `🟧syrup_img_shopping_badge_stamp`를 쓰고 있어 **`Badge / Icon`으로 교체**했습니다 → [점검 11](#11--stamp-비활성-아이콘-소스-통일-2026-10-08-완료)

**`Size=M`은 변화가 없습니다.**

> ⚠️ 변경된 간격 값 대부분이 **토큰 바인딩이 풀린 상태**입니다 → [점검 4](#4--토큰-미바인딩-값--2026-10-08-간격-변경으로-크게-늘어남)

---

## 구성 한눈에 보기

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Badge` | Component Set | `Check` × `Disabled` × `Size` × `Icon` × `Shape` (**13종**) | 20~30 높이 |
| 2 | `Badge / Icon` | Component Set | `Size` × `Image` (3종) | **15×15** · 20×20 |

---

## 1. Badge — Master Component

**Node** `8469:25159` · Component Set · **13 variants**

### Properties

| Property | Type | Default | Options | 역할 |
| --- | --- | --- | --- | --- |
| `Text` | TEXT | `3금` | — | 라벨 문구 |
| `Check` | VARIANT | `False` | `False` · `True` | 체크 완료 상태 (라벨 없는 원형) |
| `Disabled` | VARIANT | `False` | `False` · `True` | 비활성 |
| `Size` | VARIANT | `M` | `M` · `S` | 높이 M 30 / S 20 |
| `Icon` | VARIANT | `Gold` | `Gold` · `Stamp` | 좌측 아이콘 종류 |
| `Shape` | VARIANT | `Pill` | `Pill` · `Rounded` · `Flag` | 모서리 처리 |

### Variant 조합 현황

5개 축이면 **48조합**이 가능하지만 실제로는 **13개**만 존재합니다. 네 묶음으로 나뉩니다.

| 묶음 | 조합 | 개수 |
| --- | --- | --- |
| **M / Gold / Pill** | 기본 · Check=True · Disabled=True | 3 |
| **S / Pill** | 기본 · **Check=True** (둘 다 Gold 활성) | **2** |
| **S / Rounded** | Gold·Stamp × Disabled False·True | 4 |
| **S / Flag** | Gold·Stamp × Disabled False·True | 4 |

즉 **`Size=M`은 `Gold` + `Pill`로만 존재**하고, `Stamp`는 `Size=S` 전용입니다. **`Check=True`는 M·S 양쪽에 생겼으며 둘 다 `Gold` + `Pill` + 활성 조합**입니다.

### 지원 조합과 완료 상태 적용 범위 (2026-11-18)

- 실제 지원은 위 표의 13종뿐입니다. 속성 옵션을 자유롭게 곱해 새 조합을 만들지 않아요.
- M은 Gold·Pill의 기본/비활성/체크 3종입니다. S·Pill은 Gold의 기본/체크 2종이며 비활성이 없어요. S·Rounded와 S·Flag는 각각 Gold/Stamp × 활성/비활성의 4종입니다.
- `Check=True`는 **Gold·Pill·Disabled=False의 M/S에만** 적용해요. 적립 완료 시 금액·아이콘이 사라지고 체크 원형이 되며, 높이는 M 30/S 20을 유지해요. 폭까지 유지하는 뜻은 아니에요.
- Rounded·Flag·Stamp에는 체크 완료 variant가 없어요. 완료를 표현하려고 Pill로 바꾸거나 체크를 임의로 추가하지 않아요. 해당 상위 컴포넌트의 완료 규칙이 없으면 확인이 필요해요. 체크와 비활성은 함께 사용할 수 없어요.
- 비활성은 **현재 원본 표현이 의도된 기준**입니다(사용자 재확인, 2026-11-18). M은 배경 `Color/Gray_500`·글자 `Color/Gray_White`, S는 배경 `Color/Opacity_Black_200`·글자 `Color/Gray_800`을 유지해요. M의 흰 글자는 오류가 아니며 S 기준으로 통일하거나 보정하지 않아요.

### 상위 컴포넌트 안의 배치 기준 (2026-11-18)

- 뉴스는 `Card / News` 기본 인스턴스 내부의 기존 Badge를 사용해요. M·Gold·Pill을 카드 상단·우측 각각 8px에 배치해요. 문구 변경으로 HUG 너비가 바뀌거나 체크 30×30으로 전환돼도 높이 30과 우측 8px을 유지해요.
- 쇼핑은 `Product Grid`의 Shopping 내부 배지를 사용해요. 기본 인스턴스에서는 외부 그리드가 Shopping이어도 내부 상품이 Live일 수 있어요. 각 `Product Grid / List Item`의 `Variant`도 Shopping으로 선택한 뒤 배지를 설정해요. S·Rounded를 **상품 썸네일** 왼쪽·위 각각 10px에 배치해요. 카드 전체나 상품명 영역이 기준이 아니에요. 쿠팡은 Stamp, 그 외 쇼핑몰은 Gold를 선택하고 비활성 표현도 해당 원본을 따라요.
- 지금 탭은 `Card / Now`의 기존 S·Gold·Flag를 사용해요. 배지 시작점은 **카드 바깥이 아닌 썸네일의 (0,0)**이에요. 문구 변경 시 높이 20과 좌상단 밀착을 유지하며 너비만 HUG로 바뀌어요.
- 배지를 별도로 겹쳐 추가하거나 중복 배치하지 말고, 상위 인스턴스 내부의 기존 Badge 속성을 변경해요. 지원하지 않는 체크 상태는 추가하지 않아요.

### 전체 스펙

| Variant | 크기 | Padding (T/R/B/L) | Gap | 배경 | 텍스트 색 | Radius |
| --- | --- | --- | --- | --- | --- | --- |
| M · Gold · Pill | 64 × 30 | **5** / 10 / **5** / 10 | 4 | `Color/Primary_Orange` | `Color/Gray_White` | `Corner radius/500` (20) |
| M · Gold · Pill · **Check** | 30 × 30 | 0 | 0 | `Color/Primary_Orange` | — | `Corner radius/circle` |
| M · Gold · Pill · **Disabled** | 85 × 30 | 4 / 8 / 4 / 8 | 4 | `Color/Gray_500` | `Color/Gray_White` | `Corner radius/500` (20) |
| **S · Gold · Pill** | 45 × 20 | **1** / 6 / **1** / 6 | **1** | `Color/Primary_Orange` | `Color/Gray_White` | **`Corner radius/circle`** |
| **S · Gold · Pill · Check** 🆕 | 20 × 20 | 0 | 0 | `Color/Primary_Orange` | — | `Corner radius/circle` |
| S · Gold · Rounded | 43 × 20 | **1 / 5 / 1 / 5** | **1** | `Color/Primary_Orange` | `Color/Gray_White` | `Corner radius/100` (4) |
| S · Stamp · Rounded | 50 × 20 | **1 / 5 / 1** / 2 | 0 | **#BA44FF** ⚠️ | `Color/Gray_White` | `Corner radius/100` (4) |
| S · Gold · Rounded · **Disabled** | 96 × 20 | **1 / 5 / 1 / 5** | **1** | `Color/Opacity_Black_200` | `Color/Gray_800` | `Corner radius/100` (4) |
| S · Stamp · Rounded · **Disabled** | 83 × 20 | **1 / 5 / 1** / 2 | 0 | `Color/Opacity_Black_200` | `Color/Gray_800` | `Corner radius/100` (4) |
| S · Gold · Flag | 43 × 20 | **1 / 5 / 1 / 5** | **1** | `Color/Primary_Orange` | `Color/Gray_White` | BR만 `Corner radius/150` (6) |
| S · Stamp · Flag | 50 × 20 | **1 / 5 / 1** / 2 | 0 | **#BA44FF** ⚠️ | `Color/Gray_White` | BR만 `Corner radius/150` (6) |
| S · Gold · Flag · **Disabled** | 96 × 20 | **1 / 5 / 1 / 5** | **1** | `Color/Opacity_Black_200` | `Color/Gray_800` | BR만 `Corner radius/150` (6) |
| S · Stamp · Flag · **Disabled** | 83 × 20 | **1 / 5 / 1** / 2 | 0 | `Color/Opacity_Black_200` | `Color/Gray_800` | BR만 `Corner radius/150` (6) |

모든 variant는 **HORIZONTAL 오토레이아웃**이며 폭은 라벨 길이에 따라 HUG로 늘어납니다.

Stamp의 좌측 패딩 2만 `Spacing/50` 토큰이고, **굵게 표시한 값은 전부 토큰 미바인딩**입니다.

### Shape별 모서리 처리

| Shape | 모서리 (TL / TR / BR / BL) | 비고 |
| --- | --- | --- |
| `Pill` (M) | 20 / 20 / 20 / 20 | `Corner radius/500` — 높이 30이라 완전 pill |
| **`Pill` (S)** 🆕 | **100 / 100 / 100 / 100** | `Corner radius/circle` — 완전 pill |
| `Rounded` (S) | 4 / 4 / 4 / 4 | `Corner radius/100` — 라운드 사각형 |
| `Flag` (S) | 0 / 0 / **6** / 0 | 우하단만 `Corner radius/150` — 깃발 꼬리 형태 |
| `Check=True` | 100 (circle) | `Corner radius/circle` |

**이름과 모양이 일치합니다.** M·S 모두 `Pill`이 알약형이고 `Rounded`가 라운드 사각형입니다 ([점검 8](#8--pill과-rounded-이름-교환-2026-10-08-완료)).

다만 `Pill`의 라운드 토큰이 **M은 `Corner radius/500`(20), S는 `Corner radius/circle`(100)** 로 다릅니다. 높이 30·20에서는 둘 다 완전 pill로 보여 결과는 같습니다.

### 아이콘 크기

| Variant | 아이콘 | 소스 |
| --- | --- | --- |
| M · Gold | 20 × 20 | `Badge / Icon` ▸ `Size=M, Image=Gold` |
| M · Check | 30 × 30 | `Checkbox` ▸ `Variant=Circle, Size=L, Checked=True` |
| **S · Check** 🆕 | **20 × 20** | `Checkbox` ▸ `Variant=Circle, Size=L, Checked=True` |
| **S 라벨형 (9종)** | **15 × 15** | `Badge / Icon` ▸ `Size=S` |
| M · Disabled | — | 아이콘을 일반 프레임으로 감쌈 |

**`Size=S`의 아이콘이 원본까지 15 × 15로 통일**되었습니다 ([점검 9](#9--s-아이콘-15px-통일-2026-10-08-완료)). 인스턴스 쪽 축소 지정이 없어져 원본과 값이 일치합니다.

| 내부 이미지 | 크기 |
| --- | --- |
| `Size=M, Image=Gold` › `gold_test4 1` | 20 × 13 |
| `Size=S, Image=Gold` › `gold_test4 1` | 15 × 10 |
| `Size=S, Image=Stamp` › `image 3244` | 10 × 11 |

> `S · Stamp · Rounded · Disabled`를 포함한 Stamp variant는 `Badge / Icon`을 사용합니다. 구 에셋 교체 기록은 아래 점검 11을 참고하세요. → [점검 11](#11--stamp-비활성-아이콘-소스-통일-2026-10-08-완료)

### 타이포그래피

| Size | 스타일 | 스펙 |
| --- | --- | --- |
| M | `t1060_13_bold` | 13 / 18 / 0 |
| S | **미적용** ⚠️ | Pretendard **11 Bold** / line-height 18 |

`Size=M`은 2026-09-21에 신설된 `t1060_13_bold`가 적용되어 있습니다. `Size=S`의 라벨형 9개 variant는 스타일 없이 11px Bold를 직접 지정하고 있습니다.

### `Check=True` 구조

라벨 없는 원형이며 **M은 30×30, S는 20×20**입니다. 내부는 `Checkbox` 인스턴스 하나예요. 아래 내부 레이어 치수는 M 기준입니다.

| 레이어 | 크기 | 색 |
| --- | --- | --- |
| `Oval` | 30 × 30 | `Color/Primary_Orange` |
| `Fill` (체크 표시) | 16 × 11 | `Color/Gray_White` |

### `Disabled=True` 구조 차이

`Size=M`의 비활성 variant만 **아이콘·텍스트를 컴포넌트 인스턴스가 아닌 일반 프레임**(`Frame 1171276799` · `Frame 1171277333`)으로 감싸고 있습니다. 나머지 variant는 `Badge / Icon` 인스턴스를 직접 씁니다.

---

## 2. Child Item — Badge / Icon

**Node** `8469:25130` · Component Set · 3 variants

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `M` | `S` · `M` |
| `Image` | VARIANT | `Gold` | `Gold` · `Stamp` |

| Variant | 크기 | 내용 | 내부 이미지 |
| --- | --- | --- | --- |
| `Size=M, Image=Gold` | 20 × 20 | `gold_test4 1` (금 이미지) | 20 × 13 |
| `Size=S, Image=Gold` | **15 × 15** | `gold_test4 1` | 15 × 10 |
| `Size=S, Image=Stamp` | **15 × 15** | `image 3244` (스탬프 이미지) | 10 × 11 |

`Size=S` 두 종이 2026-10-08에 16 × 16 → **15 × 15**로 변경되었습니다.

- `Size=M, Image=Stamp` 조합은 **없습니다.** Badge 본체에 M + Stamp 조합이 없는 것과 대응됩니다.
- 세 variant에 있던 숨겨진 `#00D9FF` 30% fill은 **2026-10-08 제거**했습니다 → [점검 7](#7--숨겨진-작업-흔적-제거-2026-10-08-완료)

---

## 설계 규칙 요약

| 항목 | 규칙 |
| --- | --- |
| 높이 | M = 30, **S = 20** (폭은 라벨 길이에 따라 HUG) |
| 활성 배경 | Gold: `Color/Primary_Orange` (#FF6315) · Stamp: 원본 보라색 (#BA44FF 표기) · 선택한 variant의 실제 원본을 우선 |
| 기본 텍스트 | `Color/Gray_White` |
| 비활성 배경 | M `Color/Gray_500` · S `Color/Opacity_Black_200` |
| 비활성 텍스트 | M `Color/Gray_White` · S `Color/Gray_800` (#E4E4E4) |
| 아이콘 | M 20×20 · **S 15×15** (원본 포함), 라벨 좌측 |
| 체크 상태 | M 30×30 · **S 20×20**, 내부는 `Checkbox` 인스턴스 |
| 모서리 | **Pill = 알약형** (M 20 · S 원형) · **Rounded = 라운드 사각형** (4) · Flag 우하단만 6 · Check 원형 |
| 패딩 (M) | 상하 5 / 좌우 10 (비활성 4 / 8) |
| 패딩 (S) | 상하 **1** / 좌우 **5** (Stamp 좌 `Spacing/50` 2 · `Pill` 좌우 `Spacing/150` 6) |
| 간격 | M 4 · S **1** (Stamp 0) |
| 라벨 | M `t1060_13_bold` · S 11px Bold (스타일 미적용) |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11224:22`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11224-22) · 2160 × 914.5 |
| 구성 | 5패턴 · 폭 360 · 높이는 내용에 맞춰 243~714.5 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-03).

패턴 하나가 `Usage` 템플릿 인스턴스 하나입니다. 템플릿은 `Title`(제목 + 설명)과 `Component` **슬롯**으로 이루어져 있고, 슬롯 안에 그 패턴을 보여 줄 인스턴스를 넣습니다. 가로 간격은 40입니다.

**패턴을 가르는 기준이 바뀌었습니다.** 전에는 variant별로(`Pill` · `Check` · `Disabled` · `S` · `Rounded` · `Stamp`) 6패턴이었는데, 지금은 **배지가 놓이는 자리**별로 5패턴입니다. 배지는 혼자 놓이는 일이 거의 없어(아래 [직접 놓는 것과 따라오는 것](#직접-놓는-것과-따라오는-것이-다릅니다)) 담기는 컴포넌트까지 함께 보여야 규칙이 보입니다.

| | 패턴 | 설명 | 담은 컴포넌트 | 배지 | 슬롯 높이 |
| --- | --- | --- | --- | --- | --- |
| **A** | 기본 · 완료 | 적립 전에는 받을 금액을 표시하고, 적립을 완료하면 금액 대신 체크 아이콘을 표시해요. 배지 높이는 30으로 유지해요. | `Card / News` × 2 (360 × 291.3 · 간격 16) | `M`·`Pill`·`Gold` 「3금」 64 × 30 / `Check=True`·`M` 30 × 30 — 둘 다 카드 우상단 | 598.5 |
| **B** | 비활성 | 아직 받을 수 없는 상태에는 회색 배지를 사용해요. 「방송예정」처럼 받을 수 없는 이유를 함께 적어요. | `Product Grid`·`Shopping` — 내부 `Grid List Item`·`Live` 2칸 | `Disabled=True`·`M` 「방송예정」 85 × 30 · 썸네일 (67, 6) | 251 |
| **C** | 작은 크기 | 2열 카드처럼 개별 항목의 너비가 좁은 경우 Size=S를 사용해요. 배지 높이는 기본 30에서 20으로 줄어들어요. | `img_contents` × 2 (156 × 127 · 간격 8) | `S`·`Pill` 「3금」 45 × 20 / `Check=True`·`S` 20 × 20 | 127 |
| **D** | 쇼핑 리스트 | 쇼핑 리스트의 상품 썸네일에는 Shape=Rounded 배지를 사용해요. 썸네일 왼쪽 위에서 가로·세로 각각 10 안쪽에 배치해요. | `Product Grid`·`Shopping` 4칸 (158 × 248 · 가로 12 · 세로 24) | `Rounded`·`S` 4종 · 전부 (10, 10) | 520 |
| **E** | 지금 탭 콘텐츠 카드 | 지금 탭 콘텐츠 영역의 Card / Now에는 Shape=Flag 배지를 사용해요. | `Card / Now`·`Type=Action` (328 × 156) | `Flag`·`S`·`Gold` 「2,400금」 66 × 20 · 썸네일 (0, 0) | 188 |

**D의 네 칸은 `Rounded` 4종을 한 번에 보여 줍니다.**

| 칸 | 배지 | 크기 | 상점 |
| --- | --- | --- | --- |
| 왼쪽 위 | 금 「2,400금」 | 66 × 20 | 핫딜쇼핑 |
| 오른쪽 위 | 스탬프 「스탬프」 | 50 × 20 | 쿠팡 |
| 왼쪽 아래 | 금 · 비활성 「만원 당 1,000금」 | 96 × 20 | 핫딜쇼핑 |
| 오른쪽 아래 | 스탬프 · 비활성 「만원 당 스탬프」 | 83 × 20 | 쿠팡 |

### 다섯 패턴 모두 맥락 컴포넌트를 함께 넣었습니다

**배지 단독 컷은 하나도 없습니다.** Shape를 무엇으로 쓸지가 전부 **어느 컴포넌트에 담기느냐**로 갈리기 때문입니다 ([Guidelines 3 · 4](#3-쇼핑몰에-맞는-리워드-배지를-사용해요)).

| 패턴 | 담은 컴포넌트 | 이 자리에서만 보이는 것 |
| --- | --- | --- |
| **A** | `Card / News` | 적립 전·후가 **같은 자리에서 바뀌는** 것. 카드 두 장을 위아래로 두어 비교합니다 |
| **B** | `Product Grid`·`Live` | 비활성이 **썸네일 위**에서 어떻게 읽히는지. 회색 배지는 배경이 있어야 의미가 생깁니다 |
| **C** | `img_contents` | 「너비가 좁은 경우」가 설명의 전제라, 156 폭 카드가 없으면 S를 쓰는 이유가 안 보입니다 |
| **D** | `Product Grid`·`Shopping` | 「왼쪽 위에서 10 안쪽」이라는 **위치** 규칙 |
| **E** | `Card / Now` | `Flag`가 **썸네일 모서리에 딱 붙는다**는 것. 깃발 모양은 모서리에 붙어야 성립합니다 |

**C의 슬롯에만 레이아웃용 빈 프레임이 하나 더 있습니다** (`Frame 1` · 320 × 127). 카드 두 장을 가로로 8 띄워 놓으려고 필요해서, 칠도 선도 없는 투명 프레임입니다. E는 슬롯 안쪽 여백 16으로 처리했습니다.

### 직접 놓는 것과 따라오는 것이 다릅니다

제품 파일 [`Syrup_App`](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i/Syrup_App) 기준 **328건**인데, 그중 **280건이 다른 컴포넌트 안에 들어 있는 것**입니다. 축별로 보면 갈림이 뚜렷합니다.

| 축 | 직접 배치 | 다른 컴포넌트 안 | 합계 |
| --- | --- | --- | --- |
| `Pill` | 28 | 245 | 273 |
| `Rounded` | 20 | 17 | 37 |
| **`Flag`** | **0** | **15** | 15 |
| **`Stamp`** | **0** | **9** | 9 |
| **`Disabled`** | **0** | **14** | 14 |

**위 직접 배치 건수는 2026-11-03 조사 당시의 사용 현황이며 직접 배치를 금지하는 규칙이 아닙니다.** Flag·Stamp·Disabled는 당시 상위 컴포넌트 안에서 사용됐어요. 기존 화면 제작에서는 해당 상위 컴포넌트의 배지와 상태 속성을 우선 사용하고, 수정 시 상위 맥락도 함께 확인해요.

> 직접 집계만 보면 `Flag`가 0건이라 미사용으로 보이지만, **중첩까지 세면 15건이 쓰이고 있습니다.** 13개 variant가 전부 어딘가에서 쓰이고 있어 삭제 후보는 없습니다.

이번 개편의 Usage가 바로 이 집계를 그대로 따릅니다. **`Flag`와 `Stamp`도 이제 제 패턴을 가졌고**(E · D), 어느 상위 컴포넌트에 들어 있는지까지 컷에 드러나 있습니다.

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11224:35`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11224-35)** (960 × 1908) 에 들어 있습니다. 규칙이 1개에서 **4개**로 늘었습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 `Do` · `Don't` **슬롯**이 좌우로 들어갑니다. 세로 간격은 100입니다.

### 1. 리워드가 있는 항목에 금 배지를 사용해요

리워드가 제공되는 항목에 금 배지를 표시해요. 받을 수 있는 금액을 안내할 때는 ‘20금’, 적립 행동을 유도할 때는 ‘더 모으기’처럼 문구를 사용해요.

| 라벨 | 컷 | 배지 |
| --- | --- | --- |
| **리워드 금액 안내** | `Card / News` 「Syrup 만족도 평가하고 20금 받기」 | `M`·`Pill`·`Gold` 「20금」 72 × 30 |
| **적립 행동 유도** | `Card / News` 「누르면 금이 더 쌓이는 광고판」 | `M`·`Pill`·`Gold` 「더 모으기」 92 × 30 |

두 컷 모두 **같은 `Card / News` 인스턴스 320 × 250**이고, 레이어 이름도 화면에 보이는 라벨과 같습니다. 카드 종류·크기·배지 variant가 전부 같아서 **다른 것은 문구와 소재뿐**입니다.

**이 규칙만 Do / Don't가 아닙니다.** 슬롯 라벨을 「리워드 금액 안내」·「적립 행동 유도」로 바꿔 **두 경우를 나란히 비교**합니다. 「더 모으기」가 틀린 문구가 아니라 쓰이는 자리가 다를 뿐이기 때문입니다.

제품 파일 **328건 중 325건이 금액**입니다. 행동 문구는 3건뿐이고 **전부 같은 자리** — 「누르면 금이 더 쌓이는 광고판」입니다. 보는 광고마다 적립액이 달라 숫자를 쓸 수 없는 경우입니다.

| 상황 | 문구 | 건수 |
| --- | --- | --- |
| 받을 금액이 정해짐 | 「3금」 처럼 숫자 | 325 |
| 적립액이 유동적 (광고판) | 「더 모으기」 | 3 |

> 초판에서는 이 3건을 규칙 위반으로 보고 Don't 샘플로 썼습니다. **의도된 쓰임**으로 확인된 뒤 한번 더 바뀌어, 지금은 Don't가 아니라 **두 번째 정상 사례**로 나란히 놓여 있습니다.

### 2. 좁은 영역에서는 작은 배지를 사용해요

2열 카드처럼 개별 항목의 너비가 좁은 경우 Size=S를 사용해요. 큰 배지는 상품 이미지를 과도하게 가릴 수 있어요.

| | 컷 | 배지 |
| --- | --- | --- |
| **Do** | `img_contents` 2열 (각 156 폭) | `S`·`Pill` 「3금」 45 × 20 + `Check=True`·`S` 20 × 20 |
| **Don't** | `P_AD`·`Type=Popup` (360 폭) | `S`·`Pill` 「3금」 45 × 20 |

Do는 Usage **C**와 같은 컷입니다. Don't는 반대로 **폭이 넉넉한 팝업 광고에 작은 배지를 쓴 경우**입니다. 설명의 둘째 문장은 Do 쪽 근거만 말하고 있어, 넓은 자리에서는 왜 M이 맞는지 한 줄이 더 있으면 컷과 문구가 맞아떨어집니다.

### 3. 쇼핑몰에 맞는 리워드 배지를 사용해요

쇼핑 콘텐츠의 리워드 배지는 Shape=Rounded를 사용해요. 쿠팡에는 스탬프 배지를, 그 외 쇼핑몰에는 금 배지를 사용해요.

배경색은 선택한 variant의 원본을 따라요. 활성 Gold는 `Color/Primary_Orange`, 활성 Stamp는 원본의 보라색 배경을 사용해요. Gold에서 Stamp로 변경할 때 주황색 배경 오버라이드를 유지하지 않아요. 비활성·완료 상태도 해당 variant의 원본 표현을 유지해요.

| | 핫딜쇼핑 | 쿠팡 |
| --- | --- | --- |
| **Do** | 금 「2,400금」 | 스탬프 「스탬프」 |
| **Don't** | 스탬프 「스탬프」 | 금 「2,400금」 |

두 컷의 차이는 **배지를 맞바꾼 것** 하나입니다. 상품·가격·썸네일은 그대로 두고 제휴사 이름만 바뀔 때 어떤 배지가 따라와야 하는지를 보여 줍니다.

### 4. 지금 탭의 콘텐츠 카드에는 Flag 배지를 사용해요

지금 탭 콘텐츠 영역의 Card / Now에는 Shape=Flag를 사용해요. 다른 영역에서는 각 콘텐츠의 배지 형태 기준을 따라요.

| | 배지 | 크기 |
| --- | --- | --- |
| **Do** | `Flag`·`S`·`Gold` 「2,400금」 | 66 × 20 |
| **Don't** | 같은 카드에 `Rounded` | 66 × 20 |

두 배지 모두 썸네일 **(0, 0)** — 모서리에 딱 붙어 있습니다. 이 위치에서 `Rounded`를 쓰면 배지의 둥근 왼쪽 위 모서리와 썸네일 모서리 사이가 비어 보입니다. `Flag`는 왼쪽 위·오른쪽 위·왼쪽 아래가 직각이라 그 틈이 없습니다 ([Shape별 모서리 처리](#shape별-모서리-처리)).

### Shape 선택 기준이 정해졌습니다

초판에는 「`Pill`과 `Rounded` 중 무엇을 쓸지 기준을 세우지 못했다」고 적어 두었는데, 이번 개편에서 **놓이는 자리로 가르는 기준**이 정해졌습니다.

| 놓이는 자리 | Shape | 근거 |
| --- | --- | --- |
| 뉴스·광고 카드 (`Card / News` · `img_contents` · `P_AD`) | `Pill` | Usage A · C · 규칙 1 · 2 |
| 쇼핑 상품 썸네일 (`Product Grid`) | `Rounded` | Usage D · 규칙 3 |
| 지금 탭 콘텐츠 카드 (`Card / Now`) | `Flag` | Usage E · 규칙 4 |

수집본만 봐서는 판단이 안 됐던 것이 **제품 맥락으로 풀렸습니다.** 어떤 모양이 더 예쁘냐가 아니라 **어느 컴포넌트에 들어가느냐**가 기준입니다. 그래서 Usage의 다섯 컷이 전부 맥락 컴포넌트를 끼고 있습니다.

다만 표의 첫 줄은 **규칙으로 적혀 있지 않고** Usage 컷에서만 보입니다. `Pill`이 기본값이라 굳이 적지 않은 것으로 보이지만, 3·4번이 예외를 명시하는 형식이라 기본값도 한 줄 있는 편이 더 읽히기 쉽습니다.

---

## 점검 필요 사항

### 1. ℹ️ `Size=S` 라벨이 시스템 밖 타이포 (**9곳**) — 토큰화하지 않음

`Size=S`의 9개 variant 라벨이 **텍스트 스타일 없이 Pretendard 11 Bold / line-height 18**로 지정되어 있습니다. (`Rounded` 신설로 8 → 9건)

- Syrup에 **11px Bold 스타일이 없습니다.** 11px은 `c200_11_regular`(Regular, lh 16, ls −0.3)뿐입니다.
- line-height 18도 타입 램프(11 → 16) 밖입니다.

**11px은 토큰으로 등록하지 않기로 했습니다** (2026-10-08). 13px이 시스템으로 관리하는 하한이며, 그보다 작은 크기는 예외로 둡니다. Card 페이지의 `11 Medium` 12건도 같은 기준으로 유지됩니다.

따라서 이 9건은 **스타일 미적용 상태가 정상**입니다.

### 2. Stamp 배경색이 팔레트 밖 (2곳)

`S · Stamp · Rounded`와 `S · Stamp · Flag`(활성)의 배경이 **#BA44FF (보라)** 이며 베리어블에 바인딩되어 있지 않습니다. Syrup 팔레트에 없는 색입니다.

Gold 뱃지는 `Color/Primary_Orange`를 쓰는데 Stamp만 보라를 쓰는 구조이므로, **Stamp 전용 브랜드 컬러를 토큰으로 승격**할지 결정이 필요합니다.

### 3. 비활성 배경이 Size별로 다름

| Size | 비활성 배경 | 성격 |
| --- | --- | --- |
| M | `Color/Gray_500` (#999999) | **불투명** |
| S | `Color/Opacity_Black_200` (검정 50%) | **반투명** |

반투명이면 뒤 배경이 비치므로 놓이는 위치에 따라 색이 달라집니다. 두 사이즈의 비활성 표현이 서로 다른 결과를 냅니다.

### 4. ⚠️ 토큰 미바인딩 값 — **2026-10-08 간격 변경으로 크게 늘어남**

초판 작성 시에는 `Size=S`의 패딩·간격이 **전부 토큰에 바인딩**되어 있었고 미바인딩은 M의 패딩 `5` 2건뿐이었습니다. 이번 간격 변경으로 **S 계열 대부분이 리터럴 값**이 되었습니다.

| 값 | 건수 | 위치 | Spacing 스케일 |
| --- | --- | --- | --- |
| **1** (상·하 패딩) | 18 | S 9개 variant 전부 | ❌ 없음 |
| **1** (간격) | 5 | S Gold 계열 | ❌ 없음 |
| **5** (우 패딩) | 8 | S `Rounded` · `Flag` 8종 | ❌ 없음 |
| **5** (좌 패딩) | 4 | S Gold `Rounded` · `Flag` | ❌ 없음 |
| **5** (상·하 패딩) | 2 | M · Gold · Pill | ❌ 없음 |
| `#BA44FF` | 2 | S Stamp 활성 2종 | 위 2번 항목 |

**미바인딩 라운드는 0건**입니다 (2026-10-08 정리 → [점검 10](#10--s-check의-라운드-토큰-바인딩-2026-10-08-완료)).

#### ✅ S `Pill` 좌우 패딩 바인딩 (2026-10-08 완료)

`S · Gold · Pill` `10908:1860`의 좌우 패딩 `6`은 **`Spacing/150`과 값이 같아 무손실 바인딩**했습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| `paddingLeft` · `paddingRight` | `6` 리터럴 | **`Spacing/150`** (6) |
| 크기 | 45 × 20 | 변화 없음 |

스케일에 있는 값은 이것 하나뿐이었고, 나머지 `1`·`5`는 Spacing 스케일(2 · 4 · 6 · 8 · 10 · 12 · 16 · 20 · 24 · 30) 밖입니다.

나머지 `1`과 `5`는 Spacing 스케일(2 · 4 · 6 · 8 · 10 · 12 · 16 · 20 · 24 · 30)에 없는 값입니다. 선택지는 둘입니다.

| 방향 | 내용 |
| --- | --- |
| **스케일에 맞추기** | 상하 1 → `Spacing/50`(2), 좌우 5 → `Spacing/150`(6) 또는 `Spacing/100`(4). 높이·폭이 다시 바뀜 |
| **토큰 신설** | `Spacing/25`(1) · `Spacing/125`(5) 추가. 스케일이 촘촘해져 관리 부담 증가 |

높이 20을 유지해야 한다면 상하 패딩은 1이어야 하므로(1 + 18 + 1 = 20), **의도된 값일 가능성이 큽니다.** 그렇다면 토큰 신설 쪽이 맞습니다.

> 이 밖에 중첩 인스턴스 내부에 `paddingBottom = 3` 1건, `1.333` 2건이 있습니다. `🟧syrup_img_shopping_badge_stamp` 등 아이콘 에셋 내부 값이라 이 페이지에서 고칠 대상이 아닙니다.

### 5. Stamp variant의 좌우 패딩 비대칭

`Icon=Gold`는 좌우 모두 5인데 `Icon=Stamp`는 **좌측만 2**(`Spacing/50`)입니다. 스탬프 이미지의 여백을 보정한 것으로 보이나, 아이콘 에셋 자체의 여백을 정리하고 패딩을 통일하는 편이 관리가 쉽습니다.

공교롭게도 **Stamp의 좌측 패딩만 유일하게 토큰에 바인딩**되어 있습니다.

### 6. Variant 조합 공백

| 없는 조합 | 비고 |
| --- | --- |
| `Size=M` + `Icon=Stamp` | M은 Gold만 지원 |
| `Size=M` + `Shape=Rounded` · `Flag` | M은 Pill만 지원 |
| `Check=True` + `Disabled=True` | 체크된 비활성 상태 없음 |
| `Size=S` + `Shape=Pill` + `Icon=Stamp` | S의 Pill은 Gold만 |
| `Size=S` + `Shape=Pill` + `Disabled=True` | S의 Pill은 활성만 |

**`Size=S` + `Check=True`는 2026-10-08에 추가되어 공백이 해소**되었습니다. 이제 체크 상태가 M·S 양쪽에 존재합니다.

의도된 제한이면 컴포넌트 설명에 명시해 두는 편이 좋습니다. `Size`가 사실상 두 개의 다른 컴포넌트를 하나의 축에 묶고 있는 형태입니다.

`Size=S`의 `Pill`은 기본·체크 2종이라, 라벨형 기준으로는 `Rounded`·`Flag`(각 4종)와 여전히 대칭이 맞지 않습니다. Stamp·Disabled 조합이 필요한지 확인이 필요합니다.

### 7. ✅ 숨겨진 작업 흔적 제거 (2026-10-08 완료)

`visible: false`인 임시색 fill이 컴포넌트 안에 남아 있었습니다. 화면에는 영향이 없지만 작업 중 흔적이라 정리했습니다.

| Node | 레이어 | 크기 | 제거한 fill |
| --- | --- | --- | --- |
| `8469:25129` | `Badge / Icon` ▸ `Size=M, Image=Gold` | 20 × 20 | `#00D9FF` 30% |
| `8469:25131` | `Badge / Icon` ▸ `Size=S, Image=Gold` | 15 × 15 | `#00D9FF` 30% |
| `8469:25219` | `Badge / Icon` ▸ `Size=S, Image=Stamp` | 15 × 15 | `#00D9FF` 30% |
| `8469:25059` | `Badge` ▸ M·Disabled › `Frame 1171276799` (아이콘 래퍼) | 20 × 20 | `#00D9FF` 30% |
| `8469:25061` | `Badge` ▸ M·Disabled › `Frame 1171277333` (텍스트 래퍼) | 45 × 20 | `#00A1FF` 30% |

**총 5건**입니다. 초판에는 `Badge / Icon`의 3건만 기록했는데, 조사 범위가 좁아 **`Size=M` 비활성 variant 내부의 래퍼 프레임 2건을 놓쳤습니다.** 같은 계열 임시색(`#00D9FF` · `#00A1FF`, 둘 다 30%)으로 동일한 작업 흔적입니다.

공교롭게도 이 두 프레임은 [위 `Disabled=True` 구조 차이](#disabledtrue-구조-차이)에서 "M 비활성만 인스턴스가 아닌 일반 프레임으로 감싼다"고 지적한 바로 그 프레임입니다.

제거 후 크기·렌더링 모두 변화 없습니다(M·Disabled 85 × 30 유지).

#### 남은 숨은 fill 2건 — 제외 대상

| Node | 크기 | fill | 성격 |
| --- | --- | --- | --- |
| `8469:24885` | 1312 × 470 | `#F6F6F7` | **문서 보드 섹션 배경** |
| `8469:25080` | 1312 × 260 | `#F6F6F7` | **문서 보드 섹션 배경** |

컴포넌트가 아니라 보드 레이아웃의 꺼둔 배경색이라 성격이 다릅니다. 그대로 두었습니다.

### 8. ✅ `Pill`과 `Rounded` 이름 교환 (2026-10-08 완료)

알약형 variant를 신설한 직후에는 **이름과 실제 모양이 뒤바뀐 상태**였습니다. 일반적으로 "pill"은 양끝이 반원인 형태를, "rounded"는 모서리만 둥근 사각형을 가리키는데 정반대였습니다.

| Shape | Radius | 모양 | 변경 전 이름 | 변경 후 이름 |
| --- | --- | --- | --- | --- |
| 알약형 | `Corner radius/circle` | ⬭ | `Rounded` | **`Pill`** |
| 라운드 사각형 | `Corner radius/100` (4) | ▢ | `Pill` | **`Rounded`** |

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Shape` 옵션 | `Pill` · `Flag` · `Rounded` | **`Pill` · `Rounded` · `Flag`** |
| Shape별 분포 | Pill 7 · Rounded 1 · Flag 4 | **Pill 4 · Rounded 4 · Flag 4** |

**세 Shape가 4종씩 균등**해졌고, `Size=M`의 `Pill`(`Corner radius/500`, 높이 30)도 실제 pill이라 **M과 S의 `Pill`이 같은 모양**을 가리키게 되었습니다.

> 기존 `Size=S` + `Shape=Pill`을 참조하던 코드·인스턴스는 **이제 다른 모양을 가리킵니다.** 라운드 사각형이 필요한 곳은 `Shape=Rounded`로 바꿔야 합니다.

### 9. ✅ S 아이콘 15px 통일 (2026-10-08 완료)

신설 variant의 아이콘만 15 × 15이고 나머지 S는 16 × 16이어서 어긋나 있었습니다. **15로 통일**했습니다.

| 대상 | 변경 전 | 변경 후 |
| --- | --- | --- |
| Badge 내 S 인스턴스 (9종) | 16 × 16 (신설분만 15) | **15 × 15** |
| **원본 `Badge / Icon` ▸ `Size=S`** | 16 × 16 | **15 × 15** |
| M | 20 × 20 | 변화 없음 |

폭이 1px씩 줄어, 결과적으로 **S variant의 폭이 높이 변경 전 값(43 · 50 · 96 · 83)으로 돌아왔습니다.**

**원본까지 15로 맞춰 인스턴스 쪽 축소 지정이 없어졌습니다.** 파일 전체 27곳의 사용처를 조사한 결과 **전부 원본 크기와 일치**해(`Size=M` 16곳 @20 · `Size=S, Gold` 8곳 @15 · `Size=S, Stamp` 3곳 @15), 다른 페이지에 미친 영향은 없습니다.

### 10. ✅ S `Check`의 라운드 토큰 바인딩 (2026-10-08 완료)

신설된 `Check=True, Size=S`의 라운드가 **토큰이 아닌 `66.67`** 이었습니다. M의 체크는 `Corner radius/circle`을 쓰고 있어 어긋났습니다.

| Variant | 크기 | 변경 전 | 변경 후 |
| --- | --- | --- | --- |
| M · Check | 30 × 30 | `Corner radius/circle` | 변화 없음 |
| **S · Check** `10919:2072` | 20 × 20 | **66.67 리터럴** | **`Corner radius/circle`** (100) |

20 × 20에서 66.67이든 100이든 완전한 원으로 렌더링되어 **시각적 변화는 없습니다.** Chip `Chip / Filter / Item`의 라운드 `60` 건과 같은 성격이었습니다.

**Badge 컴포넌트셋의 미바인딩 라운드는 0건**이 되었습니다. (`Flag`의 TL·TR·BL은 값이 `0`이라 바인딩 대상이 아닙니다.)

### 11. ✅ Stamp 비활성 아이콘 소스 통일 (2026-10-08 완료)

Stamp 아이콘의 출처가 대부분 `Badge / Icon`으로 정리되었으나 1종이 남아 있었습니다.

| Variant | 변경 전 | 변경 후 |
| --- | --- | --- |
| S · Stamp · Rounded | `Badge / Icon` | 변화 없음 |
| S · Stamp · Flag | `Badge / Icon` | 변화 없음 |
| S · Stamp · Flag · Disabled | `Badge / Icon` | 변화 없음 |
| **S · Stamp · Rounded · Disabled** `8469:25197` | **`🟧syrup_img_shopping_badge_stamp`**<br>(`Frame 1171276799` ▸ `Property 1=스탬프`) | **`Badge / Icon`** ▸ `Size=S, Image=Stamp` |

인스턴스 `8469:25185`를 `swapComponent`로 교체했습니다. 교체 전후 모두 15 × 15 · FIXED · 순서 0으로 동일해 **variant 크기(83 × 20)는 변화가 없습니다.**

교체 후 레이어 이름이 구 에셋명(`🟧syrup_img_shopping_badge_stamp`)으로 남아 있어 다른 variant와 같은 **`Badge / Icon`으로 정리**했습니다.

#### 결과

**13개 variant의 아이콘 소스가 두 가지로 정리**되었습니다.

| 소스 | 건수 |
| --- | --- |
| `Badge / Icon` | 10 |
| `Checkbox` (M·S 체크 2종) | 2 |
| 없음 (M · Disabled — 프레임으로 감쌈) | 1 |

구 에셋 `Frame 1171276799`는 **파일 전체에서 사용처 0건**이 되었습니다.

### 12. 정리 대기 노드

[`원본 컷 (정리 전)` `11238:1117`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11238-1117) · 6560 × 1085 · 컷 **16개**

2026-11-03에 컷을 컴포넌트 인스턴스로 바꾸면서 `Usage` 6컷과 `Guidelines` 2컷을 이 섹션으로 옮겼습니다. 앞서 잘라내기 전 원본 8컷이 이미 들어 있어 **합쳐서 16개**입니다. 확인 후 지우면 됩니다.

### 13. ✅ Figma 쪽 자잘한 정리 (2026-11-03 완료)

개편 직후 남아 있던 것들입니다. 모두 반영했고 **렌더링은 어느 것도 바뀌지 않았습니다.**

| 항목 | 결과 |
| --- | --- |
| `Guidelines` 섹션 이름이 비어 있던 것 | `Guidelines`로 복구 |
| 규칙 3 설명의 `사용해요.단,` · 규칙 4와 겹친 문장 | 문장 삭제 (규칙 3 높이 392 → 374) |
| Usage D 왼쪽 아래 칸이 「쿠팡」인데 금 배지 | 상점을 「핫딜쇼핑」으로 바꿔 규칙 3과 맞춤 |
| `Usage` 인스턴스 레이어 이름이 제목과 어긋남 | 다섯 개 모두 제목과 같게 변경 |
| 규칙 1 Do / `Don’t`의 **컴포넌트 레벨이 서로 다름** | Do를 `.primitive / Card / News` ▸ `Horizontal=False` → **`Card / News`** 로 교체. 두 컷 모두 320 × 250, 렌더링 변화 없음 |
| 규칙 1 두 인스턴스 이름 | `Frame 1171276636` · `광고 피드 (P.AD / default)` → **「리워드 금액 안내」 · 「적립 행동 유도」** (화면 라벨과 동일) |
| `Usage` 섹션 아래가 280 비어 있던 것 | 높이 1096 → **914.5** (내용 끝 814.5 + 여백 100). `Guidelines`는 1908로 이미 맞아 있었습니다 |

레벨을 바깥쪽(`Card / News`)으로 맞춘 이유는 두 가지입니다. 이 마스터의 **기본 내용이 Do 컷과 거의 같아**(같은 이미지 소재 · 같은 「20금」 배지) 교체해도 잃는 오버라이드가 없었고, Usage **A**도 같은 바깥 레벨을 쓰고 있어 페이지 전체가 한 레벨로 모입니다. 교체 후 제목에서 마스터의 「[우수 고객 전용]」 접두어만 떼어 원래 문구로 되돌렸습니다.
