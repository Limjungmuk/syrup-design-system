# Syrup Design System — Bubble 컴포넌트

| 항목 | 값 |
| --- | --- |
| Figma File | [Syrup_Design-System](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System) |
| Page / Section | `Bubble` 페이지 → [Bubble 섹션 `8800:24689`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=8800-24689) |
| 섹션 구성 | `Bubble` 1440×1104 → `Guidelines` 960×1175 → `Usage` 2160×484 (가로 일렬) |
| 기준일 | 2026-11-05 (Usage · Guidelines 신설 / 스펙 정리: 2026-10-01) |
| 관련 문서 | [syrup-design-tokens.md](syrup-design-tokens.md) · [syrup-dialog-components.md](syrup-dialog-components.md) · [syrup-alert-components.md](syrup-alert-components.md) · [syrup-badge-components.md](syrup-badge-components.md) · [syrup-banner-components.md](syrup-banner-components.md) · [syrup-border-components.md](syrup-border-components.md) · [syrup-bottom-info-components.md](syrup-bottom-info-components.md) · [syrup-bottom-cta-components.md](syrup-bottom-cta-components.md) · [syrup-bottom-sheet-components.md](syrup-bottom-sheet-components.md) · [syrup-ad-components.md](syrup-ad-components.md) · [syrup-button-components.md](syrup-button-components.md) · [syrup-checkbox-components.md](syrup-checkbox-components.md) · [syrup-chip-components.md](syrup-chip-components.md) · [syrup-card-components.md](syrup-card-components.md) · [syrup-dim-components.md](syrup-dim-components.md) · [syrup-grid-list-components.md](syrup-grid-list-components.md) · [syrup-grid-scroll-components.md](syrup-grid-scroll-components.md) · [syrup-header-components.md](syrup-header-components.md) · [syrup-icon-button-components.md](syrup-icon-button-components.md) · [syrup-indicator-components.md](syrup-indicator-components.md) · [syrup-keypad-components.md](syrup-keypad-components.md) · [syrup-label-components.md](syrup-label-components.md) · [syrup-list-footer-components.md](syrup-list-footer-components.md) · [syrup-list-header-components.md](syrup-list-header-components.md) · [syrup-list-row-components.md](syrup-list-row-components.md) · [syrup-loader-components.md](syrup-loader-components.md) · [syrup-lottie-components.md](syrup-lottie-components.md) · [syrup-product-grid-components.md](syrup-product-grid-components.md) · [syrup-product-list-components.md](syrup-product-list-components.md) · [syrup-product-scroll-components.md](syrup-product-scroll-components.md) · [syrup-progress-stepper-components.md](syrup-progress-stepper-components.md) · [syrup-result-components.md](syrup-result-components.md) · [syrup-search-field-components.md](syrup-search-field-components.md) · [syrup-stepper-components.md](syrup-stepper-components.md) · [syrup-swipe-components.md](syrup-swipe-components.md) · [syrup-switch-components.md](syrup-switch-components.md) · [syrup-tab-components.md](syrup-tab-components.md) · [syrup-tab-bar-components.md](syrup-tab-bar-components.md) · [syrup-text-button-components.md](syrup-text-button-components.md) · [syrup-text-field-components.md](syrup-text-field-components.md) · [syrup-ticker-components.md](syrup-ticker-components.md) · [syrup-toast-components.md](syrup-toast-components.md) |

> **말풍선 형태의 컴포넌트로 채팅, 가이드, 피드백 등 사용자와의 대화를 시각화할 때 사용해요.**

---

## 목차

1. [구성 한눈에 보기](#구성-한눈에-보기)
2. [Bubble — Master Component](#1-bubble--master-component)
3. [말풍선 본문](#2-말풍선-본문)
4. [Tail (꼬리)](#3-tail-꼬리)
5. [선택 요소](#4-선택-요소)
6. [설계 규칙 요약](#설계-규칙-요약)
7. [Usage](#usage)
8. [Guidelines](#guidelines)
9. [점검 필요 사항](#점검-필요-사항)

---

## 구성 한눈에 보기

**컴포넌트셋 하나**로만 구성되어 있습니다. Child Item 섹션이 없는 단순한 구조지만, variant 수는 24개로 가장 많습니다.

| # | 이름 | 타입 | Variant 축 | 크기 |
| --- | --- | --- | --- | --- |
| 1 | `Bubble` | Component Set | `Placement` × `Align` × `Size` × `2 Line` (**24종**) | 49~58 × 31~52 |

---

## 1. Bubble — Master Component

**Node** `8884:15696` · Component Set · **24 variants**

### Properties

| Property | Type | Default | Options | 역할 |
| --- | --- | --- | --- | --- |
| `Placement` | VARIANT | `Top` | `Top` · `Bottom` | 꼬리가 위/아래 중 어디에 붙는지 |
| `Align` | VARIANT | `Left` | `Left` · `Center` · `Right` | 꼬리의 수평 위치 |
| `Size` | VARIANT | `S` | `S` · `M` | 크기 |
| `2 Line` | VARIANT | `False` | `False` · `True` | 본문 2줄 여부 |
| `Checkbox` | BOOLEAN | `false` | — | 체크 아이콘 노출 |
| `Gold` | BOOLEAN | `false` | — | 금 아이콘 노출 |

### Variant 매트릭스

2 × 3 × 2 × 2 = **24조합이 모두 존재합니다.** 지금까지 문서화한 컴포넌트 중 **유일하게 빈칸 없는 완전 매트릭스**입니다.

### 크기

폭은 라벨 길이에 따라 HUG로 늘어납니다. 아래는 샘플 문구 "레이블" 기준입니다.

| Size | 1줄 | 2줄 |
| --- | --- | --- |
| `S` | 49 × 31 | 49 × 41 |
| `M` | 58 × **38** | 58 × **56** |

> `Size=M`의 높이는 2026-10-01에 `t1360_13_medium` 적용으로 36 → 38, 52 → 56으로 바뀌었습니다. 아래 점검 2번 참고.

### 레이아웃

루트는 VERTICAL · gap 0이며, `Placement`와 `Align`이 다음을 결정합니다.

| Property | 값 | 결과 |
| --- | --- | --- |
| `Placement` | `Top` | 레이어 순서 **Tail → 본문** |
| | `Bottom` | 레이어 순서 **본문 → Tail** |
| `Align` | `Left` | 루트 `counterAxisAlignItems: MIN` |
| | `Center` | `CENTER` |
| | `Right` | `MAX` |

---

## 2. 말풍선 본문

| 항목 | `Size=S` | `Size=M` |
| --- | --- | --- |
| Padding (상하 / 좌우) | `Spacing/150`(6) / `Spacing/250`(10) | `Spacing/200`(8) / `Spacing/300`(12) |
| Gap | `Spacing/50` (2) | `Spacing/100` (4) |
| Radius | `Corner radius/250` (10) | `Corner radius/300` (12) |
| 배경 | `Color/Gray_200` (#464646) | `Color/Gray_200` |
| 텍스트 색 | `Color/Gray_White` | `Color/Gray_White` |
| 타이포 | 11 Medium — 스타일 미적용 (예외) | **`t1360_13_medium`** (13 / 18 / 0) |

본문은 HORIZONTAL 오토레이아웃이며 `counterAxisAlignItems: CENTER`입니다.

---

## 3. Tail (꼬리)

꼬리 색은 본문과 같은 `Color/Gray_200`입니다. **24개 variant 전부 동일한 구조**입니다 — `FRAME` 래퍼 안에 `VECTOR` 꼬리.

| Size | 래퍼 크기 | 꼬리 크기 | 래퍼 좌우 Padding |
| --- | --- | --- | --- |
| `S` | 38 × 3 | 6 × 3 | `Spacing/400` (16) |
| `M` | 40 × 4 | 8 × 4 | `Spacing/400` (16) |

래퍼의 좌우 패딩 16이 꼬리를 모서리에서 안쪽으로 밀어 넣습니다. 래퍼 폭(38 · 40)은 패딩 32 + 꼬리(6 · 8)와 정확히 일치합니다.

꼬리의 **수평 위치는 루트의 `counterAxisAlignItems`** 가 결정합니다. `Align` 값에 따라 Tail 프레임 전체가 좌 / 중앙 / 우로 이동하는 방식입니다.

| `Align` | 루트 정렬 | 결과 |
| --- | --- | --- |
| `Left` | `MIN` | Tail 프레임이 왼쪽 |
| `Center` | `CENTER` | 가운데 |
| `Right` | `MAX` | 오른쪽 |

---

## 4. 선택 요소

두 요소 모두 **기본 숨김**이며 BOOLEAN 프로퍼티로 켭니다.

| 레이어 | 타입 | 크기 | 프로퍼티 | 기본값 |
| --- | --- | --- | --- | --- |
| `Gold` | RECTANGLE | 20 × 11 | `Gold` | `false` |
| `Checkbox` | INSTANCE | 16 × 16 | `Checkbox` | `false` |

`Checkbox`는 24개 variant 전부에 있지만, **`Gold`는 12개에만 있습니다.** 아래 점검 1번 참고.

---

## 설계 규칙 요약

| 항목 | 값 |
| --- | --- |
| 폭 | 라벨 길이에 따라 HUG |
| 높이 | S 31(1줄) · 41(2줄) / M 38(1줄) · 56(2줄) |
| 배경 · 꼬리 | `Color/Gray_200` (#464646) |
| 텍스트 | `Color/Gray_White` |
| 모서리 | S `Corner radius/250`(10) · M `Corner radius/300`(12) |
| 여백 | S 6 / 10 · M 8 / 12 |
| 꼬리 들여쓰기 | `Spacing/400` (16) — 전 variant 공통 |
| 타이포 | S 11 Medium (스타일 미적용 · 예외) · M `t1360_13_medium` |

---

## Usage

| 항목 | 값 |
| --- | --- |
| 섹션 | [`Usage` `11438:3694`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11438-3694) · 2160 × 484 |
| 구성 | 5패턴 · 폭 360 · 슬롯 높이 38~168 |
| 템플릿 | `Usage` 컴포넌트 [`11237:46733`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-46733) (`❖System Components` 페이지) |

> **컷은 화면 캡처가 아니라 실제 컴포넌트 인스턴스입니다.**
> 해당 컴포넌트와 **꼭 필요한 맥락 요소만** 남기고 나머지 화면 요소는 모두 지웠습니다. 남은 요소도 잘라낸 그림이 아니라 마스터를 직접 참조하는 인스턴스라, 컴포넌트 디자인이 바뀌면 문서가 함께 바뀝니다 (2026-11-05).

**Bubble은 맥락 없이는 한 컷도 성립하지 않습니다.** 꼬리가 무엇을 가리키는지가 이 컴포넌트의 전부라서, **가리키는 대상이 함께 있어야** 패턴이 읽힙니다. 그래서 다섯 컷 모두 `Switch` · `Button` · 수치 묶음 같은 **대상 요소를 함께 세웠습니다.** Border와 같은 이유입니다.

**패턴을 가르는 축은 variant가 아니라 「무엇을 말하는가」입니다.** 제품에서 쓰이는 variant 조합이 여섯 가지뿐이라 variant로 가르면 컷이 거의 같아집니다 → [점검 6](#6-24종-매트릭스-중-제품이-쓰는-조합은-6종입니다)

| | 패턴 | 설명 | 대상 요소 | Bubble |
| --- | --- | --- | --- | --- |
| **A** | 행동 유도 | 버튼이나 스위치를 사용하면 할 수 있는 일을 안내해요. 대상 요소 가까이에 배치해 어떤 행동에 대한 설명인지 보여줘요. | `Switch` (`Check=On`) | `Top` · `Center` · **`M`** 「누르고 골드톡 알림 받기!」 |
| **B** | 실행 전 조건 안내 | 광고 노출이나 스탬프 차감처럼 실행 전에 알아야 할 조건을 안내해요. 행동의 결과를 예상할 수 있도록 구체적으로 작성해요. | `Button` (`Icon=true` 「2배 받기」) | `Bottom` · `Center` · **`S`** 「광고가 나와요」 |
| **C** | 리워드 안내 · 적립 완료 | 받을 수 있는 금 리워드를 Gold 아이콘과 함께 안내해요. 적립이 완료되면 Gold=False, Checkbox=True로 변경해 완료 상태를 표시해요. | `Button` 296 (「시럽 쿠팡가기」) **2단** | `Bottom` · `Center` · `S` 「매일 3금」 — **`Gold=true` ↔ `Checkbox=true`** |
| **D** | 상태와 횟수 안내 | 횟수나 진행 상태처럼 추가로 알아야 할 정보를 짧게 안내해요. 관련 버튼이나 항목 가까이에 배치해 함께 확인할 수 있도록 해요. | `Button` (`Variant=Weak` · `Disabled=True` 「정답」) | `Bottom` · `Center` · `S` 「1콤보」 |
| **E** | 변화 안내 | 금 시세나 적립 결과처럼 달라진 정보를 안내해요. 변화와 관련된 수치 가까이에 배치해요. | 금 시세 수치 묶음 (`3.223원 (+0.2%)`) | `Bottom` · `Center` · `M` 「금 시세가 올랐어요!」 |

**C만 두 상태를 한 컷에 담았습니다.** 「적립 전」과 「적립 완료」 라벨(Bold 13)을 슬롯 안에 두고 같은 버튼을 두 번 세웠습니다. 바뀌는 것은 Bubble의 BOOLEAN 두 개뿐입니다.

| C의 두 상태 | `Gold` | `Checkbox` | 폭 |
| --- | --- | --- | --- |
| 적립 전 | **`true`** | `false` | 81 |
| 적립 완료 | `false` | **`true`** | 77 |

**A만 꼬리가 위에 붙습니다.** `Switch` 아래에 말풍선을 두었기 때문입니다. 나머지 넷은 대상 위에 띄우므로 `Placement=Bottom`입니다 — 제품에서도 `Bottom`이 106 / `Top`이 10입니다.

### 제품 실측 (2026-11-05)

제품 파일 **[Syrup_App](https://www.figma.com/design/LekNzN0LrcSKQYdutQFI1i)** 전체에서 `Bubble` 인스턴스 **320건**을 전수 조사했습니다. 이 중 204건은 아이데이션 페이지의 것이라, 실제 제품 화면은 **116건**입니다. 아래 수치는 제품 116건 기준입니다.

| 항목 | 값 | 건수 |
| --- | --- | --- |
| 배치 | **다른 컴포넌트 안에 중첩** | **90** |
| | 직접 배치 | 26 |
| `Placement` | `Bottom` | **106** |
| | `Top` | 10 |
| `Align` | `Center` | 73 |
| | `Right` | 43 |
| | **`Left`** | **0** |
| `Size` | `S` | 81 |
| | `M` | 35 |
| `2 Line` | `False` | **116** |
| | **`True`** | **0** |
| `Gold` | `true` | 9 |
| `Checkbox` | `true` | **2** |
| variant 조합 | 24종 중 사용 | **6종** |
| 높이 | 31 (S) | 79 |
| | 38 (M) | 28 |
| | 36 · 28 (구버전) | 9 |

**중첩이 90건으로 78%입니다.** Bubble은 혼자 배치되기보다 **다른 컴포넌트가 자기 안에 품고 있는** 요소입니다.

| 품고 있는 컴포넌트 | 건수 |
| --- | --- |
| `Stepper Item` (`Progress Stepper / Check-In`) | **27** |
| `pocket` · `Progress Stepper / Pig` · `Swipe` · `.primitive / Header / Tailing Acc` | 각 5 |
| `.primitive / Dialog / Button` | 4 |
| `List Row / Shopping / Gold` | 3 |
| `Card / Shopping` · `Product Grid / Stamp` · `List Item` | 각 2 |
| `List Row / Quiz` · `Button / News` · `.primitive / Header / Timer` | 각 1 |

`Stepper Item`에는 아예 **`Bubble` BOOLEAN 프로퍼티**가 있어 켜고 끌 수 있습니다. [Guidelines 3](#3-주변-요소와-여백에-맞춰-크기를-선택해요)이 그 컴포넌트를 컷으로 쓴 이유입니다.

**제품에서 가장 많이 쓰이는 조합은 여섯 가지뿐입니다.**

| 조합 | 건수 |
| --- | --- |
| `Bottom` / `Center` / `S` | **54** |
| `Bottom` / `Right` / `S` | 27 |
| `Bottom` / `Center` / `M` | 18 |
| `Top` / `Right` / `M` | 9 |
| `Bottom` / `Right` / `M` | 7 |
| `Top` / `Center` / `M` | 1 |

**Usage · Guidelines의 컷은 모두 이 여섯 안에서 골랐습니다.** 나머지 18종은 제품에 쓰인 예가 없습니다 → [점검 6](#6-24종-매트릭스-중-제품이-쓰는-조합은-6종입니다)

---

## Guidelines

지켜지지 않으면 결과가 깨지는 것만 올렸습니다. 각 항목은 Figma **[`Guidelines` 섹션 `11438:3695`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11438-3695)** (960 × 1175) 에 한 쌍씩 들어 있습니다.

규칙 하나가 `Guidelines` 템플릿 인스턴스 [`11237:44468`](https://www.figma.com/design/KiAKYEpdiOFwGzFUrqfW77/Syrup_Design-System?node-id=11237-44468) (`❖System Components` 페이지) 하나입니다. 폭 760, `Title`(제목 + 설명) 아래 `Image` 프레임에 슬롯이 좌우로 들어갑니다.

**세 규칙 모두 대상 요소를 함께 세웠습니다.** 1 · 2는 `Bottom CTA`(360 × 112), 3은 `Progress Stepper / Check-In`(316 × 123)입니다. Bubble만 두면 꼬리가 어디를 가리키는지, 무엇을 가리는지가 보이지 않습니다.

| 형식 | 규칙 | 슬롯 라벨 | 라벨 색 |
| --- | --- | --- | --- |
| Do / Don't | 1 · 2 | `Do` · `Don’t` | `#222222` · **`#FF3E00`** |
| 두 경우 비교 | **3** | 「S 적용 · 좁은 간격에 사용」 · 「M 적용 · 크기 비교」 | `#222222` · **`#222222`** |

3은 **둘 다 정상인 선택**이라 Do / Don't로 두지 않았고, [Bottom Sheet 규칙 6](syrup-bottom-sheet-components.md#6-부가-설명은-보조-설명으로-나눌-수-있어요)에서 정한 대로 **오른쪽 라벨 색도 검정으로 맞췄습니다.**

### 1. 꼬리가 안내 대상을 가리키도록 배치해요

대상의 위치에 맞춰 Placement와 Align을 선택해요.
Top은 꼬리가 위쪽, Bottom은 아래쪽에 있으며, Align은 꼬리의 가로 위치를 정해요.

| | `Placement` | 꼬리 | 결과 |
| --- | --- | --- | --- |
| **Do** | **`Bottom`** | 말풍선 **아래** | 꼬리가 버튼을 가리킴 |
| **Don't** | `Top` | 말풍선 **위** | 꼬리가 버튼 반대쪽을 가리킴 |

두 컷 모두 같은 `Bottom CTA` 위 같은 자리(101, 10)에 같은 크기(159 × 38)의 Bubble을 띄웠고, **다른 것은 `Placement` 하나**입니다.

**꼬리의 방향은 내용이 아니라 자리가 정합니다.** 말풍선이 대상 **위**에 있으면 꼬리는 아래(`Bottom`), **아래**에 있으면 꼬리는 위(`Top`)입니다. 이름이 꼬리의 위치를 가리킨다는 점을 놓치면 반대로 고르기 쉽습니다.

### 2. 대상의 문구와 주요 정보를 가리지 않아요

버튼 문구나 본문의 주요 정보를 가리지 않도록 배치해요.
가장자리에 일부 겹치더라도 내용을 읽거나 조작하는 데 방해되지 않도록 해요.

| | 세로 위치 | 결과 |
| --- | --- | --- |
| **Do** | y = **10** | 버튼 위에 떠 있어 「간식 쿠폰 뽑기」가 그대로 보임 |
| **Don't** | y = **45** | 말풍선이 버튼 라벨을 덮어 문구를 읽을 수 없음 |

두 컷 모두 `Placement=Bottom` · 같은 크기이고, **다른 것은 세로 위치 35뿐**입니다.

**「겹치지 마세요」가 아니라 「가리지 마세요」입니다.** 설명이 밝히듯 가장자리에 일부 겹치는 것은 괜찮습니다. 깨지는 것은 **읽어야 할 글자와 눌러야 할 자리**를 덮을 때입니다.

### 3. 주변 요소와 여백에 맞춰 크기를 선택해요

주변 요소가 많거나 배치 공간이 좁은 경우 Size=S를 사용해요.
안내 문구가 잘 읽히고 주변 요소를 가리지 않도록 크기를 선택해요.

| 라벨 | `Size` | Bubble 폭 | 결과 |
| --- | --- | --- | --- |
| **S 적용 · 좁은 간격에 사용** | **`S`** | 63 · 65 · 65 | 항목 폭 74 안에 들어감 |
| **M 적용 · 크기 비교** | `M` | 75 · 77 · 78 | 항목 폭을 넘어 좌우로 삐져나옴 |

컷은 `Progress Stepper / Check-In`에 `Stepper Item` 네 개를 세우고 뒤 세 개의 **`Bubble` BOOLEAN을 켠** 것입니다. 항목 하나의 폭이 **74**, 항목 사이 간격이 **7**이라 여유가 거의 없습니다.

**M은 틀린 것이 아니라 자리가 없는 것입니다.** 같은 문구인데 `S` 63~65가 `M` 75~78로 커지면서 항목 밖으로 나가고, 옆 말풍선과의 간격도 사라집니다. 넓은 자리라면 `M`이 맞습니다 — 제품에서도 `S` 81건 · `M` 35건으로 둘 다 쓰입니다.

---

## 점검 필요 사항

### 1. ℹ️ `Gold` 레이어가 2줄 variant에 없음 — **의도된 설계**

`Gold` BOOLEAN은 24개 variant 전부의 프로퍼티 패널에 노출되지만, 실제 `Gold` 레이어는 `2 Line=False` 12개에만 존재합니다.

| 조건 | `Gold` 레이어 | 프로퍼티 동작 |
| --- | --- | --- |
| `2 Line=False` (12개) | 있음 | 정상 |
| `2 Line=True` (12개) | 없음 | 변화 없음 |

**2줄 말풍선에서 금 이미지를 쓰는 케이스가 없어 의도적으로 넣지 않았습니다.** 수정 대상이 아닙니다.

다만 프로퍼티 패널에는 `Gold` 토글이 계속 보이므로, 2줄 variant를 쓰는 사람이 켜 보고 아무 변화가 없어 혼란스러울 수 있습니다. 컴포넌트 description에 한 줄 남겨 두면 좋겠습니다.

`Checkbox`는 24개 전부에 있어 문제없습니다.

### 2. 텍스트 스타일 — `Size=M` 적용 완료 / `Size=S` 예외 유지

| Size | 실제 값 | 처리 |
| --- | --- | --- |
| `S` | 11 Medium | ❎ **예외 유지** — 시스템 미등록 |
| `M` | 13 Medium | ✅ **`t1360_13_medium` 적용** (2026-10-01) |

**방침** — 아주 작은 폰트는 예외 케이스로 보고 텍스트 스타일로 관리하지 않습니다. 11px Medium·Bold는 신설 대상이 아닙니다.

`13 Medium`은 파일 전체 25곳에서 쓰이고 있어 시스템에 등록했습니다.

#### `Size=M` 적용 영향 — **높이가 바뀌었습니다**

적용 전 `Size=M`의 본문은 line-height가 **AUTO**(Pretendard 13px 기준 약 16)였습니다. `t1360_13_medium`의 line-height 18이 적용되면서 높이가 늘었습니다.

| Variant | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Size=M, 2 Line=False` (6개) | 58 × 36 | 58 × **38** |
| `Size=M, 2 Line=True` (6개) | 58 × 52 | 58 × **56** |

`Size=S`(11 Medium)는 스타일을 적용하지 않았으므로 **49 × 31 · 49 × 41 그대로**입니다.

이로써 S와 M의 높이 간격이 커졌습니다(1줄 기준 31 → 38). 의도와 다르면 `t1360_13_medium`의 line-height를 16으로 조정하거나, Bubble만 line-height를 오버라이드하는 방법이 있습니다.

#### 타이포 공백 전체 현황

| 조합 | 발견 위치 | 상태 |
| --- | --- | --- |
| 13 Bold | Alert · Badge · Chip 등 28곳 | ✅ `t1060_13_bold` 신설 (2026-09-21) |
| 14 Medium | AD · Bottom CTA 등 6곳 | ✅ `t1350_14_medium` 신설 (2026-09-21) |
| **13 Medium** | **Bubble 12 · Progress Stepper 9 · 기타 4** | ✅ **`t1360_13_medium` 신설 (2026-10-01)** |
| 11 Bold | Badge `Size=S` 등 21곳 | ❎ 예외 — 등록하지 않음 |
| 11 Medium | Bubble `Size=S` 등 15곳 | ❎ 예외 — 등록하지 않음 |

### 3. ✅ 본문 프레임 이름 불일치 (2026-10-01 수정 완료)

24개 중 23개는 본문 프레임 이름이 `Text`인데 **`Placement=Top, Align=Left, Size=S, 2 Line=False` 하나만 `Frame 1171276890`** 이었습니다.

Figma는 variant를 전환할 때 레이어 이름으로 오버라이드를 매칭하므로, 이 variant를 오가면 입력해 둔 텍스트가 초기화될 수 있는 상태였습니다.

**`Text`로 변경되어 24개 전부 통일**되었습니다.

### 4. ✅ Tail 구조 불일치 (2026-10-01 수정 완료)

`Tail` 레이어의 노드 타입이 `Align` 값에 따라 달랐습니다.

| `Align` | 변경 전 | 변경 후 |
| --- | --- | --- |
| `Left` · `Right` | FRAME 래퍼 + 내부 VECTOR | 동일 |
| `Center` | **VECTOR 직접** (래퍼 없음) | **FRAME 래퍼 + 내부 VECTOR** |

**24개 전부 `FRAME` 래퍼 + `VECTOR` 구조로 통일**되었습니다. 래퍼 크기(S 38 × 3 / M 40 × 4)와 좌우 패딩(`Spacing/400` = 16)도 전 variant 동일합니다.

이 구조 변경만으로는 variant 크기가 달라지지 않았습니다. (`Size=M`의 높이 변화는 별건인 점검 2번의 텍스트 스타일 적용 때문입니다.)

> 참고 — Tail 래퍼의 `primaryAxisAlignItems`가 `Placement=Top`은 `MAX`, `Bottom`은 `MIN`으로 갈립니다. 다만 래퍼 폭이 패딩 + 꼬리 크기와 정확히 일치해 남는 공간이 없으므로 **시각적 차이는 없습니다.** 정리한다면 한 값으로 통일해도 무방합니다.

### 5. 토큰 상태

| 항목 | 결과 |
| --- | --- |
| 미바인딩 radius · gap | **0건** |
| 미바인딩 padding | `100` 2건 — 문서 보드 레이아웃 프레임 |
| 미바인딩 fill | **0건** |
| 스타일 미적용 텍스트 | **12건** — `Size=S`의 11 Medium (예외 방침) |
| 원격 텍스트 스타일 | **0건** |
| 외부 토큰 | `Spec docs/margin` 2 · paragraph 계열 24 — 둘 다 전역 이슈 |

**spacing · radius · 색상은 전부 Syrup 토큰에 바인딩되어 있습니다.**

구조 문제 2건(3 · 4번)은 2026-10-01에 해결되었고, 1번(`Gold` 레이어)은 의도된 설계로 확인되었습니다.

### 6. 24종 매트릭스 중 제품이 쓰는 조합은 6종입니다

`Placement` × `Align` × `Size` × `2 Line` = **24조합이 빈칸 없이 다 만들어져 있지만**, 제품 116건이 실제로 쓰는 것은 **6종**입니다.

| | 조합 수 | 제품 사용 |
| --- | --- | --- |
| `2 Line=False` | 12 | **6종 / 116건** |
| **`2 Line=True`** | 12 | **0종 / 0건** |

쓰이지 않는 18종의 내역은 이렇습니다.

| 쓰이지 않는 축 | 조합 수 | 비고 |
| --- | --- | --- |
| **`2 Line=True`** 전체 | 12 | 제품 0건 — 2줄 말풍선은 아이데이션(`🛍️ 쇼핑적립`)에서만 14건 |
| **`Align=Left`** 전체 | 4 | 제품 0건 — `Center` 73 · `Right` 43 |
| `Top` / `Center` / `S`, `Top` / `Right` / `S` | 2 | `Top`은 10건뿐이고 전부 `M` |

**`Align=Left`가 한 번도 쓰이지 않는 것이 눈에 띕니다.** 꼬리가 왼쪽에 붙는 말풍선은 대상이 화면 왼쪽 끝에 있을 때 필요한데, 제품의 말풍선은 버튼·항목의 **가운데나 오른쪽**에 붙습니다.

줄일지 남길지는 쓰임 추이를 보고 판단할 일이지만, **2줄 12종은 제품에 한 번도 들어간 적이 없다**는 점은 기록해 둡니다. 아이데이션에서만 쓰였고, 그 14건은 전부 `Top` / `Left` / `M` 한 조합입니다.

### 7. Bubble은 대부분 다른 컴포넌트 안에 심겨 있습니다

제품 116건 중 **90건(78%)이 다른 컴포넌트 안에 중첩**되어 있습니다. 직접 배치는 26건뿐입니다.

| 품고 있는 컴포넌트 | 건수 | Bubble 전용 프로퍼티 |
| --- | --- | --- |
| `Stepper Item` | **27** | **`Bubble` BOOLEAN 있음** |
| `pocket` · `Progress Stepper / Pig` · `Swipe` · `.primitive / Header / Tailing Acc` | 각 5 | — |
| `.primitive / Dialog / Button` | 4 | — |
| `List Row / Shopping / Gold` | 3 | — |
| `Card / Shopping` · `Product Grid / Stamp` · `List Item` | 각 2 | — |
| `List Row / Quiz` · `Button / News` · `.primitive / Header / Timer` | 각 1 | — |

**`Stepper Item`만 켜고 끄는 프로퍼티를 갖고 있습니다.** 나머지는 말풍선을 레이어로 품고 있을 뿐이라, Bubble 마스터가 바뀌면 따라오지만 **쓸지 말지를 프로퍼티로 고를 수 없습니다.**

말풍선을 자주 품는 컴포넌트(`pocket` · `Swipe` · `List Row / Shopping / Gold`)에 `Stepper Item`처럼 BOOLEAN을 두면 쓰는 쪽이 편해집니다. 각 컴포넌트 문서에서 함께 다룰 항목입니다.

### 8. Guidelines 3 안의 Progress Stepper 임시색

[Guidelines 3](#3-주변-요소와-여백에-맞춰-크기를-선택해요)의 두 컷에 쓴 `Progress Stepper / Check-In` 안에 **`#F43437`** 이 fill로 들어 있습니다.

| 위치 | 건수 |
| --- | --- |
| `Stepper Item` > `Icon` > `.primitive / Progress Stepper / Check-In / Button` > `Image` (50 × 50) | **2** |

**Bubble이 아니라 Progress Stepper 쪽 건입니다.** 여기서 고칠 대상은 아니고, [Progress Stepper 문서](syrup-progress-stepper-components.md)에서 함께 확인하면 됩니다. Bubble의 Usage · Guidelines에서 미바인딩 fill은 이 2건이 전부입니다.

**이 컴포넌트에 남은 열린 항목은 `13 Medium` 시스템 등록 여부(2번)와 매트릭스 정리(6번)** 이며, 둘 다 사용처 추이를 보고 판단합니다.
