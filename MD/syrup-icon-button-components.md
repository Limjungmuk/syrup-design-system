# Syrup Design System — Icon Button 컴포넌트

> 이름 확인 (2026-11-11): `🟧`로 시작하는 컴포넌트·컴포넌트 세트는 없어요. 아래 구 에셋명과 접두사 건수는 과거 점검 기록이며, 일부 그룹·프레임·벡터·인스턴스 레이어에는 해당 이름이 남아 있어요. 하위 레이어명을 현재 라이브러리 컴포넌트 이름으로 사용하지 않아요.


| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Icon Button` 페이지 → [Icon Button 섹션 `8914:26983`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8914-26983) |
| 섹션 구성 | Icon Button 1440×1162 → Guidelines 960×1688 → Usage 2160×538 |
| 컴포넌트 수 | **3개** (전부 Component Set) |
| 기준일 | 2026-11-06 (가이드라인 5항목 · 예제 5패턴 · 사용자 조정 간격 반영) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-bubble-components.md](syrup-bubble-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **새로고침, 추가 정보 확인, 맨 위로 이동 등 간단한 기능을 제공하는 버튼 컴포넌트예요.**
> 기능과 배치 위치에 맞는 유형을 사용하고, 필요한 경우 문구를 함께 표시해요.

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Icon Button / Refresh](#1-icon-button--refresh)
3. [Icon Button / Info](#2-icon-button--info)
4. [Icon Button / Floating](#3-icon-button--floating)
5. [설계 규칙 요약](#설계-규칙-요약)
6. [Usage](#usage)
7. [Guidelines](#guidelines)
8. [AI 도구 적용 기준](#ai-도구-적용-기준)
9. [현재 확인 사항](#현재-확인-사항)

---

## 구성 한눈에 보기

마스터 섹션은 1440×1162입니다. `Child Item` · `Icon` 별도 섹션 없이 Master Component에 세 유형을 정리하고, 별도 Guidelines와 Usage에서 사용 기준을 설명합니다.

| # | 이름 | 타입 | Variant 축 | 크기 | 이전 집계 인스턴스 (2026-10-12) |
| --- | --- | --- | --- | --- | --- |
| 1 | `Icon Button / Refresh` | Set | `Size` × `Text` × `Shadow` (**8종**) | 20~59 × 20 / 24 |  2 |
| 2 | `Icon Button / Info` | Set | `Size` 3종 | 16 / 20 / 24 정사각 | **10** |
| 3 | `Icon Button / Floating` | Set | `Variant` 2종 | 40 × 40 | **0** |

세 컴포넌트가 **용도도 크기도 서로 다릅니다.** 간단한 기능을 제공하며, Refresh는 필요한 경우 문구를 함께 표시합니다.

---

## 1. Icon Button / Refresh

**Node** `8918:6292` · Component Set · **8 variants**

새로고침 버튼입니다. 마지막 갱신 시각을 함께 보여줄 수 있습니다.

### Properties

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` |
| `Text` | VARIANT | `False` | `False` · `True` |
| `Shadow` | VARIANT | **`True`** | `False` · `True` |

2 × 2 × 2 = **8조합이 모두 존재하는 완전 매트릭스**입니다. Bubble · Checkbox · Chip에 이은 사례입니다.

### Variant별 스펙

| Size | Text | 크기 | Padding | Gap |
| --- | --- | --- | --- | --- |
| `S` | `False` | 20 × 20 | 0 | 0 |
| `M` | `False` | 24 × 24 | 0 | 0 |
| `S` | `True` | **57 × 20** | 0 / `Spacing/200`(8) | **`Spacing/50`** (2) |
| `M` | `True` | **59 × 24** | 0 / `Spacing/200`(8) | **`Spacing/100`** (4) |

공통 — 배경 `Color/Gray_White`, 라운드 `Corner radius/circle`, 아이콘 `syrup_refresh` **12 × 12 고정**

**아이콘은 Size와 무관하게 12 × 12**입니다. 바뀌는 건 버튼 크기와 간격뿐입니다.

`Text=True`일 때 간격이 S는 2, M은 4로 **사이즈에 따라 다릅니다.**

### Shadow 축 — 그림자 ↔ 테두리 교체

`Shadow`는 그림자를 켜고 끄는 것이 아니라 **테두리와 맞바꿉니다.**

| Shadow | 효과 | 테두리 |
| --- | --- | --- |
| `True` | `DROP_SHADOW` `#000000` 14% · blur 5 · offset(0, 2) | **없음** |
| `False` | 없음 | **`Color/Gray_800` 1px** |

버튼 자체를 주변 정보와 구분할 때는 쉐도우형, 갱신 시각이나 목록의 보조 동작을 주변 정보와 함께 표시할 때는 스트로크형을 사용합니다. 아이콘·텍스트 유무와는 별도로 선택합니다. 이름만 보면 "그림자 유무"로 읽히지만 **실제로는 경계 표현 방식의 선택**입니다

> 기존 Refresh 마스터의 그림자는 직접 지정된 효과입니다. 이번 문서 구성의 토큰 바인딩과 마스터 효과 정비는 구분합니다. 정확히 일치하는 토큰이 없는 효과를 임의의 값으로 교체하지 않습니다.

### 텍스트

| 항목 | 값 |
| --- | --- |
| 스타일 | `c200_11_regular` (11 / 16 / −0.3) |
| 색 | `Color/Gray_400` |
| 샘플 | `13:00` (레이어명은 `2019.04.23.21:24`) |

11px이지만 **토큰 스타일이 적용**되어 있습니다. `c200_11_regular`는 Syrup에 존재하는 유일한 11px 스타일입니다.

---

## 2. Icon Button / Info

**Node** `8924:13881` · Component Set · **3 variants**

"ⓘ" 도움말 버튼입니다. 혜택·조건 등 설명이 필요한 대상 가까이에 배치합니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Size` | VARIANT | `S` | `S` · `M` · `L` |

| Size | 버튼 | 아이콘 에셋 |
| --- | --- | --- |
| `S` | 16 × 16 | `🟧syrup_img_info_12` 12 × 12 |
| `M` | 20 × 20 | `🟧syrup_img_info_16` 16 × 16 |
| `L` | 24 × 24 | `🟧syrup_img_info_20` 20 × 20 |

공통 — 배경 `Color/Gray_White`, 라운드 **0**, 패딩 0

**버튼보다 아이콘이 4px 작습니다**(16→12 · 20→16 · 24→20). 터치 영역을 아이콘보다 넓게 잡은 구조입니다.

Refresh와 달리 **사이즈마다 다른 아이콘 에셋**을 씁니다. 작은 크기에서도 선명하도록 각각 그린 것으로 보입니다.

### 사용처 (2026-10-12 이전 집계)

| 페이지 | 건수 |
| --- | --- |
| `Card` | 3 |
| `List Header` | 3 |
| `AD` · `Header` · `List Row` · `Progress Stepper` | 각 1 |

**6개 페이지에 걸쳐 쓰이는** 공용 컴포넌트입니다.

---

## 3. Icon Button / Floating

**Node** `8918:6052` · Component Set · **2 variants** · 40 × 40

화면 위에 떠 있는 둥근 버튼입니다.

| Property | Type | Default | Options |
| --- | --- | --- | --- |
| `Variant` | VARIANT | `Refresh` | `Refresh` · `Top` |

| Variant | 아이콘 | 비고 |
| --- | --- | --- |
| `Refresh` | `ico / 12 / refresh` 20 × 20 | 인스턴스 (배치 크기; 기존 인스턴스 레이어명과 원본 이름은 다를 수 있어요) |
| `Top` | `Group 1012` 15 × 15 | **그룹 (컴포넌트 아님)** |

공통 — 40 × 40, 배경 `Color/Gray_White`, 테두리 **`Color/Gray_700` 1px**, 라운드 `Corner radius/circle`, 세로 오토레이아웃

두 가지가 눈에 띕니다.

- **테두리가 `Color/Gray_700`** 입니다. Refresh의 `Gray_800`, 다른 페이지의 `Gray_850`보다 진합니다
- **그림자가 없습니다.** 떠 있는 버튼인데 `Icon Button / Refresh`의 `Shadow=True`와 달리 효과가 없습니다.

> 현재 Section 1과 Usage D·E, Guidelines 2에서 사용하는 구성입니다. 이전 0건 집계를 현재 미사용의 근거로 해석하지 않습니다.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 크기 | Info 16·20·24 · Refresh 20·24 · Floating 40 |
| 라운드 | **`Corner radius/circle`** (Info만 0) |
| 배경 | `Color/Gray_White` (3종 공통) |
| 테두리 | Refresh `Color/Gray_800` 1px · Floating `Color/Gray_700` 1px |
| 그림자 | `#000000` 14% · blur 5 · offset(0, 2) — Refresh `Shadow=True`만 |
| 텍스트 | `c200_11_regular` + `Color/Gray_400` |
| 좌우 패딩 | `Spacing/200` (8) — Refresh `Text=True`만 |

**세 컴포넌트 모두 배경이 흰색이고 라운드가 원형**(Info 제외)이라는 점이 공통 규칙입니다.

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [Usage `11556:4585`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11556-4585) · 2160×538 |
| 구성 | A~E 5패턴 · 각 슬롯 폭 360 |
| 템플릿 | Usage `11237:46733` · ❖System Components |

실제 컴포넌트 인스턴스와 필요한 주변 정보만 남깁니다. 전체 제품 화면을 복제하지 않습니다. 사용자가 정리한 현재 배치·간격을 기준으로 기록하며, 설명 영역과 슬롯 사이 간격은 50입니다.

| 예제 | Node | 설명 | 주요 설정 |
| --- | --- | --- | --- |
| A. 값 새로고침 | `11556:4586` | 금액이나 환산 값처럼 갱신할 정보 옆에 Refresh를 배치해요. 주변 정보로 기능을 알 수 있으면 아이콘만 사용해요. | S · Text=False · Shadow=True |
| B. 문구와 함께 새로고침 | `11556:4608` | 최신 내역을 불러오는 등 동작을 구체적으로 알려야 할 때 문구를 함께 표시해요. 갱신 시각이 필요한 경우에는 시간을 표시할 수 있어요. | M · Text=True · Shadow=False · 「최신 내역 불러오기」 |
| C. 추가 정보 안내 | `11556:4630` | 혜택이나 이용 조건처럼 설명이 필요한 정보 옆에 Info를 배치해요. 어떤 정보에 대한 설명인지 알 수 있도록 가까이 두어요. | Info L · 대상 문구와 함께 배치 |
| D. 화면 위 플로팅 | `11556:4652` | 하단 고정 ETMS 광고가 없으면 화면 오른쪽에서 24, 하단에서 20을 띄워요. 버튼이 두 개면 세로 간격 10을 유지해요. | Floating Refresh + Top |
| E. 하단 광고 위 플로팅 | `11558:4806` | 하단 ETMS 광고가 최하단에 고정되면 광고 상단부터 20을 띄워요. 오른쪽 간격은 화면 가장자리에서 24로 유지해요. | Floating Refresh + Top · 하단 광고 영역 |

### 현재 예제의 간격과 크기

| 항목 | 현재 문서값 | 해석 |
| --- | --- | --- |
| 설명 영역–슬롯 | 50 | 문서 템플릿 간격 |
| A 대상 정보–버튼 | 4 | 해당 맥락 행의 간격 |
| B 금액–새로고침 구성 | 8 | 사용자 조정값 · 행 폭 360, 높이 35 |
| C 대상 문구–Info | 4 | 해당 맥락 행의 간격 |
| A / B / C 슬롯 높이 | 24 / 35 / 24 | 예제 콘텐츠에 따른 높이 |
| D / E 화면 크기 | 360×222 | 위치 설명을 위한 축약 화면 · 제품 화면 높이 규격 아님 |
| Floating 묶음 | 40×90 · 세로 간격 10 | 40 버튼 2개 + 간격 10 |

내부 행의 간격을 모든 제품 화면에 적용할 공통 규칙으로 확대하지 않습니다. 공통 위치 기준은 Floating의 오른쪽 24 / 하단 기준선 위 20 / 버튼 간격 10입니다.

---

## Guidelines

[Guidelines `11556:4584`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11556-4584) · 960×1688 · 5항목

Guidelines 템플릿 `11237:44468`의 좌우 슬롯에 유형·상태를 비교합니다. 모두 허용된 사용 방식이며 Do / Don’t 구성이 아닙니다. 문서 항목 사이 간격은 100, 설명 영역과 슬롯 간격은 50입니다.

### 1. 실행과 설명에 맞는 버튼을 사용해요

**Node** `11556:4702`

정보를 갱신할 때는 Refresh, 추가 설명을 확인할 때는 Info를 사용해요.
화면에 고정하는 새로고침·맨 위로 이동에는 Floating을 사용하고, 콘텐츠 안의 작은 버튼과 구분해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Refresh · 정보 갱신 | Info · 추가 설명 |
| 환산 값 옆 새로고침 | 혜택 문구 옆 안내 |

### 2. Floating은 화면 하단 오른쪽을 기준으로 배치해요

**Node** `11558:4688`

화면 오른쪽에서 24, 하단에서 20을 띄워요. 하단 고정 ETMS 광고가 있으면 광고 상단부터 20을 띄워요.
버튼이 두 개면 세로 간격 10을 유지하고, 콘텐츠와 하단 고정 요소를 가리지 않도록 여유 공간을 확보해요.

| 조건 | 오른쪽 기준 | 하단 기준 |
| --- | --- | --- |
| ETMS 광고 없음 | 화면 오른쪽에서 24 | 화면 하단에서 20 |
| ETMS 광고 있음 | 화면 오른쪽에서 24 | 고정 광고의 전체 영역 상단에서 20 |

오른쪽·하단 간격은 버튼 묶음의 외곽으로 계산합니다. 두 버튼은 Refresh가 위, Top이 아래이며 각 40×40, 간격 10입니다. 하나만 쓸 때도 실제 버튼 외곽을 같은 기준에 맞춥니다. 광고가 있는 경우 광고 내부 이미지·문구가 아닌 광고 영역 상단을 기준으로 합니다.

축약 화면 360×222에서 광고가 없으면 묶음 위치는 x=296, y=112입니다. 광고 예제는 광고 상단 y=141, 버튼 묶음 y=31로 광고와의 간격 20을 표현합니다. 이 좌표는 문서 예시이며 제품에서는 화면 높이와 실제 광고 영역에 따라 다시 계산합니다.

### 3. 역할에 맞게 쉐도우형과 스트로크형을 사용해요

**Node** `11560:4742`

버튼 자체를 주변 정보와 구분해야 할 때는 쉐도우형(Shadow=True)을 사용해요.
갱신 시각이나 목록의 보조 동작처럼 주변 정보와 함께 표시할 때는 스트로크형(Shadow=False)을 사용해요. 아이콘·텍스트 유무와는 별도로 선택해요.

| 구분 | 실제 속성 | Section 1의 사용 맥락 | 가이드 예시 |
| --- | --- | --- | --- |
| 쉐도우형 | Shadow=True | 금액·환산 값, 추천 영역의 새로고침 | 「1금 당 0.086원」 옆 버튼 |
| 스트로크형 | Shadow=False | 목록 갱신 시각, 최신 내역 불러오기 | 「선물왕 랭킹 TOP 100」의 「13:00」 |

쉐도우형은 그림자, 스트로크형은 테두리로 경계를 만듭니다. Text=True/False와 Shadow=True/False는 독립된 축이며 두 표현 모두 아이콘 단독·문구 포함이 가능합니다. 특정 화면 위치나 텍스트 유무만으로 타입을 고정하지 않습니다. 이 기준은 Refresh의 Shadow 축에 대한 기준이며 Floating에 임의로 그림자를 추가하라는 의미가 아닙니다.

### 4. 필요한 경우 Refresh에 문구를 함께 표시해요

**Node** `11556:4756`

주변 정보로 새로고침 기능을 알 수 있으면 아이콘만 사용해요. 동작이나 갱신 시각을 알려야 하면 Text=True로 설정해요.
문구는 실제 동작에 맞게 작성하고, 쉐도우·스트로크형은 버튼의 역할에 따라 별도로 선택해요.

| 왼쪽 | 오른쪽 |
| --- | --- |
| Text=False · 아이콘만 | Text=True · 문구 포함 |
| M · 24×24 | M · 「최신 내역 불러오기」 · 111×24 |

마스터 샘플 「13:00」만 허용된 문구는 아닙니다. 실제 동작이나 갱신 시각에 맞게 텍스트를 바꾸며 텍스트형 폭은 내용에 따라 달라집니다. 57/59는 마스터의 시간 샘플 기준 폭입니다.

### 5. 주변 요소에 맞는 크기를 선택해요

**Node** `11556:4808`

Info는 S(16)·M(20)·L(24), Refresh는 S(20)·M(24)를 제공해요.
주변 텍스트와 기존 영역의 크기에 맞는 variant를 사용하고, 화면 위 고정 버튼은 Floating(40)을 사용해요.

| 비교 | 마스터 기준 크기 | 현재 비교 행 간격 |
| --- | --- | --- |
| Info S / M / L | 16 / 20 / 24 | 24 |
| Refresh S / M | 20 / 24 | 24 |
| Floating | 40 | 화면 배치 기준은 2번 참조 |

Info와 Refresh에서 같은 S/M이 같은 픽셀 크기를 뜻하지 않습니다. 크기는 각 컴포넌트의 표를 따릅니다. 현재 Info 비교용 인스턴스는 높이 12/16/20으로 표시되지만 마스터 규격은 16×16 / 20×20 / 24×24입니다. 비교 행의 크기 오버라이드를 제품 기본 규격으로 복제하지 않습니다.

---

## AI 도구 적용 기준

1. 역할에 맞는 Refresh·Info·Floating 인스턴스를 재사용합니다. 기존 디자인을 분리해 버튼을 새로 그리지 않습니다.
2. Refresh의 Size·Text·Shadow는 독립적으로 선택합니다. Shadow=False는 경계 없는 버튼이 아니라 스트로크형입니다. 실제 VARIANT 값은 문자열 True/False입니다.
3. 새로고침 문구는 실제 동작에 맞게 수정합니다. 마스터의 시간 샘플과 폭 57/59를 모든 텍스트형의 고정 규격으로 해석하지 않습니다.
4. Floating은 오른쪽 24, 광고가 없으면 화면 하단 위 20, 광고가 있으면 광고 영역 상단 위 20입니다. 두 버튼은 간격 10을 유지합니다.
5. 문서 화면 360×222, 예제의 패딩 140, 문서 행 간격 24는 설명을 위한 배치값이며 제품 전체의 화면·여백 규격이 아닙니다.
6. 제품에는 마스터 크기를 사용합니다. 문서에서 개별적으로 조정된 비교용 인스턴스의 높이를 기본 크기로 간주하지 않습니다.
7. 기존 토큰과 정확히 대응하는 색상·간격·라운드는 토큰을 사용합니다. 원본 아이콘 내부 색상이나 기존 효과에 동일 값의 토큰이 없으면 가까운 토큰으로 임의 치환하지 않습니다.
8. 사용자 조정 후 최신 문서 배치를 유지합니다. 이 문서 업데이트는 Figma의 간격·컴포넌트·토큰을 다시 변경하지 않습니다.

---

## 현재 확인 사항

2026-11-06 Icon Button 페이지의 마스터, Guidelines, Usage를 확인했습니다. 제품 파일 전체 사용량을 조사한 자료는 아닙니다.

| 항목 | 확인 결과 |
| --- | --- |
| 컴포넌트 정의 | Component Set 3개 · Refresh 8 / Info 3 / Floating 2 variants |
| Refresh 기본값 | Size=S · Text=False · Shadow=True (이전 문서의 Shadow=False 수정) |
| 사용 사례 | Section 1의 아노테이션 41개 제거 완료 · 문서에 필요한 요소만 재사용 |
| 토큰 연결 | 앞선 작업에서 신규 구성의 속성 212개를 기존 토큰에 연결. 이후 사용자가 수정한 간격은 현재 배치를 우선함 |
| 일치하는 토큰 없는 배치 | 광고 예시 프레임의 paddingTop=140 유지 · 공통 Spacing 규격으로 해석하지 않음 |
| 원본 아이콘 내부 색상·그림자 | 기존 직접 지정값 유지 · 마스터 정비와 문서 토큰 연결을 구분 |
| 과거 인스턴스 집계 | 구성 표와 사용처의 과거 건수는 2026-10-12 자료이며 최신 총 사용량이 아님 |

이전 문서의 정리 우선순위, 전체 노드 수와 미바인딩 건수는 최신 문서 추가 이후의 현황으로 재검증하지 않아 현황 표에서 제외했습니다. 크기 명칭이나 테두리 차이는 현재 컴포넌트별 규격으로 기록하며, MD 업데이트를 이유로 마스터를 통합·변경하지 않습니다.
