# Syrup Design System — Label 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Label` 페이지 → [Label 섹션 `9354:42673`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=9354-42673) |
| 섹션 구성 | Label 1440×1773 → Guidelines 960×1254 → Usage 1360×444 |
| 컴포넌트 수 | **4개** (전부 Component Set) |
| 기준일 | 2026-11-09 (Guidelines 4항목 · Usage 3패턴 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **콘텐츠의 부가 정보를 간결하게 표시하는 읽기 전용 컴포넌트예요.**
> 재료, 속성, 카테고리, 수치 정보 등을 표현할 때 사용해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Label / Tag](#1-label--tag)
3. [Label / Metric](#2-label--metric)
4. [Child Item](#3-child-item)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [AI 도구 적용 기준](#ai-도구-적용-기준)
9. [현재 확인 사항과 기존 결정](#현재-확인-사항과-기존-결정)

---

## 구성 한눈에 보기

마스터 섹션은 1440×1773이며, **Tag·Metric 두 계열이 각각 마스터와 primitive 쌍**을 이룹니다. 별도 Guidelines 4항목과 Usage 3패턴으로 목록·상세·일일 요약의 사용 기준을 설명합니다.

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 1086 | Master Component | `Label / Tag` · `Label / Metric` |
| y 1760 | Child Item | `.primitive / Label / Tag` · `.primitive / Label / Metric` |

| # | 이름 | 타입 | Variant 축 | 크기 | 과거 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Label / Tag` | Set | `Wrap` 2종 | 224~404 × 25 / 54 | **0** |
| 2 | `Label / Metric` | Set | `Stacked` × `Size` (**3종**) | 155~272 × 18~42 | **0** |
| 3 | `.primitive / Label / Tag` | Set | `Size` 2종 | 49~55 × 25 / 26 | 14 |
| 4 | `.primitive / Label / Metric` | Set | `Item` × `Stacked` × `Size` (**9종**) | 42~96 × 18~42 | 9 |

**읽기 전용 컴포넌트**라 상태(hover·선택 등) 축이 없습니다. [Chip](syrup-chip-components.md)·[Badge](syrup-badge-components.md)와 구분되는 점입니다.

> 섹션 좌표는 2026-10-12에 y=0으로 정리했습니다. 이전 음수 좌표를 현재 문제로 해석하지 않습니다.

---

## 1. Label / Tag

**Node** `9482:56921` · Component Set · **2 variants**

태그를 가로로 나열한 행입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Wrap` | VARIANT | `False` | `False` · `True` |

| Variant | 크기 | 방향 |
| --- | --- | --- |
| `False` | 404 × 25 | 가로 1줄 |
| `True` | 224 × 54 | 가로 **2줄** |

공통 — Padding 0, Gap `Spacing/100` (4), 배경 없음

`Chip / Action`의 `Wrap` 축과 같은 방식입니다. 태그가 많아지면 줄바꿈합니다.

---

## 2. Label / Metric

**Node** `9482:55271` · Component Set · **3 variants**

영양 성분 같은 **수치 정보 3개를 나란히** 보여줍니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Stacked` | VARIANT | `False` | `False` · `True` |
| `Size` | VARIANT | `S` | `S` · `M` |

현재 지원 조합은 **3개**입니다. **`Stacked=True, Size=M`은 지원하지 않습니다**

| Variant | 크기 | 방향 | Padding | Gap |
| --- | --- | --- | --- | --- |
| `False` · `S` | 185 × 18 | 가로 | 0 | `Spacing/250` (10) |
| `False` · `M` | 272 × 19 | 가로 | 0 | `Spacing/250` (10) |
| `True` · `S` | 155 × 42 | 가로 | 0 | `Spacing/300` (12) |

세 variant 모두 **패딩 0 · 가로 HUG · 세로 HUG**입니다. (2026-10-12 `Stacked=True` 패딩 정리)

---

## 3. Child Item

### .primitive / Label / Tag

**Node** `9482:56745` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |

| Size | 크기 | 텍스트 스타일 |
| --- | --- | --- |
| `S` | 49 × 25 | `c100_12_regular` |
| `M` | 55 × 26 | `b400_14_regular` |

공통 — Padding `Spacing/100`(4) / `Spacing/150`(6), Gap `Spacing/50`(2), 배경 `Color/Gray_950`, 라운드 `Corner radius/150`(6)

구성은 **`Label` + `Number`** 텍스트 2개이며, 둘 다 색이 **`Color/Opacity_Black_200`**(검정 50%)입니다.

> 글자색에 **불투명 회색 토큰이 아닌 반투명 검정**을 씁니다. 배경이 `Gray_950`(#F6F6F7)으로 거의 흰색이라 결과는 비슷하지만, 다른 배경 위에서는 비쳐 보입니다

### .primitive / Label / Metric

**Node** `9482:55162` · Component Set · **9 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Item` | VARIANT | `1` | `1` · `2` · `3` |
| `Stacked` | VARIANT | `False` | `False` · `True` |
| `Size` | VARIANT | `S` | `S` · `M` |

현재 지원 조합은 **9개**입니다. Item 1~3 각각 한 줄 S/M과 위아래 배치 S를 제공하며, `Stacked=True, Size=M`은 지원하지 않습니다.

#### Item — 색으로 구분

항목마다 **5 × 5 원형 점**의 색이 다릅니다.

| Item | 내용 | 점 색 |
| --- | --- | --- |
| `1` | 탄수화물 | **`Color/Secondary_Coral`** ✅ 토큰 |
| `2` | 단백질 | **`#50B3FF`** ⚠️ 미바인딩 |
| `3` | 지방 | **`#6DC56F`** ⚠️ 미바인딩 |

**Item 2·3의 색상은 도메인 전용 값으로 토큰을 지정하지 않기로 한 기존 결정(2026-10-12)을 유지합니다.** 유사한 팔레트 색으로 치환하지 않습니다

#### Stacked — 배치 방식

| Stacked | 방향 | Gap | 구성 |
| --- | --- | --- | --- |
| `False` | 가로 | `Spacing/100` (4) | 점 + `탄 250g` 한 줄 |
| `True` | **세로** | `Spacing/150` (6) | 점 + `탄수화물` / **`250g`** 두 줄 |

| Stacked | Size | 라벨 스타일 | 수치 스타일 |
| --- | --- | --- | --- |
| `False` | `S` | `b500_13_regular` + `Color/Gray_100` | (한 줄로 합침) |
| `False` | `M` | `b300_15_regular` + `Color/Gray_100` | (한 줄로 합침) |
| `True` | `S` | `c100_12_regular` + **`Color/Gray_400`** | **`t1300_15_medium`** + `Color/Gray_100` |

`Stacked=True`는 **라벨을 흐리게, 수치를 진하게** 나눠 수치를 강조합니다. `False`는 한 줄에 합쳐 같은 색으로 보여줍니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 태그 배경 | `Color/Gray_950` (#F6F6F7) |
| 태그 라운드 | `Corner radius/150` (6) |
| 태그 패딩 | 상하 `Spacing/100`(4) · 좌우 `Spacing/150`(6) |
| 태그 간격 | `Spacing/100` (4) |
| Metric 점 | 5 × 5 원형, 항목별 색 구분 |
| Metric 간격 | 가로 `Spacing/250`(10) · 세로 `Spacing/150`(6) |
| 본문 색 | `Color/Gray_100` |
| 보조 색 | `Color/Gray_400` |

### 텍스트 스타일

| 스타일 | 용도 |
| --- | --- |
| `c100_12_regular` | 태그 `S` · Metric 라벨(Stacked) |
| `b400_14_regular` | 태그 `M` |
| `b500_13_regular` | Metric `S` |
| `b300_15_regular` | Metric `M` |
| `t1300_15_medium` | Metric 수치 (Stacked) |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11582:524`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11582-524) · 1360×444 |
| 구성 | A~C 3패턴 · 슬롯 폭 360 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

Section 1의 식단 목록·상세 화면에서 Label과 이해에 필요한 주변 문구만 재사용합니다. 전체 화면이나 큰 이미지를 복제하지 않습니다. 설명 영역–슬롯 간격은 50이며, 사례마다 콘텐츠 높이에 맞춰 배치합니다.

| 예제 | Node | 설명 | 주요 구성 |
| --- | --- | --- | --- |
| A. 목록의 식단 정보 | `11582:525` | 식단 목록에서는 S 크기의 Tag와 Metric으로 재료와 영양 정보를 간결하게 보여줘요. 음식명 가까이에 배치하고, 재료가 많으면 Tag를 줄바꿈해요. | 식단명·열량 + Tag S + Metric S/Stacked=False |
| B. 상세의 식단 정보 | `11582:563` | 상세 화면에서는 M 크기로 재료와 영양 정보를 보여줘요. Metric은 항목명을 풀어 쓰고, 수치를 단위와 함께 표시해요. | 식단명·열량 + Tag M + Metric M/Stacked=False |
| C. 일일 영양 요약 | `11582:597` | 하루의 영양 정보를 요약할 때는 Metric의 항목명과 수치를 위아래로 배치해요. 같은 항목의 이름과 값이 연결되어 보이도록 정렬해요. | 오늘 총 칼로리 + Metric S/Stacked=True |

### 현재 예제의 크기

| 항목 | A 목록 | B 상세 | C 일일 요약 |
| --- | --- | --- | --- |
| 슬롯 높이 | 100 | 110 | 44 |
| Tag 행 | 224×25 · Wrap=True | 360×26 · Wrap=True | 없음 |
| Metric 행 | 224×18 · S | 360×19 · M | 140×42 · S/Stacked=True |

Tag의 Size는 바깥 Label / Tag가 아니라 안쪽 primitive에서 선택합니다. 목록 S의 Metric은 「탄·단·지」로, 상세 M은 「탄수화물·단백질·지방」으로 표시합니다. 예제의 문구·수치는 샘플이며 실제 데이터에 맞게 변경합니다.

문서 슬롯 폭 360, 목록의 가용 폭 224와 상세의 360은 현재 사례의 배치값입니다. Label 자체의 고정 공통 폭으로 적용하지 않습니다. Tag는 현재 세 항목만 보여도 Wrap=True를 유지할 수 있으며, 실제로 줄이 바뀌는지는 가용 폭과 콘텐츠 길이에 따라 결정됩니다.

---

## Guidelines

[Guidelines `11582:523`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11582-523) · 960×1254 · 4항목

Guidelines 템플릿 `11237:44468`의 좌우 슬롯으로 허용된 유형과 배치를 비교합니다. Do / Don’t 형식은 아닙니다. 설명 영역–슬롯 간격은 50입니다.

### 1. 정보의 성격에 맞는 Label을 사용해요

**Node** `11582:696`

재료명과 수량처럼 개별 정보를 묶어 보여줄 때는 Tag, 영양 항목과 수치에는 Metric을 사용해요.
Label은 읽기 전용 정보예요. 선택·필터·실행이 필요한 요소와 구분하고 선택 상태나 버튼 동작을 부여하지 않아요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Tag · 재료와 수량 | Metric · 영양 정보 |
| 「계란 50 / 시금치 50 / 토마토소스 200」 | 「탄 250g / 단 218g / 지 392g」 |

배경이 있는 Tag를 Chip처럼 선택 가능한 요소로 해석하지 않습니다. 영양 정보는 숫자만 독립적으로 두지 않고 항목과 함께 표시합니다.

### 2. 목록과 상세에 맞는 크기를 사용해요

**Node** `11582:770`

좁은 목록에서는 S로 정보를 요약하고, 상세처럼 여유 있는 영역에서는 M을 사용해요.
Metric은 S의 축약 표기와 M의 전체 항목명을 구분하고, 같은 정보 묶음에서는 크기와 단위를 일관되게 맞춰요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| S · 목록 요약 | M · 상세 정보 |
| Tag S + Metric S/Stacked=False | Tag M + Metric M/Stacked=False |
| 슬롯 높이 55 | 슬롯 높이 57 |

한 묶음의 크기와 표기를 일관되게 맞춥니다. Tag 상위 컴포넌트에는 Size 속성이 없으므로 내부 Tag primitive에서 설정합니다. Metric은 상위 Size와 Stacked의 지원 조합을 선택합니다.

### 3. Tag가 많으면 영역 안에서 줄바꿈해요

**Node** `11582:876`

재료가 많아 한 줄에 들어가지 않으면 Wrap=True로 설정해 영역 안에서 줄바꿈해요.
줄바꿈할 영역의 폭을 정하고, 내용이 늘어나면 높이가 함께 늘어나도록 구성해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 적은 항목 · 한 줄 배치 | 많은 항목 · 줄바꿈 |
| 3개 · 높이 25 | 7개 · 높이 54 |
| Wrap=True | Wrap=True |

**현재 비교는 Wrap=False와 True의 비교가 아닙니다.** 두 경우 모두 Wrap=True이며, 같은 가용 폭 360에서 항목 수에 따라 실제 줄바꿈이 달라지는 사례입니다. Wrap=True를 두 줄 고정으로 해석하지 않고 높이는 콘텐츠를 따라가도록 구성합니다. Wrap=False가 자동으로 가로 스크롤을 제공한다고 가정하지 않습니다.

### 4. 요약 정보는 항목명과 수치를 나누어 보여줘요

**Node** `11582:962`

영양 정보를 한 줄로 요약할 때는 Stacked=False, 항목별 수치를 위아래로 구분할 때는 Stacked=True를 사용해요.
각 항목의 순서와 표시 색상을 유지하고, 수치는 해당 항목의 단위와 함께 표시해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Stacked=False · 한 줄 요약 | Stacked=True · 항목별 요약 |
| S · 360×18 | S · 140×42 |
| 「탄 250g / 단 218g / 지 392g」 | 「탄수화물 212g / 단백질 4g / 지방 12g」 |

Stacked=True여도 세 항목 전체를 세로 목록으로 쌓는 것은 아닙니다. 세 항목은 가로로 나란히 유지하고, 각 항목 안에서 이름과 수치를 위아래로 나눕니다. 현재 Stacked=True는 Size=S만 지원합니다.

---

## AI 도구 적용 기준

1. Label은 읽기 전용입니다. 선택·필터·실행을 위한 상호작용이 필요하면 해당 역할의 컴포넌트를 검토하며 Label에 선택 상태를 임의로 추가하지 않습니다.
2. Tag는 재료명·수량, Metric은 항목별 수치에 사용합니다. 기존 인스턴스를 재사용하고 이름·숫자를 직접 그린 요소로 대체하지 않습니다.
3. Tag는 상위 Wrap와 내부 primitive Size를 구분합니다. 한 줄로 보인다는 이유만으로 Wrap=False라고 추정하지 않습니다.
4. Metric은 Stacked=False의 S/M, Stacked=True의 S만 지원합니다. Stacked=True/Size=M을 지정하거나 없는 variant를 임의로 생성하지 않습니다.
5. Wrap=True는 가용 폭 안에서 내용에 따라 줄바꿈합니다. 폭을 정하고 높이를 Hug로 유지해 항목이 늘 때 잘리지 않도록 확인합니다.
6. Stacked는 각 항목 내부의 이름·수치 배치 방식입니다. 전체 Metric 행의 가로 배열과 혼동하지 않습니다.
7. Item 1/2/3은 탄수화물/단백질/지방의 순서와 표시 색을 가집니다. 수치·단위를 해당 항목과 맞춰 수정합니다.
8. 단백질 #50B3FF와 지방 #6DC56F는 기존에 토큰 지정하지 않기로 결정한 도메인 전용 색입니다. 가까운 공통 팔레트로 임의 바인딩하지 않습니다.
9. Tag 숫자만 보고 단위를 새로 추정하지 않습니다. Metric의 g 같은 단위와 실제 데이터의 의미를 확인해 사용합니다. 예제 수치·열량은 영양 계산 규칙이나 고정 정책값이 아닙니다.
10. 문서의 폭·간격·슬롯 높이는 현재 배치의 예시입니다. 모든 제품 화면에 고정값으로 확대 적용하지 않습니다. MD 업데이트는 Figma 배치·마스터·토큰을 변경하지 않습니다.

---

## 현재 확인 사항과 기존 결정

2026-11-09 현재 Label 페이지의 가이드라인과 예제를 대조했습니다. 제품 파일 전체 사용량 통계가 아닙니다.

| 항목 | 확인 내용 |
| --- | --- |
| 문서 구성 | Guidelines 4항목 · Usage 3패턴 |
| 사용 맥락 | 식단 목록 / 상세 / 일일 영양 요약 |
| 읽기 전용 | 선택·필터·동작 상태를 부여하지 않음 |
| Tag 줄바꿈 | 가이드 3 양쪽 모두 Wrap=True · 항목 수에 따라 1줄/2줄 표시 |
| Metric Stacked | True는 S만 지원 · 전체 행이 아닌 각 항목 내부를 위아래로 배치 |
| 원본 자료 | Section 1 아노테이션 6개 제거 완료 |
| 이번 작업 | MD 업데이트만 수행 · Figma 수정 없음 |

### 유지하는 기존 결정 (2026-10-12)

- Label 섹션은 y=0으로 정리했습니다. 음수 좌표를 현재 문제로 반복 기록하지 않습니다.
- Metric의 Stacked=True/S는 상하 패딩 118을 0으로 정리하고 세로 Hug로 변경했습니다. 오래된 값을 신규 구성에 복제하지 않습니다.
- 단백질·지방 점 색은 도메인 전용 값으로 토큰을 지정하지 않기로 했습니다. 이 예외는 유지합니다.
- Stacked=True의 이름·수치 정렬을 위한 기존 패딩 7은 별도 값입니다. 문서 업데이트를 이유로 6이나 8로 반올림하지 않습니다.

이전 문서의 노드·인스턴스·미바인딩 건수와 정리 우선순위는 문서 추가 이후 현황으로 재검증되지 않아 최신 현황에서 제외했습니다. 구성 표의 과거 집계에는 기준일을 표시했습니다. 마스터 미사용 0건이라는 과거 설명은 현재 Section 1과 Guidelines·Usage에 인스턴스가 존재하므로 현재 사용 여부의 근거로 쓰지 않습니다.
