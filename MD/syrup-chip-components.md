# Syrup Design System — Chip 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Chip` 페이지 → [Chip 섹션 `8760:18651`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8760-18651) |
| 섹션 구성 | `Chip` 1440×2678 → `Guidelines` 960×1696 → `Usage` 2560×436 (가로 일렬) |
| 기준일 | 2026-11-06 (Usage · Guidelines 신설 / 스펙 정리: 2026-10-01) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **사용자가 항목을 선택하거나 콘텐츠를 필터링할 수 있도록 돕는 입력형 컴포넌트에요.**
> 최소 2개 이상의 칩을 조합해 사용하는 것을 원칙으로 해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Chip / Action / Item` | `8782:22028` |
| `Chip / Filter / Item` | `9970:27294` |

2026-11-11 중복 이름을 Item·Icon·Image 역할로 구분했어요. 상위 묶음 이름과 원본 연결은 유지해요.
- `Chip / Action / Item`: 이번에 공개 이름으로 정리한 개별 에셋 `8782:22028` / 기존 상위 묶음 `8784:13432`.
- `Chip / Filter / Item`: 이번에 공개 이름으로 정리한 개별 에셋 `9970:27294` / 기존 상위 묶음 `9970:27417`.

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Chip / Action — Master Component](#1-chip--action--master-component)
3. [Chip / Filter — Master Component](#2-chip--filter--master-component)
4. [Chip / Action / Item](#3-chip--action--item)
5. [Chip / Filter / Item](#4-chip--filter--item)
6. [Chip / Filter / Icon — 아이콘](#5-chip--filter--icon--아이콘)
7. [설계 규칙 요약](#설계-규칙-요약)
8. [Usage](#usage)
9. [Guidelines](#guidelines)
10. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

보드는 **Master Component → Child Item / Chip Item → Icons** 3단 구조입니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Chip / Action`, `Chip / Filter` |
| y 1628 → 1768 | Child Item → Chip Item | `Chip / Action / Item`, `Chip / Filter / Item` |
| y 2232 | Icons | `Chip / Filter / Icon` |

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Chip / Action` | Component Set | `Kind` × `Wrap` (**8종**) | 377 × 40 / 88 |
| 2 | `Chip / Filter` | Component Set | `Type` (**2종**) | 298~300 × 32 |
| 3 | `Chip / Action / Item` | Component Set | `Selected` × `Type` (**5종**) | 72 × 40 |
| 4 | `Chip / Filter / Item` | Component Set | `Circle` × `Selected` (**4종**) | 60/32 × 32 |
| 5 | `Chip / Filter / Icon` | Component Set | `Color` (**2종**) | 12 × 12 |

**Action 계열(40px)과 Filter 계열(32px)은 완전히 독립된 두 체계**입니다. 높이·타이포·패딩·라운드 처리 방식이 모두 다릅니다.

---

## 1. Chip / Action — Master Component

**Node** `8784:13432` · Component Set · **8 variants**

칩 하나가 아니라 **칩을 가로로 나열한 행(row) 전체**가 컴포넌트입니다. 칩은 최소 2개 이상 조합해 쓰는 것이 원칙이라, 마스터 단위도 행으로 잡혀 있습니다.

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Kind` | VARIANT | `Select` | `Select` · `Action` · `Action2` · `Action3` |
| `Wrap` | VARIANT | `False` | `False` · `True` |

### Variant 매트릭스

| Kind | Wrap=False | Wrap=True | 사용하는 primitive |
| --- | --- | --- | --- |
| `Select` | ✅ | ✅ | `Secondary` 1개 + `Fill` 7개 |
| `Action` | ✅ | ✅ | `Weak` |
| `Action2` | ✅ | ✅ | `Weak2` |
| `Action3` | ✅ | ✅ | `Outline` |

4 × 2 = **8조합이 모두 존재합니다.** Bubble · Checkbox · `Chip / Filter`에 이은 **빈칸 없는 완전 매트릭스** 사례입니다. (2026-10-01 정리 완료 → [점검 1](#1--kind5--select-정리-2026-10-01-완료))

### 레이아웃

| 항목 | 값 |
| --- | --- |
| 폭 | 377 고정 |
| 높이 | `Wrap=False` 40 · `Wrap=True` 88 (40 + 8 + 40) |
| 방향 | 가로 오토레이아웃 |
| 칩 간격 | `Spacing/200` (8) |
| 패딩 | 0 |
| 넘침 처리 | `Wrap=False` → `NO_WRAP` + **클리핑** · `Wrap=True` → `WRAP` 2줄 |

- `Wrap=False`는 칩 8개(69 × 8 + 8 × 7 = 608)가 377 폭을 넘겨 **잘려 나갑니다.** 실제 구현에서 **가로 스크롤**이 되는 상태를 Figma에서 표현한 것입니다.
- `Wrap=True`는 같은 칩이 2줄로 접히며, 줄 간격도 `Spacing/200`(8)입니다.

### Kind별 선택 상태 표현

| Kind | 선택됨 | 선택 안 됨 |
| --- | --- | --- |
| `Select` | `Secondary` (검정 배경 + 흰 글자) | `Fill` (회색 배경 + 흐린 글자) |
| `Action` / `Action2` / `Action3` | — (선택 개념 없음) | `Weak` / `Weak2` / `Outline` |

**`Select` 계열만 선택 상태를 가집니다.** 행의 **첫 번째 칩 하나만** `Secondary`로 켜져 있어, 단일 선택(single select) 동작을 전제한 구성입니다. `Action` 계열은 전부 미선택 상태만 나열되어 있어 **누르면 동작이 실행되는 버튼형 칩**입니다.

---

## 2. Chip / Filter — Master Component

**Node** `9970:27417` · Component Set · **2 variants**

필터 바 전체가 하나의 컴포넌트입니다. 역시 행 단위입니다.

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Category` | `Category` · `Day` |

(2026-10-01 `Property 1` → `Type` 정리 완료 → [점검 2](#2--chip--filter-프로퍼티명-정리-2026-10-01-완료))

### Variant 구성

| Variant | 크기 | 칩 구성 | 샘플 레이블 |
| --- | --- | --- | --- |
| `Category` | 298 × 32 | `Circle=False` 5개 (첫 번째만 선택) | 추천 · 일상 · 건강 · 집안 일/육아 · 여가 |
| `Day` | 300 × 32 | `Circle=False` 1 + `Circle=True` 7 | 전체 · 월 · 화 · 수 · 목 · 금 · 토 · 일 |

### 레이아웃

| 항목 | 값 |
| --- | --- |
| 높이 | 32 |
| 방향 | 가로 오토레이아웃 |
| 칩 간격 | `Spacing/100` (4) |
| 패딩 | 0 |
| 배경 | `Color/Gray_White` |
| 넘침 처리 | `NO_WRAP`, 클리핑 **없음** |

`Day`는 **"전체"만 글자 폭에 맞춰 늘어나고 요일 7개는 32 정사각 원형**입니다. 한 글자짜리 항목을 균일한 원으로 보여주기 위해 `Circle=True`를 씁니다.

Action 계열과 달리 **칩 간격이 4로 절반**입니다. 32px 소형 칩을 촘촘하게 붙여 한 줄에 많이 담는 것이 목적입니다.

---

## 3. Chip / Action / Item

**Node** `8782:22028` · Component Set · **5 variants** · 전부 72 × 40

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Selected` | VARIANT | `True` | `True` · `False` |
| `Type` | VARIANT | `Secondary` | `Fill` · `Weak` · `Outline` · `Secondary` · `Weak2` |

### Variant별 스펙

| Selected | Type | 배경 | 테두리 | 레이블 스타일 | 레이블 색 |
| --- | --- | --- | --- | --- | --- |
| `True` | `Secondary` | `Color/Gray_Black` | — | `t1060_13_bold` | `Color/Gray_White` |
| `False` | `Weak` | `Color/Gray_900` | — | `b500_13_regular` | `Color/Gray_100` |
| `False` | `Fill` | `Color/Gray_900` | — | `b500_13_regular` | `Color/Gray_400` |
| `False` | `Weak2` | `Color/Gray_White` | — | `b500_13_regular` | `Color/Gray_100` |
| `False` | `Outline` | `Color/Gray_White` | `Color/Gray_800` 1px | `b500_13_regular` | `Color/Gray_100` |

**`Selected=True`는 `Secondary` 하나뿐이고, 나머지 4개는 `Selected=False` 전용입니다.** 두 축이 독립적이지 않습니다 → [점검 3](#3--미사용-primary-variant-삭제-2026-10-01-완료)

`Weak`와 `Fill`은 배경이 `Color/Gray_900`으로 같고 **글자 진하기만 다릅니다**(`Gray_100` vs `Gray_400`). `Fill`이 더 흐린 "꺼짐" 표현으로, `Kind=Select` 행에서 선택되지 않은 나머지 칩에 쓰입니다.

`Weak`와 `Weak2`는 **배경만 다르고(회색 vs 흰색) 글자색은 같습니다.** 흰 배경 위에 올릴지 회색 배경 위에 올릴지에 따라 골라 씁니다. `Weak2`는 테두리도 없어 흰 화면 위에서는 **글자만 떠 있는 것처럼 보입니다.**

### 레이아웃

| 항목 | 값 |
| --- | --- |
| 리사이징 | 가로 HUG · 세로 HUG |
| 최소 크기 | **minWidth 69 · minHeight 40** |
| 패딩 | 상하 `Spacing/50` (2) · 좌우 `Spacing/300` (12) |
| 간격 | `Spacing/50` (2) |
| 라운드 | `Corner radius/circle` (100) |
| 정렬 | 가로·세로 모두 중앙 |

높이 40은 **패딩이 아니라 `minHeight`로 고정**됩니다. 레이블(라인하이트 18) + 상하 패딩 2 = 22이므로, 실제로는 `minHeight 40`이 높이를 결정하고 레이블이 중앙 정렬됩니다. 폭도 `minWidth 69` 때문에 짧은 레이블에서는 69 아래로 줄지 않습니다.

### 구성 레이어

| 레이어 | 타입 | 비고 |
| --- | --- | --- |
| `레이블` | TEXT | 가로·세로 HUG |
| `Chip / Filter / Icon` | INSTANCE | 12 × 12 고정, `Icon#8784:0` BOOLEAN(기본 `true`)으로 on/off |

아이콘은 **레이블 오른쪽**에 붙으며 `Type=Goto`의 화살표 모양을 사용합니다. 눌렀을 때 다른 화면으로 이동함을 알리는 표시입니다.

---

## 4. Chip / Filter / Item

**Node** `9970:27294` · Component Set · **4 variants**

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Circle` | VARIANT | `False` | `False` · `True` |
| `Selected` | VARIANT | `False` | `False` · `True` |

### Variant별 스펙

| Circle | Selected | 크기 | 배경 | 테두리 | 레이블 스타일 | 레이블 색 |
| --- | --- | --- | --- | --- | --- | --- |
| `False` | `True` | 60 × 32 | `Color/Gray_White` | `Color/Primary_Orange` 1px | `t1050_14_bold` | `Color/Primary_Orange` |
| `False` | `False` | 60 × 32 | `Color/Gray_White` | `Color/Gray_850` 1px | `b400_14_regular` | `Color/Gray_200` |
| `True` | `True` | 32 × 32 | `Color/Gray_White` | `Color/Primary_Orange` 1px | `t1050_14_bold` | `Color/Primary_Orange` |
| `True` | `False` | 32 × 32 | `Color/Gray_White` | `Color/Gray_850` 1px | `b400_14_regular` | `Color/Gray_200` |

**2 × 2 = 4 조합이 모두 존재하는 완전 매트릭스**입니다. Chip 페이지에서는 `Chip / Action / Item`과 함께 두 개의 컴포넌트셋이 빈칸 없는 매트릭스를 이룹니다.

Action과 달리 **선택 상태를 배경이 아니라 테두리와 글자색으로** 표현합니다. 배경은 네 variant 모두 흰색으로 고정입니다. 필터 바는 콘텐츠 위에 얹히는 경우가 많아 면을 채우지 않는 쪽을 택한 것으로 보입니다.

### 레이아웃

| 항목 | 값 |
| --- | --- |
| 리사이징 | `Circle=False` → 가로 HUG / 세로 FIXED 32<br>`Circle=True` → 가로·세로 FIXED 32 |
| 최소 크기 | **minHeight 32** |
| 패딩 | 상하 `Spacing/50` (2) · 좌우 `Spacing/300` (12) |
| 간격 | `Spacing/250` (10) |
| 라운드 | `Corner radius/circle` (100) |
| 정렬 | 가로·세로 모두 중앙 |

상하 패딩 2 + 레이블 18 = 22이고, 높이 32는 **`minHeight`가 결정**합니다. 레이블은 32 안에서 중앙 정렬됩니다. (2026-10-01 상하 패딩 10 → 2 정리 → [점검 4](#4--filter의-상하-패딩-정리-2026-10-01-완료))

`Chip / Action / Item`과 **패딩 규칙이 완전히 같습니다** — 상하 `Spacing/50`(2) · 좌우 `Spacing/300`(12), 높이는 `minHeight`로 지정. 두 primitive의 차이는 `minHeight` 값(40 vs 32)뿐입니다.

### 구성 레이어

레이블 TEXT 하나뿐입니다. **Action과 달리 아이콘 슬롯이 없습니다.**

---

## 5. Chip / Filter / Icon — 아이콘

**Node** `8784:13076` · Component Set · **2 variants** · 12 × 12

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Color` | VARIANT | `White` | `White` · `Gray_400` |

내부에 `Type=Goto` 프레임(화살표 ↗)을 담고 있습니다. 크기는 12 × 12 고정입니다.

`Chip / Action / Item` 안에서 `Selected=True`(오렌지·검정 배경)에는 `White`를, 그 외에는 `Gray_400`을 씁니다.

---

## 설계 규칙 요약

| 항목 | Action 계열 | Filter 계열 |
| --- | --- | --- |
| 칩 높이 | **40** (`minHeight`) | **32** (`minHeight` + FIXED) |
| 좌우 패딩 | `Spacing/300` (12) | `Spacing/300` (12) |
| 상하 패딩 | `Spacing/50` (2) | `Spacing/50` (2) |
| 아이콘 간격 | `Spacing/50` (2) | — |
| 칩 사이 간격 | `Spacing/200` (8) | `Spacing/100` (4) |
| 라운드 | `Corner radius/circle` (100) | `Corner radius/circle` (100) |
| 레이블 (선택) | `t1060_13_bold` 13px | `t1050_14_bold` 14px |
| 레이블 (미선택) | `b500_13_regular` 13px | `b400_14_regular` 14px |
| 선택 표현 | **배경 채우기** | **테두리 + 글자색** |
| 아이콘 | ↗ 12 × 12 (on/off) | 없음 |
| 최소 개수 | 2개 이상 | 2개 이상 |

### 색상 사용

| 역할 | 토큰 |
| --- | --- |
| 강조 선택 | `Color/Primary_Orange` |
| 기본 선택 | `Color/Gray_Black` |
| 미선택 배경 | `Color/Gray_900` |
| 미선택 테두리 (Action) | `Color/Gray_800` |
| 미선택 테두리 (Filter) | `Color/Gray_850` |
| 레이블 기본 | `Color/Gray_100` |
| 레이블 흐림 | `Color/Gray_200` · `Color/Gray_400` |
| 반전 레이블 | `Color/Gray_White` |

### 타이포그래피

| 스타일 | 폰트 | 크기 | 라인하이트 | 자간 |
| --- | --- | --- | --- | --- |
| `t1060_13_bold` | Pretendard Bold | 13 | 18 | 0 |
| `b500_13_regular` | Pretendard Regular | 13 | 18 | 0 |
| `t1050_14_bold` | Pretendard Bold | 14 | 18 | −0.3 |
| `b400_14_regular` | Pretendard Regular | 14 | 18 | −0.5 |

네 스타일 모두 라인하이트 18로 통일되어 있어, 13px·14px가 섞여도 높이 계산이 어긋나지 않습니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11499:1889`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11499-1889) · 2560 × 436 |
| 구성 | 6패턴 · 폭 360 · 슬롯 높이 32~120 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-06).

**패턴을 가르는 축은 「무슨 일을 하는가」입니다.** `Chip / Action`과 `Chip / Filter`라는 두 체계가 따로 있지만, 쓰는 사람이 먼저 정하는 것은 컴포넌트가 아니라 **분류를 고를지 · 검색을 실행할지 · 값을 넣을지**입니다. 그래서 여섯 패턴이 두 체계를 가로질러 놓여 있습니다.

| | 패턴 | 설명 | 컴포넌트 | 칩 구성 |
| --- | --- | --- | --- | --- |
| **A** | 콘텐츠 분류 선택 | 브랜드나 미션 종류에 따라 콘텐츠를 나눠 볼 때 사용해요. 선택한 항목을 강조하고, 별도 페이지로 이동하는 칩에는 이동 아이콘을 표시해요. | `Chip / Action` `Kind=Select` · `Wrap=False` | `Secondary` 1 + `Fill` 3 (**마지막 1개 `Icon=true`**) |
| **B** | 추천 검색어 실행 | 검색어를 직접 입력하지 않고 추천 키워드로 검색할 때 사용해요. 키워드를 누르면 해당 검색을 실행해요. | `Chip / Action` `Kind=Action` · **`Wrap=True`** | `Weak` 6 (2줄) |
| **C** | 배경 위의 추천 검색어 | 배경색이 있는 영역에서는 흰색 칩으로 검색어를 구분해요. 주변 배경과 문구가 명확하게 구분되도록 표현을 선택해요. | `Chip / Action` `Kind=Action2` · `Wrap=True` | `Weak2` 6 (배경 `Color/Gray_950`) |
| **D** | 카테고리·조건 선택 | 목록의 카테고리나 설정 조건을 선택할 때 사용해요. Chip / Filter의 Category를 사용하고 현재 선택한 항목을 표시해요. | `Chip / Filter` `Type=Category` **2행** | `Circle=False` 9 (행마다 1개 선택) |
| **E** | 요일 선택 | 요일별 콘텐츠를 나눠 볼 때 Chip / Filter의 Day를 사용해요. 전체와 각 요일을 함께 보여주고 선택한 항목을 강조해요. | `Chip / Filter` `Type=Day` | `Circle=False` 1 + **`Circle=True` 7** |
| **F** | 빠른 값 입력 | 정해진 값을 더하거나 전체 값을 빠르게 입력할 때 사용해요. 각 칩의 문구로 입력 방식과 값을 알려줘요. | `Chip / Action` `Kind=Action3` · `Wrap=False` | `Outline` 3 |

**여섯 컷이 두 체계의 모든 variant를 한 번씩 씁니다.**

| 축 | 값 | 쓰이는 컷 |
| --- | --- | --- |
| `Chip / Action`의 `Kind` | `Select` · `Action` · `Action2` · `Action3` | A · B · C · F |
| `Chip / Filter`의 `Type` | `Category` · `Day` | D · E |
| `Chip / Action / Item`의 `Type` | `Secondary` · `Fill` · `Weak` · `Weak2` · `Outline` | A · A · B · C · F |

**A만 선택 상태를 가집니다.** 「노란깃발」 하나가 `Secondary`(검정 배경)로 켜져 있고 나머지 셋은 `Fill`입니다. B · C · F의 칩은 전부 미선택인데, **누르면 동작이 실행되고 끝나는 칩**이라 켜진 상태가 없습니다 → [Guidelines 2](#2-선택형과-실행형을-구분해요)

**A의 네 번째 칩이 아이콘을 답니다 (2026-11-06).** 「파란깃발」만 `Icon=true`라 `Chip / Filter / Icon`(12 × 12 · `Color=Gray_400`)가 붙고 폭이 69 → **83**으로 늘어납니다. 한 행 안에서 **아이콘이 있는 칩과 없는 칩이 섞이는** 모습으로, 제품의 깃발 분류 화면과 같은 구성입니다 → [Guidelines 5](#5-별도-페이지로-이동할-때는-아이콘을-표시해요)

**A의 컷은 한 줄에 담기지 않습니다.** `Chip / Action`이 383 폭인데 슬롯이 360이라 마지막 칩의 오른쪽이 잘립니다. 실제 구현에서 **가로 스크롤**이 되는 상태를 그대로 세운 것입니다 → [Guidelines 3](#3-배치-방식에-맞춰-wrap을-선택해요)

> A만 `화면` 래퍼 프레임 없이 `Chip / Action`을 슬롯에 바로 넣었습니다. 잘리는 결과는 같지만, B~F는 모두 래퍼를 거칩니다.

**D만 두 행입니다.** 「추천 · 일상 · 건강 · 집안 일/육아 · 여가」와 「매일 · 주중 · 주말 · 직접선택」을 위아래로 두어, 같은 화면에서 **성격이 다른 조건을 각각 고르는** 모습을 보여 줍니다. 행마다 선택이 하나씩 켜져 있습니다.

### 제품 실측 (2026-11-06)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체에서 칩 세트 **35건**을 전수 조사했습니다. 이 중 8건은 아이데이션 페이지의 것이라, 실제 제품 화면은 **27세트 · 개별 칩 201개**입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 세트 | `Chip / Action` | **19** |
| | `Chip / Filter` | 8 |
| 배치 | 직접 배치 | **22** |
| | 중첩 (전부 `Keypad` 안) | 5 |
| `Kind` | `Select` | 8 |
| | `Action` · `Action3` | 각 5 |
| | `Action2` | **1** |
| `Wrap` | `False` | **16** |
| | `True` | 3 |
| `Type` (Filter) | `Category` | 5 (`지금`) |
| | `Day` | 3 (`⇥ 내 할 일 관리`) |
| 세트당 칩 수 | 8개 | 11 |
| | 6개 · 3개 | 각 5 |
| | 5개 | 4 |
| | 4개 | 2 |

**개별 칩 201개의 분포입니다.**

| 체계 | 값 | 건수 |
| --- | --- | --- |
| Action (154) | `Fill` | **88** |
| | `Weak` | 29 |
| | `Secondary` | 16 |
| | `Outline` | 15 |
| | `Weak2` | **6** |
| Filter (47) | `Circle=False` | 26 |
| | `Circle=True` | 21 |
| 공통 | `Selected=True` | **24** |
| | `Icon=true` | **18** |

**칩은 거의 언제나 직접 배치됩니다.** 27세트 중 22건이 화면에 바로 놓이고, 중첩 5건은 전부 `Keypad` 안입니다. [Checkbox 96%](syrup-checkbox-components.md#7-checkbox는-거의-전부-다른-컴포넌트-안에-있습니다)·[Bubble 78%](syrup-bubble-components.md#7-bubble은-대부분-다른-컴포넌트-안에-심겨-있습니다)와 정반대입니다 — 칩은 **자기가 영역을 차지하는 요소**이기 때문입니다.

**`Wrap=True`는 3건뿐입니다.** 16건이 한 줄 + 가로 스크롤을 씁니다. 여러 줄로 펼치는 것은 추천 검색어처럼 **한눈에 다 보여야 하는 자리**에 한정됩니다.

**제품에서 쓰이는 칩 조합은 아홉 가지입니다.**

| 체계 | 조합 | 건수 |
| --- | --- | --- |
| Action | `Fill` / 미선택 / 아이콘 없음 | **70** |
| | `Weak` / 미선택 | 29 |
| | `Fill` / 미선택 / **아이콘 있음** | **18** |
| | `Secondary` / **선택** | 16 |
| | `Outline` / 미선택 | 15 |
| | `Weak2` / 미선택 | 6 |
| Filter | `Circle=True` / 미선택 | 21 |
| | `Circle=False` / 미선택 | 18 |
| | `Circle=False` / **선택** | 8 |

**선택 상태는 `Selected` 플래그가 아니라 `Type` 교체로 표현됩니다.** Action 계열에서 `Selected=True`인 칩은 **전부 `Secondary`**(16/16)이고, `Fill` + `Selected=True`는 **0건**입니다. 선택을 켜는 것이 아니라 **다른 모양의 칩으로 바꿔 끼우는** 방식입니다 → [Guidelines 2](#2-선택형과-실행형을-구분해요)

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11499:2170`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11499-2170)** (960 × 1696) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**다섯 규칙이 전부 「두 경우 비교」입니다 — Do / Don't가 한 항목도 없습니다.** 지금까지 문서화한 페이지 중 처음입니다. 칩에서 갈리는 것은 **맞고 틀림이 아니라 어느 쪽을 고르느냐**이기 때문입니다. 다섯 쌍 모두 양쪽 라벨이 `#222222`입니다.

| 규칙 | 왼쪽 | 오른쪽 | 고르는 기준 |
| --- | --- | --- | --- |
| **1** | Chip / Action · 콘텐츠 탐색 | Chip / Filter · 카테고리 선택 | 탐색·실행인가, 목록의 조건인가 |
| **2** | 분류 선택 | 검색 실행 | 선택 상태를 남기는가, 누르면 끝인가 |
| **3** | 여러 줄 · `Wrap=True` | 한 줄 · `Wrap=False` | 한눈에 다 보여야 하는가 |
| **4** | 흰 배경 · `Weak` | 컬러 배경 · `Weak2` | 뒤에 배경색이 있는가 |
| **5** | 탭 내 콘텐츠 전환 · `Icon=False` | 별도 페이지 이동 · `Icon=True` | 화면을 떠나는가 |

### 1. 용도에 맞는 Chip 컴포넌트를 사용해요

콘텐츠 탐색이나 검색·입력 실행에는 Chip / Action을 사용해요. 목록의 카테고리·조건·요일을 간결하게 선택할 때는 Chip / Filter를 사용해요.
기존 화면에서는 해당 영역에 적용된 컴포넌트를 따라요.

| 라벨 | 컴포넌트 | 높이 | 칩 간격 |
| --- | --- | --- | --- |
| **Chip / Action · 콘텐츠 탐색** | `Chip / Action` `Kind=Select` | **40** | `Spacing/200` (8) |
| **Chip / Filter · 카테고리 선택** | `Chip / Filter` `Type=Category` | **32** | `Spacing/100` (4) |

**두 체계는 섞어 쓸 수 없습니다.** 높이(40 ↔ 32)도 칩 간격(8 ↔ 4)도 타이포도 다릅니다. 한 화면에서 둘을 나란히 두면 같은 역할인데 다른 크기로 보입니다.

**설명의 마지막 문장이 현실적인 지침입니다.** 「기존 화면에서는 해당 영역에 적용된 컴포넌트를 따라요」 — 새로 고르는 자리가 아니라면 그 화면이 이미 쓰는 쪽에 맞추라는 뜻입니다.

### 2. 선택형과 실행형을 구분해요

분류나 조건을 선택하는 칩은 Selected로 현재 선택 상태를 표시해요.
검색어나 빠른 값 입력처럼 누르면 행동이 실행되는 칩과 구분해 사용해요.

| 라벨 | `Kind` | 선택 표시 | 누른 뒤 |
| --- | --- | --- | --- |
| **분류 선택** | `Select` | 「전체」가 `Secondary`(검정 배경) | 선택이 그 칩에 남음 |
| **검색 실행** | `Action` | 없음 — 전부 `Weak` | 검색이 실행되고 칩은 그대로 |

**선택을 표시하는 방법이 플래그가 아닙니다.** 제품 실측에서도 `Selected=True`인 Action 칩 16건이 **전부 `Secondary`**이고 `Fill` + 선택은 0건입니다. 켜고 끄는 것이 아니라 **다른 `Type`의 칩으로 바꿔 끼웁니다.**

### 3. 배치 방식에 맞춰 Wrap을 선택해요

여러 줄로 보여줄 때는 Wrap=True, 한 줄로 배치할 때는 Wrap=False를 사용해요.
한 줄에 담기지 않는 항목은 가로 스크롤 등으로 접근할 수 있도록 구성해요.

| 라벨 | `Wrap` | 높이 | 넘치는 칩 |
| --- | --- | --- | --- |
| **여러 줄 · Wrap=True** | `True` | **88** (40 + 8 + 40) | 둘째 줄로 접힘 |
| **한 줄 · Wrap=False** | `False` | **40** | 오른쪽으로 잘림 — 가로 스크롤 |

두 컷 모두 같은 여섯 칩(로켓배송 · 물티슈 · 신학기준비물 · 신라면 · 햇반 · 티셔츠)이고, **다른 것은 `Wrap` 하나**입니다.

**제품은 한 줄을 훨씬 많이 씁니다** — `Wrap=False` 16건 · `True` 3건. 여러 줄은 추천 검색어처럼 **스크롤 없이 전부 보여야 하는 자리**에만 씁니다.

### 4. 배경과 구분되는 표현을 선택해요

칩의 문구와 경계가 주변 배경에서 명확하게 보이도록 표현을 선택해요.
같은 역할의 칩은 선택·미선택 상태를 일관되게 적용해요.

| 라벨 | `Kind` | 칩 `Type` | 배경 |
| --- | --- | --- | --- |
| **흰 배경 · Weak** | `Action` | `Weak` | `Color/Gray_White` |
| **컬러 배경 · Weak2** | `Action2` | `Weak2` | `Color/Gray_950` (#F6F6F7) |

**`Weak`와 `Weak2`는 같은 역할의 다른 배경용입니다.** 흰 배경 위에서는 연회색 `Weak` 칩이 보이지만, 배경 자체가 회색이면 칩이 묻힙니다. 그때 흰색 `Weak2` 칩으로 바꿉니다.

**제품에서 `Weak2`는 6건뿐입니다.** 배경색이 깔린 영역 자체가 드물기 때문이고, 쓰임이 적다고 지울 축은 아닙니다 — 없으면 그 자리에서 칩이 사라집니다.

### 5. 별도 페이지로 이동할 때는 아이콘을 표시해요

현재 탭 안의 콘텐츠를 바꾸는 경우에는 이동 아이콘을 표시하지 않아요.
별도 페이지로 이동하는 칩에는 Icon=True를 적용해 이동 방식을 구분해요.

| 라벨 | `Icon` | 폭 | 누르면 |
| --- | --- | --- | --- |
| **탭 내 콘텐츠 전환 · Icon=False** | `false` | 69 | 같은 화면의 목록만 바뀜 |
| **별도 페이지 이동 · Icon=True** | **`true`** | **83** | 다른 페이지로 떠남 |

아이콘은 `Chip / Filter / Icon`(12 × 12)이고, 켜면 칩 폭이 **14 늘어납니다**(아이콘 12 + 간격 2).

**이 규칙만 칩 한 개씩으로 비교합니다.** 나머지 넷은 행 전체를 보여 주는데, 여기서는 차이가 칩 하나 안에서 끝나기 때문입니다.

**제품에서 `Icon=true`는 18건이고 전부 `Fill`입니다.** 분류 칩 중 일부만 바깥으로 나가는 구성이라, 같은 행 안에서 **아이콘 있는 칩과 없는 칩이 섞입니다.** [Usage A](#usage)가 그 행을 통째로 보여 줍니다 — 이 규칙의 「빨간깃발」·「파란깃발」이 거기서 온 라벨입니다.

---

## 점검 필요 사항

### 1. ✅ `kind5` → `Select` 정리 (2026-10-01 완료)

`Chip / Action`의 `Kind` 옵션에 **`kind5`** 라는 값이 있었습니다. 형제 값들이 `Select`·`Action`·`Action2`·`Action3`인데 혼자만 소문자에 숫자가 붙은, Figma가 자동으로 붙인 이름 형태였습니다.

자식 구성을 비교하면 **`Kind=Select, Wrap=False`와 `Kind=kind5, Wrap=True`의 내용이 완전히 동일**했습니다.

| | `Select, Wrap=False` | `kind5, Wrap=True` |
| --- | --- | --- |
| 자식 수 | 8 | 8 |
| 구성 | `Secondary` 1 + `Fill` 7 | `Secondary` 1 + `Fill` 7 |
| 크기 | 377 × 40 | 377 × 88 |
| layoutWrap | `NO_WRAP` | `WRAP` |

즉 `kind5`는 **`Select`의 두 줄 버전**이었고, 차이는 `Wrap` 유무뿐이라 이름만 잘못 붙은 상태였습니다.

`Kind=kind5`를 `Select`로 변경해 두 variant가 `Wrap` 축으로 묶였습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Kind` 옵션 | `["Select", "Action", "Action2", "Action3", "kind5"]` | **`["Select", "Action", "Action2", "Action3"]`** |
| 옵션 수 | 5 | **4** |
| 매트릭스 | 5 × 2 = 10칸 중 8개 (2칸 비어 있음) | **4 × 2 = 8, 빈칸 없음** |
| 수정된 variant | — | **1개** (`kind5, Wrap=True` → `Select, Wrap=True`) |

변경 전에는 코드에서 `Kind=Select` + `Wrap=True`를 지정하면 매칭에 실패했습니다. 이제 정상 매칭됩니다.

### 2. ✅ `Chip / Filter` 프로퍼티명 정리 (2026-10-01 완료)

`Chip / Filter` `9970:27417`의 variant 프로퍼티 이름이 Figma 기본값 `Property 1` 그대로였습니다. 값은 `Category`·`Day`로 의미가 분명한데 축 이름만 비어 있는 상태였습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 프로퍼티명 | `Property 1` | **`Type`** |
| 옵션 | `Category` · `Day` | 변경 없음 |
| variant 이름 | `Property 1=Category` / `=Day` | **`Type=Category` / `=Day`** |

`Chip / Action / Item`·`Chip / Filter / Item`가 이미 `Type`·`Selected`를 쓰고 있어, **Chip 페이지 전체의 축 이름이 통일**됐습니다.

같은 날 Button 페이지의 `Button / News`·`Button / Quiz`도 함께 정리되어, **Chip·Button 두 페이지에는 기본 생성 이름이 0건** 남았습니다. 파일 전체로는 **61개 컴포넌트셋**에 `Property 1`이 남아 있습니다 → [syrup-button-components.md 점검 2](syrup-button-components.md#2--기본-생성-이름-property-1--variant2-정리-2026-10-01-완료)

### 3. ✅ 미사용 `Primary` variant 삭제 (2026-10-01 완료)

`Chip / Action / Item`은 `Selected` 2 × `Type` 6 = 12 조합 중 **6개만 존재**했고, 빈칸이 대각선으로 갈려 있었습니다.

| | Primary | Secondary | Weak | Fill | Weak2 | Outline |
| --- | --- | --- | --- | --- | --- | --- |
| `Selected=True` | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| `Selected=False` | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ |

`Type`을 고르는 순간 `Selected`가 자동으로 결정되는 구조라, `Selected`가 새로운 정보를 담지 못했습니다. `Selected=True, Type=Outline` 같은 조합을 코드에서 지정하면 매칭에 실패하는 상태였습니다.

#### 사용 현황 조사

파일 전체(15개 페이지, 인스턴스 **1,832개**)를 수동 재귀로 훑어 마스터 컴포넌트 ID를 대조했습니다.

| Type | 사용 횟수 |
| --- | --- |
| `Weak2` | 16 |
| `Weak` | 14 |
| `Fill` | 14 |
| `Outline` | 14 |
| `Secondary` | 2 |
| **`Primary`** | **0** |

선택/미선택 쌍으로 실제 작동하는 조합은 **`Secondary` ↔ `Fill` 하나뿐**이었습니다. `Weak`·`Weak2`·`Outline`은 선택 개념이 없는 `Kind=Action` 계열 전용이고, `Primary`는 짝도 없고 사용처도 없었습니다.

> **측정 범위 주의** — 위 수치는 **이 Figma 파일 안에서의 배치 횟수**입니다. 라이브러리를 가져다 쓰는 다른 파일, 디태치된 인스턴스, 개발 코드에서의 사용은 포함되지 않습니다. 실제 제품 화면에 사용처가 없다는 점은 디자이너가 별도로 확인했습니다.

#### 조치

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| variant 수 | 6 | **5** |
| `Type` 옵션 | `Primary` · `Fill` · `Weak` · `Outline` · `Secondary` · `Weak2` | **`Fill` · `Weak` · `Outline` · `Secondary` · `Weak2`** |
| `Type` 기본값 | `Primary` | **`Secondary`** (Figma가 자동 이동) |
| 끊긴 인스턴스 | — | **0건** (1,832개 전수 검사) |

**추후 오렌지 선택 칩이 필요해지면 다시 만드는 것으로 합의**했습니다. 그때는 짝이 될 미선택 모습까지 함께 정의하면 됩니다.

#### 남은 사항

`Primary`가 빠지면서 `Selected=True`는 `Secondary` 하나만 남았습니다. **두 축이 종속적인 구조 자체는 그대로**입니다.

| | Secondary | Weak | Fill | Weak2 | Outline |
| --- | --- | --- | --- | --- | --- |
| `Selected=True` | ✅ | ❌ | ❌ | ❌ | ❌ |
| `Selected=False` | ❌ | ✅ | ✅ | ✅ | ✅ |

`Selected` 축을 없애고 `Type` 5개만 남기면 정보 손실 없이 더 단순해지지만, 코드에서 `selected` 플래그를 쓰는 편이 자연스러울 수 있어 **현행 유지**합니다. 선택 전환은 `Type`을 `Secondary` ↔ `Fill`로 바꿔 처리합니다.

### 4. ✅ Filter의 상하 패딩 정리 (2026-10-01 완료)

`Chip / Filter / Item` 네 variant 모두 상하 패딩이 `Spacing/250`(10)인데 **세로 리사이징이 FIXED 32**였습니다.

| 계산 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 상 패딩 + 레이블 18 + 하 패딩 | 10 + 18 + 10 = **38** | 2 + 18 + 2 = **22** |
| 실제 높이 | 32 | 32 |
| 관계 | **38 > 32 — 패딩이 높이와 모순** | **22 ≤ 32 — 모순 없음** |

변경 전에는 선언된 패딩이 실제 높이보다 6px 커서, 스펙을 보고 구현하면 38을 기대하게 되는 상태였습니다.

| 항목 | 변경 전 | 변경 후 |
| --- | --- | --- |
| 상하 패딩 | `Spacing/250` (10) | **`Spacing/50` (2)** |
| `minHeight` | 없음 | **32** |
| 좌우 패딩 · 간격 | `Spacing/300` (12) · `Spacing/250` (10) | 변경 없음 |
| 수정된 variant | — | **4개 전부** |

`minHeight`가 높이를 결정하고 상하 패딩은 최소 여백 역할만 하는 구조가 되어, **`Chip / Action / Item`과 규칙이 완전히 같아졌습니다.** 두 primitive의 차이는 이제 `minHeight` 값(40 vs 32)뿐입니다.

렌더링은 스크린샷으로 확인했고, 칩 크기(60×32 · 32×32)와 상위 `Chip / Filter` 두 variant(298×32 · 300×32) 모두 변화가 없습니다.

### 5. ✅ Filter 라운드 리터럴 `60` → 토큰 교체 (2026-10-01 완료)

`Chip / Filter / Item` 및 상위 인스턴스까지 **라운드 `60`이 토큰 없이 직접 입력**되어 있었습니다. 페이지 전체에서 **17건**이었습니다.

| 컴포넌트 | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Chip / Action / Item` | `Corner radius/circle` (100) | 변경 없음 |
| `Chip / Filter / Item` | **60 (리터럴)** | **`Corner radius/circle` (100)** |

높이가 32라 60이든 100이든 **렌더링 결과는 동일한 완전 원형**이어서, 교체에 따른 시각적 변화는 없습니다.

| 항목 | 값 |
| --- | --- |
| 직접 바인딩 | 마스터 COMPONENT **4개** × 4모서리 = 16건 |
| 자동 상속 | `Chip / Filter` 내부 인스턴스 **13개** (오버라이드 없어 전부 따라옴) |
| 합계 | **17건** |
| 잔여 미바인딩 radius | **0건** |

마스터 variant만 바인딩하면 인스턴스가 바인딩 자체를 상속하므로, 인스턴스를 개별로 건드릴 필요가 없었습니다. 파일 전체에서 라운드 `60`은 이 17건이 전부였습니다.

### 6. ℹ️ `Chip / Action` 샘플 칩 개수 차이 — **의도된 구성**

행 안에 들어 있는 칩 개수가 일정하지 않습니다.

| Variant | 칩 개수 | 칩 폭 |
| --- | --- | --- |
| `Action, Wrap=False` | **6** | 69 |
| `Action3, Wrap=False` | **3** | **120** |
| 나머지 6종 | 8 | 69 |

`Action3, Wrap=False`만 120px짜리 칩 3개로 채워져 있어, 같은 `Action3`인데 `Wrap=True`(69px 8개)와 내용이 다릅니다.

**의도된 구성이며 통일 대상이 아닙니다.** 마스터에 담긴 샘플 콘텐츠로, 실제 사용 시 교체됩니다. 칩 폭이 길어지는 경우와 많아지는 경우를 각각 보여주려는 배치입니다.

### 7. 토큰 상태 — 양호

| 항목 | 결과 |
| --- | --- |
| 미바인딩 fill | **0건** |
| 미바인딩 stroke | `#9747FF` 5건 — Figma 컴포넌트셋 기본 점선 테두리 (컴포넌트셋 5개), 디자인 값 아님 |
| 미바인딩 radius | **0건** (2026-10-01 17건 교체 완료 → [점검 5](#5--filter-라운드-리터럴-60--토큰-교체-2026-10-01-완료)) |
| 미바인딩 padding | `100` 6건 — 문서 보드 레이아웃 프레임 |
| 미바인딩 gap | **0건** |
| 원격 텍스트 스타일 | **0건** |
| 스타일 미적용 텍스트 | **0건** |
| 제어문자 | **0건** |
| 폰트 | Pretendard Bold 8 · Pretendard Regular 39 — **전부 Pretendard** |
| 외부 토큰 | `Spec docs` 7 — 문서 레이아웃 전용 |

**색상·간격·라운드·타이포가 모두 Syrup 토큰과 로컬 스타일에 바인딩**되어 있습니다. 남은 미바인딩 항목은 Figma가 컴포넌트셋에 자동으로 그리는 점선 테두리와 문서 보드 레이아웃 프레임뿐으로, 둘 다 디자인 값이 아닙니다.

스타일 미적용 텍스트가 0건인 것은 지금까지 문서화한 컴포넌트 중 처음입니다 — 보드 축 라벨까지 전부 인스턴스로 만들어져 있기 때문입니다.

**새로 만든 Usage · Guidelines 두 섹션도 같습니다** — 스타일 없는 텍스트 **0건**, 미바인딩 fill **0건**, 인스턴스 11개의 레이어 이름이 모두 제목과 일치합니다. 제품 블록을 복제해 넣은 컷이 없어 정리되지 않은 값이 섞이지 않았습니다.

### 8. 제품의 `Chip / Filter`가 아직 옛 프로퍼티명을 씁니다

[점검 2](#2--chip--filter-프로퍼티명-정리-2026-10-01-완료)에서 `Property 1` → `Type`으로 바꾼 것이 **제품 파일에 반영되지 않았습니다.**

| 파일 | 프로퍼티명 | 건수 |
| --- | --- | --- |
| 디자인 시스템 | **`Type`** | — |
| 제품 (`지금` · `⇥ 내 할 일 관리`) | **`Property 1`** | **8 / 8** |

값(`Category` · `Day`)은 그대로라 화면은 멀쩡하지만, 제품 쪽 인스턴스가 **옛 컴포넌트를 가리키고 있습니다.** 라이브러리 업데이트를 받으면 해소될 건으로 보이나, 받은 뒤에도 남는다면 인스턴스를 다시 연결해야 합니다.

`Chip / Action` 19건은 `Kind` · `Wrap`으로 **현재 이름을 쓰고 있어** 이 건은 Filter에만 해당합니다.

### 9. ✅ Usage A의 설명과 컷이 맞춰짐 (2026-11-06)

A의 설명은 「별도 페이지로 이동하는 칩에는 이동 아이콘을 표시해요」로 끝나는데 **네 칩이 모두 `Icon=false`** 였습니다. 2026-11-06에 **칩 내용을 바꿔 해결**했습니다.

| | 전 | 후 |
| --- | --- | --- |
| 라벨 | 전체 · 버거킹 · 롯데리아 · 엔제리너스 | **노란깃발 · 주황깃발 · 빨간깃발 · 파란깃발** |
| 아이콘 | 없음 | **「파란깃발」만 `Icon=true`** (폭 69 → 83) |
| 선택 | 「전체」 `Secondary` | 「노란깃발」 `Secondary` |

이제 A 한 컷에서 **선택 강조와 이동 아이콘이 함께** 보이고, [Guidelines 5](#5-별도-페이지로-이동할-때는-아이콘을-표시해요)의 「빨간깃발」·「파란깃발」과도 같은 화면에서 온 라벨이 됩니다.

### 10. Select 행의 라벨이 컷마다 다릅니다

같은 `Kind=Select` 행인데 **Usage A와 Guidelines 1 · 2의 라벨이 갈립니다.**

| 컷 | 라벨 | 아이콘 |
| --- | --- | --- |
| [Usage A](#usage) | 노란깃발 · 주황깃발 · 빨간깃발 · 파란깃발 | 마지막 칩에 있음 |
| [Guidelines 1](#1-용도에-맞는-chip-컴포넌트를-사용해요) | 전체 · 버거킹 · 롯데리아 · 엔제리너스 | 없음 |
| [Guidelines 2](#2-선택형과-실행형을-구분해요) | 전체 · 버거킹 · 롯데리아 · 엔제리너스 | 없음 |
| [Guidelines 5](#5-별도-페이지로-이동할-때는-아이콘을-표시해요) | 빨간깃발 · 파란깃발 | 오른쪽 칩에 있음 |

A를 깃발로 바꾸면서 Guidelines 1 · 2만 브랜드 라벨로 남았습니다. **읽는 데 문제가 되지는 않지만**, 한 페이지 안에서 같은 행이 두 가지 내용으로 나오면 다른 컴포넌트처럼 보일 수 있습니다.

Guidelines 1 · 2도 깃발로 맞추면 페이지 전체가 한 화면에서 온 예제가 됩니다. 다만 1은 「Action ↔ Filter」를, 2는 「선택형 ↔ 실행형」을 비교하는 항목이라 **라벨이 달라도 규칙은 그대로 성립**합니다 — 맞출지는 선택입니다.
