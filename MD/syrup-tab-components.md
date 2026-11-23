# Syrup Design System — Tab 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Tab` 페이지 → [`Tab` 섹션 `8884:13896`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8884-13896) |
| 섹션 크기 | 1440 × 2364 |
| 컴포넌트 수 | **6개** (Master 1 · Child Item 5) |
| Variant 총수 | **25개** (3 · 2 · 2 · 2 · 2 · 14) |
| 기준일 | 2026-11-10 (최종 가이드라인 2개·Usage A~B 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **여러 콘텐츠 영역 중 하나를 선택해 전환할 수 있는 컴포넌트예요.**
> 같은 화면 안에서 콘텐츠를 그룹별로 구분해 보여줄 때 사용해요.

---

## 공개 에셋 이름 정리

2026-11-11 아래 원본의 `.primitive / ` 접두사만 제거했어요. 노드·컴포넌트 키·variant·인스턴스 연결은 유지했으며 게시 작업은 별도로 진행해요. 숨김 유지·검토 대상의 접두사는 유지해요.

| 현재 전체 이름 | 원본 노드 |
| --- | --- |
| `Tab / Tab Item / Underline` | `8905:11010` |
| `Tab / Tab Item / Rounded` | `8905:11166` |
| `Tab / Tab Item / Circle` | `8905:11212` |
| `Tab / Rounded / Icon` | `8914:5701` |
| `Tab / Circle / Image` | `8914:7074` |

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Tab — Master Component](#1-tab--master-component)
3. [Tab Item 3종](#tab-item-3종)
4. [아이콘·이미지 2종](#아이콘이미지-2종)
5. [가이드라인](#가이드라인)
6. [Usage — 사용 예제](#usage--사용-예제)
7. [예제 레이아웃과 AI 사용 기준](#예제-레이아웃과-ai-사용-기준)
8. [설계 규칙 요약](#설계-규칙-요약)
9. [점검 필요 사항](#점검-필요-사항)
10. [정리 우선순위](#정리-우선순위)

---

## 구성 한눈에 보기

마스터 1종과 하위 구성 5종을 유지하고, 별도 섹션에 가이드라인 2개와 Usage A~B를 정리했어요.

기존 마스터 섹션 집계는 높이 2,364 · 노드 **139개** · 텍스트 **21개**예요. 노드·인스턴스·파일 전체 수치는 2026-10-12 점검 기록으로, 이후 추가된 사용 화면과 문서 예제는 포함하지 않아요.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 0 | Title Bar | 페이지 제목 |
| y 434 | Section Header | Master Component |
| y 574 | (높이 446) | `Tab` 1종 |
| y 1020 · y 1160 | Section Header ×2 | (상위 · 하위 제목) |
| y 1234 | (높이 550) | `Tab Item` 3종 |
| y 1784 | Section Header | |
| y 1914 | (높이 386) | 아이콘·이미지 2종 |

### 타입 3종이 각자 Tab Item을 가집니다

```
Tab  (Type = Underline | Rounded | Circle)
├─ Underline → Tab / Tab Item / Underline
├─ Rounded   → Tab / Tab Item / Rounded → Tab / Rounded / Icon
└─ Circle    → Tab / Tab Item / Circle  → Tab / Circle / Image
```

| # | 이름 | 타입 | Variant 축 | 크기 | 인스턴스 |
| --- | --- | --- | --- | --- | --- |
| 1 | `Tab` | Set 3 | `Type` | 360 × 50 | **0** |
| 2 | `Tab / Tab Item / Underline` | Set 2 | `Selected` | 180 × 42 | 2 |
| 3 | `Tab / Tab Item / Rounded` | Set 2 | `Selected` | 164 × 40 | 2 |
| 4 | `Tab / Tab Item / Circle` | Set 2 | `Selected` | 54 × 76 | 5 |
| 5 | `Tab / Rounded / Icon` | Set 2 | `Icon` | 24 × 24 | 2 |
| 6 | `Tab / Circle / Image` | **Set 14** | `Brand` | 46 × 46 | **8** ([List Row](syrup-list-row-components.md) 1) |

2026-10-12 집계에서는 `Tab / Circle / Image`의 다른 페이지 사용이 확인됐어요([List Row](syrup-list-row-components.md) 1건). 현재 파일 전체 사용량을 다시 집계한 수치는 아니에요.

---

## 1. Tab — Master Component

**Node** `8914:5641` · Component Set · **3 variants**

| Property | Type | Options |
| --- | --- | --- |
| `Type` | VARIANT | `Underline` · `Rounded` · `Circle` |

| Type | 크기 | 레이아웃 | 구성 |
| --- | --- | --- | --- |
| `Underline` | **360 × 50** | 가로 · Padding 좌우 16 (`Spacing/400`) · Gap 0 | Tab Item ×2 (164 × 50) · 하단선 `Color/Gray_850` |
| `Rounded` | **328 × 40** | 가로 · Padding 0 · Gap 0 | Tab Item ×2 (164 × 40) |
| `Circle` | **310 × 76** | 가로 · Padding 0 (`Spacing/0`) · Gap 10 (`Spacing/250`) | Tab Item ×5 (54 × 76) |

`Underline`만 컨테이너에 **하단 구분선**이 있고, 나머지 둘은 Tab Item이 스스로 배경·테두리를 가집니다.

---

## Tab Item 3종

### 2. `Tab / Tab Item / Underline`

**Node** `8905:11010` · Set 2 · **180 × 42**
가로 오토레이아웃 CENTER / CENTER · Padding `10` 전면 (`Spacing/250`) · Gap 6 (`Spacing/150`)

| Selected | 하단선 | 텍스트 |
| --- | --- | --- |
| `True` | `Color/Gray_100` | 17 **Bold** `t800_17_bold` · `Color/Gray_100` |
| `False` | `Color/Gray_850` | 17 Regular `b100_17_regular` · `Color/Gray_500` |

선택 시 **선 색과 글자 굵기가 함께** 바뀝니다. 가장 단순한 구조입니다.

### 3. `Tab / Tab Item / Rounded`

**Node** `8905:11166` · Set 2 · **164 × 40**
가로 오토레이아웃 · Padding `2 / 20 / 2 / 20` (`Spacing/50` · `Spacing/500`) · Gap 4 (`Spacing/100`)
테두리 `Color/Gray_850` · 라운드 16 (`Corner radius/400`)

| Selected | 배경 | 텍스트 | 아이콘 |
| --- | --- | --- | --- |
| `True` | 없음 | 14 **Bold** `t1050_14_bold` · `Color/Gray_Black` | **`Tab / Rounded / Icon` 인스턴스** |
| `False` | `Color/Gray_900` | 14 Regular `b400_14_regular` · `Color/Gray_400` | `Tab / Rounded / Icon` 인스턴스 (숨김) ✅ |

이전엔 같은 자리에 하나는 인스턴스, 하나는 생짜 프레임이었고 해소됐습니다 ✅ → [점검 3](#3-rounded의-구조-불일치---해소)

선택 상태의 배경 처리도 뒤집혀 있습니다 — **선택된 쪽이 배경 없음**이고 선택 안 된 쪽이 `Gray_900` 배경입니다.

### 4. `Tab / Tab Item / Circle`

**Node** `8905:11212` · Set 2 · **54 × 76**
세로 오토레이아웃 · Padding 0 · Gap 4 (`Spacing/100`)

| 레이어 | 타입 | 크기 | 내용 |
| --- | --- | --- | --- |
| `Tab` | Frame | 54 × 54 | Padding 4 (`Spacing/100`) · Gap 10 (`Spacing/250`) · 라운드 `circle` |
| └ `Tab / Circle / Image` | Instance | 46 × 46 | 브랜드 이미지 |
| └ `Circle` | Ellipse | 46 × 46 | 테두리 `Color/Gray_950` 1px (이미지 경계) |
| `Title` | Text | 22 × 18 | 이전 `tilte` → [점검 2](#2-tilte-오타---완료-2건) |

| Selected | `Tab` 테두리 | 텍스트 |
| --- | --- | --- |
| `True` | `Color/Primary_Orange` 2px **보임** | 13 Medium `t1360_13_medium` · `Color/Primary_Orange` |
| `False` | `Color/Primary_Orange` 2px **`visible: false`** | 13 Regular `b500_13_regular` ✅ · `Color/Gray_400` |

선택 표시는 **주황 링의 표시/숨김**으로 처리합니다. 숨긴 상태에서도 테두리 설정이 남아 있어, 켜기만 하면 선택 상태가 되는 구조입니다.

`Selected=False`의 텍스트만 스타일이 빠져 있었고 적용했습니다 ✅ → [점검 4](#4-스타일-미적용-텍스트-1건---완료)

---

## 아이콘·이미지 2종

### 5. `Tab / Rounded / Icon`

**Node** `8914:5701` · Set 2 · **24 × 24** · 세로 오토레이아웃 CENTER / CENTER · Gap 12 (`Spacing/300`)

| Icon | 자식 | 크기 | Padding |
| --- | --- | --- | --- |
| `Gold` | `gold_test4 1` | 24 × 15.6 | `4.8 / 0 / 3.6 / 0` — **비정수** |
| `Stamp` | `Stamp` (이전 `image 3244`) ✅ | 16 × 17 | `0 / 0 / 2 / 0` (`Spacing/50`) |

`Gold`의 Padding 4.8 · 3.6은 **비정수 보정값**이고 토큰이 없습니다 → [점검 6](#6-비정수-패딩-48--36)

### 6. `Tab / Circle / Image`

**Node** `8914:7074` · Component Set · **14 variants** · 모두 **46 × 46** · 라운드 `circle`

| Brand | 배경 | 자식 레이어 |
| --- | --- | --- |
| `핫딜쇼핑` | `Color/Primary_Orange` ✅ | `Layer_1` |
| `지마켓` | **#00C01E** | `지마켓` |
| `오늘의집` | **#00A1FF** | `image 3153` |
| `네이버스토어` | `Color/Gray_White` ✅ | `syrup_img_56_naverstore` |
| `옥션` | 없음 | `image 3223` |
| `SSG` · `이마트` · `지그재그` · `아이허브` · `11번가` · `컬리` · `엘지전자` | 없음 | **`image 3231`** (7건 같은 이름) |
| `쿠팡` | 없음 | `image 3231` · `Circle` |
| `알리익스프레스` | 없음 | `image 3231` · `image 3245` |

위 표의 이미지 레이어명은 정리 전 기록이에요. 실제 중복은 쿠팡·알리익스프레스를 포함한 9건이었고 브랜드별 이름으로 수정했어요 → [점검 5](#5-브랜드-이미지-레이어명---완료-14건)

`네이버스토어`만 `syrup_img_56_naverstore`로 제대로 명명돼 있고, `지마켓`은 한글 브랜드명을 씁니다.

---

## 가이드라인

[Figma Guidelines](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11765-3726) · 최종 2개

### 1. 탐색할 정보에 맞는 유형을 사용해요

상위 콘텐츠를 구분할 때는 Underline을 사용해요. 쇼핑몰 이미지와 이름으로 탐색할 때는 Circle을 사용해요.
같은 탐색 묶음에서는 하나의 유형을 유지해 항목의 역할을 일관되게 보여줘요.

- 비교: 콘텐츠 구분 · Underline / 쇼핑몰 탐색 · Circle
- [Figma 가이드라인 1](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11765-3728)

### 2. 현재 선택한 항목을 명확히 표시해요

한 탐색 묶음에서 현재 선택한 항목은 Selected=True, 나머지는 Selected=False로 표시해요.
선택 상태는 기존 Tab Item의 선·색상·글자 굵기로 구분하고, 표시되는 콘텐츠와 일치시켜요.

- 비교: 첫 번째 항목 선택 / 두 번째 항목 선택
- [Figma 가이드라인 2](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11765-3795)

---

## Usage — 사용 예제

[Figma Usage](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11765-3727) · 최종 A~B

| 예제 | 유형 | 설명 | Figma |
| --- | --- | --- | --- |
| A. 콘텐츠 구분 | `Type=Underline` | 금 모으는 쇼핑과 간식 받는 쿠팡 쇼핑처럼 상위 콘텐츠를 구분해요. 선택한 항목에 해당하는 콘텐츠를 보여줘요. | [A](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11765-3957) |
| B. 쇼핑몰별 탐색 | `Type=Circle` | 쇼핑몰 이미지와 이름을 함께 보여줘요. Circle의 선택 표시로 현재 탐색하는 쇼핑몰을 구분해요. | [B](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11765-3976) |

A는 ‘금 모으는 쇼핑’을 선택하고 다른 항목은 미선택으로 표시해요. B는 ‘핫딜쇼핑’을 선택하고 G마켓·SSG·이마트몰·오늘의집은 미선택으로 보여줘요. 항목명과 선택 값은 예제이며 모든 화면의 항목 수·순서·초기 선택값을 규정하지 않아요.

### 최종 문서 범위

스크롤 후 상단에 유지하는 동작은 Tab 자체보다 화면의 스크롤 정책에 가까워, 가이드라인과 Usage에서 제외했어요. **가이드라인은 1~2번, 예제는 A~B만** 사용해요. 상단 고정 여부를 이 문서의 공통 사용 규칙으로 추정하지 않아요.

Rounded는 기존 마스터에 유지돼 있지만 Section 1에서 사용 사례가 확인되지 않아 이번 가이드라인·Usage에는 포함하지 않았어요. Rounded 마스터는 현재 투명도 0.3으로 표시되며, 이 사실만으로 공식 사용 중단이나 사용 금지 상태라고 단정하지 않아요.

---

## 예제 레이아웃과 AI 사용 기준

| 항목 | 현재 문서 구성 |
| --- | --- |
| Guidelines 섹션 | **960 × 714**, 가이드라인 2개 |
| Usage 섹션 | **960 × 392**, 예제 A·B |
| 섹션 스타일 | 원본 Tab 섹션과 동일한 흰 배경, 모서리 **24**, 테두리 없음. 기존 색상·모서리 토큰 연결 유지 |
| Slot | 폭 **360**, 패딩 **0**, 좌측·상단 정렬, 내용에 맞춘 높이 |
| Slot 내부 | Tab 인스턴스를 직접 배치. 불필요한 ‘화면’ 프레임이나 보조 콘텐츠를 추가하지 않음 |
| Underline 예제 | **360 × 50**, 내부 좌우 패딩 **16** 유지, 항목 2개 |
| Circle 예제 | **310 × 76**, 내부 패딩 0, 항목 간격 **10**, 항목 5개 |
| 설명과 Slot 사이 | **50**, 예제끼리 시각 요소의 시작 높이를 맞춤 |

- `Type`은 상위 Tab의 VARIANT 속성이고, `Selected`는 각 하위 Tab Item의 VARIANT 속성이에요. 상위 Tab에 `Selected`나 `SelectedIndex` 같은 속성이 있다고 가정하지 않아요.
- 유형에 맞는 기존 Tab과 Tab Item을 사용해요. 선택 상태를 표현하려고 선·테두리·글자색만 임의로 덮어쓰지 않고 `Selected=True` / `False`를 적용해요.
- 한 탐색 묶음에서 선택된 항목 1개와 나머지 미선택 항목을 구분해요. 상위 콘텐츠 탭과 별도 쇼핑몰 탭은 서로 다른 탐색 묶음이므로 선택 상태를 각각 관리할 수 있어요.
- Circle의 쇼핑몰 이미지와 이름은 탐색 대상을 구분하는 핵심 정보예요. 문서를 단순화한다는 이유로 이미지를 숨기거나 일반적인 자리표시자로 바꾸지 않아요. 기존 Brand 이미지 인스턴스를 활용해요.
- Underline의 좌우 16은 컴포넌트 내부 패딩이에요. Slot 패딩 0과 구분하고, 예제를 왼쪽에 맞추기 위해 마스터 내부 여백을 제거하지 않아요.
- 예제의 360·310 폭과 문서 섹션 크기는 현재 배치 수치예요. 모든 제품 화면의 고정 폭이나 Tab 항목 수의 제한으로 확대 해석하지 않아요.
- Slot의 itemSpacing은 16 토큰에 연결돼 있지만 현재 Slot마다 인스턴스 1개만 있어 시각적으로 요소 사이 간격을 만들지 않아요. Circle 내부 항목 간격 10과 혼동하지 않아요.
- 현재 시럽 토큰과 기존 텍스트 스타일을 사용해요. 같은 값의 이전 토큰을 신규 구성에 다시 연결하지 않아요. 브랜드 고유색을 임의의 시럽 색으로 바꾸지 않아요.
- 가이드라인의 양쪽은 모두 유효한 유형·선택 상태의 비교예요. 템플릿의 Do / Don’t 레이어 이름만 보고 오른쪽을 금지 사례로 해석하지 않아요.
- Section 1의 아노테이션 13개를 제거했어요. 실제 화면 전체를 복제하지 않고 Tab 컴포넌트만으로 사용 패턴을 설명해요.
- 아래 기존 구조 개선 제안은 과거 점검 기록이에요. 신규 사용 규칙이나 마스터 변경 지시로 해석하지 않아요.

---

## 설계 규칙 요약

### 타입별 선택 표현

| Type | 선택 표시 | 글자 변화 |
| --- | --- | --- |
| `Underline` | 하단선 `Gray_850` → `Gray_100` | Regular → **Bold** |
| `Rounded` | 배경 `Gray_900` → 없음 | Regular → **Bold** · `Gray_400` → `Gray_Black` |
| `Circle` | 주황 링 숨김 → 보임 | Regular → **Medium** · `Gray_400` → `Primary_Orange` |

세 타입 모두 **글자 굵기를 함께 바꿉니다.** 색만으로 구분하지 않아 접근성 면에서 좋습니다.

### 토큰 적용 상태

| 항목 | 상태 |
| --- | --- |
| Padding | `Spacing/50` · `100` · `250` · `400` · `500` ✅ — **비정수 4.8 / 3.6 제외** |
| Gap | `Spacing/0` · `100` · `150` · `250` · `300` ✅ |
| 라운드 | `Corner radius/400` · `circle` ✅ |
| 텍스트 색 | `Gray_100` · `Gray_400` · `Gray_500` · `Gray_Black` · `Primary_Orange` ✅ |
| 선 색 | `Gray_100` · `Gray_850` · `Gray_950` · `Primary_Orange` ✅ |
| 텍스트 스타일 | 기존 점검에서 Circle 미선택 텍스트의 누락 1건을 수정 완료 ([점검 4](#4-스타일-미적용-텍스트-1건---완료)) |
| 미바인딩 색상 | **2건** (브랜드 색) |
| 원격 텍스트 스타일 | **0건** ✅ |
| 줄 구분자(U+2028/9) | **0건** ✅ |

### 타 페이지 의존

| 출처 | 컴포넌트 | 건수 |
| --- | --- | --- |
| ❖System Components | `Section Header` 4 · `Title Bar` 1 | 5 |

컴포넌트 내부 참조와 외부 라이브러리 인스턴스가 모두 **0건**입니다.

---

## 점검 필요 사항

> 아래는 2026-10-12에 작성한 마스터 구조·네이밍 점검 기록이에요. 2026-11-10에는 최종 가이드라인 2개와 예제 A~B를 반영했으며, 이번 문서 작업에서 마스터의 유형·선택 표현을 변경하지 않았어요.

### 1. 섹션명이 페이지명과 다름 — ✅ 완료

| 항목 | 값 |
| --- | --- |
| 페이지명 | `Tab` |
| 섹션명 | ~~`Tab Bar`~~ → **`Tab`** ✅ |
| 컴포넌트명 | `Tab` |

섹션만 `Tab Bar`였고, 사용자가 `Tab`으로 변경했습니다.

파일 안에 **`Tab Bar`라는 이름의 다른 컴포넌트가 따로 존재**하므로(소문자 `state` 속성을 가진 것으로 앞서 확인됨), 그대로 두었다면 **두 개념이 섞일 수 있었습니다.**

### 2. `tilte` 오타 — ✅ 완료 (2건)

| 변경 전 | 변경 후 |
| --- | --- |
| `tilte` | **`Title`** ✅ |

`Tab / Tab Item / Circle`의 텍스트 레이어명으로, **`title`의 철자가 뒤바뀌어** 있었습니다. 두 variant 모두에 있어 2건이었습니다.

| 컴포넌트 | 텍스트 레이어명 |
| --- | --- |
| `Tab Item / Underline` | `Tab` |
| `Tab Item / Rounded` | `Tab` |
| `Tab Item / Circle` | ~~`tilte`~~ → **`Title`** ✅ |

다른 둘은 `Tab`을 쓰지만, **철자를 바로잡고 첫 글자만 대문자로** 올리는 쪽으로 정했습니다. `Title`은 역할을 더 분명히 드러냅니다.

[Stepper](syrup-stepper-components.md)의 `Desription` → `Description`, [Search Field](syrup-search-field-components.md)의 `btn_serach` → `Search`와 같은 성격입니다.

### 3. Rounded의 구조 불일치 — ✅ 해소

| Selected | 수정 전 | 수정 후 |
| --- | --- | --- |
| `True` | `Tab / Rounded / Icon` **INSTANCE** | 동일 |
| `False` | `Icon` **FRAME** (생짜 이미지) | **`Tab / Rounded / Icon` INSTANCE** ✅ |

같은 자리인데 한쪽은 인스턴스, 한쪽은 생짜 프레임이었습니다. 둘 다 안에 `gold_test4 1` 24 × 15.6을 담아 **내용은 같았지만** 다음 문제가 있었습니다.

| 영향 | 설명 |
| --- | --- |
| 오버라이드 단절 | `Selected`를 바꾸면 아이콘 교체(`Icon=Gold`↔`Stamp`)가 유지되지 않음 |
| 아이콘 선택 불가 | `Selected=False`에는 `Icon` 속성이 닿지 않아 Stamp로 바꿀 수 없음 |
| 레이어명 | ~~`Frame 1171276799`~~ → `Icon` ✅ |

사용자가 **같은 컴포넌트를 쓰도록 교체**해 해소됐습니다.

#### 검증 결과

| 항목 | 상태 |
| --- | --- |
| 두 variant 모두 같은 원본 참조 | ✅ `Tab / Rounded / Icon` |
| 중첩 인스턴스 노출 | ✅ 양쪽 `노출됨=true` |
| 표시 상태 | ✅ `True`=보임 · `False`=숨김 (의도대로) |
| 레이어명 | ✅ 양쪽 `Tab / Rounded / Icon` |

구조가 같아져 **variant를 전환해도 `Icon` 선택이 이어받는 조건**을 갖췄고, `Selected=False`도 이제 `Icon` 속성을 가집니다.

> **측정 한계** — 임시 인스턴스로 전환 동작을 시험했으나, **플러그인 실행 중에 variant를 바꾸고 곧바로 읽으면 값이 불안정**해 확정적으로 측정하지 못했습니다(같은 조건에서 서로 다른 결과가 나옴). 구조가 일치한다는 점만 확인했습니다. 실제 전환 동작은 Figma에서 직접 토글해 보는 편이 확실합니다. 시험에 쓴 임시 인스턴스는 모두 삭제했고, 잔여 노드 0건을 확인했습니다.

### 4. 스타일 미적용 텍스트 1건 — ✅ 완료

| 위치 | 크기/굵기 | 조치 |
| --- | --- | --- |
| `Tab Item / Circle` ▸ `Selected=False` ▸ `Title` | 13 Regular | **`b500_13_regular` 적용** ✅ |

`Selected=True`는 `t1360_13_medium`이 적용돼 있는데 `False`만 빠져 있었습니다.

13px는 **시스템이 관리하는 하한**이고 토큰도 있어 바로 적용했습니다. 페이지의 **스타일 미적용 텍스트가 0건**이 됐습니다.

### 5. 브랜드 이미지 레이어명 — ✅ 완료 (14건)

`Tab / Circle / Image` 14개 variant의 자식 레이어명이었습니다.

| 상태 | 브랜드 | 변경 전 | 변경 후 |
| --- | --- | --- | --- |
| **❌ 9건 중복** | `SSG` · `이마트` · `지그재그` · `아이허브` · `11번가` · `컬리` · `쿠팡` · `엘지전자` · `알리익스프레스` | **전부 `image 3231`** | **각 브랜드명** ✅ |
| ⚠️ 기본 이름 | `핫딜쇼핑` | `Layer_1` | `핫딜쇼핑` ✅ |
| ⚠️ 기본 이름 | `오늘의집` | `image 3153` | `오늘의집` ✅ |
| ⚠️ 기본 이름 | `옥션` | `image 3223` | `옥션` ✅ |
| ⚠️ 기본 이름 | `알리익스프레스` (2번째) | `image 3245` | `알리익스프레스 2` ✅ |
| ⚠️ 기본 이름 | `Stamp` 아이콘 | `image 3244` | `Stamp` ✅ |
| ✅ 그대로 | `네이버스토어` | `syrup_img_56_naverstore` | 유지 |
| ✅ 그대로 | `지마켓` | `지마켓` | 유지 |

**서로 다른 브랜드 이미지 9개가 같은 이름**이었습니다. 레이어 패널에서 구분할 수 없고, 어느 것이 어느 브랜드인지 variant 이름으로만 알 수 있었습니다.

> **정정** — 처음 이 항목을 **7건 중복**으로 적었는데, `쿠팡`과 `알리익스프레스`도 같은 `image 3231`을 쓰고 있어 **실제로는 9건**이었습니다. 두 variant는 자식이 2개라 따로 분류했다가 중복 집계에서 빠졌습니다.

`네이버스토어`가 쓰는 `syrup_img_56_naverstore` 형식이 가장 명확하지만 **에셋 파일명을 알아야** 하므로, 이미 `지마켓`이 쓰고 있던 **브랜드명 그대로** 방식으로 맞췄습니다.

자식이 2개인 두 variant는 다음과 같이 처리했습니다.

| 브랜드 | 자식 |
| --- | --- |
| `쿠팡` | `쿠팡` · `Circle`(기본 이름이 아니라 유지) |
| `알리익스프레스` | `알리익스프레스` · `알리익스프레스 2` |

정리 후 **기본 이름 0건**입니다.

### 6. 비정수 패딩 4.8 / 3.6

| 위치 | Padding |
| --- | --- |
| `Tab / Rounded / Icon` ▸ `Icon=Gold` | 상 **4.8** · 하 **3.6** |
| `Tab Item / Rounded` ▸ `Selected=False` ▸ 아이콘 인스턴스 | 상 **4.8** · 하 **3.6** |

24 × 24 틀 안에 24 × 15.6 이미지를 세로 가운데 두려다 나온 값입니다. (24 − 15.6) ÷ 2 = 4.2인데 4.8 / 3.6으로 **위아래가 다릅니다.**

| 선택지 | 내용 |
| --- | --- |
| A | Padding 0 + **가운데 정렬**로 대체 — [Result](syrup-result-components.md)에서 쓴 방식 |
| B | 현행 유지 — 0.6px 차이는 보이지 않음 |

A는 [Result](syrup-result-components.md)의 `Empty` 아이콘에서 Padding 14/23을 CENTER 정렬로 바꿔 토큰 없는 값 4건을 없앤 것과 같은 방식입니다. 다만 **위아래 비대칭이 의도라면 모양이 0.6px 바뀝니다.**

### 7. 브랜드 색 2건 미바인딩

| 색 | 브랜드 |
| --- | --- |
| **#00C01E** | 지마켓 |
| **#00A1FF** | 오늘의집 |

둘 다 **브랜드 고유색**입니다. [Progress Stepper](syrup-progress-stepper-components.md)의 Express 계열 21건, [Label](syrup-label-components.md)의 Metric 색과 같이 **도메인 색은 토큰화 대상에서 제외**해 온 기준을 따르면 그대로 둡니다.

나머지 12개 브랜드는 배경 없이 이미지만 쓰거나 토큰(`Primary_Orange` · `Gray_White`)을 씁니다.

### 8. `Selected` 옵션 순서 불일치

| 컴포넌트 | 옵션 순서 |
| --- | --- |
| `Tab Item / Underline` | `True` · `False` |
| **`Tab Item / Rounded`** | **`False` · `True`** |
| `Tab Item / Circle` | `True` · `False` |

`Rounded`만 반대입니다. 세 Tab Item의 **레이어 순서는 모두 `Selected=True`가 먼저**인데 옵션 표시만 다릅니다.

[Stepper](syrup-stepper-components.md)에서 확인한 대로 **레이어 재정렬로는 표시 순서가 바뀌지 않고 값 개명으로만 다시 계산**됩니다. 기본값은 세 컴포넌트 모두 `True`로 같으므로 **표시 순서만 남은 문제**입니다.

### 9. `gold_test4 1` 2건

`Tab` 페이지의 `Rounded / Icon` ▸ `Icon=Gold`와 숨겨진 `Frame 1171276799`에 있습니다.

**파일 전체 56건 / 12개 페이지**에 퍼져 있어 이 페이지만 고치면 어긋납니다 → [Swipe 점검 7](syrup-swipe-components.md#7-gold_test4-3--파일-전체-56건)

### 10. 인스턴스 현황 — 2026-10-12 기록

| 구분 | 인스턴스 |
| --- | --- |
| `Tab` | **0** |
| `Tab / Circle / Image` | 8 (Tab 7 · **[List Row](syrup-list-row-components.md) 1**) |
| `Tab / Tab Item / Circle` | 5 |
| `Tab / Tab Item / Underline` · `Rounded` · `Rounded / Icon` | 각 2 |

당시 집계에서는 Tab 마스터 인스턴스가 0건이었지만, 현재는 사용 화면과 가이드라인·Usage에 인스턴스가 있어요. 과거 0건을 현재 사용량이나 변경 영향 범위로 해석하지 않아요. `Circle / Image`는 탭 밖에서도 사용된 기록이 있으므로 개명 시 참조 범위를 확인해야 해요.

> **이 수치는 이 Figma 파일 기준**입니다. 다른 파일·디태치·코드 사용은 포함되지 않습니다.

---

## 정리 우선순위

### 문서 업데이트 완료 (2026-11-10)

최종 가이드라인 2개와 Usage A~B, Figma 링크, 사용 범위와 예제 배치 기준을 반영했어요. 사용자가 제외하기로 한 스크롤 관련 가이드라인 3번·예제 C는 현행 가이드에서 제외하고, 남은 항목에 맞춰 정리된 섹션 크기를 기록했어요. Rounded는 마스터 규격만 유지하고 이번 사용 예제에는 포함하지 않았어요.

### ✅ 완료 (2026-10-12)

모양이 바뀌지 않는 작업 **18건**을 처리했습니다.

| # | 항목 | 결과 |
| --- | --- | --- |
| 1 | `tilte` → `Title` ([2](#2-tilte-오타---완료-2건)) | 2건 |
| 2 | `b500_13_regular` 적용 ([4](#4-스타일-미적용-텍스트-1건---완료)) | 1건 |
| 3 | 브랜드 이미지 레이어명 ([5](#5-브랜드-이미지-레이어명---완료-14건)) | **14건** |
| 4 | `Frame 1171276799` → `Icon` ([3](#3-rounded의-구조-불일치---해소)) | 1건 |
| — | 섹션명 `Tab Bar` → `Tab` ([1](#1-섹션명이-페이지명과-다름---완료)) | **사용자 직접 처리** |

정리 후 **기본 이름 0건 · 오타 0건 · 스타일 미적용 텍스트 0건**입니다.

### 남은 과제

| 순위 | 항목 | 성격 | 비용 |
| --- | --- | --- | --- |
| 1 | 비정수 패딩 4.8 / 3.6 ([6](#6-비정수-패딩-48--36)) | 0.6px 변화 가능 | 중간 |
| 2 | `gold_test4` ([9](#9-gold_test4-1-2건)) | **파일 전체 56건과 함께** | 중간 |
| 3 | `Selected` 옵션 표시 순서 ([8](#8-selected-옵션-순서-불일치)) | 현행 유지 권장 | — |
| 4 | 브랜드 색 2건 ([7](#7-브랜드-색-2건-미바인딩)) | 도메인 색 — 제외 | — |

**실제 결함은 모두 해소됐습니다.** 남은 4건은 전부 판단 사항이거나 파일 전체 작업입니다.

1번(비정수 패딩)은 0.6px 차이라 화면에서 구분되지 않고, 2번은 12개 페이지에 걸친 56건이라 파일 전체를 한 번에 다루는 편이 낫습니다. 3·4번은 현행 유지를 권합니다.
