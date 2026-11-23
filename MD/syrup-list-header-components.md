# Syrup Design System — List Header 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `List Header` 페이지 → [List Header 섹션 `8917:7270`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8917-7270) |
| 섹션 구성 | List Header 1440×2644 → Guidelines 960×1853 → Usage 4160×398 |
| 컴포넌트 수 | **5개** (전부 Component Set) |
| 기준일 | 2026-11-23 (N 뱃지·가이드라인 6항목·예제 A~J·I 패딩 0 확인) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **목록이나 콘텐츠 묶음의 주제와 필요한 안내·기능을 보여주는 헤더 컴포넌트예요.**
> 제목을 중심으로 보조 설명과 부가 요소를 선택하고, 아래 콘텐츠의 시작선에 맞춰 배치해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [List Header — Master Component](#1-list-header--master-component)
3. [Child Item — Title](#2-child-item--title)
4. [Child Item — Sub Text](#3-child-item--sub-text)
5. [Child Item — Right Area](#4-child-item--right-area)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [Usage](#usage)
8. [Guidelines](#guidelines)
9. [AI 도구 적용 기준](#ai-도구-적용-기준)
10. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440×2644입니다. 마스터 하나에 primitive 4종이 붙는 구조로, [Header](syrup-header-components.md)와 역할이 다릅니다. 별도 Guidelines 6항목과 Usage 10패턴을 사용합니다.

| | Header | **List Header** |
| --- | --- | --- |
| 위치 | **화면 최상단** (내비게이션) | **리스트 바로 위** (섹션 제목) |
| 높이 | 55 / 57 | **24 / 47** |
| 구성 | 뒤로가기 · 닫기 · 타이머 | 제목 · 보조설명 · 우측 액션 |
| 배경 | `Color/Gray_White` | **없음** |

| 보드 위치 | 섹션 | 내용 |
| --- | --- | --- |
| y 434 | Master Component | `List Header` 6종 |
| y 1269 | Child Item → Title | `Title` · `Title Acc` |
| y 1755 | Child Item → Sub Text | `Sub Text` |
| y 2184 | Child Item → Right Area | `Tailing Acc` |

| # | 이름 | 타입 | Variant 축 | 크기 | 과거 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `List Header` | Set | `Padding` × `Sub Text` (**6종**) | 360 × 24 / 47 | **0** |
| 2 | `.primitive / List Header / Title` | Set | `Size` 2종 + `Title Acc` | 73~77 × 24 | 6 |
| 3 | `.primitive / List Header / Title Acc` | Set | `Type` 3종 | 20~69 × 18~24 | 2 |
| 4 | `.primitive / List Header / Sub Text` | Set | `Size` 2종 | 116 × 18 / 19 | 3 |
| 5 | `.primitive / List Header / Tailing Acc` | Set | `Type` **6종** + `Text` | 24~63 × 18~24 | 6 |

---

## 1. List Header — Master Component

**Node** `10083:6224` · Component Set · **6 variants**

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Padding` | VARIANT | `0` | **`0` · `8` · `24`** |
| `Sub Text` | VARIANT | `False` | `False` · `True` |
| `Tailing Acc#10083:0` | BOOLEAN | `true` | — |

3 × 2 = **6조합이 모두 존재하는 완전 매트릭스**입니다.

> `Padding` 축의 값이 **숫자 그 자체**(`0` · `8` · `24`)입니다. 파일에서 드문 방식입니다

### Variant별 스펙

| Padding | Sub Text | 크기 | 방향 | 좌우 패딩 | Gap |
| --- | --- | --- | --- | --- | --- |
| `0` | `False` | 360 × 24 | 가로 | 0 | 0 |
| `8` | `False` | 360 × 24 | 가로 | `Spacing/200` (8) | 0 |
| `24` | `False` | 360 × 24 | 가로 | `Spacing/600` (24) | 0 |
| `0` | `True` | 360 × **47** | **세로** | 0 | `Spacing/100` (4) |
| `8` | `True` | 360 × **47** | **세로** | `Spacing/200` (8) | `Spacing/100` (4) |
| `24` | `True` | 360 × **47** | **세로** | `Spacing/600` (24) | `Spacing/100` (4) |

**`Sub Text=True`가 되면 방향이 가로 → 세로로 바뀝니다.** 제목 줄 아래에 보조설명이 붙기 때문입니다.

- 상하 패딩은 **전부 0**입니다. 배경도 없어 리스트 위에 그대로 얹힙니다.
- 높이 24(제목만) → 47(제목 + 보조설명 + 간격 4)

---

## 2. Child Item — Title

### .primitive / List Header / Title

**Node** `10094:14848` · Component Set · **2 variants**

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |
| `Title Acc#10105:13` | BOOLEAN | `true` | — |

| Size | 크기 | 스타일 | 색 |
| --- | --- | --- | --- |
| `S` | 73 × 24 | **`t800_17_bold`** (17 / 22 / 0) | `Color/Gray_100` |
| `M` | 77 × 24 | **`t700_19_bold`** (19 / 24 / −0.3) | `Color/Gray_100` |

공통 — Gap `Spacing/100`(4), 구성 `Title` 텍스트 + `Title Acc` 인스턴스

**한 줄 기본 샘플은 높이 24**이며 글자 크기는 17 → 19로 달라집니다. 긴 제목을 높이 24에 강제로 맞추지 않습니다.

### .primitive / List Header / Title Acc

**Node** `10105:21553` · Component Set · **4 variants**

제목 **오른쪽에 붙는 보조 요소**입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Info` | `Info` · `Arrow` · `Alarm` · `Badge` |

| Variant | 크기 | 내용 | 출처 |
| --- | --- | --- | --- |
| `Info` | 24 × 24 | ⓘ 도움말 | **[Icon Button](syrup-icon-button-components.md)** ▸ `Icon Button / Info` |
| `Arrow` | 20 × 20 | 화살표 | **`❖Components`** ▸ `Icon / Arrow` |
| `Alarm` | 69 × 18 | "알림받기" | **[Button](syrup-button-components.md)** ▸ `Button / Alert` |
| `Badge` | 20 × 20 | 새로운 내용 N | [Badge](syrup-badge-components.md) · Type=New |

**네 variant 모두 다른 페이지의 컴포넌트**를 가져다 씁니다

(2026-10-12 `Property 1` → `Type` 정리 완료)

---

## 3. Child Item — Sub Text

### .primitive / List Header / Sub Text

**Node** `10109:22285` · Component Set · **2 variants** · 116 폭

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |

| Size | 높이 | 스타일 | 색 |
| --- | --- | --- | --- |
| `S` | 18 | `b500_13_regular` (13 / 18 / 0) | `Color/Gray_400` |
| `M` | 19 | `b300_15_regular` (15 / 19 / −0.5) | `Color/Gray_400` |

배경이 **`Color/Gray_White`** 입니다. 마스터는 배경이 없는데 이 primitive만 흰 배경을 갖습니다.

`Title`의 `S`/`M`과 짝을 이룹니다(17 Bold ↔ 13 Regular · 19 Bold ↔ 15 Regular).

---

## 4. Child Item — Right Area

### .primitive / List Header / Tailing Acc

**Node** `10083:10501` · Component Set · **6 variants**

헤더 **오른쪽 끝에 붙는 정보·기능**입니다. 읽기 전용 Text·광고 표기와 실행 가능한 Text Button·새로고침·알림을 구분합니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Type` | VARIANT | `Text` | `Text` · `Text Button` · `AD` · `Refresh` · `Refresh Circle` · `Alarm` |
| `Text#10094:7` | BOOLEAN | `true` | — |

| Variant | 크기 | 내용 | 스타일 · 색 | 출처 |
| --- | --- | --- | --- | --- |
| `Text` | 36 × 18 | "텍스트" | `b400_14_regular` · **`Color/Gray_250`** | 자체 |
| `Text Button` | 63 × 19 | "버튼레이블" | `b300_15_regular` · `Color/Gray_100` | **Text Button** 페이지 |
| `AD` | 63 × 18 | "텍스트" + 배지 | `c100_12_regular` · `Color/Gray_500` | 일부 외부 |
| `Refresh` | 59 × 24 | 🔄 + "13:00" | `c200_11_regular` · `Color/Gray_400` | **[Icon Button](syrup-icon-button-components.md)** |
| `Refresh Circle` | 24 × 24 | 🔄 만 | — | **[Icon Button](syrup-icon-button-components.md)** |
| `Alarm` | 65 × 18 | "알림받기" | `b400_14_regular` · `Color/Gray_400` | **[Button](syrup-button-components.md)** ▸ `Button / Alert` |

(2026-10-12 `Refresh_Circle` → `Refresh Circle` 표기 통일)

> `Text` variant의 색 **`Color/Gray_250`**(#555555)은 파일에서 드물게 쓰이는 토큰입니다. Gray 스케일에는 존재합니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 폭 | 기준 360 · 부모 영역과 콘텐츠 폭에 맞춤 |
| 높이 | 기본 샘플 24 / 47 · 여러 줄 제목은 내용에 맞춰 증가 |
| 좌우 패딩 | `0` · `Spacing/200`(8) · `Spacing/600`(24) 중 선택 |
| 상하 패딩 | **0** |
| 제목–보조설명 간격 | `Spacing/100` (4) |
| 제목–Acc 간격 | `Spacing/100` (4) |
| 배경 | **없음** (`Sub Text` primitive만 `Gray_White`) |
| 제목 | `S` `t800_17_bold` · `M` `t700_19_bold` + `Color/Gray_100` |
| 보조설명 | `S` `b500_13_regular` · `M` `b300_15_regular` + `Color/Gray_400` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11594:6662`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11594-6662) · 4160×398 |
| 구성 | A~J 10패턴 · 슬롯 폭 360 · List Header 인스턴스 12개 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

실제 List Header 인스턴스를 재사용하고, 설명에 필요한 요소만 남깁니다. 전체 제품 화면을 복제하지 않습니다. 설명 영역–슬롯 간격은 50이며 현재 사례의 배치와 문구를 유지합니다.

| 예제 | Node | 설명 | 현재 구성 |
| --- | --- | --- | --- |
| A. 기본 섹션 제목 | `11594:6663` | 목록이나 콘텐츠 묶음의 시작에서 제목으로 내용을 구분해요. 별도 안내나 기능이 필요하지 않으면 제목만 표시해요. | 「더 많이 모으기」 · Sub Text=False · Tailing Acc=false |
| B. 보조 설명 포함 | `11594:6725` | 제목만으로 부족한 조건이나 갱신 주기는 Sub Text로 나누어 안내해요. 제목 아래에 배치하고, 같은 내용을 반복하지 않아요. | 「오늘 하루 이 가격」 + 갱신 주기 · Sub Text=True |
| C. 광고·추가 안내 | `11594:6789` | 광고 콘텐츠는 오른쪽 AD 표시로 구분하고, 추가 설명이 필요한 경우 제목 옆 Info를 사용해요. 출처명이 필요한 영역에서는 함께 표시해요. | 「11번가 상품 추천」 + Info + AD / 「추천 상품」 + 쿠팡 + AD |
| D. 갱신 시각과 새로고침 | `11594:6858` | 갱신이 필요한 목록은 오른쪽에 시각과 새로고침 기능을 제공해요. 실제 갱신 시각과 동작을 맞추고, 아이콘만 필요한 경우 Refresh Circle을 사용해요. | 「선물왕 랭킹 TOP 100」 + Refresh 13:00 / 「보너스 70금 받기」 + Refresh Circle |
| E. 기준 시각 안내 | `11594:6926` | 데이터의 기준 시각처럼 읽기 전용 정보는 오른쪽 텍스트로 보여줘요. 새로고침처럼 실행하는 기능과 구분해요. | 「실시간 금 시세」 + Text 「2024.11.30 13:00 기준」 |
| F. 날짜·알림 기능 | `11594:6989` | 날짜나 현재 영역에 관련된 기능을 제목 옆과 오른쪽에 배치해요. 알림은 설정 상태에 맞는 문구와 아이콘을 사용해요. | 「2025년 7월 4일」 + Title Acc Arrow / 오른쪽 Alarm |
| G. 여러 줄 제목 | `11594:7064` | 제목이 길면 내용에 맞게 줄바꿈해요. 제목 높이가 늘어날 때 전체 Header와 아래 콘텐츠도 함께 밀려나도록 구성해요. | 「챌린지 적립 도전하고 / 금 모으기!」 · Sub Text=False · 높이 48 |
| H. 텍스트 버튼 | `11595:5090` | 안내 보기처럼 제목과 관련된 추가 행동은 오른쪽 Text Button으로 제공해요. 기준 시각처럼 읽는 정보와 구분하고, 실행할 내용을 문구로 알려줘요. | 「금돼지 두드리고 50금 더 받기」 + 「안내」 Text Button + Sub Text=True |
| I. 검색 결과 제목 | `11597:5145` | 검색 결과 제목에서는 검색 키워드만 굵게 표시하고, 나머지 문구는 Regular로 표시해요. 검색 결과에 한정해 적용하고, 일반 섹션 제목은 기존 스타일을 유지해요. | 「검색어 검색결과」 · 키워드 Bold / 나머지 Regular · Padding=0 |

| J. 새로운 내용 안내 | `12412:463` | 새롭게 제공하는 내용이 있는 제목 옆에 N을 표시해요. 수량이나 완료 표시와 구분해요. | List Header 인스턴스만 사용 · Padding=0 · Title Acc=Badge · Badge Type=New |

C와 D는 각각 두 가지 구성으로 기능 차이를 보여줍니다. H는 제목 중 「50금」만 강조 컬러를 사용하며, 안내 버튼은 읽기 전용 Text와 달리 실행 기능입니다.

### 사례별 크기와 여백

- 현재 A~J의 내부 Header는 Padding=0입니다. 문서 슬롯 폭 360을 제품 전체의 고정 폭·패딩으로 해석하지 않습니다.
- A·C·D·E·F·I·J의 각 Header는 한 줄 기준 높이 24, B는 47, G는 48, H는 현재 문구 기준 46입니다. 모든 높이를 마스터 샘플 24/47로 강제하지 않습니다.
- 날짜, 기준 시각, 시각 숫자, 리워드는 설명용 샘플입니다. 실제 상태·데이터·행동에 맞춰 변경합니다.

### 검색 결과 제목에 한정된 굵기 규칙

I의 실제 문구는 「검색어 검색결과」입니다. 「검색어 」구간은 Pretendard Bold, 「검색결과」는 Pretendard Regular입니다. 검색 키워드만 강조하고 나머지는 Regular로 두는 규칙은 **검색 결과 제목에만 적용**합니다. 일반 섹션 제목이나 리워드 제목 전체를 Regular로 바꾸는 기준이 아닙니다.

---

## Guidelines

[Guidelines `11594:6661`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11594-6661) · 960×1853 · 6항목

각 항목은 Guidelines 템플릿 `11237:44468`의 좌우 슬롯으로 허용된 구성을 비교합니다. Do / Don’t 형식은 아닙니다. 순서는 제목·보조 설명 → 컬러 강조 → 새로운 내용 N 뱃지 → 부가 정보·기능 → 여백 → 긴 제목이며, 설명 영역–슬롯 간격은 50입니다.

### 1. 제목과 보조 설명의 역할을 나눠요

**Node** `11594:7126`

제목은 아래 목록의 주제를 짧게 나타내고, 조건이나 갱신 주기는 Sub Text로 나누어 안내해요.
추가 설명이 필요할 때만 Sub Text=True로 사용해 제목과 설명이 같은 내용을 반복하지 않도록 해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 제목만 · Sub Text=False | 보조 설명 · Sub Text=True |
| 「더 많이 모으기」 | 「오늘 하루 이 가격」 + 「매일 오전 9시에 특가 상품이 변경됩니다」 |

제목이 길다는 이유만으로 나머지를 보조 설명에 넣지 않습니다. 제목의 주제와 조건·보조 안내의 의미를 나눕니다.

### 2. 중요한 정보는 컬러로 강조할 수 있어요

**Node** `11596:5121`

리워드나 핵심 수치, 현재 상태처럼 주목이 필요한 부분은 강조 컬러로 표시할 수 있어요.
제목 전체보다 필요한 단어나 수치에만 적용하고, 기존 컬러 토큰을 사용해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 기본 · 단일 컬러 | 컬러 강조 · 핵심 단어만 |
| 「금 받는 LIVE 지금 ON AIR!」 전체 기본색 | 같은 제목 중 「ON AIR!」만 강조 |

기본 구간은 색상 변수 `VariableID:8188:11893`, 강조 구간은 기존 색상 변수 `VariableID:8188:11883`에 연결되어 있습니다. H의 「50금」도 같은 강조 변수를 사용합니다. 직접 입력한 유사 색이나 제목 전체의 일괄 색상 교체 대신 필요한 텍스트 구간에 기존 토큰을 적용합니다.

컬러 강조는 글자 굵기를 바꾸는 검색 결과 제목 규칙과 별개입니다. 현재 컬러 비교 예제는 두 경우 모두 Bold를 유지합니다.

### 3. 새로운 내용은 제목 옆 N 뱃지로 안내해요

**Node** `12412:434` · Guidelines 템플릿 `11237:44468`의 인스턴스

새로운 내용이 있는 영역은 제목 바로 옆에 N 뱃지를 붙여 안내해요. Title의 `Title Acc=True`를 켜고, Title Acc의 `Type=Badge`, 내부 Badge의 `Type=New`를 사용해요. 제목–뱃지 간격은 기존 4를 유지하며 뱃지는 20×20이에요. N은 새로운 내용 표시이며 수량·읽지 않은 개수·완료를 뜻하지 않아요. 표시하지 않을 때는 Title Acc를 꺼요.

좌우 슬롯은 N 표시 있음 / 없음의 List Header 인스턴스로 구성해요. 문서용 Guidelines와 Usage 템플릿도 연결을 유지하고 분리하지 않아요. 예제 J에는 List Header만 넣고 금 이미지·금액·Bubble·Alert 등 다른 요소를 포함하지 않아요.

### 4. 부가 정보와 기능은 목적에 맞게 선택해요

**Node** `11594:7194`

추가 설명·날짜 등 제목에 연결되는 요소는 제목 옆에 두고, 기준 시각·광고 표기·목록 갱신 기능은 오른쪽 영역에서 제공해요.
필요한 요소만 사용하고, 알림이나 새로고침은 실제 상태와 동작에 맞춰 표시해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 제목 옆 Info · 오른쪽 AD | 오른쪽 · 갱신 시각과 새로고침 |
| 「11번가 상품 추천」 + Info + AD | 「선물왕 랭킹 TOP 100」 + Refresh 13:00 |

Title Acc는 제목에 붙는 Info/Arrow/Alarm/Badge, Tailing Acc는 헤더 오른쪽 정보·기능입니다. Text와 Text Button은 읽기 전용 정보와 실행 행동이라는 역할이 다르며 서로 대체하지 않습니다. 텍스트 버튼은 Usage H, 광고 출처·아이콘 새로고침은 Usage C·D에서 추가로 설명합니다.

### 5. 부모 영역과 제목의 좌우 여백을 맞춰요

**Node** `11594:7273`

부모 영역에 이미 여백이 있으면 Padding=0, 여백이 더 필요하면 8 또는 24를 선택해요.
부모 여백과 Header 패딩을 함께 계산해 제목 시작선이 아래 콘텐츠와 맞도록 하고, 같은 여백을 중복 적용하지 않아요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 부모 여백 24 · Padding=0 | 전체 폭 · Padding=24 |
| 부모 360 내 Header 폭 312 | Header 폭 360 |
| 제목 시작선 x=24 | 제목 시작선 x=24 |

Padding은 상하 여백이나 제목 크기를 뜻하지 않습니다. 부모의 16과 Header의 8을 합쳐 시작선을 맞추는 등 실제 컨테이너 구조를 함께 계산합니다. 숫자로 표시된 variant 값은 문자열 0/8/24입니다.

### 6. 긴 제목은 줄바꿈에 맞춰 높이를 늘려요

**Node** `11594:7352`

제목이 길면 의미가 이어지도록 줄바꿈하고, Header 높이가 내용을 따라가도록 구성해요.
두 줄 제목을 Sub Text로 대신하지 않고, 아래 목록이나 오른쪽 요소와 겹치지 않는지 확인해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| 한 줄 제목 | 두 줄 제목 |
| 「더 많이 모으기」 · 24 | 「챌린지 적립 도전하고 / 금 모으기!」 · 48 |

두 경우 모두 Sub Text=False입니다. 48은 현재 두 줄 사례의 높이이며 모든 제목에 강제하는 값이 아닙니다. 내용과 줄바꿈에 맞춰 높이를 유지하고 잘림·겹침을 확인합니다.

---

## AI 도구 적용 기준

1. List Header는 목록·콘텐츠 묶음의 제목입니다. 화면 상단 Header의 신규 타이틀 숨김 기준을 적용해 목록 제목을 제거하지 않습니다.
2. 기존 List Header 인스턴스를 재사용하고 필요한 Sub Text·Tailing Acc만 선택합니다. 불필요한 기본 보조 요소가 남지 않았는지 확인합니다.
3. 실제 상위 속성은 VARIANT Padding(문자열 0/8/24), Sub Text(문자열 False/True), BOOLEAN `Tailing Acc#10083:0`입니다. 부가 요소 종류는 하위 primitive의 Type에서 선택합니다.
4. 제목 옆 표시 여부는 Title의 BOOLEAN `Title Acc#10105:13`으로 구분하며, Info/Arrow/Alarm/Badge는 하위 Title Acc에서 선택합니다. 상위 오른쪽 표시 여부와 혼동하지 않습니다.
5. 오른쪽은 Text/Text Button/AD/Refresh/Refresh Circle/Alarm 중 역할에 맞게 선택합니다. `Refresh Circle`은 공백이 있는 실제 값이며 이전 이름 Refresh_Circle을 사용하지 않습니다.
6. 읽기 전용 Text·광고 표기를 실행 버튼으로 취급하지 않습니다. 안내 등 추가 행동은 Text Button을 사용합니다. 알림은 실제 설정 상태, 새로고침은 현재 갱신 시각과 맞춥니다.
7. 컬러 강조는 제목의 필요한 구간에만 기존 토큰을 적용합니다. 샘플에서 강조된 ON AIR!·50금이라는 문자열을 모든 화면에 고정하지 않습니다.
8. 검색 결과에서는 키워드만 Bold, 그 외 문구는 Regular입니다. 이 예외를 일반 섹션 제목에 확대 적용하거나 혼합 스타일 전체를 한 가지 굵기로 덮어쓰지 않습니다.
9. 제목의 여러 줄과 보조 설명을 구분합니다. 긴 제목·보조 설명의 실제 높이를 따라 아래 콘텐츠를 배치하며 24/47 고정으로 잘라내지 않습니다.
10. Padding은 부모 여백과 합산해 아래 콘텐츠의 시작선에 맞춥니다. 문서의 폭 360이나 예제별 패딩을 모든 제품 컨테이너에 일괄 적용하지 않습니다.
11. Figma 마스터·토큰·사용자 속성명은 유지합니다. 문서는 기존 Guidelines·Usage 컴포넌트 인스턴스로 구성합니다. 웹 이미지 반영은 다음 배포 때 진행합니다.

---

## 현재 확인 사항

2026-11-09 현재 List Header 페이지의 가이드라인·예제와 일부 혼합 스타일을 확인했습니다. 제품 파일 전체를 전수 조사한 통계가 아닙니다.

| 항목 | 확인 결과 |
| --- | --- |
| 정의 | Component Set 5개 · List Header 6 / Title 2 / Title Acc 3 / Sub Text 2 / Tailing Acc 6 variants |
| Guidelines | 5항목 · 컬러 강조를 2번으로 추가하고 기존 항목 재정렬 |
| Usage | 9패턴 · C/D에 사례 2개씩, H 텍스트 버튼, I 검색 결과 제목 |
| 컬러 강조 | 기본 Bold 유지 · ON AIR!와 50금 구간에 기존 컬러 변수 적용 |
| 검색 결과 | 「검색어 」 Bold / 「검색결과」 Regular · 검색 결과에 한정 |
| 원본 자료 | Section 1 아노테이션 50개 제거 완료 |
| 이름 정리 | Title Acc/Tailing Acc의 Type, Refresh Circle 표기 유지 |

이전 2026-10-12 문서의 전체 노드·인스턴스·미바인딩·외부 토큰 건수와 정리 우선순위는 현재 문서 추가 이후 현황으로 재검증하지 않아 최신 현황에서 제외했습니다. 구성 표의 과거 인스턴스 집계는 기준일을 표시했습니다. 과거 마스터 사용 0건은 현재 Section 1과 문서의 사용 여부를 설명하는 수치가 아닙니다.

기존 본체·primitive 스펙은 유지하며 MD 업데이트를 이유로 속성 이름을 재설계하거나 기존 아이콘·색상을 임의 치환하지 않습니다. Icon Button·Text Button·Button/Alert 같은 재사용 컴포넌트가 변경되면 List Header의 관련 조합도 함께 확인합니다.


## 2026-11-23 확인 및 다음 웹 반영 대기

- 가이드라인 3은 Guidelines 컴포넌트 인스턴스 `12412:434`, 예제 J는 Usage 컴포넌트 인스턴스 `12412:463`을 사용한다. 이전 분리 프레임 `12411:446`·`12411:459`는 대체됐다.
- 예제 I `11597:5145`의 List Header는 사용자가 Padding=0으로 변경했으며 실제 좌우 패딩 0을 확인했다. 검색 키워드 Bold / 나머지 Regular 규칙은 유지한다.
- 다음 웹 업데이트 때 가이드라인 3과 재정렬된 4~6, 예제 J, 예제 I의 최신 Figma 이미지를 다시 내보내 반영한다. 이번 작업은 Figma와 MD 반영이며 웹 이미지·다운로드·배포는 대기한다.
