# Syrup Design System — Indicator 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Indicator` 페이지 → [Indicator 섹션 `8792:57071`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8792-57071) |
| 섹션 구성 | Indicator 1440×1531 → Guidelines 960×1660 → Usage 2160×478 |
| 컴포넌트 수 | **4개** (전부 Component Set) |
| 기준일 | 2026-11-09 (사용자가 수정한 Guidelines · Usage 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **점이나 숫자로 콘텐츠의 현재 위치와 참여·시청 횟수를 보여주는 컴포넌트예요.**
> 안내할 정보와 배경에 맞는 유형을 사용하고, 실제 상태에 맞춰 값을 표시해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Indicator — Master Component](#1-indicator--master-component)
3. [Child Items](#2-child-items)
4. [설계 규칙 요약](#설계-규칙-요약)
5. [Usage](#usage)
6. [Guidelines](#guidelines)
7. [AI 도구 적용 기준](#ai-도구-적용-기준)
8. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440×1531이며, Indicator 마스터가 primitive 3종을 감쌉니다. 별도 Guidelines 4항목과 Usage 5패턴으로 실제 사용 기준을 설명합니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `Indicator` 3종 |
| y 851 | Child Items | `Dot` · `Number` · `Background` |

| # | 이름 | 타입 | Variant 축 | 크기 | 과거 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Indicator` | Set | `Type` 3종 | 16~50 × 6~37 | **12** |
| 2 | `.primitive / Indicator / Dot` | Set | `White` 2종 | 30 × 6 | 3 |
| 3 | `.primitive / Indicator / Number` | Set | `Size` × `Bold` (**4종**) + `More` | 16~24 × 13 / 19 | 6 |
| 4 | `.primitive / Indicator / Background` | Set | `Size` × `Variant` × `Padding` (**8종**) + `More` · `Text` | 97~156 × 21~52 | 3 |

---

## 1. Indicator — Master Component

**Node** `8792:57061` · Component Set · **3 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Dot` | `Dot` · `Number` · `Number_Background` |

| Variant | 크기 | 내용 |
| --- | --- | --- |
| `Dot` | 30 × 6 | `.primitive / Indicator / Dot` 인스턴스 |
| `Number` | 16 × 13 | `.primitive / Indicator / Number` 인스턴스 |
| `Number_Background` | 50 × 37 | `.primitive / Indicator / Background` 인스턴스 |

**세 variant 모두 primitive 인스턴스 하나만 담은 래퍼**입니다. 패딩·배경·간격이 전부 0이고, 실제 모양은 안쪽이 결정합니다.

> 실제 Type 값은 `Number_Background`입니다. MD나 자동화에서 임의로 `Background`로 변경하지 않습니다.

### 사용처 (2026-10-12 과거 집계)

| 페이지 | 건수 |
| --- | --- |
| `AD` · `Card` | 각 4 |
| `Progress Stepper` | 2 |
| `Banner` · `List Row` | 각 1 |

**5개 페이지에 걸쳐 12건** 쓰이는 공용 컴포넌트입니다.

---

## 2. Child Items

### .primitive / Indicator / Dot

**Node** `8827:30427` · Component Set · **2 variants** · 30 × 6

캐러셀 페이지 표시용 점 3개입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `White` | VARIANT | `False` | `False` · `True` |

| Variant | 1번째 (현재) | 2·3번째 |
| --- | --- | --- |
| `White=False` | `Color/Gray_500` | `Color/Gray_750` |
| `White=True` | **`Color/Gray_White`** | `Color/Gray_500` |

점 크기 6 × 6, 간격 `Spacing/150`(6)입니다.

`White=True`는 **사진·영상 위**에 올릴 때 씁니다. 현재 위치를 흰색으로, 나머지를 회색으로 표시합니다.

> 현재 위치가 **항상 첫 번째 점**에 고정되어 있습니다. 2번째·3번째가 현재인 상태는 variant로 제공되지 않아, 사용 시 인스턴스 안에서 직접 색을 바꿔야 합니다.

### .primitive / Indicator / Number

**Node** `8812:60317` · Component Set · **4 variants**

`1 / 7` 형태의 숫자 표시입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |
| `Bold` | VARIANT | `False` | `True` · `False` |
| `More` | BOOLEAN | `true` | — |

2 × 2 = **4조합이 모두 존재하는 완전 매트릭스**입니다.

| Size | Bold | 크기 | 텍스트 스타일 |
| --- | --- | --- | --- |
| `S` | `False` | 16 × 13 | **스타일 없음** — 11 Regular |
| `S` | `True` | 18 × 13 | **스타일 없음** — 11 Bold |
| `M` | `False` | 22 × 19 | `b300_15_regular` |
| `M` | `True` | 24 × 19 | `t1000_15_bold` |

**`Size=M`만 토큰 스타일이 적용**되어 있고 `S`는 미적용입니다

#### 색 구분

세 텍스트(`현재` · `/` · `전체`)의 색이 나뉩니다.

| 요소 | 색 |
| --- | --- |
| 현재 번호 | **`Color/Gray_Black`** |
| `/` · 전체 번호 | `Color/Gray_500` |

현재 위치만 진하게 강조하는 구조입니다. 네 variant 모두 동일합니다.

### .primitive / Indicator / Background

**Node** `8824:10832` · Component Set · **8 variants**

배경이 있는 형태로, 텍스트 + 숫자를 함께 보여줍니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |
| `Variant` | VARIANT | `Fill` | `Fill` · `Weak` |
| `Padding` | VARIANT | **`True`** | `False` · `True` |
| `More` · `Text` | BOOLEAN | `true` | — |

2 × 2 × 2 = **8조합이 모두 존재하는 완전 매트릭스**입니다.

#### Variant — 배경과 글자색

| Variant | 배경 | `Text` · 현재 번호 | `/` · 전체 번호 |
| --- | --- | --- | --- |
| `Fill` | **`Color/Opacity_Black_300`** (검정 25%) | `Color/Gray_White` | `Color/Gray_White` |
| `Weak` | **`Color/Gray_950`** (#F6F6F7) | `Color/Gray_Black` | `Color/Gray_500` |

`Fill`은 **반투명 검정**이라 사진 위에 올리는 용도이고, `Weak`는 밝은 배경용입니다.

`Fill`은 세 텍스트가 모두 흰색이라 **현재/전체 구분이 없고**, `Weak`는 `Number`와 같은 방식으로 구분합니다.

#### Size

| Size | 내부 크기 | 텍스트 스타일 |
| --- | --- | --- |
| `S` | 97 × 21 | `c100_12_regular` |
| `M` | 140 × 36 | `b300_15_regular` |

#### Padding

| Padding | 바깥 크기 | 안쪽 |
| --- | --- | --- |
| `False` | 내부 크기 그대로 (97 × 21 · 140 × 36) | — |
| `True` | **+16** (113 × 37 · 156 × 52) | `Spacing/200`(8) 사방 |

`Padding` 축은 **배경 바깥에 여백만 더합니다.** 화면 가장자리에서 띄울 때 쓰는 것으로 보입니다.

> Padding=True는 배경 바깥에 사방 8을 더합니다. 예제 C의 50×37에는 이 여백이 포함되어 있습니다. 문구·숫자 표시 여부에 따라 폭이 달라지므로 전체 마스터 샘플 폭을 고정값으로 쓰지 않습니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 점 크기 · 간격 | 6 × 6 · `Spacing/150` (6) |
| 현재 위치 강조 | `Color/Gray_Black` (밝은 배경) · `Color/Gray_White` (어두운 배경) |
| 비활성 | `Color/Gray_500` · `Color/Gray_750` |
| 배경 (어두움) | `Color/Opacity_Black_300` (25%) |
| 배경 (밝음) | `Color/Gray_950` |
| 패딩 | `Spacing/200` (8) — `Padding=True`만 |
| 타이포 (S) | `c100_12_regular` · **11px 미적용** |
| 타이포 (M) | `b300_15_regular` · `t1000_15_bold` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11569:4260`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11569-4260) · 2160×478 |
| 구성 | A~E 5패턴 · 슬롯 폭 360 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

전체 제품 화면 대신 실제 컴포넌트와 설명에 필요한 주변 요소를 사용합니다. 설명 영역–슬롯 간격은 50입니다. 슬롯과 내부 요소의 크기·간격은 사용자가 수정한 현재 구성을 따르며, 예제의 배치값을 모든 화면의 공통 규격으로 해석하지 않습니다.

| 예제 | Node | 현재 설명 | 소재와 설정 |
| --- | --- | --- | --- |
| A. Dot으로 위치 안내 | `11569:4261` | 카드처럼 여러 콘텐츠를 넘겨 볼 때 Dot으로 현재 위치를 보여줘요. 전체 콘텐츠 수와 현재 위치에 맞춰 점의 개수와 활성 상태를 표시해요. | 밝은 콘텐츠 영역 328×130 · Type=Dot · White=False |
| B. 숫자로 위치 안내 | `11569:4287` | 배너나 콘텐츠 묶음에서 현재 순서와 전체 개수를 숫자로 보여줘요. 연결된 콘텐츠 가까이에 배치해 어떤 항목의 위치인지 알 수 있게 해요. | Banner 328×86 · 「쇼핑 적립이 처음이라면?」 · Number S · 1/2 |
| C. 이미지 위 위치 안내 | `11569:4315` | 이미지나 색이 있는 콘텐츠 위에서는 배경이 있는 숫자형을 사용할 수 있어요. 내용 위에서도 현재 순서와 전체 개수가 읽히도록 해요. | 어두운 영역 328×130 · Number_Background · Fill/S/Padding=True · 1/7 |
| D. 참여 횟수 안내 | `11569:4345` | 참여 횟수처럼 현재 수와 전체 기준을 함께 보여줄 때 숫자형을 사용해요. 주변 문구로 숫자가 무엇을 뜻하는지 안내해요. | 「많이 보고 보너스 100금」 + 5/20 · Number S |
| E. 문구와 함께 수량 안내 | `11569:4373` | 숫자만으로 의미가 부족하면 설명 문구나 단위를 함께 표시해요. 배경이 있는 구성에서는 Text와 배경 옵션을 내용에 맞게 선택해요. | 「내가 본 영상 2/5개」 · Number_Background · Weak/M/Padding=False · Text=true |

C와 E는 모두 Background의 More=false입니다. E는 Text=true로 의미를 함께 표시하며, C는 Text=false로 현재 순서와 전체 개수만 표시합니다.

### 현재 슬롯과 배치값

| 항목 | 현재 값 | 범위 |
| --- | --- | --- |
| A / B / C 슬롯 높이 | 130 / 86 / 130 | 문서 예제 |
| D / E 슬롯 높이 | 22 / 36 | 문서 예제 |
| D 문구–숫자 행 간격 | 61 | 사용자 조정값 · 폭 360의 설명용 행 |
| E 표시 크기 | 151×36 | 현재 문구·수치·단위 기준 |
| C Indicator 외곽 | 50×37 | S + Padding=True · Text/More=false |

61 등 예제별 여백은 텍스트 길이와 배치에 따른 값이며 신규 공통 간격 토큰이나 제품 기본 여백이 아닙니다. 숫자형의 폭은 자리 수·단위·문구에 따라 달라집니다.

---

## Guidelines

[Guidelines `11569:4259`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11569-4259) · 960×1660 · 4항목

Guidelines 템플릿 `11237:44468`을 사용합니다. 좌우는 모두 허용된 유형·상태의 비교이며 Do / Don’t가 아닙니다. 항목의 설명 영역–슬롯 간격은 50입니다.

### 1. 안내할 정보에 맞는 유형을 사용해요

**Node** `11569:4408`

콘텐츠의 현재 위치는 Dot이나 숫자형으로 표시해요. 현재 순서와 전체 개수를 숫자로 명시할 때는 숫자형을 사용해요.
참여·시청 횟수도 숫자형으로 표시하고, 무엇을 나타내는 값인지 알 수 있도록 관련 문구와 함께 배치해요.

| 위치 | 현재 Figma 라벨 | 소재 | 의미 |
| --- | --- | --- | --- |
| 왼쪽 | Dot · 콘텐츠 위치 | Card / News 320×288 + 점 3개 | 넘겨 보는 콘텐츠의 현재 위치 |
| 오른쪽 위 | Number · 횟수 안내 | Progress Stepper / News 328×142 · 「많이 보고 보너스 100금」 · 5/20 | 참여·시청 횟수 |
| 오른쪽 아래 | 위 라벨 아래 함께 배치 | Banner 328×86 · 「쇼핑 적립이 처음이라면?」 · 1/2 | 현재 순서와 전체 개수 |

오른쪽은 횟수와 위치의 두 숫자형 사례를 함께 보여줍니다. 현재 라벨은 「Number · 횟수 안내」지만 아래 배너의 1/2는 횟수가 아닌 콘텐츠 위치입니다. 이 문서는 현재 라벨을 그대로 기록하며, 오른쪽 전체를 횟수 안내로만 해석하지 않습니다.

숫자형을 고르는 기준은 Dot보다 정확하다는 뜻이 아니라 **순서와 전체 개수를 숫자로 명시할 필요가 있는지**입니다.

### 2. Dot은 배경에서 구분되는 색을 사용해요

**Node** `11569:4462`

밝은 배경에서는 기본 Dot을, 어두운 이미지나 컬러 위에서는 White=True를 사용해요.
현재 위치의 활성 점과 나머지 점이 배경에서 구분되는지 확인해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| White=False · 밝은 배경 | White=True · 어두운 배경 |
| 328×130의 밝은 영역 | 328×130의 어두운 영역 |

White는 안쪽 Dot primitive에서 선택합니다. 바깥 Indicator의 Type=Dot만 선택하면 배경에 맞는 색까지 자동 설정된다고 가정하지 않습니다.

### 3. 숫자 배경은 배치되는 영역에 맞춰 선택해요

**Node** `11569:4514`

이미지 위에서 숫자를 구분해야 할 때는 Fill, 밝은 영역에서 정보를 묶어 보여줄 때는 Weak를 활용해요.
배경 없이 읽히는 영역에서는 Number를 사용하고, Size와 Padding은 기존 영역의 구성에 맞춰 선택해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Fill · 이미지 위 | Weak · 정보 영역 |
| 어두운 영역 328×130 위 1/7 | 「한달 모두 출석하면 / 개근상 300금」 옆 3/31 |
| Background · S · Fill · Padding=True | Background · S · Weak · Padding=False |
| Text=false · More=false | Text=false · More=false |

오른쪽은 출석 정보의 주변 문구와 Weak 숫자 배경을 함께 사용한 사례입니다. 설명용 행은 229×21, 간격 8이며 숫자 표시 자체는 42×21입니다. 왼쪽 배경 바깥 패딩과 오른쪽 패딩 없음의 차이도 함께 유지합니다.

### 4. 숫자의 의미가 드러나도록 표시해요

**Node** `11569:4575`

현재 순서·횟수와 전체 기준을 실제 데이터에 맞게 표시해요. 의미가 모호하면 주변 문구나 Text, 단위를 함께 사용해요.
콘텐츠가 바뀌거나 참여가 완료되면 현재 값과 활성 상태도 함께 갱신해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 주변 문구 · 참여 횟수 | Text · 내가 본 영상 |
| 「많이 보고 보너스 100금」 + 5/20 | 「내가 본 영상 2/5개」 |
| Number S · Bold=False | Background M · Weak · Padding=False · Text=true · More=false |

왼쪽 행은 폭 360, 높이 36, 문구–숫자 간격 61입니다. 오른쪽은 151×36입니다. 두 예제는 숫자의 의미를 외부 문구 또는 내부 Text·단위로 설명하는 서로 다른 방식입니다.

---

## AI 도구 적용 기준

1. Indicator의 실제 Type 값 `Dot` / `Number` / `Number_Background`를 사용합니다. 표시 문구를 이유로 Type 이름을 임의 변경하지 않습니다.
2. 콘텐츠 위치와 참여·시청 횟수를 구분합니다. 1/2는 현재 콘텐츠 순서, 5/20은 연결된 안내에 따른 횟수이며 숫자 모양만 보고 의미를 결정하지 않습니다.
3. Dot의 White, Number의 Size/Bold, Background의 Size/Variant/Padding/Text/More는 각각 하위 primitive에서 설정합니다. 바깥 Type만 바꾸는 것으로 모든 구성이 완료된다고 가정하지 않습니다.
4. 실제 데이터에 맞춰 현재 값·전체 값·단위를 갱신합니다. 예제의 1/2, 1/7, 5/20, 3/31, 2/5개를 고정 규칙으로 쓰지 않습니다.
5. Dot 마스터는 3개·첫 번째 활성의 대표 상태입니다. 실제 콘텐츠 수와 활성 위치가 다를 때 마스터 샘플 그대로 두지 않습니다. 현재 파일에 Active나 Count 속성이 있다고 가정하지 않습니다.
6. Text는 설명 문구, Background의 More는 「더 보기」의 표시 여부입니다. 단순 위치·횟수 안내 사례는 More=false입니다. 더 보기 문구의 노출만으로 실제 이동 동작이 자동 제공된다고 가정하지 않습니다.
7. Background의 현재 Padding 기본값은 True입니다. Padding=True는 배경 바깥 사방 8을 포함하므로 배치 시 같은 여백을 중복 계산하지 않습니다.
8. 숫자·문구에 맞춰 콘텐츠 폭을 유지합니다. 문구 포함 샘플 폭이나 화면 슬롯 폭을 Indicator 자체의 고정 폭으로 복제하지 않습니다.
9. 사용자가 조정한 61·8 등 설명용 행 간격과 슬롯 크기는 문서 배치값입니다. 공통 제품 규격과 구분하며 임의로 원복하지 않습니다.
10. 이 문서 업데이트는 Figma의 구성·간격·라벨·마스터를 변경하지 않습니다. 확인 범위는 디자인 시스템 Indicator 페이지이며 제품 전체 사용량 통계가 아닙니다.

---

## 현재 확인 사항

2026-11-09 현재 Figma의 사용자 수정 사례와 본문, 마스터 기본값을 대조했습니다.

| 항목 | 확인 결과 |
| --- | --- |
| 구성 | Component Set 4개 · Indicator 3 / Dot 2 / Number 4 / Background 8 variants |
| 배경 Padding 기본값 | True · 이전 문서의 False 수정 |
| Guidelines | 4항목 · 1번은 Card / News + Progress Stepper / News + Banner로 변경 |
| Usage | 5패턴 · B는 실제 Banner, D는 보너스 안내와 횟수, E는 문구·단위 포함 Weak 구성 |
| 원본 자료 | Section 1의 아노테이션 20개 제거 완료 (2026-11-06) |
| 라벨 기록 | 1번 오른쪽은 현재 「Number · 횟수 안내」이며 아래 Banner는 위치 안내 사례임을 본문에서 구분 |
| 배치 | 최신 사용자 수정값을 반영 · Figma 수정 없음 |

이전 2026-10-12 문서의 전체 노드·인스턴스·미바인딩 건수와 정리 우선순위는 현재 문서 추가 이후 현황으로 재검증하지 않아 최신 현황에서 제외했습니다. 구성 표와 과거 사용처의 건수는 집계일을 따로 표시했습니다.

Dot의 3개·첫 번째 활성은 현재 대표 구성으로 기록하며, 4개 이상을 지원하려면 실제 구현·레이아웃에서 별도로 구성해야 합니다. 마스터를 반드시 확장하거나 분리해야 한다는 결정은 이 MD 업데이트에 포함하지 않습니다. 기존 타이포·색상 규격 설명은 유지하되, 과거 점검 기록을 현재 확정된 수정 지시로 해석하지 않습니다.
