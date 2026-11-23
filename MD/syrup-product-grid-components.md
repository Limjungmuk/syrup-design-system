# Syrup Design System — Product Grid 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Product Grid` 페이지 → [Product Grid 섹션 `9354:17937`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9354-17937) |
| 섹션 크기 | 1440 × 5004 |
| 컴포넌트 수 | **8개** (전부 Component Set) |
| 기준일 | 2026-11-09 (가이드라인·Usage 및 주요 규격 갱신) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **상품 정보를 다양한 그리드 레이아웃으로 구성해 보여주는 컴포넌트예요.**
> 상품 이미지, 가격, 혜택, 상태 등 필요한 정보를 조합하여 상품 목록을 구성할 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Product Grid / List Item` | `9024:8810` |
| `Product Grid / Naver / Item` | `9002:10142` |
| `Product Grid / Stamp / Item` | `9110:26923` |
| `Product Grid / Icon / Stamp` | `9110:26607` |

2026-11-11 중복 이름을 Item·Icon·Image 역할로 구분했어요. 상위 묶음 이름과 원본 연결은 유지해요.
- `Product Grid / Naver / Item`: 이번에 공개 이름으로 정리한 개별 에셋 `9002:10142` / 기존 상위 묶음 `9110:27033`.
- `Product Grid / Stamp / Item`: 이번에 공개 이름으로 정리한 개별 에셋 `9110:26923` / 기존 상위 묶음 `9110:27055`.

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Master Component 3종](#1-master-component-3종)
3. [Child Item — List Item](#2-child-item--list-item)
4. [Icon](#3-icon)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [AI 도구에서 사용할 때](#ai-도구에서-사용할-때)
8. [설계 규칙 요약](#설계-규칙-요약)
9. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440 × 5004예요. 별도 섹션에 가이드라인 4개와 Usage 6개를 구성했어요. 기존 노드·인스턴스 수는 2026-10-12 점검 기록이며, 새 예제까지 포함한 최신 집계가 아니에요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | 그리드 **3종** |
| y 3329 | Child Item → List Item | 상품 카드 **3종** |
| y 4384 | Icon | 아이콘 **2종** |
| 별도 섹션 | [Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-3837) | 가이드라인 **4개** |
| 별도 섹션 | [Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-3838) | 사용 예제 **6개** |

인스턴스 열은 기존 점검 당시의 수치예요. 0건 표기를 현재 사용되지 않는 컴포넌트라는 뜻으로 해석하지 않아요.

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스(기존 집계) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Product Grid` | Set | `Variant` 3종 | 312~360 × 396~526 | **0** |
| 2 | `Product Grid / Naver` | Set | `Variant` 2종 | 360 × 217 / 264 | **0** |
| 3 | `Product Grid / Stamp` | Set | `Last` 2종 + `Bubble` · `Or` | 296 × 140 | **5** (`Card`) |
| 4 | `Product Grid / List Item` | Set | `Variant` 4종 + BOOLEAN **8개** | 104~158 × 172~233 | 14 |
| 5 | `Product Grid / Naver / Item` | Set | `Variant` 2종 + `Partner` | 96~148 × 163 / 216 | 5 |
| 6 | `Product Grid / Stamp / Item` | Set | `Variant` 3종 | 148 × 140 | 14 |
| 7 | `.primitive / Product Grid / Icon / Like` | Set | `State` 2종 | 50 × 50 | 1 |
| 8 | `Product Grid / Icon / Stamp` | Set | `Type` 7종 | 60 × 60 | **19** |

(2026-10-12 마스터 3종 이름을 `Grid List /` → `Product Grid /` 로 정리 → [점검 1](#1--마스터-3종-이름-정리-2026-10-12-완료))

---

## 1. Master Component 3종

### Product Grid

**Node** `9098:24020` · Component Set · **3 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Shopping` | `Personality Test` · `Recommend` · `Shopping` |

| Variant | 마스터 크기 | 좌우 패딩 | 열 간격 | 행 간격 | 줄바꿈 |
| --- | --- | --- | --- | --- | --- |
| `Shopping` | 360 × 526 | `Spacing/400` (16) | 12 | 24 | **WRAP** |
| `Personality Test` | 328 × 396 | 0 | 8 | 16 | **WRAP** |
| `Recommend` | 312 × 454 | 0 | 16 | 20 | **WRAP** |

세 Variant 모두 가로 줄바꿈 그리드예요. 상품 아이템의 구성과 크기, 열·행 간격이 달라요. 높이는 표시 정보와 상품 수에 따라 달라질 수 있어요.

**그리드의 `Variant=Shopping`과 내부 아이템의 `Variant=Shopping`은 별도 속성이에요.** 현재 Shopping 마스터에는 Live 아이템이 들어 있어요. 일반 상품을 구성할 때는 내부 아이템을 Shopping으로 선택하고, 라이브 상품은 Live로 사용해요.

안쪽은 `Product Grid / List Item` 인스턴스를 4~6개 담습니다.

### Product Grid / Naver

**Node** `9110:27033` · Component Set · **2 variants** · 360 폭

| Variant | 크기 | 하단 패딩 | Gap | 구성 |
| --- | --- | --- | --- | --- |
| `3column` | 360 × 217 | `Spacing/900` (36) | `Spacing/300` (12) | `.primitive / … / Naver` **3개** |
| `2column` | 360 × 264 | `Spacing/750` (30) | `Spacing/400` (16) | `.primitive / … / Naver` **2개** |

네이버쇼핑 제휴 영역입니다. 좌우 패딩은 둘 다 `Spacing/600`(24)입니다.

2026-11-09 확인 기준, `2column`의 표시 아이템 2개는 자체 primitive `9002:10171`을 사용해요. 과거 외부 의존 기록은 아래 점검 항목과 구분해요.

### Product Grid / Stamp

**Node** `9110:27055` · Component Set · **2 variants** · 296 × 140

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Last` | VARIANT | `False` | `False` · `True` |
| `Bubble` · `Or` | BOOLEAN | `true` | — |

| 항목 | 값 |
| --- | --- |
| 구성 | `.primitive / … / Stamp` 2개 + `Bubble` + `or` 프레임 |
| 행 구분 | 중간 행은 `Last=False`, 마지막 행은 `Last=True` |
| Padding · Gap | 0 |

커피·간식 상품을 한 행에 2개씩 보여줘요. 두 상품 중 하나를 제공할 때는 `Or=True`, 여러 상품 중 랜덤으로 제공할 때는 `Or=False`로 사용해요. `Bubble`은 추가 안내가 필요할 때만 표시해요.

`Card / Stamp` 안에서도 사용해요. 새 Usage에서는 상품 묶음만 남겨 제공 방식을 설명해요.

---

## 2. Child Item — List Item

### Product Grid / List Item

**Node** `9024:8810` · Component Set · **4 variants**

**이 파일에서 BOOLEAN 프로퍼티가 가장 많은 컴포넌트**입니다(8개).

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Live` | `Shopping` · `Live` · `Recommend` · `Personality Test` |
| `Partner` · `Discount` · `Like` · `Live` · `Time` · `Price` · `Badge` | BOOLEAN | `true` | — |
| `Image` | BOOLEAN | `false` | — |

| Variant | 크기 | 텍스트 스타일 |
| --- | --- | --- |
| `Live` | 158 × 233 | `t1060_13_bold` |
| `Shopping` | 158 × 230 | **스타일 없음** (11 Bold) |
| `Recommend` | 148 × 199 | `b400_14_regular` |
| `Personality Test` | 104 × 172 | `b500_13_regular` |

공통 — Padding 0, Gap `Spacing/250`(10), 세로 오토레이아웃, 구성 `Image` + `Content`

**크기가 104 ~ 158로 제각각**입니다. 마스터의 그리드 폭에 맞춘 값입니다.

### Product Grid / Naver / Item

**Node** `9002:10142` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `3column` | `3column` · `2column` |
| `Partner` | BOOLEAN | `true` | — |

| Variant | 크기 | Gap |
| --- | --- | --- |
| `3column` | 96 × 163 | `Spacing/200` (8) |
| `2column` | 148 × 216 | `Spacing/200` (8) |

(2026-10-12 `Phatner` → `Partner` 오타 수정 → [점검 2](#2--phatner--partner-오타-수정-2026-10-12-완료))

### Product Grid / Stamp / Item

**Node** `9110:26923` · Component Set · **3 variants** · 148 × 140

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Left` | `Left` · `Center` · `Right` |

| Variant | Padding (T/R/B/L) | 테두리 |
| --- | --- | --- |
| `Left` | `400` / `200` / `400` / **0** | `Gray_850` **우측 1px** |
| `Center` | `400` / `200` / `400` / `200` | `Gray_850` **우측 1px** |
| `Right` | `400` / **0** / `400` / `200` | `Gray_850` **우측 1px** |

**격자에서의 위치에 따라 바깥쪽 패딩을 0으로** 만듭니다. 세 칸을 나란히 놓으면 양 끝이 여백 없이 맞춰집니다.

`Card` 10건 · `Product Grid` 4건으로 **총 14건** 쓰입니다.

---

## 3. Icon

### .primitive / Product Grid / Icon / Like

**Node** `9093:39794` · Component Set · **2 variants** · 50 × 50

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `State` | VARIANT | `Off` | `Off` · `On` |

찜하기(하트) 버튼입니다. Padding `Spacing/250`(10) 사방.

(2026-10-12 내부 레이어명 `syrup_img_방송예정` → `Like` 정리 → [점검 5](#5--레이어명-잔재-정리-2026-10-12-완료))

### Product Grid / Icon / Stamp

**Node** `9110:26607` · Component Set · **7 variants** · 60 × 60

| Property | Type | Options |
| --- | --- | --- |
| `Type` | VARIANT | `배스킨라빈스` · `메가커피` · `스타벅스` · `파리바게트` · `교촌치킨` · `뚜레쥬르` · `KFC` |

제휴 브랜드 로고입니다. **이 페이지에서 가장 많이 쓰입니다**(19건 — `Card` 10 · `Product Grid` 7 · `Product List` 2).

---

## 가이드라인

### 1. 콘텐츠에 맞는 상품 아이템을 사용해요

일반 쇼핑 상품은 Shopping, 라이브 상품은 Live 아이템을 사용해요. 추천 상품과 네이버 제휴 상품, 스탬프 상품은 각각의 전용 구성을 사용해요.

- 일반·라이브 상품: `Product Grid` 안의 `Product Grid / List Item`을 콘텐츠에 맞게 선택해요.
- 추천 상품: `Product Grid`의 `Variant=Recommend`를 사용해요.
- 네이버 제휴 상품: `Product Grid / Naver`를 사용해요.
- 스탬프 상품: `Product Grid / Stamp`를 사용해요.

[Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-3839)

### 2. 바깥 여백을 중복해서 넣지 않아요

화면 전체 폭에 배치할 때는 그리드의 좌우 여백을 사용해요. 부모 영역에 이미 여백이 있으면 그리드의 여백을 빼요. 같은 목록에서는 상품 폭과 열·행 간격을 일정하게 유지해요.

| Shopping 배치 예 | 부모 좌우 여백 | 그리드 폭 | 그리드 좌우 여백 | 상품 폭 / 열 간격 |
| --- | --- | --- | --- | --- |
| 화면 전체 폭 360 | 0 | 360 | 16 | 158 / 12 |
| 부모가 여백을 제공 | 16 | 328 | 0 | 158 / 12 |

두 경우 모두 상품 영역의 전체 폭은 328이에요. 16 여백과 12 간격은 이 Shopping 예제의 기준이며, Recommend·Naver의 서로 다른 규격까지 같은 값으로 바꾸지 않아요.

[Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4037)

### 3. 상품에 필요한 정보만 표시해요

할인율·제휴처·찜하기는 해당 정보나 기능이 있을 때 표시해요. 리워드가 있는 상품에 배지를 사용하고, 라이브 표시와 시간은 방송 상태에 맞춰 구성해요.

- 아이템의 `Discount`·`Partner`·`Like`·`Badge`·`Live`·`Time` 등 필요한 속성만 켜요. 기본값이 true라는 이유로 모든 상품에 정보를 추가하지 않아요.
- 배지는 리워드 유무와 상태에 맞게 사용해요. 방송 예정·받기 완료 등의 상태 표현은 [Badge 문서](syrup-badge-components.md)를 함께 확인해요.

[Figma 가이드라인 3](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4266)

### 4. 스탬프 상품은 제공 방식에 맞게 구성해요

두 상품 중 하나를 제공하는 구성에서는 or를 표시해요. 여러 상품 중 랜덤으로 제공할 때는 or를 숨기고 조건을 안내해요. 여러 행을 쌓을 때는 중간 행과 마지막 행을 구분하고, 추가 안내가 필요할 때만 Bubble을 표시해요.

| 구성 | `Or` | `Last` | `Bubble` |
| --- | --- | --- | --- |
| 한 행의 두 상품 중 하나 제공 | `True` | `True` | 추가 안내가 없으면 `False` |
| 여러 행 중 중간 행 | `False` | `False` | 예제에서는 `False` |
| 여러 행 중 마지막 행 | `False` | `True` | 랜덤 제공 조건을 안내하는 예제에서는 `True` |

`Or`·`Bubble`은 BOOLEAN, `Last`는 `False`·`True`를 값으로 갖는 VARIANT예요. `Last`를 상품 만료나 수령 완료 상태로 해석하지 않아요.

[Figma 가이드라인 4](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4495)

---

## Usage — 사용 예제

[Usage 섹션](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-3838)에 상품 구성만 남긴 예제 6개를 정리했어요.

| 예제 | 사용 구성 | 설명 |
| --- | --- | --- |
| [A. 쇼핑 상품](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4603) | Shopping 그리드 + Shopping 아이템 | 상품명과 가격을 중심으로 상품을 비교해요. 할인율·제휴처·찜하기·리워드 배지는 필요한 항목만 표시해요. |
| [B. 라이브 상품](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4718) | Shopping 그리드 + Live 아이템 | Live 아이템으로 방송 상품을 구성해요. 방송 상태에 맞는 배지와 LIVE 표시, 시간을 함께 사용해요. |
| [C. 추천 상품](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4802) | `Product Grid / Variant=Recommend` | 추천 상품을 간결하게 보여줄 때 Recommend 구성을 사용해요. 상품 이미지와 상품명, 가격을 함께 표시해요. |
| [D. 네이버 제휴 상품](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4845) | `Product Grid / Naver / Variant=2column` | 네이버 제휴 상품은 Product Grid / Naver를 사용해요. 예제는 2column 구성으로, 제휴처는 필요한 경우에 표시해요. |
| [E. 스탬프 상품 두 개](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4882) | `Product Grid / Stamp`, `Or=True` | 두 상품 중 하나를 제공하는 경우 Or=True로 표시해요. 필요한 동작 버튼은 상품 묶음 아래에 별도로 배치해요. |
| [F. 스탬프 상품 여러 개](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11636-4916) | Stamp 3행, `Or=False` | 여러 상품 중 랜덤으로 제공하는 경우 Or=False로 구성해요. 중간 행은 Last=False, 마지막 행은 Last=True로 구분하고 Bubble로 조건을 안내해요. |

`Personality Test`와 Naver의 `3column`은 마스터에 있는 별도 구성이고, 이번 Usage에는 포함하지 않았어요. 예제에 없다는 이유로 삭제하거나 다른 Variant로 대체하지 않아요. 예제의 상품명·금액·상품 수는 소재이며 모든 사용처의 고정값이 아니에요.

## AI 도구에서 사용할 때

1. 그리드와 내부 상품 아이템의 Variant를 각각 확인해요. `Product Grid`에 `Live` Variant를 새로 만들지 않고, 기존 Shopping 그리드 안에서 Live 아이템을 사용해요.
2. 그리드와 부모 중 어느 쪽이 바깥 여백을 제공하는지 먼저 확인해요. 중복 패딩으로 상품 폭이 줄거나 열 수가 달라지지 않도록 해요.
3. 상품 정보의 유무에 맞춰 속성을 설정해요. 숨겨진 할인율·리워드·시간을 임의의 값으로 채우지 않아요.
4. 높이는 상품명 줄 수, 표시 정보와 행 수에 맞춰 구성해요. 마스터의 샘플 높이를 모든 목록의 고정 높이로 적용하지 않아요.
5. 스탬프의 `Last`는 행 위치, `Or`는 제공 관계, `Bubble`은 추가 안내 여부를 뜻해요. 브랜드 이미지와 상품 문구가 서로 맞는지 확인해요.
6. 전체 서비스 화면 대신 상품 묶음과 설명에 필요한 보조 요소만 사용해요. 원본 인스턴스 연결을 유지해요.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 그리드 폭 | 312 · 328 · 360 |
| 상품 카드 폭 | 96 · 104 · 148 · 158 (그리드에 맞춤) |
| 카드 간격 | `Spacing/200`(8) · `Spacing/300`(12) · `Spacing/400`(16) |
| 이미지–내용 간격 | `Spacing/250` (10) |
| 좌우 패딩 | `Spacing/400`(16) · `Spacing/600`(24) |
| 구분선 | `Color/Gray_850` 1px (Stamp 계열) |
| 배치 | Product Grid·Naver는 가로 WRAP, Stamp는 2개씩 한 행을 구성 |
| Shopping 열 / 행 간격 | 12 / 24 |
| Recommend 열 / 행 간격 | 16 / 20 |

### 텍스트 스타일

| 스타일 | 용도 |
| --- | --- |
| `b400_14_regular` | 상품명 · 제휴처 |
| `b500_13_regular` | 작은 상품명 |
| `t1060_13_bold` | 금액 강조 (Live) |

---

## 점검 필요 사항

> 아래는 2026-10-12의 점검 기록이에요. 이번에는 공통 사용 기준·가이드라인·Usage와 주요 속성을 갱신했으며, 파일 전체의 인스턴스·토큰·스타일 건수는 재집계하지 않았어요. 과거 통계는 최신 사용 규칙과 구분해요.

### 1. ✅ 마스터 3종 이름 정리 (2026-10-12 완료)

**페이지명과 컴포넌트 이름이 어긋나 있었습니다.** primitive 5종은 `Product Grid /`를 쓰는데 마스터 3종만 `Grid List /`로 시작했습니다.

| Node | 변경 전 | 변경 후 | 인스턴스 |
| --- | --- | --- | --- |
| `9098:24020` | `Grid List / Product Grid` | **`Product Grid`** | 0 |
| `9110:27033` | `Grid List / Product Grid / Naver` | **`Product Grid / Naver`** | 0 |
| `9110:27055` | `Grid List / Product Grid / Stamp` | **`Product Grid / Stamp`** | **5** (`Card`) |

[Grid List](syrup-grid-list-components.md)는 **별도 페이지**이고 성격도 다릅니다.

| | Grid List | **Product Grid** |
| --- | --- | --- |
| 내용 | 메뉴 아이콘 격자 | **상품 카드 격자** |
| 아이템 | 아이콘 + 라벨 | 이미지 + 상품명 + 가격 + 배지 |

Figma 에셋 패널에서 **`Grid List` 폴더 아래에 묶여** 보여 찾기 어려웠는데, 이제 페이지·primitive와 같은 `Product Grid` 폴더로 모입니다.

이름 충돌이 없음을 사전 확인했고, 인스턴스 5건은 Figma가 자동 반영했습니다.

### 2. ✅ `Phatner` → `Partner` 오타 수정 (2026-10-12 완료)

`Product Grid / Naver / Item` `9002:10142`의 BOOLEAN 프로퍼티명에 오타가 있었습니다.

| 변경 전 | 변경 후 |
| --- | --- |
| **`Phatner`** | **`Partner`** |

같은 페이지의 `Product Grid / List Item`이 이미 `Partner`를 쓰고 있어, **같은 역할 프로퍼티가 두 이름으로 갈려 있던 상태**가 해소되었습니다.

> [Button](syrup-button-components.md)의 `Coner`, [List Footer](syrup-list-footer-components.md)의 `Viariant`, [List Row](syrup-list-row-components.md)의 `Cancle`에 이은 네 번째 오타 수정입니다.

### 3. `2column`이 외부 컴포넌트를 섞어 씀 — 과거 기록

2026-10-12에는 외부 `List_네이버쇼핑` 4개와 자체 primitive 2개를 함께 사용하는 것으로 기록했어요. 2026-11-09 재확인한 `2column` 마스터의 표시 아이템은 자체 `Product Grid / Naver / Item` 2개(`9002:10171`)예요. 과거 기록을 현재 구성이나 필수 외부 의존으로 해석하지 않아요.

### 4. ✅ `Property 1` 2건 정리 (2026-10-12 완료)

| 컴포넌트 | 변경 전 | 변경 후 | 값 |
| --- | --- | --- | --- |
| `.primitive / Product Grid / Icon / Like` `9093:39794` | `Property 1` | **`State`** | `Off` · `On` |
| `Product Grid / Icon / Stamp` `9110:26607` | `Property 1` | **`Type`** | 브랜드 6종 |

variant 이름도 함께 바뀌었습니다(`Property 1=배스킨라빈스` → **`Type=배스킨라빈스`**). 인스턴스 20건은 Figma가 자동 반영했습니다.

**`Product Grid` 페이지의 `Property 1`은 0건**이 되었습니다. 파일 전체로는 **44개** 컴포넌트셋에 남아 있습니다(46 → 44).

> `Like`는 값이 `Off`/`On` 둘뿐이라 **BOOLEAN 프로퍼티로 바꾸는 것**도 방법이지만, 구조 변경이라 이번에는 이름만 정리했습니다.

### 5. ✅ 레이어명 잔재 정리 (2026-10-12 완료)

`.primitive / Product Grid / Icon / Like`의 바깥 프레임 이름이 **찜하기 아이콘과 무관**했습니다.

| 레이어 | 크기 | 변경 전 | 변경 후 |
| --- | --- | --- | --- |
| 바깥 프레임 | 30 × 30 | **`syrup_img_방송예정`** | **`Like`** |
| 아이콘 | 24 × 24 | `🟧syrup_img_shopping_like` | 변화 없음 |
| 벡터 | 16 × 15 | `Vector` | 변화 없음 |

**`방송예정`**(방송 예정)은 다른 에셋을 복제해 만들면서 이름을 바꾸지 않은 흔적이었습니다. 두 variant(`State=Off` · `State=On`) 모두 정리했습니다.

### 6. 타 페이지·외부 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| [Badge](syrup-badge-components.md) | `Badge` · `Badge / Icon` | **10** |
| [Bubble](syrup-bubble-components.md) | `Bubble` | 2 |
| [Checkbox](syrup-checkbox-components.md) | `Checkbox` | 1 |
| **외부 라이브러리** | **`List_네이버쇼핑`** | **4** |
| `❖System Components` | `Title Bar` · `Section Header` | 5 (보드 표기) |

Badge 의존이 10건으로 가장 많습니다. 상품 카드의 할인율·적립금 배지에 쓰입니다.

> 2026-10-08 Badge 페이지에서 `Shape` 이름을 교환(`Pill` ↔ `Rounded`)했으므로, **Product Grid의 Badge 인스턴스가 의도한 모양을 쓰고 있는지 확인**이 필요합니다.

### 7. 스타일 미적용 텍스트 8건

보드 표기 6건을 제외한 수치입니다.

| 크기 · 굵기 | 건수 | 위치 |
| --- | --- | --- |
| **`12 Bold`** | 7 | `LIVE` 배지 5 · `or` 2 |
| `11 Bold` | 1 | 금액 (`2,400금`) |

**전부 9~12px**로 **토큰화하지 않기로 한 범주**입니다. 그대로 두는 것이 기준에 맞습니다.

> `12 Bold`는 [Grid List](syrup-grid-list-components.md) 13건 · [Header](syrup-header-components.md) 3건에 이어 여기서도 7건이 나왔습니다. **파일 전체에서 반복되는 크기**라, 지속되면 13px 하한을 12px로 낮출지 재검토할 만합니다.

### 8. 미바인딩 값

| 값 | 건수 | 성격 |
| --- | --- | --- |
| fill `#00C05A` | 7 | **네이버 녹색** — 브랜드 |
| fill `#FF5700` | 5 | 오렌지 (브랜드 유사색) |
| padding `5` | 14 | 스케일 밖 |
| padding `3` | 11 | 스케일 밖 |
| gap `5` | 7 | 스케일 밖 |
| gap `15` · `1` | 2 | 스케일 밖 |

**미바인딩 radius는 0건**입니다.

`#00C05A`는 네이버 브랜드 색이라 토큰화 대상이 아닙니다. **`#FF5700` 5건은 `Color/Primary_Orange`(#FF6315)와 비슷하지만 다른 값**이라 확인이 필요합니다.

padding `5` · `3`과 gap `5`는 Spacing 스케일(2 · 4 · 6 · 8 …)에 없는 값입니다. [Badge](syrup-badge-components.md)의 `1` · `5`와 같은 성격으로, **토큰 신설 여부를 함께 판단**하면 좋습니다.

### 9. 토큰 상태 — 양호

| 항목 | 결과 |
| --- | --- |
| **원격 텍스트 스타일** | **0건** |
| **미바인딩 radius** | **0건** |
| **제어문자 · U+2028** | **0건** |
| 미바인딩 fill | 12건 (브랜드 색 위주) |
| 외부 토큰 | `Spec docs` 7 — 문서 레이아웃 전용 |
| 폰트 | 전부 Pretendard |

Badge 페이지에서 정리한 원격 스타일 10건이 이 페이지의 `Product Grid / Stamp`를 통해 들어오던 것이었는데, **현재는 0건**입니다.

---

## 정리 우선순위

### ✅ 처리 완료 (2026-10-12)

| 항목 | 내용 |
| --- | --- |
| 마스터 3종 이름 ([1](#1--마스터-3종-이름-정리-2026-10-12-완료)) | `Grid List /` → **`Product Grid /`** · 인스턴스 5건 자동 반영 |
| `Phatner` → `Partner` ([2](#2--phatner--partner-오타-수정-2026-10-12-완료)) | 네 번째 오타 수정 |
| `Property 1` 2건 ([4](#4--property-1-2건-정리-2026-10-12-완료)) | `State` · `Type` — **페이지 내 0건** |
| 레이어명 `syrup_img_방송예정` ([5](#5--레이어명-잔재-정리-2026-10-12-완료)) | → **`Like`** (2 variant) |

전부 **이름만 변경**이며 크기·렌더링 변화가 없습니다. 작업 후 컴포넌트셋 178개 · 인스턴스 1,828개를 전수 검증해 오류·끊긴 참조 **0건**을 확인했습니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | `#FF5700` 5건 확인 ([8](#8-미바인딩-값)) | 값 확인 필요 | 중간 |
| 2 | `2column` 외부 의존 기록 ([3](#3-2column이-외부-컴포넌트를-섞어-씀--과거-기록)) | 2026-11-09 표시 아이템은 자체 primitive 2개로 확인 | 재확인 완료 |
| 3 | padding `3` · `5` · gap `5` ([8](#8-미바인딩-값)) | **Badge와 함께 판단** | 중간 |
| 4 | Badge 인스턴스 `Shape` 확인 ([6](#6-타-페이지외부-의존)) | 2026-10-08 이름 교환 영향 | 낮음 |
